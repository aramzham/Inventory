# Inventory
Simple application imitating an inventory from where you can make orders and payments[^1].

Add products to the inventory :hammer:. The frontend will make a call to the inventory service.<br/>
Make a payment on an item :euro:. A message will be sent to Redis indicating that payment is made. :incoming_envelope: This message will be caught by inventory service which will decrease the amount of the item correspondingly.<br/>
A complex scenario :heart_on_fire: :
<ol>
  <li>Create a payment on an inventory item.</li>
  <li>Manage to delete the product in 5 seconds.</li>
</ol>
In the end the payment status should become 'refunded'.

Technologies used:
<ul>
  <li>Microservices architecture</li>
  <li>Event sourcing using Redis</li>
  <li>Database: RedisJSON</li>
  <li>Backend: Python FastAPI :snake:</li>
  <li>Frontend: ReactJS :atom_symbol:</li>
</ul>

[^1]: <a href="https://www.youtube.com/watch?v=Cy9fAvsXGZA">link</a> to the tutarial
