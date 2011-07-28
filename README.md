# ANAdvancedNavigationController

**ANAdvancedNavigationController** is a subclass of *UIViewController* and works as a parent view controller.

## Setup ANAdvancedNavigationController for your project

* link against <**QuartzCore.framework**>
* add the *ANAdvancedNavigationController* folder to your project

## How to use ANAdvancedNavigationController

### Setup an instance of ANAdvancedNavigationController

```objective-c
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    // create the viewControllers that are displayed
    UIViewController *leftViewController = ...;

    // create an instance of ANAdvancedNavigationController
    ANAdvancedNavigationController *navigationController = [[ANAdvancedNavigationController alloc] initWithLeftViewController:leftViewController];
    
    // set your instance of ANAdvancedNavigationController as your applicationDelegates rootViewController
    self.window.rootViewController = navigationController;

    [self.window makeKeyAndVisible];
    return YES;
}
```

### Push a view controller

To push a viewController, simply call

```objective-c
- (void)pushViewController:(UIViewController *)viewController afterViewController:(UIViewController *)afterViewController animated:(BOOL)animated;
```

* viewController: the view controller, that will be pushes
* afterViewController: the view controller, after which viewController should appear. **Note**: if afterViewController is `nil`
* animated: push animated or not

*Sample*:

```objective-c
UIViewController *nextViewController = ...;
[self.advancedNavigationController pushViewController:nextViewController afterViewController:self animated:YES];
```

## Screenshots in my application [iHub - Social Coding](http://itunes.apple.com/de/app/ihub-social-coding/id433507459?mt=8)
<img src="https://github.com/OliverLetterer/ANAdvancedNavigationController/raw/master/Screenshots/1.jpg">
<img src="https://github.com/OliverLetterer/ANAdvancedNavigationController/raw/master/Screenshots/2.jpg">