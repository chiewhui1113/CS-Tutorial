# SRAM和DRAM的区别
	
![CISC](../Assets/CO/cisc_risc.jpg)

## 评论区指正
诺丁山下的大渣猫：指令数目和寄存器数量是没有具体界定的，这事情我问过 Patterson。CISC可以有固定字长，比如PDP-8架构。访存指令和RISC CISC无关，比如m2m型RISC不利用load store 访存。控制方式归根结底都是时序逻辑电路，而且CISC不一定要使用微指令。现代处理器设局周期和指令集关系也不大了，真正瓶颈包括eda软件等等。应用方面，电脑上用RISC的也越来越多了，比如华为泰山芯片，苹果m系列芯片。