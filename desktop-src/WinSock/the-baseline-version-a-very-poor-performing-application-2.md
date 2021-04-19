---
description: 在 Windows 通訊端中執行效能不佳的應用程式的基準版本 (Winsock) 。
ms.assetid: 923884c4-f1bd-4f72-983e-6158f368e0dd
title: 基準版本：執行效能不佳的應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c094be5fd5cf6e3b9eaeb07c7ff38880e651dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971844"
---
# <a name="the-baseline-version-a-very-poor-performing-application"></a>基準版本：執行效能不佳的應用程式

用來計算更新的初始、不良執行程式碼範例如下所示：

> [!Note]  
> 為了簡單起見，下列範例中沒有錯誤處理。 任何實際執行應用程式一律會檢查傳回值。

 

> [!WARNING]
> 應用程式的前幾個範例提供刻意不佳的效能，以說明程式碼變更可能帶來的效能改進。 請勿在您的應用程式中使用這些程式碼範例;它們僅供說明之用。

 


```C++
#include <windows.h>

BOOL Map[ROWS][COLS];

void LifeUpdate()
{
    ComputeNext( Map );
    for( int i = 0 ; i < ROWS ; ++i )     //serialized
        for( int j = 0 ; j < COLS ; ++j )
            Set( i, j, Map[i][j] );    //chatty
}

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    setsockopt( s, SO_SNDBUF, &Zero, sizeof(int) );
    bind( s, ... );
    connect( s, ... );
    send( s, &row, 1 );
    send( s, &col, 1 );
    send( s, &bAlive, 1 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



在此狀態下，應用程式會有最差的可能網路效能。 這個範例應用程式版本的問題包括：

-   應用程式很多對話。 每個交易太小，不需要逐一更新資料格。
-   即使可以同時更新資料格，仍會將交易嚴格序列化。
-   傳送緩衝區會設定為零，而且應用程式會針對每個傳送產生200毫秒的延遲，每個資料格三次。
-   應用程式非常大量連接，每個資料格連接一次。 由於每一筆交易的等候時間狀態超過600毫秒，因此應用程式會根據指定目的地的每秒連線數限制。
-   應用程式為 fat;許多交易對伺服器狀態沒有任何影響，因為許多資料格不會因為更新而變更。
-   應用程式表現不良的串流;小型傳送會耗用大量的 CPU 和 RAM。
-   應用程式針對其傳送採用位元組由小到大的標記法。 這對目前的 Windows 平臺是自然的假設，但長期的程式碼可能會有危險。

## <a name="key-performance-metrics"></a>關鍵效能計量

下列效能度量會以來回時程表示 (RTT) 、Goodput 和通訊協定額外負荷。 請參閱 [網路術語](network-terminology-2.md) 主題以取得這些詞彙的說明。

-   儲存格時間、單一資料格更新的網路時間，需要 \* 有4個 RTT + 600 毫秒的 Nagle 和延遲的 ACK 互動。
-   Goodput 小於6個位元組。
-   通訊協定額外負荷為99.6%。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[改善應用程式緩慢](improving-a-slow-application-2.md)
</dt> <dt>

[網路術語](network-terminology-2.md)
</dt> <dt>

[修訂1：清除明顯的](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[修訂2：重新設計較少的連接](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[修訂3：壓縮的區區塊轉送](revision-3-compressed-block-send-2.md)
</dt> <dt>

[未來的改進](future-improvements-2.md)
</dt> </dl>

 

 



