---
description: DirectDraw 串流介面
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: DirectDraw 串流介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc922bfed03fd2fac3581168bda35f072871a52
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025705"
---
# <a name="directdraw-streaming-interfaces"></a>DirectDraw 串流介面

> [!Note]  
> 這些 Api 已被取代。 應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md) 篩選器或執行自訂篩選，以從 DirectShow 篩選圖形取得資料。

 

如果您在資料流程中使用支援 DirectDraw 的影片格式，下列介面可讓您更有效地控制資料，而不是更多泛型基底介面。



| 介面                                                  | 描述                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | 設定和抓取資料流程格式以及與媒體資料流程相關聯的 DirectDraw 物件;這個介面衍生自 [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)。 您也可以使用此介面來建立影片範例。 |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | 可讓您將影片範例附加至 DirectDraw 表面;這個介面衍生自 [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) 介面。 每個附加表面都包含裁剪矩形，讓轉譯更容易。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[多媒體串流介面的清單](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



