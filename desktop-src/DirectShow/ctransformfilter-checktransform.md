---
description: CheckTransform 方法會檢查輸入媒體類型是否與輸出媒體類型相容。
ms.assetid: 349145e5-c12d-41df-ae37-7846f8aaa423
title: 'CTransformFilter. CheckTransform 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ea4b0bdfefcbbf1003031cd43be7c570a9a95bca235f4a1175b0671e0b4706f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119330748"
---
# <a name="ctransformfilterchecktransform-method"></a>CTransformFilter. CheckTransform 方法

`CheckTransform`方法會檢查輸入媒體類型是否與輸出媒體類型相容。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*mtIn* 
</dt> <dd>

指定輸入類型之 [**CMediaType**](cmediatype.md) 物件的指標。

</dd> <dt>

*mtOut* 
</dt> <dd>

指定輸出類型之 [**CMediaType**](cmediatype.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                                | Description                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 媒體類型是相容的。<br/>     |
| <dl> <dt>**\_ \_ \_ 未接受 VFW E \_ 類型**</dt> </dl> | 媒體類型不相容。<br/> |



 

## <a name="remarks"></a>備註

衍生的類別必須執行此方法。 \_如果篩選器可以接受兩個指定的媒體類型，則傳回 [確定]，否則傳回錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




