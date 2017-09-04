# LoadingImageFromUrl
simple using example of Picasso libary
Picasso是square公司出品的一款非常优秀的开源图片加载库，是目前Android开发中超级流行的图片加载库之一。
使用简介
首先在项目中引入Picasso以（gradle为例）
compile “com.square.picasso:picasso:2.5.2”
传统的Imageview设置图片
Picasso.with(context).load(url).placeholder(R.drawable.tab_item_bg).into(imageView);
自定义的布局设置图片，target是指实现了target接口的自定义view
Picasso.with(context).load(url).placeholder(R.drawable.tab_item_bg).into(target);
adapter中的使用
//view复用会自动察觉并取消之前的下载任务
@override
public void getView(int position, View convertView,ViewGroup parent){
  SquaredImageView view = (SquaredImageView) convertView;
  if(view == null){
    view = new SquaredImageView(context);
  }
  String url = getItem(position);
  Picasso.with(context).load(rul).into(view);
}
自动设置图片宽高像素的大小
Picasso
  .with(context)
  .load(url)
  .resize(50,50)
  .centerCrop()
  .into(imageView)
  
  流程分析：
  
