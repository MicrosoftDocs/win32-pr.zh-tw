---
description: Set 方法會設定另一種媒體類型的媒體類型。
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: CMediaType： Set 方法 (Mtype .h) -Mtype [ref] 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 350e88cefa7c0f5f6946218d220fcad4a118cf53e203a68eeb9f75c0d0eace1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156061"
---
# <a name="cmediatypeset-method-mtypeh"></a>CMediaType： Set 方法 (Mtype. h) 

`Set`方法會設定另一種媒體類型的媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mtype* \[裁判\]
</dt> <dd>

[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 \_ [確定] 或 [E \_ OUTOFMEMORY]。

## <a name="remarks"></a>備註

這個方法會從 *mtype* 複製整個媒體類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




