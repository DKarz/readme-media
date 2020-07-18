# readme-media

<p>
As a proper application, the simulator has a login window which allows to sign up a profile or sign in an existing profile:<br/><br/></p>
<p align="center">  <img width="450" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui1.gif?raw=true">
  <br/><br/><br/>
</p>


<p>
As a user signs in, the following window appears.<br/><br/></p>
 <p align="center"> <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui2.gif?raw=true">
  <br/><br/><br/>
</p>


<p>
  The main window has many interactive widgets that update every 3 seconds showing relevant market information. If we look at the left top corner, four buttons can be seen — the first two are BUY and SELL buttons that open corresponding dialog windows; CONFIGURING opens the settings window where the user can config the filters. The last element is the row is product Combobox – if a product is chosen in the Combobox all the data at the main window will switch to the relevant data corresponding to the product. Under the row, there is a graph area that contains the price dynamics for buy and sell orders respectively. If we look at the middle of the main window, we can see two stacks that are called “Available Bids” and “Available Asks”. Two remarks about the stacks: firstly, the orders in the stacks are merged with respect to the price i.e. if two orders have the same cost, they will be combined with the summed up amount. The second remark is that the orders in the stacks are sorted, this means that there is the best order in the market on the top of each stack. If we move to the right, we see two separate stacks that are the user order’s stack (for user’s orders that are currently in the system) and history stack (for orders that were executed). The upper bar contains essential to user information such as the time, the date, user’s name, and the balance.<br/><br/></p>
 <p align="center"> 
  <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui3.gif?raw=true">
  <br/><br/><br/>
</p>



<p>
  Let us try to buy something – we open the BUY dialog window by clicking the BUY button. The window has an edit line where the user can type the product name, however, the edit line is autocompleted with the product chosen in the Combobox. Then the user chooses the order type (Limit or FOK), amount, and price per unit. Note that the price is already autocompleted with the best price in the market. The GUI says that it is success, so the order appears in the Order’s history stack.<br/><br/></p>
  <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui4.gif?raw=true">
  <br/><br/><br/>
</p>


<p>
If we tried to buy something for a very low price, our order would not be executed but would go to the system orders stack:<br/><br/></p>
  <p align="center"><img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui5.gif?raw=true">
  <br/><br/><br/>
</p>



<p>
We are able to cancel our order if we click on the order. After confirming that we, indeed want to cancel the order, it vanishes from the system. Remark, when a user has created the order, the price was subtracted from the user’s balance. If an order is canceled, the money is returned.<br/><br/></p>
<p align="center">
  <p align="center"><img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui6.gif?raw=true">
  <br/><br/><br/>
</p>


<p align="center">
To sell something, we need to have something. Let us look at our assets by clicking the username or the upper bar – the assets window opens that contains the relevant information about the user's assets.<br/><br/>
  <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui7.gif?raw=true">
  <br/><br/><br/>
</p>



<p align="center">
If there are enough assets, the user is able to make sell FoK order:<br/><br/>
  <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui8.gif?raw=true">
  <br/><br/><br/>
</p>


<p align="center">
Let us open the config window. The first tab: delete-history button, color scheme button, the checkbox that allows to join the buy and sell graphs for products; a user can inform developers about bugs occurring in the program and send it to the server which will save them to the bug_log.txt file.
The second tab consists of the user’s preferable products.
<br/><br/>
  <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui9.gif?raw=true">
  <br/><br/><br/>
</p>



<p align="center">
Preferable products are the products the user wants to see in the Combobox, in the config he/she can add new products and delete old ones. <br/><br/>
  <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui10.gif?raw=true">
  <br/><br/><br/>
</p>


<p align="center">
Apart from switching between products using Combobox, we can use shortcuts on the keyboard (1 for the first product, 2 for the second, etc.). Note that all the windows in the GUI have their shortcuts either. <br/><br/>
  <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui11.gif?raw=true">
  <br/><br/><br/>
</p>
The shortcuts:

Button|	Action
| ------ | ------ |
B|	BUY order window will be opened
S|	SELL order window will be opened
C|	Configuring window will be opened
A|	User assets window will be opened
0|	Chooses “No filter” in the Combobox of preferable products
1-10|	Chooses corresponding product in the Combobox



<p align="center">
If we want to delete a product from the Combobox we can do it in the config.<br/><br/>
  <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui12.gif?raw=true">
  <br/><br/><br/>
</p>


<p align="center">
DELETE HISTORY button clears orders in the Orders’ history stack as well orders stored by the server.<br/><br/>
  <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui13.gif?raw=true">
  <br/><br/><br/>
</p>



<p align="center">
The developers can be informant about the bugs. The message sent from config to the server will be stored in the special file. Apart from the user’s message the server receives other information. It allows us to track the last actions of the user and find out what could cause the issues.<br/><br/>
  <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui14-1.gif?raw=true">
  <br/><br/><br/>
</p>


<p align="center">
The graphs have a slider that narrows down the period of the observation. The leftist position shows the price dynamics throughout the whole period of observation. <br/><br/>
  <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui16.gif?raw=true">
  <br/><br/><br/>
</p>



<p align="center">
If you hover over at a point on the plots, the point’s precise coordinate will be shown.<br/><br/>
  <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui17.gif?raw=true">
  <br/><br/><br/>
</p>


<p align="center">
Sometimes, it so happens that it difficult to compare the price fluctuations using two separate graphs, hence, to make the graphs’ information more readable, a user can join the buy and sell graphs. As a bonus, we have bar charts of the data distribution (Best_Ask/2 + Best_Bid/2) for the last 24 hours of observation.<br/><br/>
  <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui18.gif?raw=true">
  <br/><br/><br/>
</p>



<p align="center">
Studying the analogues made us notice that modern graphical interfaces have dark mode feature. To be up-to-date we have added such a feature, so the color scheme of the GUI can be changed to the dark one in the config.<br/><br/>
  <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui19.gif?raw=true">
  <br/><br/><br/>
</p>


<p align="center">
Now, we are going to demonstrate two important scenarios.
The first is GUI + GUI.
If one GUI makes an order, it appears in the corresponding stack in the other GUI so it can interact with new orders. If one GUI cancels an order, it vanishes from the system, consequently in the other GUI.
<br/><br/>
  <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui20.gif?raw=true">
  <br/><br/><br/>
</p>



<p align="center">
The second scenario is GUI + Market Maker. As MM is launched, the GUI immediately represents the situation in the changing market. <br/><br/>
  <img width="750" src="https://github.com/DKarz/media-lfs/blob/master/GUI/gui21-1.gif?raw=true">
  <br/><br/><br/>
</p>





