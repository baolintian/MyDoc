## 操作

### redis

```
d:
cd D:\Redis
redis-server.exe redis.windows.conf
```



### elasticsearch

```
d:
cd D:\elasticsearch-6.2.2\bin
elasticsearch.bat
```



### mongodb

管理员模式下

```
net start MongoDB
```



### rabbit MQ

```
d:
cd D:\Rabbit MQ\rabbitmq_server-3.7.14\sbin
rabbitmq-plugins enable rabbitmq_management
```

http://localhost:15672/#/



### 自动装配(autowired)

CompactDisc.java

```
package soundsystem;

public interface CompactDisc {
  void play();
}
```

SgtPeppers.java

```
package soundsystem;

import org.springframework.stereotype.Component;

@Component
public class SgtPeppers implements CompactDisc {

  private String title = "Sgt. Pepper's Lonely Hearts Club Band";  
  private String artist = "The Beatles";
  
  public void play() {
    System.out.println("Playing " + title + " by " + artist);
  }
  
}
```

CDPlayer.java

```
package soundsystem;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Component;

@Component
public class CDPlayer implements MediaPlayer {
  private CompactDisc cd;

  @Autowired
  public CDPlayer(CompactDisc cd) {
    this.cd = cd;
  }

  public void play() {
    cd.play();
  }

}
```

