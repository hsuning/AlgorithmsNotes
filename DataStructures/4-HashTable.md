#HashTable #Dictionary
- Search, insert, delete : O(1), instant
- Hash functions: put in a string/int/float (any kind of data) and get back a number (index)
	- consistently maps a name to the same index
	- map different strings to different indexes
	- only returns valid indexes
- Use: 
	- create a mapping from one thing to another thing and look something up
	- filtering out duplicates
	- Caching/memorizing data instead of making your server do work
- Example: {"A":3, "B":2}
- Collision: get assigned a value to a slot that is already assigned to other value
- To avoid collisions (worst case performance): 
	- A low load factor = fewer collision, $\frac{Number Of Items}{Number Of Slots}$ estimate how many empty slots remain in your hash table, grater than 0.7 means you have more items than slots in your array => resize by creating a new array with double size and re-insert all the items
	- A good hash function: distribute values in the array evenly