# 常用插件

- 微信接入 https://github.com/Wechat-Group/WxJava

# 在单元测试里获取上下文

```
@RunWith(SpringJUnit4ClassRunner.class)
@SpringBootTest(classes = {BootApiApplication.class})
public class UserServiceTest {
}
```

`@RunWith(SpringJUnit4ClassRunner.class)`是核心
