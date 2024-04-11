# UnityIOSPushView

# Usage

    [[HXUnityFrameworkManager sharedManager] hxStartUnity];
    [[HXUnityFrameworkManager sharedManager] UnityPause:true];
    UnityAppController * unityAppController = [[HXUnityFrameworkManager sharedManager] GetUnityAppController];
    //UIViewController* viewCtr = unityAppController.ViewCtrDic[@"root"];//rootVC
    NSString *key = self.vcKey.length > 0 ? self.vcKey : @"Test";
    
    UIViewController* viewCtr = [unityAppController AllocNewViewController:key];//NewVC
    [self.navigationController pushViewController:viewCtr animated:false completion:nil];
    self.navigationController.navigationBarHidden = YES;
    
    [unityAppController ChangeShow:key];//ChangeViewShow
    [[HXUnityFrameworkManager sharedManager] UnityPause:false];
