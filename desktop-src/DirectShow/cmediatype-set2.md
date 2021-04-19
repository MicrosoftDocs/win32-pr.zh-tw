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
ms.openlocfilehash: e8fd9145ee33dbe4b589b34833836466efa62ada
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "107001056"
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

 

 




