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
