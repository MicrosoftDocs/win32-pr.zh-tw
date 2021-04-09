---
description: 在此修訂中，已重新設計範例應用程式，以消除不必要的連接。
ms.assetid: 0db6ded4-0a59-454e-824e-8cd7f0dc9fec
title: 修訂2：重新設計較少的連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d5a8c8648f43f9ddac93c9d17f667b4b97011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114912"
---
# <a name="revision-two-redesigning-for-fewer-connects"></a>修訂2：重新設計較少的連接

在此修訂中，已重新設計範例應用程式，以消除不必要的連接。

> [!WARNING]
> 此應用程式範例也會提供刻意不佳的效能，以說明程式碼變更可能帶來的效能改進。 請勿在您的應用程式中使用此程式碼範例;這僅供說明之用。

 


```C++
ComputeNext( Map );
bind( s, ... );
connect( s, ... );
for(int i=0 ; i < ROWS ; ++i)
  for(int j=0 ; j < COLS ; ++j)
  {
    BYTE tmp[3];
    tmp[0] = i;
    tmp[1] = j;
    tmp[2] = Map[i][j];
    send( s, tmp, 3 );
    recv( s, &byRet, 1 );
  }
closesocket( s );
```



## <a name="remaining-problems"></a>剩餘問題

修訂中的變更已重新設計應用程式，每個更新只會進行一個 connect。 應用程式仍包含下列效能問題：

-   應用程式仍在序列化和對話中。
-   應用程式仍有 fat 設計;有許多傳送不需要在此設計中進行任何操作。
-   傳送只是3個位元組，這是不佳的串流。

## <a name="key-performance-metrics"></a>關鍵效能計量

下列效能度量會以來回時程表示 (RTT) 、Goodput 和通訊協定額外負荷。 請參閱 [網路術語](network-terminology-2.md) 主題以取得這些詞彙的說明。

此版本會反映下列效能計量：

-   儲存格時間— 1 \* RTT
-   Goodput-4 個位元組/RTT
-   通訊協定額外負荷-96.8%

## <a name="related-topics"></a>相關主題

<dl> <dt>

[改善應用程式緩慢](improving-a-slow-application-2.md)
</dt> <dt>

[網路術語](network-terminology-2.md)
</dt> <dt>

[基準版本：執行效能不佳的應用程式](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[修訂1：清除明顯的](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[修訂3：壓縮的區區塊轉送](revision-3-compressed-block-send-2.md)
</dt> <dt>

[未來的改進](future-improvements-2.md)
</dt> </dl>

 

 



