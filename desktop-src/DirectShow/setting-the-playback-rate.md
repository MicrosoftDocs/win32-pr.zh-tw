---
description: 設定播放速率
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: 設定播放速率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8a3297ca376b0cc55e4df4884b22d1cb2df81b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972295"
---
# <a name="setting-the-playback-rate"></a>設定播放速率

若要變更播放速率，請呼叫 [**IMediaSeeking：： SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) 方法。 以原始費率的分數指定新的速率。 例如，若要以兩倍的一般速度播放，請使用下列程式：


```C++
pSeek->SetRate(2.0)
```



大於1的速率比平常更快。 介於零和1之間的速率低於一般。 負數會定義為回溯播放，但實際上大部分的篩選都不支援。 目前沒有任何標準的 DirectShow 篩選支援反向播放。

無論播放速率為何，目前的位置和停止位置一律會相對於原始來源來表示。 例如，如果原始程式檔的長度為20秒，且正常播放速率為10秒，則將目前的位置設為10秒將會搜尋到檔案的中間。 如果播放速率為2.0，則停止位置為20秒，而您要搜尋10秒的位置，該檔案將會播放5秒的即時：10秒鐘的時間，這兩倍的正常播放速度。 在2.0 的播放速率中，目前的位置會以參考時鐘的速率倍增加。

 

 



