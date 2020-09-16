问：@Component 已经可以支持声明一个 bean 了，为何还要再弄个 @Bean 出来？

答：虽然@Component和@Bean都是定义bean的方式，但@Bean的自定义性更强一些。

①@Component是一种自动配置的方式，用诸如@Controller、@Service、@Repository类的注解，自动侦测并自动配置到Spring容器当中。

②而@Bean用于显式声明单个bean，不是自动执行的，当我们需要自定义一个类并且装配到Spring容器当中时，就可以采用@Bean的方式进行配置。而且@Bean注解的方法返回值是对象，可以在方法中为对象设置属性。

总之，@Bean可以用在自定义的场景下，比@Component拥有更强的灵活性。