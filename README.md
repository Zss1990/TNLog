# TNLog
具有打包,上传,分级的本地日志记录系统


- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    // Override point for customization after application launch.
    

    NSSetUncaughtExceptionHandler(&UncaughtExceptionHandle);

    return YES;
}


void UncaughtExceptionHandle(NSException *exception)
{    
    [TNLog logCrash:exception];
}
