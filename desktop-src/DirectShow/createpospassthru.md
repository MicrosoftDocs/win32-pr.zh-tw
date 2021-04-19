---
description: CreatePosPassThru 函數會建立 CPosPassThru 物件或 CRendererPosPassThru 物件。
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: 'CreatePosPassThru 函式 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePosPassThru
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08735a0bac2cc5aa8f5bb61461f10097435ad9c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981655"
---
# <a name="createpospassthru-function"></a>CreatePosPassThru 函式

`CreatePosPassThru`函數會建立 [**CPosPassThru**](cpospassthru.md)物件或 [**CRendererPosPassThru**](crendererpospassthru.md)物件。

## <a name="syntax"></a>語法


```C++
STDAPI CreatePosPassThru(
   LPUNKNOWN pAgg,
   BOOL      bRenderer,
   IPin      *pPin,
   IUnknown  **ppPassThru
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAgg* 
</dt> <dd>

這個物件之擁有者的指標。 如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。 否則，請將此參數設定為 **Null**。

</dd> <dt>

*bRenderer* 
</dt> <dd>

指定篩選是否為轉譯器的布林值。 如果篩選器是轉譯器，請使用 **TRUE** 值，否則為 **FALSE** 。 如果值為 **TRUE**，這個方法會建立 [**CRendererPosPassThru**](crendererpospassthru.md) 類別的實例。 如果值為 **FALSE**，則方法會建立 **CPosPassThru** 類別的實例。

</dd> <dt>

*pPin* 
</dt> <dd>

篩選器輸入釘選上 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。

</dd> <dt>

*ppPassThru* 
</dt> <dd>

接收物件的 **IUnknown** 介面指標之變數的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 S OK。 否則，會傳回 **HRESULT** 值，指出錯誤的原因。

## <a name="remarks"></a>備註

這個方法會使用 [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) 介面來建立物件。 物件是從 Quartz.dll 動態載入的。

如果函式成功，則傳回的 **IUnknown** 介面具有未處理的參考計數。 呼叫端必須釋放介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPosPassThru 類別**](cpospassthru.md)
</dt> </dl>

 

 




