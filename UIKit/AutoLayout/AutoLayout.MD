#AutoLayout
###简介
###Demo
####居中的Demo
```objc
//beging  
UIImageView* imagevew = [UIImageView new];
imagevew.translatesAutoresizingMaskIntoConstraints = NO;  
[self.view addSubview:imagevew];  

NSDictionary* views = NSDictionaryOfVariableBindings(imagevew);  
//设置高度  
[self.view.contentView addConstraints:[NSLayoutConstraint constraintsWithVisualFormat:@"V:[imagevew(60)]" options:0 metrics:nil views:views]];  
//设置宽度  
[self.view.contentView addConstraints:[NSLayoutConstraint constraintsWithVisualFormat:@"[imagevew(60)]" options:0 metrics:nil views:views]];  
//垂直居中  
[self.view addConstraint:[NSLayoutConstraint constraintWithItem:imagevew attribute:NSLayoutAttributeCenterY relatedBy:NSLayoutRelationEqual toItem:self.view attribute:NSLayoutAttributeCenterY multiplier:1 constant:0]];  
//水平居中  
[self.view addConstraint:[NSLayoutConstraint constraintWithItem:imagevew attribute:NSLayoutAttributeCenterX relatedBy:NSLayoutRelationEqual toItem:self.view attribute:NSLayoutAttributeCenterX multiplier:1 constant:0]];  
//end
```
