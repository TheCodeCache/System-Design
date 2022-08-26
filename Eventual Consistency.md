# How to handle Eventual Consistency - 

1. Read your own writes
2. Poll the read model (separate read interface component)
3. Pub/Sub model
4. We can classify requests as strongly consistent and eventually consistent.  
   The less important data can be eventually consistent and important/significant data can be ensured to be strongly consistent  
5. Using Version Number

Reference(s):  
1. https://www.beautifulcode.co/blog/38-how-to-handle-eventual-consistency
