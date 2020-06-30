# xcode-ios-objc-codesnippets

Useful code snippets for Xcode / Objective-C / iOS.

# Installation

## Auto Installation

- Download this repository.
- Navigate to the root directory of this repository in Terminal.
- Run `sh install.sh`.
- Restart Xcode.

## Manual Installation

- Download this repository.
- Open Xcode user data directory.

```sh
open ~/Library/Developer/Xcode/UserData
```

- Copy the `CodeSnippets` directory from this repository to Xcode user data directory.
- Restart Xcode.

# Code Snippets

> The snippets below are sorted alphabetically.

<blockquote>
Unlike builtin Xcode snippets, snippets here don't have starting braces appear on their own line. Therefore, some snippets have an extra letter at the beginning just to make them similar while not to conflict with Xcode builtin snippets, for example:

```objective-c
// Xcode `init` snippet:
- (instancetype)init
{
    self = [super init];
    if (self) {
        <#statements#>
    }
    return self;
}

// Ours is `iinit`:
- (instancetype)init {
    self = [super init];
    if (self) {
        <#statements#>
    }
    return self;
}
```

Some snippets also offer complementary functions to builtin snippets:

```objective-c
// Xcode `for` snippet:
for (<#initialization#>; <#condition#>; <#increment#>) {
    <#statements#>
}

// Our `ffor` snippet:
for (int i = 0; i < <#length#>; i++) {
    <#statements#>
}
```

</blockquote>

**alertview** creates a `UIAlertView`.

```objective-c
UIAlertView *alert = [[UIAlertView alloc] initWithTitle:@"Title" message:@"<message>" delegate:nil cancelButtonTitle:@"OK" otherButtonTitles:nil, nil];
[alert show];
```

**aprop** `nonatomic`, `assign` property.

```objective-c
@property (nonatomic, assign) <type> <name>;
```

**commoninit** common initializer methods for `UIView`(Taken from [here](http://stackoverflow.com/questions/7226239/objective-c-custom-view-and-implementing-init-method).)

```objective-c
- (void)commonInit {
    <code>
}

- (instancetype)initWithFrame:(CGRect)aRect {
    if ((self = [super initWithFrame:aRect])) {
        [self commonInit];
    }
    return self;
}

- (instancetype)initWithCoder:(NSCoder*)coder {
    if ((self = [super initWithCoder:coder])) {
        [self commonInit];
    }
    return self;
}
```

**dfn** `#define`.

```objective-c
#define <macro> <value>
```

**ffor** `for` loop.

```objective-c
for (int i = 0; i < <length>; i++) {
    <statements>
}
```

**globalq** `dispatch_async` on a global queue.

```objective-c
dispatch_async(dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0), ^{
    <code>
});
```

**handlenoti** notification handler.

```objective-c
- (void)<method>:(NSNotification *)notification {
    <code>
}
```

**iinit** object initializer.

```objective-c
- (instancetype)init {
    self = [super init];
    if (self) {
        <statements>
    }
    return self;
}
```

**initcell** overrides `UITableViewCell.initWithStyle`.

```objective-c
- (instancetype)initWithStyle:(UITableViewCellStyle)style reuseIdentifier:(NSString *)reuseIdentifier {
    self = [super initWithStyle:style reuseIdentifier:reuseIdentifier];
    if (self) {
        <statements>
    }
    return self;
}
```

**initframe** overrides `initWithFrame`.

```objective-c
- (instancetype)initWithFrame:(CGRect)frame {
    self = [super initWithFrame:frame];
    if (self) {
        <statements>
    }
    return self;
}
```

**ipt** `#import`.

```objective-c
#import <header>
```

**lstr** `NSLocalizedString`.

```objective-c
NSLocalizedString(@"<key>", nil)
```

**mainq** `dispatch_async` on a main queue.

```objective-c
dispatch_async(dispatch_get_main_queue(), ^{
    <code>
});
```

**mlcomment** multiline comments.

```objective-c
/**
 * <content>
 */
```

**newbutton** creates a `UIButton`.

```objective-c
[UIButton buttonWithType:UIButtonTypeCustom]
```

**newcview** creates a custom `UIView`.

```objective-c
[[<type> alloc] initWithFrame:CGRectZero]
```

**newlabel** creates a `UILabel`.

```objective-c
[[UILabel alloc] initWithFrame:CGRectZero]
```

**newview** creates a `UIView`.

```objective-c
[[UIView alloc] initWithFrame:CGRectZero]
```

**nslf** `NSLog` with a format string.

```objective-c
NSLog(@"%@", <object>);
```

**pinterface** private interface implementation.

```objective-c
@interface <class> ()

@end
```

**pmark** `#pragma mark`.

```objective-c
#pragma mark -
#pragma mark <name>
```

**postnoti** posts a notification.

```objective-c
[[NSNotificationCenter defaultCenter] postNotificationName:<name>; object:self userInfo:<userInfo>];
```

**prop** `nonatomic`, `strong` property.

```objective-c
@property (nonatomic, strong) <type> <name>;
```

**raprop** `nonatomic`, `assign`, `readonly` property.

```objective-c
@property (nonatomic, assign, readonly) <type> <name>;
```

**regnoti** registers a notification.

```objective-c
[[NSNotificationCenter defaultCenter] addObserver:self selector:@selector(<selector>) name:<name> object:nil];
```

**remnoti** removes a notification.

```objective-c
[[NSNotificationCenter defaultCenter] removeObserver:self name:<name> object:nil];
```

**rprop** `nonatomic`, `strong`, `readonly` property.

```objective-c
@property (nonatomic, strong, readonly) <type> <name>;
```

**sharedinstance** a shared instance.

```objective-c
+ (instancetype)sharedInstance {
    static <type> *result = nil;
    static dispatch_once_t onceToken;
    dispatch_once(&onceToken, ^{
        result = [[<type> alloc] init];
    });
    return result;
}
```

**strf** `stringWithFormat`.

```objective-c
[NSString stringWithFormat:@"%@", <object>]
```
