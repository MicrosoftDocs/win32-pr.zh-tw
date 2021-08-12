---
description: 本主題討論應用程式如何使用對等群組 Api 連接至對等群組。
ms.assetid: 56fa28d8-3b3a-4cd5-8448-c8c4ce8d0b2c
title: 如何連線到對等群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb1cfd08fde0fc733873648dfae1ffb4f86b713b3ed790430686b641a893d23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612764"
---
# <a name="how-to-connect-to-a-peer-group"></a>如何連線到對等群組

本主題討論應用程式如何使用對等群組 Api 連接至對等群組。

## <a name="joining-a-peer-group"></a>加入對等群組

若要加入對等群組，請呼叫 [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)，傳入對等的身分識別名稱和邀請 (以及選擇性的 PNRP 雲端名稱（如果邀請中的雲端名稱不明確) ）。

如果成功， [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) 會傳回對等群組的控制碼。

如果對等互連先前已加入對等群組，然後關閉該控制碼，則應該透過呼叫 [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) 並傳入對等群組的名稱來重新開啟對等群組。 此呼叫會傳回新的對等群組控制碼。

當對等群組成功聯結之後，對等可以直接連接到對等群組，並藉由呼叫 [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)來開始互動。 連接之後，對等會被視為「線上」。

如果應用程式目前不會與群組互動，它可以維持「離線」狀態。 如果它選擇直接在稍後的實例中參與對等群組，後續的 [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) 呼叫將會使其上線。 對等互連加入對等群組之後，必須至少連接一次，才能夠將記錄發行至對等群組。

## <a name="opening-a-peer-group-without-connecting-offline"></a>開啟對等群組而不連接 (離線) 

通常，您可能會想要讓應用程式連線至對等群組，但不直接參與它、接收和發行記錄更新，但不會傳送或接收資料訊息。 在呼叫 [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)、 [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)或 [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) 之後，應用程式會立即處於「離線」狀態。

離線應用程式可以隨時透過呼叫 [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)上線。 一旦連線之後，對等群組將無法離線，直到與此身分識別相關聯的其他所有應用程式和共用此群組的連接也都關閉為止。

對等群組是共用資源，具有相同的對等群組可供多個應用程式使用。 如果同一個身分識別有一個以上的應用程式，且 Windows 使用者使用相同的對等群組，則它們也會共用相同的基礎資料庫和連接 (鄰近和直接) 。 如果其中任何一個應用程式呼叫 [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)，則參與群組的這個身分識別/使用者的所有其他應用程式也會連接到群組。 如果某個應用程式在群組離線時新增了記錄，其他應用程式也可以看到它。 如此一來，應用程式就必須隨時都可上線。

## <a name="connecting-to-a-peer-group-online"></a>連接至對等群組 (線上) 

若要開始參與群組，請在建立、加入或開啟群組之後，呼叫 [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) 。 在此狀態下，您可以藉由呼叫 [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)，以其他對等參與相同群組的對等來開啟直接連接。

若要偵測連接嘗試是否失敗，請註冊對等 \_ 群組 \_ 事件 \_ 連接 \_ 失敗事件。 如果群組基礎結構找不到另一個要連接的成員，或在同步處理群組資料庫之前連接失敗，而且無法建立另一個連接，就會引發此事件。

雖然在對等上執行的多個應用程式和參與相同對等身分識別的相同群組可能已離線，但任何一個應用程式所 [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) 的呼叫都會導致所有應用程式變成上線。

此外，如果對等上的一個應用程式已連接到群組，則任何其他呼叫 [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) 或 [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) 的應用程式也會立即連線。 如果應用程式呼叫 [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose)，則只有該應用程式的控制碼會關閉。 因此，應用程式所 **PeerGroupOpen** 的後續呼叫會傳回新的群組控制碼，而如果其他任何參與相同群組的應用程式仍在連線，應用程式就會立即上線。

## <a name="sending-and-receiving-data"></a>傳送和接收資料

若要在群組中的特定成員節點之間傳送和接收資料，必須使用您想要與之互動的成員來建立直接連接。 建立直接連線是非同步呼叫 [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)，它會傳入連接群組的控制碼，以及您想要連接之群組內的對等身分識別。 這個方法會傳回連接識別碼。 如果呼叫成功，對 \_ \_ 等群組事件 \_ 直接 \_ 連接事件會在對等上引發，驗證連接識別碼。

若要接收來自其他線上對等的直接連線，請透過呼叫 PeerGroupRegisterEvent 來註冊對等 \_ 群組 \_ 事件 \_ 直接 \_ 連接事件。 [](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)

成功建立直接連線之後，應用程式就可以開始使用 [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)呼叫傳送資料，並傳遞有效的連接識別碼。 多部分資料傳輸的排序是由 **PeerGroupSendData** 處理。 不過，應用程式應該執行適當的通訊協定堆疊，以處理此 API 呼叫所傳回的不透明資料。

若要透過直接連接接收資料，應用程式必須向 PeerGroupRegisterEvent 註冊對等 \_ 群組事件內送 \_ \_ \_ 資料[](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)事件。 事件處理常式會負責取得和排序不透明的資料，並將其傳遞至應用程式。 這項資料是透過呼叫 [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) 與已註冊事件的控制碼，在事件處理常式中取得。

直接連接的關閉方式是呼叫 [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) ，並將先前呼叫所取得的連接識別碼傳入對 [](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)等 \_ 事件 \_ 群組 \_ 直接連接的事件資料中，並傳入 PeerGroupOpenDirectConnection 或接收的連接識別碼 \_ 。

 

 



