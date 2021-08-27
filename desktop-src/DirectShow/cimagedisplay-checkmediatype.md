---
description: CheckMediaType 方法會判斷建議的媒體類型是否與顯示格式相容。
ms.assetid: 567663cf-c79f-4549-9fa9-b16da957d2b1
title: 'CImageDisplay. CheckMediaType 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bad6a7242ba110ad3916d08070eef40a8fa1d5d658ea366732e14a1cd107d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087388"
---
# <a name="cimagedisplaycheckmediatype-method"></a>CImageDisplay. CheckMediaType 方法

`CheckMediaType`方法會判斷建議的媒體類型是否與顯示格式相容。

## <a name="syntax"></a>語法


```C++
HRESULT CheckMediaType(
   const CMediaType *pmtIn
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pmtIn* 
</dt> <dd>

包含媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                  | 描述                              |
|----------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**E \_ 失敗**</dt> </dl>       | 媒體類型無效。<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 媒體類型無效。<br/>           |
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 媒體類型是相容的。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageDisplay 類別**](cimagedisplay.md)
</dt> </dl>

 

 




