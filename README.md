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
