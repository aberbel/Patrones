# Patrones
## Creacionales
### Factory
```java
  EnemyFactory enemyFactory = new EnemyFactory();
  Enemy warrior = enemyFactory.createEnemy("warrior");
  Enemy mage = enemyFactory.createEnemy("mage");
```
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

<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" contentStyleType="text/css" data-diagram-type="CLASS" height="122px" preserveAspectRatio="none" style="width:281px;height:122px;background:#FFFFFF;" version="1.1" viewBox="0 0 281 122" width="281px" zoomAndPan="magnify"><title>Diagrama de clases</title><defs/><g><g class="title" data-source-line="1"><text fill="#000000" font-family="sans-serif" font-size="14" font-weight="bold" lengthAdjust="spacing" textLength="154.2461" x="59.4458" y="22.9951">Diagrama de clases</text></g><!--class EnemyFactory--><g class="entity" data-qualified-name="EnemyFactory" data-source-line="3" id="ent0002"><rect fill="#F1F1F1" height="64.2969" rx="2.5" ry="2.5" style="stroke:#181818;stroke-width:0.5;" width="260.1377" x="7" y="44.2969"/><ellipse cx="82.479" cy="60.2969" fill="#ADD1B2" rx="11" ry="11" style="stroke:#181818;stroke-width:1;"/><path d="M85.4478,65.9375 Q84.8696,66.2344 84.229,66.375 Q83.5884,66.5313 82.8853,66.5313 Q80.3853,66.5313 79.0571,64.8906 Q77.7446,63.2344 77.7446,60.1094 Q77.7446,56.9844 79.0571,55.3281 Q80.3853,53.6719 82.8853,53.6719 Q83.5884,53.6719 84.229,53.8281 Q84.8853,53.9844 85.4478,54.2813 L85.4478,57 Q84.8228,56.4219 84.229,56.1563 Q83.6353,55.875 83.0103,55.875 Q81.6665,55.875 80.979,56.9531 Q80.2915,58.0156 80.2915,60.1094 Q80.2915,62.2031 80.979,63.2813 Q81.6665,64.3438 83.0103,64.3438 Q83.6353,64.3438 84.229,64.0781 Q84.8228,63.7969 85.4478,63.2188 L85.4478,65.9375 Z " fill="#000000"/><text fill="#000000" font-family="sans-serif" font-size="14" lengthAdjust="spacing" textLength="100.6797" x="102.979" y="65.1436">EnemyFactory</text><line style="stroke:#181818;stroke-width:0.5;" x1="8" x2="266.1377" y1="76.2969" y2="76.2969"/><line style="stroke:#181818;stroke-width:0.5;" x1="8" x2="266.1377" y1="84.2969" y2="84.2969"/><g data-visibility-modifier="PUBLIC_METHOD"><ellipse cx="18" cy="97.9453" fill="#84BE84" rx="3" ry="3" style="stroke:#038048;stroke-width:1;"/></g><text fill="#000000" font-family="sans-serif" font-size="14" lengthAdjust="spacing" textLength="234.1377" x="27" y="101.292">Enemy createEnemy(String type)</text></g><?plantuml-src AyaioKbLSCbCJ2zAp4rKI4bLICv9B4ujvk82qSKAhdcfkPLkYSab-KML2jLS2WhQO165vABKn99KC5iZkAGeCozTeQIo85MJgnO0?></g></svg>
### Factory Method
```java
 Enemy warrior = new WarriorFactory().createEnemy();
 Enemy mage = new MageFactory().createEnemy();
```
```java
public abstract class EnemyFactory {
    public abstract Enemy createEnemy();
}
```
```java
public class WarriorFactory extends EnemyFactory{
    @Override
    public Enemy createEnemy() {
        return new Warrior();
    }
}
public class MageFactory extends EnemyFactory{
    @Override
    public Enemy createEnemy() {
        return new Mage();
    }
}
```


  
