---
description: 建立 PGM 會話類似于與 TCP 會話相關聯的連接建立常式。
ms.assetid: 777e0106-0314-4ec8-b064-88ceb694614b
title: PGM 寄件者和接收者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e300a0c9de199e1f836e71407caf6487812cf7b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511408"
---
# <a name="pgm-senders-and-receivers"></a>PGM 寄件者和接收者

建立 PGM 會話類似于與 TCP 會話相關聯的連接建立常式。 不過，TCP 會話的重大起飛是反轉用戶端和伺服器的語義; (PGM 傳送者的伺服器) 連線到多播群組，而 (PGM 接收器的用戶端) 等待接受連線。 下列段落詳細說明建立 PGM 傳送者和 PGM 接收器所需的程式設計步驟。 此頁面也會說明適用于 PGM 會話的可用資料模式。

## <a name="pgm-sender"></a>PGM 寄件者

**若要建立 PGM 寄件者，請執行下列步驟**

1.  建立 PGM 通訊端。
2.  [](/windows/desktop/api/winsock/nf-winsock-bind)系結通訊端至 INADDR \_ ANY。
3.  [**連接**](/windows/desktop/api/Winsock2/nf-winsock2-connect) 到多播群組傳輸位址。

任何用戶端都不會執行正式的會話信號交換。 連接程式類似于 UDP [**連接**](/windows/desktop/api/Winsock2/nf-winsock2-connect)，因為它會將端點位址 (多播群組) 與通訊端關聯。 完成之後，資料可能會在通訊端上傳送。

當傳送者建立 PGM 通訊端並將它連接到多播位址時，會建立一個 PGM 會話。 可靠的多播會話是由全域唯一識別碼 (GUID) 和來源埠的組合所定義。 GUID 是由傳輸所產生。 SSource 埠是由傳輸指定，不會提供使用來源埠的控制權。

> [!Note]  
> 不允許接收傳送者通訊端上的資料，並產生錯誤。

 

下列程式碼片段說明如何設定 PGM 寄件者：


```C++

SOCKET        s;
SOCKADDR_IN   salocal, sasession;
int           dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

salocal.sin_family = AF_INET;
salocal.sin_port   = htons (0);    // Port is ignored here
salocal.sin_addr.s_addr = htonl (INADDR_ANY);

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant sender socket options here
//

//
// Now, connect <entity type="hellip"/>
// Setting the connection port (dwSessionPort) has relevance, and
// can be used to multiplex multiple sessions to the same
// multicast group address over different ports
//
dwSessionPort = 0;
sasession.sin_family = AF_INET;
sasession.sin_port   = htons (dwSessionPort);
sasession.sin_addr.s_addr = inet_addr ("234.5.6.7");

connect (s, (SOCKADDR *)&sasession, sizeof(sasession));

//
// We're now ready to send data!
//



```



## <a name="pgm-receiver"></a>PGM 接收器

**若要建立 PGM 接收器，請執行下列步驟**

1.  建立 PGM 通訊端。
2.  [**將套**](/windows/desktop/api/winsock/nf-winsock-bind) 接字系結至傳送者正在傳輸的多播群組位址。
3.  呼叫通訊端上的 [**接聽**](/windows/desktop/api/Winsock2/nf-winsock2-listen) 函式，將通訊端置於接聽模式。 當在指定的多播群組位址和埠上偵測到 PGM 會話時，就會傳回接聽函式。
4.  呼叫 [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) 函數，以取得對應至會話的新通訊端控制碼。

只有原始的 PGM 資料 (ODATA) 會觸發新的會話的接受。 因此，傳輸可能會接收到其他的 PGM 流量 (例如 SPM 或 .RDATA 封包) ，但不會導致 [**接聽**](/windows/desktop/api/Winsock2/nf-winsock2-listen) 函數傳回。

一旦接受會話之後，就會使用傳回的通訊端控制碼來接收資料。

> [!Note]  
> 不允許在接收通訊端上傳送資料，而且會產生錯誤。

 

下列程式碼片段說明如何設定 PGM 接收器：


```C++

SOCKET        s,
              sclient;
SOCKADDR_IN   salocal,
              sasession;
int           sasessionsz, dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

//
// The bind port (dwSessionPort) specified should match that
// which the sender specified in the connect call
//
dwSessionPort = 0;
salocal.sin_family = AF_INET;
salocal.sin_port   = htons (dwSessionPort);    
salocal.sin_addr.s_addr = inet_addr ("234.5.6.7");

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant receiver socket options here
//

listen (s, 10);

sasessionsz = sizeof(sasession);
sclient = accept (s, (SOCKADDR *)&sasession, &sasessionsz);

//
// accept will return the client socket and we are now ready
// to receive data on the new socket!
//



```



## <a name="data-modes"></a>資料模式

PGM 會話有兩種資料模式選項：訊息模式和資料流程模式。

訊息模式適用于需要傳送離散訊息的應用程式，而且是由 SOCK RDM 的通訊端類型所指定 \_ 。 資料流程模式適用于需要將串流資料傳送給接收者的應用程式，例如影片或語音應用程式，且是由 SOCK 資料流程的通訊端類型所指定 \_ 。 此模式的選擇會影響 Winsock 處理資料的方式。

請考慮下列範例：訊息模式的 PGM 傳送者會對 [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) 函式進行三次呼叫，每個呼叫都有100位元組的緩衝區。 這項作業會以三個離散的 PGM 封包的形式出現在網路上。 在接收者端， [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) 函式的每個呼叫只會傳回100個位元組，即使有提供較大的接收緩衝區也是如此。 相反地，使用串流模式的 PGM 傳送者，這些 3 100 位元組傳輸可能會結合到網路上的三個實體封包中 (或合併至接收器端) 上的一個資料 blob。 如此一來，當接收者呼叫其中一個 Windows 通訊端接收函式時，由 PGM 傳輸接收的任何數量的資料都可能會傳回給應用程式，而不需考慮實際傳輸或接收資料的方式。

 

 



