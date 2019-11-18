大数据181 刘柄沣 2018310170
//数组转换成字符串函数	
	public static StringBuffer ArrayToString(String[] args) {
		StringBuffer str=new StringBuffer();
		for(int i=0;i<args.length;i++) {
			str.append(args[i]);
		}
		return str;
	//格式化输出函数  每7个汉字加入一个标点符号，奇数时加“，”，偶数时加“。
	public static StringBuffer FormatOutput(StringBuffer str) {
		StringBuffer str2=new StringBuffer();
		for(int i=0;i<str.length()/7;i++) {
			str2.append(str.substring(7*i, 7*(i+1)));
			if((i+1)%2!=0) {
				str2.append(",");
			}
			else {
				str2.append("。").append("\n");
			}
		}
		return str2;
	}
  //词频统计函数
	public static int WordFrequency(String str1,String str0) {
		int i=0;
		while(str1.indexOf(str0)!=-1) {
			if(str1.indexOf(str0)!=-1) {
				i++;
				str1=str1.substring(str1.indexOf(str0)+str0.length(), str1.length());
			}
		}
		return i;
	}
}
