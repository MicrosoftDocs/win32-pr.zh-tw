---
description: 表示特定的相關資訊。
MS-HAID: vspixengine.PixelHistoryIntersection
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixelHistoryIntersection 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D67A116D-B1D0-4E88-A2FF-611CDF4003B2
api_name:
- PixelHistoryIntersection
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 735adc5396551a18b5e2e2dfba781b358289475e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972754"
---
# <a name="span-idvspixenginepixelhistoryintersectionspanpixelhistoryintersection-structure"></a><span id="vspixengine.pixelhistoryintersection"></span>PixelHistoryIntersection 結構

代表特定的相關資訊

## <a name="syntax"></a>語法


```C++
} PixelHistoryIntersection;
```

## <a name="members"></a>成員

**frameNumber**  
使用這項作業 assocaited 的圖形事件架構。

**開齋節**  
與這項作業相關聯之圖形事件的識別碼。

**renderTargetPtr**  
原本與此作業) 的已捕捉應用程式內 (的呈現目標。

**eventType**  
與這項作業相關聯的事件種類 (具體而言，此事件是否為繪製呼叫) 。

**點**  
畫面格緩衝區中圖元的座標。

**bAssemblerStageGeneratesInstanceID**  
如果輸入組合語言產生實例識別碼，則為 true;否則為 false。

**flags**  
PIXELHISTORYFLAGS 值的組合。 如需詳細資訊，請參閱 PIXELHISTORYFLAGS 列舉。

**fbInitialRed**  
畫面格緩衝區：在合併任何圖元著色器輸出之前，畫面格緩衝區的紅色色彩元件值;也就是在此框架的開頭。

**fbInitialGreen**  
畫面格緩衝區：在合併任何圖元著色器輸出之前，畫面格緩衝區的綠色色彩元件值;也就是在此框架的開頭。

**fbInitialBlue**  
畫面格緩衝區：合併任何圖元著色器輸出之前的畫面格緩衝區藍色色彩元件值;也就是在此框架的開頭。

**fbInitialAlpha**  
畫面格緩衝區：在合併任何圖元著色器輸出之前，畫面格緩衝區 Alpha 色彩元件的值;也就是在此框架的開頭。

**LabelFBInitialRed**  
COM 字串，其中包含與畫面格緩衝區的紅色色彩元件相關聯的標籤名稱（任何圖元網底之前）;也就是在此框架的開頭。

**LabelFBInitialGreen**  
COM 字串，其中包含與畫面格緩衝區的綠色色彩元件相關聯的標籤名稱（任何圖元網底之前）;也就是在此框架的開頭。

**LabelFBInitialBlue**  
COM 字串，其中包含與畫面格緩衝區的藍色色彩元件相關聯的標籤名稱（任何圖元網底之前）;也就是在此框架的開頭。

**LabelFBInitialAlpha**  
COM 字串，其中包含與畫面格緩衝區的 Alpha 色彩元件相關聯的標籤名稱（任何圖元網底之前）;也就是在此框架的開頭。

**fbRed**  
畫面格緩衝區：合併所有圖元著色器輸出之後，畫面格緩衝區的紅色色彩元件值;也就是最後的畫面格緩衝區色彩。

**fbGreen**  
畫面格緩衝區：合併所有圖元著色器輸出之後，畫面格緩衝區的綠色色彩元件值;也就是最後的畫面格緩衝區色彩。

**fbBlue**  
畫面格緩衝區：合併所有圖元著色器輸出之後，畫面格緩衝區藍色色彩元件的值;也就是最後的畫面格緩衝區色彩。

**fbAlpha**  
畫面格緩衝區：合併所有圖元著色器輸出之後，畫面格緩衝區 Alpha 色彩元件的值;也就是最後的畫面格緩衝區色彩。

**LabelFBRed**  
COM 字串，其中包含與畫面格緩衝區的紅色色彩元件相關聯的標籤名稱（在所有圖元陰影之後）;也就是最後的畫面格緩衝區色彩。

**LabelFBGreen**  
COM 字串，其中包含與畫面格緩衝區的綠色色彩元件相關聯的標籤名稱（在所有圖元陰影之後）;也就是最後的畫面格緩衝區色彩。

**LabelFBBlue**  
COM 字串，其中包含與畫面格緩衝區的藍色色彩元件相關聯的標籤名稱（在所有圖元陰影之後）;也就是最後的畫面格緩衝區色彩。

**LabelFBAlpha**  
COM 字串，其中包含與畫面格緩衝區的 Alpha 色彩元件相關聯的標籤名稱（在所有圖元陰影之後）;也就是最後的畫面格緩衝區色彩。

**pixelKillReason**  
指定圖元的色彩比重被終止的原因。

**HResult**  
如果發生錯誤，則包含指定錯誤的 DirectX HRESULT。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



