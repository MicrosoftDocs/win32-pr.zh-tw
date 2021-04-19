---
description: 在下列情況中，multipoint 通訊端的描述通常是在兩個平面中的其中一個 (控制項或資料) 中定義其角色。
ms.assetid: 34f639e2-9363-4f3f-a8de-b7c5d12618c9
title: 聯結 Multipoint 離開的語義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df12683838fbad89f717b08d7a19802f24556761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982358"
---
# <a name="semantics-for-joining-multipoint-leaves"></a>聯結 Multipoint 離開的語義

在下列情況中，multipoint 通訊端的描述通常是在兩個平面中的其中一個 (控制項或資料) 中定義其角色。 您應該瞭解這個相同的通訊端在另一個平面中具有角色，但不會提及這項功能，以便讓參考保持簡短。 例如，當對 "c \_ 根通訊端" 進行參考時，這可以是 c \_ 根/d \_ 根或 c \_ 根/d 分 \_ 葉通訊端。

在根控制項平面配置中，會以兩種不同的方式，將新的分葉節點新增至多點會話。 在第一個方法中，根目錄會使用 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 來起始與分葉節點的連接，並邀請它成為參與者。 在分葉節點上，對等應用程式必須已建立 c 分 \_ 葉通訊端，並使用 [**接聽**](/windows/desktop/api/Winsock2/nf-winsock2-listen) 將它設定為接聽模式。 \_當受邀加入會話時，分葉節點會收到 FD 接受指示，並透過呼叫 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)來指示其聯結意願。 當聯結作業完成時，根應用程式就會收到 FD \_ 連接指示。 

在第二個方法中，角色基本上是反向的。 根應用程式會建立 c \_ 根通訊端，並將它設定為接聽模式。 希望加入會話的分葉節點會建立 c 分 \_ 葉通訊端，並使用 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 來起始連接和要求進場。 \_當傳入的進場要求抵達時，根應用程式會收到 FD 接受，並藉由呼叫 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)來認可分葉節點。 當分葉節點 \_ 被許可時，會收到 FD CONNECT。

在 nonrooted 控制平面中，如果所有節點都是 c 分 \_ 葉，則會使用 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 來起始將節點加入現有的 multipoint 會話中。 \_當聯結已完成，且傳回的通訊端描述項可在 multipoint 會話中使用時，就會提供 FD 連接指示。 在 IP 多播的案例中，這會對應至 IP \_ 新增 \_ 成員資格通訊端選項。

如果您熟悉 IP 多播使用無連接 UDP 通訊協定的 (讀者，可能會擔心此處提供的連接導向語義。 尤其是在 UDP 通訊端上使用 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 並等候 FD 連接指示的概念 \_ 可能會麻煩。 但是，將連接導向的語義套用至不需連線的通訊協定有很大的引用。 它是允許的，有時也很有用，例如在 UDP 通訊端上叫用標準 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) 函式。 將連接導向的語義套用至無連接通訊端的一般結果是這類通訊端的使用方式的限制，而這也是這種情況。 **WSAJoinLeaf** 中使用的 UDP 通訊端將會有某些限制，並等候 FD \_ 連接指示 (在此案例中，只是表示已傳送對應的 IGMP 訊息) 這種限制。 ) 

因此，應用程式會使用 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 作為下列三個實例：

-   Multipoint 根和邀請新分葉加入會話
-   對根 multipoint 會話提出進場要求的分葉
-   搜尋進場至 nonrooted multipoint 會話的分葉 (例如 IP 多播) 

 

 



