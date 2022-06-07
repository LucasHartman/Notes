# SpringBoot_Notes

# --------------------------------------------------------
# application.properties example
# --------------------------------------------------------
# Code Sample:
spring.jpa.hibernate.ddl-auto=update
spring.datasource.url=jdbc:mysql://localhost:3306/root
spring.datasource.username=root
spring.datasource.password=Shiro&Sora
spring.datasource.driver-class-name =com.mysql.jdbc.Driver

# --------------------------------------------------------
# logging
# --------------------------------------------------------
# import class:
import lombok.extern.slf4j.Slf4j;
# Class Annotation:
@Slf4j
# Code Sample:
log.info("address is: {} {}", address.getStreet(), address.getNumber() );


# --------------------------------------------------------
# Bean
Wire data from a pojo class into component class
# --------------------------------------------------------
# import:
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Component;
# Class Annotation:
@Component
# Code Sample
ClassType classType; // instance variable of a pojo class
System.out.println("get value from pojo class" +classType.varName());