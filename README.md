# Dependency-Injection-and-Interface-Driven-Development-in-Practice
Dependency Injection and Interface-Driven Development in Practice / SE211 / Project

# Course 

-> Software Construction

# Project

-> User Manager/Email&Notification Project in Java

## Project / Code Part
----------------------

/*

import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import java.util.Objects;

public interface NotificationProvider {
    void sendNotification(String message);
}

public class AwsEmailProvider implements NotificationProvider {
    private static final Logger logger = LoggerFactory.getLogger(AwsEmailProvider.class);

    @Override
    public void sendNotification(String message) {
        logger.info("Email was sent via AWS: {}", message);
    }
}

public class TwilioSmsProvider implements NotificationProvider {
    private static final Logger logger = LoggerFactory.getLogger(TwilioSmsProvider.class);

    @Override
    public void sendNotification(String message) {
        logger.info("SMS was sent via Twilio: {}", message);
    }
}

public class UserManager {
    private static final Logger logger = LoggerFactory.getLogger(UserManager.class);
    private final NotificationProvider notificationProvider;

    // DEPENDENCY INJECTION with Null Check
    public UserManager(NotificationProvider provider) {
        this.notificationProvider = Objects.requireNonNull(provider, "NotificationProvider cannot be null");
    }

    public void registerUser(String username) {
        logger.info("{} registered.", username);
        this.notificationProvider.sendNotification("Welcome " + username);
    }
}



import org.junit.jupiter.api.Test;
import org.junit.jupiter.api.extension.ExtendWith;
import org.mockito.InjectMocks;
import org.mockito.Mock;
import org.mockito.junit.jupiter.MockitoExtension;
import static org.mockito.Mockito.verify;
import static org.mockito.Mockito.times;

@ExtendWith(MockitoExtension.class) 
public class UserManagerTest {

    @Mock
    private NotificationProvider mockProvider; 

    @InjectMocks
    private UserManager userManager; 

    @Test
    public void testRegisterUser_SendsNotification() {
        // Arrange
        String testUser = "GorillaCoder";

        // Act
        userManager.registerUser(testUser);

        // Assert
        
        verify(mockProvider, times(1)).sendNotification("Welcome " + testUser);
    }
}


*/




## Video Presentation

-> https://youtu.be/xLYmU4N9ImM

### Video Presentation by

-> Ubeyd Akdemir










