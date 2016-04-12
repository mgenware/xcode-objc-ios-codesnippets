# xcode-codesnippet
Some useful code snippets for Xcode.

# Installation
* Open Xcode user data directory.
```sh
open ~/Library/Developer/Xcode/UserData
```
* Copy the `CodeSnippets` directory from this repository to Xcode user data directory.
* Restart Xcode.

# Objective-C Code Snippets
**alertview**: `UIAlertView`
```objective-c
UIAlertView *alert = [[UIAlertView alloc] initWithTitle:@"Title" message:@"<message>" delegate:nil cancelButtonTitle:@"OK" otherButtonTitles:nil, nil];
[alert show];
```

**aprop**: Property(nonatomic, assign)
```objective-c
@property (nonatomic, assign) <type> <name>;
```

**dfn**: `#define`
```objective-c
#define <macro> <value>
```

**ffor**: For Loop
```objective-c
for (int i = 0; i < <length>; i++) {
  <statements>
}
```

**globalq**: `dispatch_async` (Global Queue)
```objective-c
dispatch_async(dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0), ^{
  <code>
});
```

**handlenoti**: Notification Handler
```objective-c
- (void)<method>:(NSNotification *)notification {
  <code>
}
```

**iinit**: Object Initializer
```objective-c
- (instancetype)init {
    self = [super init];
    if (self) {
		    <code>
	  }
    return self;
}
```

**ipt**: `#import`
```objective-c
#import <header>
```

**lstr**: Localized string
```objective-c
NSLocalizedString(@"<key>", nil)
```

**mainq**: `dispatch_async` (Main Queue)
```objective-c
dispatch_async(dispatch_get_main_queue(), ^{
  <code>
});
```

**mlcomment**: Multiline comments
```objective-c
/**
 * <content>
 */
```

**nslf**: `NSLog` with Format String
```objective-c
NSLog(@"%@", <object>);
```

**TODO**
