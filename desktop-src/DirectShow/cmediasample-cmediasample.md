---
description: CMediaSample。 CMediaSample 函式-函數方法。
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: 'CMediaSample. CMediaSample (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5baa5b791078eaf292b8da89fe50adaf7de9172185f8e6cab8745781030f401f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634688"
---
# <a name="cmediasamplecmediasample-constructor"></a>CMediaSample. CMediaSample 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

忽略。

</dd> <dt>

*pAllocator* 
</dt> <dd>

建立此範例之 [**CBaseAllocator**](cbaseallocator.md) 物件的指標。

</dd> <dt>

*phr* 
</dt> <dd>

忽略。

</dd> <dt>

*pBuffer* 
</dt> <dd>

由呼叫端配置的記憶體緩衝區指標，大小 *長度*。

</dd> <dt>

*length* (長度) 
</dt> <dd>

記憶體緩衝區的長度。

</dd> </dl>

## <a name="remarks"></a>備註

基類不會修改在 *phr* 參數中傳遞的 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

 




