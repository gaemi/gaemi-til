

### AcquisitionMode

JDBC 커넥션 획득 방법을 지정합니다.

`org.hibernate.ConnectionAcquisitionMode` 에서 확인이 가능하며, 과거 버전의 하이버네이트에서는 지원하지 않습니다.

`hibernate.connection.acquisition_mode` 를 지정하는 형태로 제어하면 됩니다.

* **IMMEDIATELY** : 하이버네이트 세션이 열리면, 바로 커넥션을 획득합니다. 아래 언급할 ConnectionReleaseMode 를 우회하여 하이버네이트 세션이 닫힐때까지 커넥션을 유지합니다.
* **AS\_NEEDED** : 기존에 제공되던 방식으로, 필요한 시점에 커넥션을 획득합니다.

### ReleaseMode

JDBC 커넥션 해제 방법을 지정합니다.

`org.hibernate.ConnectionReleaseMode` 에서 확인이 가능합니다.

`hibernate.connection.release_mode` 를 지정하는 형태로 제어하면 됩니다.

* **AFTER\_STATEMENT** : SQL 문장이 실행될때마다 커넥션을 해제합니다. JTA 를 사용하는 경우 이것이 기본값이며, JTA 에서만 사용할것을 강하게! 권유하고 있습니다.
* **AFTER\_TRANSACTION** : 트랜잭션이 종료될때 커넥션을 해제합니다. JTA 를 사용하지 않을 경우 이것이 기본값이며, JTA 에서는 사용하지 않을것을 강하게! 권유하고 있습니다.
* **ON\_CLOSE** : 하이버네이트 세션이 닫힐때 커넥션을 회수합니다. 3.1 이전버전의 하이버네이트에서 이것이 기본값이었습니다. 

> 보시다시피 AcquisitionMode 와 ReleaseMode 는 서로 밀접하게 연관되어 있습니다.
>
> 그래서인지 하이버네이트에서는 PhysicalConnectionHandlingMode 를 통해 둘을 같이 제어할 수 있습니다.
>
> 개인적으로는 이것을 사용하는것을 추천합니다. `hibernate.connection.handling_mode` 를 지정하여 제어하면 됩니다.



