---
description: 在這個版本的應用程式中，會使用壓縮的區區塊轉送資料。 這項變更會導致顯著的效能改進。
ms.assetid: 3f0a129b-5b67-4334-a0aa-cd80ee7018b9
title: 修訂三：壓縮的區區塊轉送
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bba84010a09755c5b978665cbd8aa1b29068ec42294ab7b1e499c631fc6b472
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121278"
---
# <a name="revision-three-compressed-block-send"></a>修訂三：壓縮的區區塊轉送

在這個版本的應用程式中，會使用壓縮的區區塊轉送資料。 這項變更會導致顯著的效能改進。


```C++
BYTE tmp[3*ROWS*COLS];
FIELD Old = Map;
ComputeNext( Map );
n=Compact(Map,Old,tmp);
bind( s, ... );
connect( s, ... );
send( s, tmp, 3*n );
//can't do recv(s,tmp,n)
for(int i=0; i < n; )
    recv( s, tmp+i, n-i );
closesocket( s );
```



## <a name="changes-in-this-version"></a>此版本中的變更

此版本會反映下列變更：

-   儲存格更新不再序列化。
-   由於使用封鎖傳送，因此應用程式不再有對話。
-   使用資料壓縮，因而產生較不 fat 的應用程式。

這一版的應用程式仍有問題;因為使用了大型傳送而沒有接收，所以會有鎖死的風險。 伺服器會針對每3個收到的位元組傳送一個位元組。 如果此範例應用程式的接收緩衝區大小小於1000個位元組，這可能會造成鎖死。

## <a name="key-performance-metrics"></a>關鍵效能計量

下列效能度量會以來回時程表示 (RTT) 、Goodput 和通訊協定額外負荷。 請參閱 [網路術語](network-terminology-2.md) 主題以取得這些詞彙的說明。

此版本會反映下列效能計量：

-   資料格時間— 002 \* RTT
-   Goodput-2 Kb/RTT
-   通訊協定額外負荷-14%

有14% 的額外負荷，6% 是來自乙太網路標頭，而另8% 來自連線啟動和卸載。

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

[修訂2：重新設計較少的連接](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[未來的改進](future-improvements-2.md)
</dt> </dl>

 

 



