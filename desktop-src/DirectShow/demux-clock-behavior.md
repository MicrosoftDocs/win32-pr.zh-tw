---
description: Demux 時鐘行為
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Demux 時鐘行為
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ab1976bf123e971f6c3ec08e18c743352d37b73de95901a67abfee5d10a054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821183"
---
# <a name="demux-clock-behavior"></a>Demux 時鐘行為

在 push 模式中，MPEG-2 信號 (demux) 會公開 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) 介面。 它會做為即時來源，因此預設會將其選擇為圖形參考時鐘;如需詳細資訊，請參閱 [即時來源](live-sources.md) 。

-   針對傳輸資料流程，demux 會將其時鐘同步至對應至應用程式最近所對應之音訊或影片串流的 PCR 串流。 就內部而言，demux 會追蹤 PAT 和 PMT 資料表。 當應用程式將基本資料流程 PID 對應到輸出圖釘時，demux 會查閱該 PID 的 PCR 串流，並使用該 PCR 串流。  (目前沒有方法可讓應用程式直接指定 PCR PID。 ) 
-   針對程式資料流程，demux 會將其時鐘同步處理到 SCR 資料流程。

將篩選時鐘同步至 PCR 或 SCR 資料流程可防止資料溢位或下溢，這可能會導致圖形時鐘與資料流程時鐘不同的結果。 demux 也會將多值的值轉譯成 DirectShow 的參考時間，並使用這些值來為媒體範例加蓋時間戳記。 時間戳記適用于下一個畫面格界限;不保證框架界限會與媒體範例的開頭一致。

Demux 可保證時間戳記會以單純的時間增加。 這表示，如果傳輸資料流程所包含的區段（例如商業）是使用與主要程式不同的時鐘所建立的，則 demux 會調整呈現時間戳記，以隱藏下游篩選準則的不連續時間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 MPEG-2 信號信號](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



