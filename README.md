### 大数据181 刘柄沣 2018310170
# //数组转换成字符串函数
```			public void mouseClicked(MouseEvent e) {```  
```	    		StringBuffer aa = new StringBuffer();//创建StringBuffer对象```  
```	    		aa.append(Btn_click(shuru));```  
```	    		StringBuffer str=aa;```  
```	    		StringBuffer str1=new StringBuffer();```  
```	    		str1=FormatOutput(str);```  
```	    		String str2=new String(str1);```  
```	    		jta.append(str2);```  
```	    		btn.addActionListener(new ActionListener(){```  
```	    			public void actionPerformed(ActionEvent arg0) {```  
```	    				int i=WordFrequency(str2,jta1.getText());```  
```	    				JOptionPane.showMessageDialog(null, "该文字在古诗中出现的次数为:  "+i);}});}});```  
	    
上述程序是主方法里最主要的执行方法，设置了一个事件监听器-当鼠标点击时执行下面命令，既 *mouseClicked(MouseEvent e)* 。当鼠标点击后这个方法配合程序里其他方法可以实现：  
	**1.** 输入需要格式化的字符串，获取字符串并进行格式化，化为有标点的字符串。  
	**2.** 将格式化的字符串赋值给新的StringBuffer类，并设置新的监听器，监听器内容为：当“查询”按钮按下时，可获取查询框里的字符串并进行检索，检索方法在下面会提到。
# //格式化输出函数 
```	        public static StringBuffer FormatOutput(StringBuffer str) {```  
```		StringBuffer str2=new StringBuffer();```  
```		for(int i=0;i<str.length()/7;i++) {```  
```	        str2.append(str.substring(7*i, 7*(i+1)));```  
```		if((i+1)%2!=0) {```  
```		str2.append(",");}```  
```		else {```  
```		str2.append("。").append("\n");}}```  
```		return str2;}```  

索引从零开始，所以在第七个位置加逗号，第十五位置加句号。我还添加了“/n”，进行换行，让古诗整理对齐。往复循环。
# //词频统计函数
```	public static int WordFrequency(String str1,String str0) {```  
```		int i=0;```  
```		while(str1.indexOf(str0)!=-1) {```  
```			if(str1.indexOf(str0)!=-1) {```  
```				i++;```  
```				str1=str1.substring(str1.indexOf(str0)+str0.length(), str1.length());}}```  
```		return i;}}```  

这是上面提到的检索方法，当程序有索引值就继续运行往复循环，如果没有检索到就返回i。当找到字符串去掉后面所有字符串，重置原字符串并删除找到索引位前的字符串。
