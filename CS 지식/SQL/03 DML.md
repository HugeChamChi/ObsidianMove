## DML

DML(Data Manipulation Language, 데이터 조작어)은 데이터베이스에서 데이터를 실제로 조작할수있는 언어. 이미 만들어진 테이블에 데이터를 넣거나(INSERT), 바꾸거나(UPDATE), 지우거나(DELETE), 꺼내올 때(SELECT) 쓰는 명령어들의 집합임.

## DML의 주요 명령어

| 명령어    | 역할     | 예시 구문                                                    |
| ------ | ------ | -------------------------------------------------------- |
| SELECT | 데이터 선택 | `SELECT * FROM Players;`                                 |
| INSERT | 데이터 삽입 | `INSERT INTO Players (Name, Level) VALUES ('Alex', 10);` |
| UPDATE | 데이터 수정 | `UPDATE Players SET Level = 20 WHERE Name = 'Alex';`     |
| DELETE | 데이터 삭제 | `DELETE FROM Players WHERE Name = 'Alex';`               |

---

## 각 명령어 설명

- **SELECT**  
    데이터베이스에서 원하는 데이터를 조회할 때 사용 
    예시:
    ```cs
    SELECT * FROM Players;
    (Players 테이블의 모든 데이터를 조회)
    ```
    
- **INSERT**  
    새로운 데이터를 삽입할 때 사용
    예시:
    
    ```
    `INSERT INTO Players (Name, Level) VALUES ('Alex', 10);`
    
    (Players 테이블에 이름이 Alex이고 레벨이 10인 플레이어 추가)
    ```

    
- **UPDATE**  
    이미 있는 데이터를 수정할 때 사용
    예시:
    ```

    `UPDATE Players SET Level = 20 WHERE Name = 'Alex';`
    
    (이름이 Alex인 플레이어의 레벨을 20으로 변경)
    ```
    
- **DELETE**  
    데이터를 삭제 할 때 사용
    예시:
    
   ```
    `DELETE FROM Players WHERE Name = 'Alex';`
    
    (이름이 Alex인 플레이어 삭제)
    ```