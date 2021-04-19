---
description: 在下列情況中，multipoint 通訊端的特性通常是藉由在兩個平面中的其中一個 (控制項或資料) 來描述其角色。
ms.assetid: 35e4a8c9-d943-44b8-be61-605b60a6cf5d
title: 用於聯結 Multipoint 葉的 SPI 語義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0e77203e5405f6cb820baba5d545de03e3a8ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001390"
---
# <a name="spi-semantics-for-joining-multipoint-leaves"></a>用於聯結 Multipoint 葉的 SPI 語義

在下列情況中，multipoint 通訊端的特性通常是藉由在兩個平面中的其中一個 (控制項或資料) 來描述其角色。 您應該瞭解這個相同的通訊端在另一個平面中具有角色，但不會提及這項功能，以便讓參考保持簡短。 例如，c \_ 根通訊端的參考可以參考 c \_ 根/d \_ 根或 c \_ 根/d 分 \_ 葉通訊端。

在根控制項平面配置中，會以兩種不同的方式，將新的分葉節點新增至多點會話。 在第一個方法中，根目錄會使用 [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) 來起始與分葉節點的連接，並邀請它成為參與者。 在分葉節點上，對等應用程式必須已建立 c 分 \_ 葉通訊端，並使用 [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) 將它設定為接聽模式。 \_當受邀加入會話時，分葉節點將會收到 FD 接受指示，並藉由呼叫 [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)來指示其聯結意願。 當聯結作業完成時，根應用程式將會收到 FD \_ 連接指示。

在第二個方法中，角色基本上是反向的。 根用戶端會建立 c \_ 根通訊端，並將其設定為接聽模式。 希望加入會話的分葉節點會建立 c 分 \_ 葉通訊端，並使用 [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) 來起始連接和要求進場。 \_當傳入的進場要求抵達時，根用戶端會收到 FD 接受，並藉由呼叫 [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)來認可分葉節點。 當分葉節點 \_ 被許可時，會收到 FD CONNECT。

在 nonrooted 控制平面中，如果所有節點都是 c \_ 葉子，則會使用 [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) 函式來起始將節點加入現有的 multipoint 會話中。 \_當聯結已完成，且傳回的通訊端描述項可在 multipoint 會話中使用時，就會提供 FD 連接指示。 在 IP 多播的案例中，這會對應至 IP \_ 新增 \_ 成員資格通訊端選項。

因此，用戶端會使用 [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)的三個實例：

-   作為 multipoint 根，並邀請新的分葉加入會話。
-   做為對根 multipoint 會話提出進場要求的分葉。
-   作為搜尋進場至 nonrooted multipoint 會話的分葉 (例如 IP 多播。 ) 

 

 
