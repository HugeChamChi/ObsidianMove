SQL(Structured Query Language)은 관계형 데이터베이스에서 데이터를 정의, 조회, 수정, 삭제하기 위해 사용되는 표준 언어이다. 관계형 데이터베이스는 데이터를 테이블 형태로 구조화하여 저장하며, SQL은 이 테이블과 상호작용하는 데 사용된다.

## SQL의 주요 기능


- **DDL (Data Definition Language)**: 데이터베이스나 테이블 구조를 정의. 예: `CREATE TABLE` (테이블 생성).
    
- **DML (Data Manipulation Language)**: 데이터 조작. 예: `SELECT` (조회), `INSERT` (삽입), `UPDATE` (수정), `DELETE` (삭제).
    
- **DCL (Data Control Language)**: 데이터 접근 권한 관리. 예: `GRANT` (권한 부여).
    
- **TCL (Transaction Control Language)**: 트랜잭션 관리. 예: `COMMIT` (변경 저장), `ROLLBACK` (변경 취소).

## 기본 문법 예시

<br>



- **테이블 생성 (CREATE TABLE)**:
```cs
CREATE TABLE players (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    level INT
);
// 플레이어 데이터를 저장할 인벤토리 테이블을 만드는 것.
```

<br>


- **데이터 삽입 (INSERT INTO)**:
```cs
INSERT INTO players (id, name, level)
VALUES (1, 'Hero', 10);
// 새로운 플레이어 데이터를 인벤토리에 추가.
```

<br>


- **데이터 조회 (SELECT)**:
```cs
SELECT * FROM players WHERE level > 5;
// 레벨 5 이상인 플레이어만 골라서 확인.
```



<br>

- **데이터 삭제 (DELETE)**:

```cs
DELETE FROM players
WHERE level < 5;
// 레벨 5 미만인 플레이어 데이터를 인벤토리에서 제거.
```