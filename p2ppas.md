# English

## Peer-to-Peer

### Advantages:

- The room remains active even if the client acting as the server (usually the host) leaves.
- Maintains the lowest possible latency between clients.

### Disadvantages:

- Overload can occur with a large number of users.
- P2P may not be possible due to NAT environments or firewalls.
- In such cases, techniques like UDP Hole Punching are needed.
- However, even with this, connection may be impossible in certain network environments.
- A `TURN` server would be necessary in these scenarios.

## Peer-as-Server

### Advantages:

- Even if the network environments of individual clients are problematic, it only matters that the server client’s network is functioning properly.
- Less overload on clients, except for the server client, even with many users.
- No need for a `TURN` server.

### Disadvantages:

- If the server client leaves, the room is closed.
- The entire room can experience issues depending on the network environment of the server client.

---

# Korean

## peer to peer

### 장점

- 서버의 역할을 하는 클라이언트 (대부분의 경우 방장)가 나가도 계속 방 유지됨
- 각각의 클라이언트들끼리는 최저의 레이턴시 유지 가능

### 단점

- 사람들 많아지면 과부화 미침
- NAT 환경이나 방화벽으로 P2P 불가능할 수 있음
- 이 경우 UDP Hole Punching 등을 사용해야 함
- 하지만 이래도 특정한 네트워크 환경에서는 아예 접속이 불가능할 수 있음
- 이때는 `TURN` 서버 사용해야함

## peer as server

### 장점

- 각각의 클라이언트의 네트워크 환경이 이상하더라도 서버 역할의 클라이언트의 네트워크만 제대로 작동해도 됨
- 사람들 많이 접속해도 서버 역할의 클라이언트를 제외한 클라이언트들은 과부화가 비교적 덜함
- `TURN` 서버 사용할 필요 X

### 단점

- 서버 역할의 클라이언트가 나가면 방폭
- 서버 역할의 클라이언트의 네트워크 환경에 따라서 방 전체가 문제생길수도있음
