---
description: AddPin 方法會將新的輸出圖釘新增至篩選準則。
ms.assetid: 48850a1f-ecb7-460c-9bfc-ce1d1103a00b
title: 'CSource. AddPin 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.AddPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 224550756f5935ce26c106ba01c9ef64f0767140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977154"
---
# <a name="csourceaddpin-method"></a>CSource. AddPin 方法

`AddPin`方法會將新的輸出圖釘新增至篩選準則。

## <a name="syntax"></a>語法


```C++
HRESULT AddPin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStream* 
</dt> <dd>

[**CSourceStream**](csourcestream.md)物件的指標，該物件會執行釘選。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                   | Description                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | Success<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足<br/> |



 

## <a name="remarks"></a>備註

當您建立衍生自 **CSourceStream** 的新 pin 碼時， **CSourceStream** 的函式會自動呼叫此方法，以將輸出釘選至篩選準則。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSource 類別**](csource.md)
</dt> </dl>

 

 




