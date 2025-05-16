

프로토타입 패턴(Prototype Pattern)은 생성 패턴 중 하나로, 객체를 새로 생성하는 대신 기존 객체를 복제하여 새로운 객체를 만드는 디자인 패턴. 이 패턴은 객체 생성 비용이 크거나, 유사한 객체를 반복적으로 생성해야 할 때 유용. 이는 객체 생성 과정이 복잡하거나 많은 자원을 소모할 때, 매번 새로운 객체를 생성하는 대신 기존 객체를 복제하고 필요한 부분만 수정하는 방식으로 비용을 절감함.
<br>

예시는 아래와 같음

```cs
// Prototype 인터페이스: 복제 메서드를 정의
public interface IMonsterPrototype
{
    IMonsterPrototype Clone();
}

// ConcretePrototype: 몬스터 클래스
public class Monster : IMonsterPrototype
{
    public string Name { get; set; }
    public int Health { get; set; }
    public int Attack { get; set; }

    public Monster(string name, int health, int attack)
    {
        Name = name;
        Health = health;
        Attack = attack;
    }

    // 복제 메서드 구현 (깊은 복사)
    public IMonsterPrototype Clone()
    {
        return new Monster(Name, Health, Attack);
    }

    public void Display()
    {
        Debug.Log($"몬스터 정보 - 이름: {Name}, 체력: {Health}, 공격력: {Attack}");
    }
}

// Client: 몬스터를 생성하고 사용하는 클래스 (Unity MonoBehaviour로 가정)
public class MonsterSpawner : MonoBehaviour
{
    private IMonsterPrototype _goblinPrototype;

    void Start()
    {
        // 기본 고블린 프로토타입 생성
        _goblinPrototype = new Monster("고블린", 20, 5);
        SpawnMonsters();
    }

    void SpawnMonsters()
    {
        // 고블린 프로토타입을 복제하여 새로운 몬스터 생성
        IMonsterPrototype goblin1 = _goblinPrototype.Clone();
        goblin1.Display(); // 출력: 몬스터 정보 - 이름: 고블린, 체력: 20, 공격력: 5

        // 복제한 객체를 수정하여 변형된 몬스터 생성
        IMonsterPrototype goblinBoss = _goblinPrototype.Clone();
        ((Monster)goblinBoss).Name = "고블린 보스";
        ((Monster)goblinBoss).Health = 50;
        ((Monster)goblinBoss).Attack = 10;
        goblinBoss.Display(); // 출력: 몬스터 정보 - 이름: 고블린 보스, 체력: 50, 공격력: 10
    }
}
```

### 프로토타입 패턴의 구조 
- Prototype : 복제 기능을 정의하는 인터페이스 혹 추상클래스 
- ConcretePrototype : Prototype 을 구현한 구체 클래스임 . 실제 복제 로직을 정의함
- Client : 프로토타입 객체를 사용하여 새로운 객체를 생성하는 역할을 함.

### 장점 과 단점
<span style="font-size:30px"> 장점 </span>
- 객체 생성 비용을 줄일수있음.
- 유사한 객체를 반복적으로 생성할때 효율적임
- 객체 생성 로직을 중앙에서 관리 할수 있어 유연성이 높음

<br>

<span style="font-size:30px"> 단점 </span>
- 프로토타입 객체가 많아지면 메모리 사용량이 증가함
- 복잡한 객체의 경우 복제 과정에서 상태 유지나 데이터 손실문제가 발생할수있음
- 깊은복사,얕은복사를 적절히 선택해야하는 추가적 고려가 필요할수있음.




