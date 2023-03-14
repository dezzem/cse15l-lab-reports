# Less Command Line Options (Week 3 Improvement)

`-m`
* Causes `less` to display what percentage you are into the text

Examples: 

`less -m written_2/travel_guides/berlitz1/HandRHawaii.txt`
> Displays written_2/travel_guides/berlitz1/HandRHawaii.txt one line at a time. Percentage is useful to show how far your are into the text

![image](https://user-images.githubusercontent.com/122496316/224883985-bfb27a51-8bb0-4ac6-9881-7e2c55000b47.png)

![image](https://user-images.githubusercontent.com/122496316/224884095-efa68dea-e770-489d-a701-7dc135c18da0.png)

`less -m  written_2/travel_guides/berlitz1/HandRHongKong.txt`
> Displays written_2/travel_guides/berlitz1/HandRHongKong.txt one line at a time. Percentage helps show that this text is shorter than HandRHawaii.txt

![image](https://user-images.githubusercontent.com/122496316/224884582-96e245db-f64e-41c1-ad61-435aa12451a2.png)

![image](https://user-images.githubusercontent.com/122496316/224884400-a9887d70-bd6a-4d87-92c8-c8538445b3a3.png)

---

`-E`
* Causes `less` to end once you reach the end of the file

Examples: 

`less -E written_2/travel_guides/berlitz1/HandRHawaii.txt`
> Displays written_2/travel_guides/berlitz1/HandRHawaii.txt one line at a time. `-E` is helpful if you're trying 
> to read through many files quickly and you want to save the effort of exiting out.

![image](https://user-images.githubusercontent.com/122496316/224889773-d6de43ee-baf0-4b6b-a361-3a7683c456d5.png)

![image](https://user-images.githubusercontent.com/122496316/224889985-208da757-2b87-4ae2-8cde-01e309008933.png)

> Exits at last line

![image](https://user-images.githubusercontent.com/122496316/224889880-12c1fed0-c842-46cc-a784-cd886788fddd.png)


`less -E -m written_2/travel_guides/berlitz1/HandRHongKong.txt`
> Displays written_2/travel_guides/berlitz1/HandRHongKong.txt one line at a time and exits once at the end. 
> Useful with `-m` as it lets you know when `less` is going to end

![image](https://user-images.githubusercontent.com/122496316/224888777-37f30398-e28a-465d-8765-39d2fcacd1ee.png)

![image](https://user-images.githubusercontent.com/122496316/224885071-0c44ee42-d216-4d92-a26f-77be3873c8b2.png)

---

`-X`
* Causes `less` to not clear the screen when you exit

Examples: 

`less -X written_2/travel_guides/berlitz1/HandRHawaii.txt`
> Displays written_2/travel_guides/berlitz1/HandRHawaii.txt one line at a time. Keeps the data on screen after exiting,
>  useful for reading different things at a time and being able to go back to each of them in the command line.

![image](https://user-images.githubusercontent.com/122496316/224886581-d35105df-549f-4b01-a442-c8b27db88765.png)

![image](https://user-images.githubusercontent.com/122496316/224886768-3c8a4e35-2bc8-49f4-9598-c949382c5eef.png)

`less -X -E written_2/travel_guides/berlitz1/HandRHongKong.txt`
> Displays written_2/travel_guides/berlitz1/HandRHongKong.txt one line at a time. Useful because you can read 
> through everything and have it automatically close while keeping the text in the command line. 
> Saves the trouble of pulling everything up and exiting each time.

![image](https://user-images.githubusercontent.com/122496316/224887165-e6640dba-c8cb-418a-8d3a-86f2d6ee5933.png)


---

`-N`
* Causes `less` to show line numbers

Examples: 

`less -N written_2/travel_guides/berlitz1/HandRHongKong.txt`
> Less command for HandRHongKong.txt but shows the line numbers. Usefull for keeping track of position while reading something

![image](https://user-images.githubusercontent.com/122496316/224888306-6bad2cb9-c227-46e7-9608-7b43bc5bf9c8.png)

![image](https://user-images.githubusercontent.com/122496316/224889093-a91dae9b-56f3-4ee2-8a63-ecb4c705547a.png)

`less -m -E -X- N -written_2/travel_guides/berlitz1/HandRHawaii.txt`
> Combines all the options to open HandRHawaii.txt while displaying the line number and percentage through the text.
> Also automaticall exits after last line while keeping text in terminal. Overall useful for a reading while keeping track of
>  location and going through multiple texts.

![image](https://user-images.githubusercontent.com/122496316/224890438-d7565a17-08b6-4f6e-a588-12b8d1fe66d4.png)

![image](https://user-images.githubusercontent.com/122496316/224890583-19de9fe0-b4f7-4225-9531-2f51e5997a88.png)

![image](https://user-images.githubusercontent.com/122496316/224890613-a4a1461e-7c22-4b8b-8747-01c0f941c624.png)

---

### Source: https://phoenixnap.com/kb/less-command-in-linux
