#### 1.application.properties

格式：logging.level.接口dao类所在包=DEBUG

```
logging.level.com.chao.dao=DEBUG
```

#### 2.application.yml

格式：
logging:
​    level:
​      接口dao类所在包: DEBUG 

```
logging:
    level:
      com.threefivework.mymall.dao.mapper: DEBUG 
```

