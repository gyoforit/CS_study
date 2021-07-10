# CS_study_8회

## 1. [DB] 스키마&DB언어

> 데이터베이스의 스키마란 무엇인지 설명하고 DDL, DML, DCL을 설명해보아라.

스키마란 데이터베이스의 설계도라고 할 수 있습니다. 데이터베이스가 가진 속성과 각각의 속성들의 제약조건을 담고 있는 것이 스키마입니다.

DDL, DML, DCL은 모두 데이터베이스와 관련된 언어입니다. 먼저 DDL은 데이터 정의어로 데이터베이스 테이블을 생성, 수정, 삭제하는 명령어 입니다. DDL 명령어로는 CREATE, ALTER, DROP이 있습니다. DML은 데이터 조작어로 데이터베이스에 저장된 데이터들을 생성, 조회, 수정, 삭제하는 명령어 입니다. INSERT, SELECT, UPDATE, DELETE가 있습니다. 마지막으로 DCL은 데이터 제어어로 데이터베이스의 무결성을 위해 사용하는 명령어입니다. DCL에는 GRANT와 REVOKE가 있습니다.



## 2. [웹] RESTful API

> RESTful API는 무엇인가?

RESTful API란 REST를 만족하는 API입니다. REST는 HTTP URI를 통해 자원을 명시하고, HTTP 메서드 GET, POST, PUT, DELETE 를 통해 해당 자원에 대한 CRUD 명령을 적용할 수 있는 SW 아키텍처입니다.

가령 '1번 글을 삭제하는 API'를 설계할 때 REST를 지킨다면 'text/1/' 이라는 URI에 DELETE 메서드로 요청해야 합니다. 반면 'text/1/delete/' 처럼 URI에서 해당 자원에 대해 어떤 행위를 할지 확인할 수 있다면 RESTful한 API라고 할 수 없습니다.