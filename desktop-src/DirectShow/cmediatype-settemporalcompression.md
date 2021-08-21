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
ms.openlocfilehash: d29efb0ec16f99c7354621bc49bd36c4e367375d5eb68a2d94a69c27bfdce2f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954397"
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

 

 




