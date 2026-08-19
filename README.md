# Patrones
## Creacionales
### Factory
```java
public class EnemyFactory {
    public Enemy createEnemy(String type) {
        if(type.equalsIgnoreCase("warrior"))
            return new Warrior();
        else if(type.equalsIgnoreCase("mage"))
            return new Mage();
        else
            return null;
    }
}
```
```java
  EnemyFactory enemyFactory = new EnemyFactory();
  Enemy warrior = enemyFactory.createEnemy("warrior");
  Enemy mage = enemyFactory.createEnemy("mage");
```



  
