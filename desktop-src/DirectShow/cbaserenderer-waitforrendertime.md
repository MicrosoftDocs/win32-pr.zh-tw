---
description: WaitForRenderTime 方法會等候目前樣本的呈現時間。
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: 'CBaseRenderer. WaitForRenderTime 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForRenderTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43a537728ca0874fa1dfd69b4712bcc97cf23850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985938"
---
# <a name="cbaserendererwaitforrendertime-method"></a>CBaseRenderer. WaitForRenderTime 方法

`WaitForRenderTime`方法會等候目前樣本的呈現時間。

## <a name="syntax"></a>語法


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值。



| 傳回碼                                                                                           | Description                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>                                                       |
| <dl> <dt>**VFW \_ E \_ 狀態 \_ 已變更**</dt> </dl> | 篩選準則狀態會在呈現時間到達之前變更。<br/> |



 

## <a name="remarks"></a>備註

這個方法會等候，直到發生下列其中一種情況：

-   範例的呈現時間抵達，此時可以轉譯範例。
-   篩選會停止或開始排清資料。

如果呈現時間抵達， [**CBaseRenderer：： m \_ RenderEvent**](cbaserenderer-m-renderevent.md) 事件就會收到信號。 如果狀態變更，則會發出 [**CBaseRenderer：： m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md) 事件的信號。 這個方法會等候兩個事件。 必要時，衍生類別可以覆寫這個方法以等候其他事件。

當等候開始時，這個方法會呼叫 [**CBaseRenderer：： OnWaitStart**](cbaserenderer-onwaitstart.md) 方法，而當等候完成時，則會呼叫 [**CBaseRenderer：： OnWaitEnd**](cbaserenderer-onwaitend.md) 方法。 這兩種方法都不會在基類中執行任何作業，但衍生類別可以覆寫它們。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




