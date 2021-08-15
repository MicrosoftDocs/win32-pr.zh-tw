---
description: SendRepaint 方法會將重新繪製事件傳送至篩選圖形管理員。
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: 'CBaseRenderer. SendRepaint 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendRepaint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9057d1ff733c30da3b3b0d7e960607eadd033dcee0b26994478c6da9156a183e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954787"
---
# <a name="cbaserenderersendrepaint-method"></a>CBaseRenderer. SendRepaint 方法

`SendRepaint`方法會將重新繪製事件傳送至篩選圖形管理員。

## <a name="syntax"></a>語法


```C++
void SendRepaint();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果下列條件成立，則這個方法會將 [**EC 重新 \_ 繪製**](ec-repaint.md) 事件傳送至篩選圖形管理員：

-   輸入 pin 已連線。
-   篩選不會排清資料。
-   未到達資料流程結尾。
-   [**CBaseRenderer：： m \_ bAbort**](cbaserenderer-m-babort.md)旗標為 **FALSE**。
-   [**CBaseRenderer：： m \_ bRepaintStatus**](cbaserenderer-m-brepaintstatus.md)旗標為 **TRUE**。

根據圖形的狀態而定，EC \_ 重新繪製事件可能會導致上游篩選器重新傳送範例、篩選圖形來搜尋其目前位置，或篩選圖形管理員以暫時暫停。  (看到 [**EC 重新 \_ 繪製**](ec-repaint.md)。 ) 此事件可能沒有效率，因此應謹慎使用。 不過，影片轉譯器有時需要重新整理顯示畫面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




