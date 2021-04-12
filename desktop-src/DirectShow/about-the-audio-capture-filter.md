---
description: 關於音訊捕獲篩選器
ms.assetid: ff345670-5a75-40d3-a228-8bc22aa76708
title: 關於音訊捕獲篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5e28bef37ca52f0a33fc95b6d2a387cbbe2fb3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109688"
---
# <a name="about-the-audio-capture-filter"></a>關於音訊捕獲篩選器

DirectShow 可透過 [音訊捕獲篩選器](audio-capture-filter.md)，從音效卡上的類比輸入進行捕捉。 此篩選器會使用 waveIn *XXX* api 來控制驅動程式支援這些 api 的任何裝置。 系統上的每張卡片都是由篩選準則的個別實例表示。

音訊捕獲篩選器會將卡片上的每個輸入（例如麥克風或 MIDI 輸入）公開為輸入 pin。 輸入圖釘代表驅動程式公開為音訊來源行的內容。 但是，不會透過這些輸入釘傳送任何資料，也不會連接到其他的 DirectShow 篩選。 它們只是提供一種方法讓應用程式控制輸入。 應用程式可以使用輸入 pin 來啟用或停用輸入，或設定混合的屬性，例如低音均衡、高音均衡、移動流覽等等。 可用的控制項數量取決於驅動程式。 若要完全瞭解並利用特定音效卡的功能，您將需要卡片製造商提供的檔。

> [!Note]  
> 您可以從 CD-Audio 的輸入進行捕捉，但這個音訊串流已經通過數位轉類比轉換器，所以會從原始 CD 中失去音效品質。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊捕獲](audio-capture.md)
</dt> </dl>

 

 



