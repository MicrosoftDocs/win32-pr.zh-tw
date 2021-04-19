---
description: ConvertTimeFormat 方法會從一種時間格式轉換成另一種格式。 這個方法會實 IMediaSeeking：： ConvertTimeFormat 方法。
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: 'CSourceSeeking. ConvertTimeFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3869ef5bc9656414ca5b465a04d04a4ca4be41e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990128"
---
# <a name="csourceseekingconverttimeformat-method"></a>CSourceSeeking. ConvertTimeFormat 方法

`ConvertTimeFormat`方法會從一種時間格式轉換成另一種格式。 這個方法會實 [**IMediaSeeking：： ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTarget* 
</dt> <dd>

接收轉換時間之變數的指標。

</dd> <dt>

*pTargetFormat* 
</dt> <dd>

目標格式 GUID 的指標。 如果是 **Null**，則會使用目前的格式。 請參閱 [**時間格式 guid**](time-format-guids.md)。

</dd> <dt>

*來源* 
</dt> <dd>

要轉換的時間值。

</dd> <dt>

*pSourceFormat* 
</dt> <dd>

要轉換之格式的時間格式 GUID 指標。 如果是 **Null**，則會使用目前的格式。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所列的其中一個 **HRESULT** 值。



| 傳回碼                                                                                  | Description                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | Success<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 引數無效<br/>          |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | **Null** 指標引數<br/> |



 

## <a name="remarks"></a>備註

基類所支援的唯一時間格式是時間 \_ 格式 \_ 媒體 \_ 時間 (100-毫微秒單位) 。 這個方法會傳回 E \_ INVALIDARG，但在一般情況下， *PTargetFormat* 和 *pSourceFormat* 都指定時間 \_ 格式 \_ 媒體 \_ 時間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




