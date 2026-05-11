F1 — User Registration & Authentication
- User registration (FR-1)
- User login (FR-2)
- Session/token management (FR-3)
  
F2 — Private Messaging
- Send 1–1 messages (FR-4)
- Receive real-time messages (FR-7)
- Store private messages (FR-8)
- Retrieve private chat history (FR-9)
  
F3 — Group Chat System
- Create groups (FR-6)
- Join groups (FR-6)
- Send group messages (FR-5)
- Receive group messages in real time (FR-7)
- Store group messages (FR-8)
- Retrieve group history (FR-9)
  
F4 — Real-Time Delivery System (Messaging Infrastructure Layer)
- Message routing (private + group) (FR-7)
- Real-time delivery mechanism (FR-7)

(this is NOT architecture like WebSocket/Redis — just functional capability grouping)


F5 — Message Persistence System
- Store all messages (FR-8)
  
F6 — Message History System
- Retrieve messages (FR-9)
  
F7 — Input Validation System
- Validate user inputs (FR-10)
- Validate message payloads (FR-10)
