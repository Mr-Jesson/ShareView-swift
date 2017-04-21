# ShareView-swift

分享的弹出视图

首先在需要显示的ViewController中懒加载一个JSShareView

lazy var shareVc:JSShareView = {
        let shareView = JSShareView.init(title: "选择分享方式", imageArray: ["share_qq","share_qzone","share_wechat","share_weibo","share_wxtimeline"], textArray: ["QQ","Qzone","Wechat","Weibo","朋友圈"])
        return shareView
    }()
    
    然后需要显示，调用下面的方法
    
    self.shareVc.show()
    
    
    点击的回调调用下面的方法
    
    self.shareVc.itemClickBlock = { (index) in
            print("点击了")
            print(index)
        }
