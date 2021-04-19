---
description: SetTemporalCompression 方法會指定是否使用時態 (幀) 壓縮來壓縮範例。
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: 'CMediaType. SetTemporalCompression 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetTemporalCompression
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0aba07375c5b5c760c432de704562efb2bea148
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997698"
---
# <a name="cmediatypesettemporalcompression-method"></a>CMediaType. SetTemporalCompression 方法

`SetTemporalCompression`方法會指定是否使用時態性 (幀) 壓縮來壓縮範例。

## <a name="syntax"></a>語法


```C++
void SetTemporalCompression(
   BOOL bCompressed
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bCompressed* 
</dt> <dd>

指定資料流程是否使用時態性壓縮的布林值。 如果資料流程使用時態性壓縮，請將值設定為 **TRUE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會設定 **bTemporalCompression** 成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




