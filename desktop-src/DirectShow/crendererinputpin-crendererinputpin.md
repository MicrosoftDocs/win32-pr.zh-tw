---
description: CRendererInputPin 方法是一種函式方法。
ms.assetid: 272f864e-d6a8-4a9e-b72f-892147db9970
title: 'CRendererInputPin. CRendererInputPin (Renbase. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6888b234b87a48fc89f70c0db36122cbf7289ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982697"
---
# <a name="crendererinputpincrendererinputpin-constructor"></a>CRendererInputPin. CRendererInputPin 函數

`CRendererInputPin`方法是一種函式方法。

## <a name="syntax"></a>語法


```C++
CRendererInputPin(
   CBaseRenderer *pRenderer,
   HRESULT       *phr,
   LPCWSTR       Name
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pRenderer* 
</dt> <dd>

[**CBaseRenderer**](cbaserenderer.md)物件的指標，該物件會執行篩選。

</dd> <dt>

*phr* 
</dt> <dd>

接收 **HRESULT** 值之變數的指標。

</dd> <dt>

*名稱* 
</dt> <dd>

包含 pin 識別碼之寬字元字串的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CRendererInputPin 類別**](crendererinputpin.md)
</dt> </dl>

 

 




