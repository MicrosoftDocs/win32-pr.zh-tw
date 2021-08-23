---
description: IsValid 方法會判斷是否已將主要類型指派給這個物件。
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: 'CMediaType 的 IsValid 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsValid
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3611d36cfe19623840f102b820b2b312138b1e116d32fc399927da57e7f47300
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016258"
---
# <a name="cmediatypeisvalid-method"></a>CMediaType. IsValid 方法

`IsValid`方法會判斷是否已將主要類型指派給這個物件。

## <a name="syntax"></a>語法


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果已將主要類型指派給此物件，則傳回 **TRUE** 。 否則，會傳回 **FALSE**。

## <a name="remarks"></a>備註

根據預設， [**CMediaType**](cmediatype.md) 物件會使用 GUID Null 的主要類型進行初始化 \_ 。 呼叫這個方法，以判斷物件是否已正確初始化。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




