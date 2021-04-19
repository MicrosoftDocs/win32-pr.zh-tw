---
description: IsUsingTimeFormat 方法會判斷指定的時間格式是否為目前使用中的格式。
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: 'CSourceSeeking. IsUsingTimeFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8229387364a061febc7bd825e7bc76ee5d9b4a2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978764"
---
# <a name="csourceseekingisusingtimeformat-method"></a>CSourceSeeking. IsUsingTimeFormat 方法

`IsUsingTimeFormat`方法會判斷指定的時間格式是否為目前使用中的格式。

## <a name="syntax"></a>語法


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pformatetc 架構* 
</dt> <dd>

時間格式 GUID 的指標。 請參閱 [**時間格式 guid**](time-format-guids.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所列的其中一個 **HRESULT** 值。



| 傳回碼                                                                               | Description                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | 指定的格式不是目前的格式。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 指定的格式為目前的格式。<br/>     |
| <dl> <dt>**E \_ 指標**</dt> </dl> | **Null** 指標引數。<br/>                      |



 

## <a name="remarks"></a>備註

基類所支援的唯一時間格式是時間 \_ 格式 \_ 媒體 \_ 時間 (100-毫微秒單位) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




