## DCL 이란 ?

DCL(Data Control Language, 데이터 제어어)은 데이터베이스에서 권한과 보안을 관리하는 데 사용하는 SQL 언어.
쉽게 말해, 누가 어떤 데이터를 볼 수 있고, 수정할 수 있는지 등 데이터 접근 권한을 부여하거나 회수하는 역할을 함.

## DCL의 주요 명령어

| 명령어      | 역할(게임 비유) | 예시 구문                                  |
| -------- | --------- | -------------------------------------- |
| GRANT    | 권한 부여     | `GRANT SELECT ON Players TO user1;`    |
| REVOKE   | 권한 회수     | `REVOKE SELECT ON Players FROM user1;` |
| COMMIT   | 변경사항 확정   | `COMMIT;`                              |
| ROLLBACK | 변경사항 취소   | `ROLLBACK;`                            |

---

## 각 명령어 설명

- **GRANT**  
    사용자에게 특정 테이블이나 데이터에 대한 권한을 "부여"합니다.  
    예시:
    
    
    ```

    `GRANT UPDATE ON Players TO Alex;`
    
    (Alex에게 Players 테이블 수정 권한 부여)
    ```



- **REVOKE**  
    이미 부여한 권한을 "회수"합니다.  
    예시:
    
    `REVOKE UPDATE ON Players FROM Alex;`
    
    (Alex의 Players 테이블 수정 권한 회수)
    
- **COMMIT**  
    데이터베이스에 가한 변경사항을 "최종 확정"합니다. 한 번 확정하면 되돌릴 수 없습니다.
    
- **ROLLBACK**  
    변경사항을 "취소"하고, 작업 전 상태로 되돌립니다. 실수로 잘못 수정했을 때 유용합니다