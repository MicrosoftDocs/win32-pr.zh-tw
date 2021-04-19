---
description: SetFormat 方法會初始化格式區塊。
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: 'CMediaType. SetFormat 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08dd05faf514581a3325f4922076ba2053cd0c95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985573"
---
# <a name="cmediatypesetformat-method"></a>CMediaType. SetFormat 方法

`SetFormat`方法會初始化格式區塊。

## <a name="syntax"></a>語法


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pformatetc 架構* 
</dt> <dd>

包含格式區塊之記憶體區塊的指標。

</dd> <dt>

*length* (長度) 
</dt> <dd>

格式區塊的長度（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ; 如果發生錯誤，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

這個方法會為格式區塊配置記憶體，並將 *pformatetc 架構* 指定的緩衝區複製到新的格式區塊。 如果媒體類型已包含格式區塊，則會釋放舊的格式區塊。 方法也會設定 **AM \_ 媒體 \_ 類型** 結構的 **cbFormat** 成員。

若要設定格式類型，請呼叫 [**CMediaType：： SetFormatType**](cmediatype-setformattype.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




