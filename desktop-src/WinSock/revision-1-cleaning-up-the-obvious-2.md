---
description: 在此版本的範例程式中，我們進行了幾項明顯的變更，以改善效能。
ms.assetid: ef9d594c-31fe-44c0-b707-47c01e2c5bf0
title: 修訂1：清除明顯的
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5da015620727764d686a0c76649e23137de123099b978d323b94184d4df4bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111609"
---
# <a name="revision-one-cleaning-up-the-obvious"></a>修訂1：清除明顯的

在此版本的範例程式中，我們進行了幾項明顯的變更，以改善效能。 這一版的程式碼遠不受效能調整，但這是一個很好的遞增步驟，可讓您檢查漸進式更佳方法的效果。

> [!WARNING]
> 此應用程式範例提供刻意不佳的效能，以說明程式碼變更可能帶來的效能改進。 請勿在您的應用程式中使用此程式碼範例;這僅供說明之用。

 


```C++
#include <windows.h>

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    BYTE tmp[3];
    tmp[0] = (BYTE)row;
    tmp[1] = (BYTE)col;
    tmp[2] = (BYTE)bAlive;
    bind( s, ... );
    connect( s, ... );
    send( s, &tmp, 3 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



## <a name="changes-in-this-version"></a>此版本中的變更

此版本會反映下列變更：

-   已移除 SNDBUF = 0。 因為未緩衝的傳送和延遲的通知已移除，所以200毫秒的延遲。
-   已移除傳送-傳送-接收行為。 這種變更可消除由於 Nagle 和延遲的 ACK 互動所造成的200毫秒延遲。
-   移除位元組由小到小的假設。 位元組現在依序排列。

## <a name="remaining-problems"></a>剩餘問題

在此版本中，仍會發生下列問題：

-   應用程式仍會以繁重的連接。 由於已移除 600 + 毫秒的延遲，因此應用程式現在會達到每秒12個連接的持續速率。 許多並行連接現在都會發生問題。
-   應用程式仍然是 fat;未變更的儲存格仍會傳播到伺服器。
-   應用程式仍然表現不佳的串流;3位元組傳送仍是小型傳送。
-   應用程式現在會傳送2個位元組/RTT，在直接連線的乙太網路上等於 4 KB/s。 這並不太快，但時間等候可能會先造成問題。
-   額外負荷會降至99.3%，但仍不是很好的額外負荷。

## <a name="key-performance-metrics"></a>關鍵效能計量

下列關鍵效能計量是以來回時程表示 (RTT) 、Goodput 和通訊協定額外負荷。 請參閱 [網路術語](network-terminology-2.md) 主題以取得這些詞彙的說明。

此版本會反映下列效能計量：

-   儲存格時間-2 × RTT
-   Goodput-2 個位元組/RTT
-   通訊協定額外負荷-99.3%

## <a name="related-topics"></a>相關主題

<dl> <dt>

[改善應用程式緩慢](improving-a-slow-application-2.md)
</dt> <dt>

[網路術語](network-terminology-2.md)
</dt> <dt>

[基準版本：執行效能不佳的應用程式](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[修訂2：重新設計較少的連接](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[修訂3：壓縮的區區塊轉送](revision-3-compressed-block-send-2.md)
</dt> <dt>

[未來的改進](future-improvements-2.md)
</dt> </dl>

 

 



