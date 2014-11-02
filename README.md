RKGetDataWithNSURLSession
=========================
#Examples of how to use.

    - (void)viewDidLoad {
    [super viewDidLoad];
    // Do any additional setup after loading the view, typically from a nib.
    
    RKGetDataWithURLSettion*testSettion=[[RKGetDataWithURLSettion alloc]init];
    testSettion.delegate=self;
    
    [testSettion getDataWithUrlArray:[[NSArray alloc]initwithArray:someURLArray];
    //someURLArray is nsstring in array
    

    }

    - (void)didReceiveMemoryWarning {
    [super didReceiveMemoryWarning];
    // Dispose of any resources that can be recreated.
    }
    -(void)getProgressInDictionary:(NSDictionary *)progressValueInDic{
    
    NSLog(@"=====PROGRESS=====");
    for (NSNumber*num in [progressValueInDic allValues]) {
    NSLog(@"%@",num);
    }
    
    }
    -(void)completeGetData:(NSData *)data withErrorType:(RKGetDataErrorType)errorType andCompeteReciveUrl:(NSString*)urlStr{
    
    NSLog(@"=======================COMPLETE========================");
    NSLog(@"errorType=%ld",errorType);
    NSLog(@"%@",urlStr);
    NSLog(@"complete recive data %ld byte",data.length);
    
    }
    -(void)didComplteTask:(RKTaskCompletedCondition)condition taskURL:(NSString *)urlStr withError:(NSError *)error{
    
    NSLog(@"=======================Finish_.htask========================");
    NSLog(@"%ld",condition);
    NSLog(@"%@",urlStr);
    NSLog(@"%@",error);
    
    }
    
I finished support.So,there is a possibility that no longer operate correctly .

