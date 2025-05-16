빌더 패턴(Builder Pattern)은 생성 패턴중 하나로, 복잡한 객체를 단계적으로 구성할 수 있도록 도와주는 디자인 패턴이다. 이 패턴은 객체 생성 과정을 추상화하여, 동일한 생성 프로세스를 통해 다양한 형태의 객체를 만들 수 있게 한다. 특히 객체의 생성이 여러 단계로 이루어지거나, 생성 과정에서 다양한 옵션을 설정해야 할 때 유용.

- 인스턴스를 건축 하듯이 조합하여 객체를 생성한다.
- 객체의 생성 과정과 표현 방법을 분리하고 있음.

빌더 패턴은 객체의 생성 로직을 별도의 `Builder` 클래스로 분리하여, 복잡한 객체를 단계별로 구성할 수 있도록 설계한 패턴임. 이 패턴은 클라이언트 코드에서 객체 생성의 세부 사항을 숨기고, 객체를 생성하는 과정을 유연하게 조정할 수 있도록 함.. 게임 개발의 맥락에서 생각해보면, 캐릭터 생성 시스템을 예로 들 수 있는데 아래 예시를 통해 알아보도록하자.

```cs
// Product: 최종적으로 생성되는 캐릭터 객체
public class Character
{
    public string Name { get; set; }
    public int Level { get; set; }
    public string Weapon { get; set; }

    public void Display()
    {
	    Debug.Log($"캐릭터 정보 - 이름: {Name}, 레벨: {Level}, 무기: {Weapon}");
    }
}

// Builder: 캐릭터를 생성하기 위한 인터페이스
public interface ICharacterBuilder
{
    ICharacterBuilder SetName(string name);
    ICharacterBuilder SetLevel(int level);
    ICharacterBuilder SetWeapon(string weapon);
    Character Build();
}

// ConcreteBuilder: 캐릭터를 실제로 생성하는 클래스
public class CharacterBuilder : ICharacterBuilder
{
    private Character _character = new Character();

    public ICharacterBuilder SetName(string name)
    {
        _character.Name = name;
        return this;
    }

    public ICharacterBuilder SetLevel(int level)
    {
        _character.Level = level;
        return this;
    }

    public ICharacterBuilder SetWeapon(string weapon)
    {
        _character.Weapon = weapon;
        return this;
    }

    public Character Build()
    {
        return _character;
    }
}

// Director: 빌더를 사용하여 캐릭터를 생성하는 클래스
public class CharacterDirector
{
    private ICharacterBuilder _builder;

    public CharacterDirector(ICharacterBuilder builder)
    {
        _builder = builder;
    }

    public Character ConstructWarrior()
    {
        return _builder
            .SetName("전사")
            .SetLevel(10)
            .SetWeapon("검")
            .Build();
    }

    public Character ConstructMage()
    {
        return _builder
            .SetName("마법사")
            .SetLevel(8)
            .SetWeapon("지팡이")
            .Build();
    }
}

// 사용 예시 (Unity MonoBehaviour 클래스 내에서 호출한다고 가정)
public class GameManager : MonoBehaviour
{
    void Start()
    {
        ICharacterBuilder builder = new CharacterBuilder();
        CharacterDirector director = new CharacterDirector(builder);

        Character warrior = director.ConstructWarrior();
        warrior.Display(); // 출력: 캐릭터 정보 - 이름: 전사, 레벨: 10, 무기: 검

        Character mage = director.ConstructMage();
        mage.Display(); // 출력: 캐릭터 정보 - 이름: 마법사, 레벨: 8, 무기: 지팡이
    }
}
```


<br>
여기에서
- Product : 최종적으로 생성되는 객체
- Builder : 객체를 단계적으로 생성하기 위한 인터페이스 혹 추상 클래스.
- ConcreteBulider : Builder를 구현한 구체 클래스 , 특정 방식으로 Product를 생성하는 로직을 포함.
- Director : Builder를 사용하여 객체를 생성하는 과정을 관리하는 클래스임.
  클라이언트는 Director 를 통하여 최종 객체를 얻음

### 빌더 패턴의 장점
- 객체 생성 과정을 단계별로 나눠서 관리 할 수 있어 코드 가독성과 유지보수에 용이
- 동일한 생성 프로세스를 통하여 다양한 형태의 객체를 만들수있어 유연성이 높음
- 클라이언트 코드에서 복잡한 생성 로직을 몰라도 객체를 생성할 수 있음.