---
description: Render 方法會呈現範例。
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: 'CBaseRenderer：轉譯方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Render
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fefd44fe1b913fbba0e3ebfaa6f750b88d40813
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987969"
---
# <a name="cbaserendererrender-method"></a>CBaseRenderer 轉譯方法

`Render`方法會呈現範例。

## <a name="syntax"></a>語法


```C++
virtual Render(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaSample* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表中的值。



| 傳回碼                                                                             | Description                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 篩選已停止，或 *pMediaSample* 為 **Null**。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                                              |



 

## <a name="remarks"></a>備註

這個方法會呼叫純虛擬方法 [**CBaseRenderer：:D orendersample**](cbaserenderer-dorendersample.md)，這會執行實際的工作。 衍生的類別必須執行 **DoRenderSample**。

在呼叫 **DoRenderSample** 之前，這個方法會呼叫 [**CBaseRenderer：： OnRenderStart**](cbaserenderer-onrenderstart.md) 方法。 緊接在之後，它會呼叫 [**CBaseRenderer：： OnRenderEnd**](cbaserenderer-onrenderend.md) 方法。 衍生類別可以視需要覆寫這兩種方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




