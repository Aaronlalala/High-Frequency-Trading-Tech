- What is buffering the event? What does the event mean in this context? How does this relate to high frequency trading?
- UTM, QEMU.



# Lecture Content

- Market order
- Round lot: multiple of hundreds.
- What is session? What is number of messages send per session.
- What is a stop quote
- Fractional share trading
- Market order is bad. LULD, Limit up, limit down.
- Messages from traders
  - New Order: Modifying order is fater than new order. Modifying order is easier for exchange to operate, it only needs to move the queue.
  - Modify Order: how does modifying order change your queue position? If recude the size, still stay in the front of the line. If increase the size, you priority drops. This is to motivate traders to post large orders (liquidity) as soon as possible.
  - Cancel Order
    - CME Cancel on disconnect. 