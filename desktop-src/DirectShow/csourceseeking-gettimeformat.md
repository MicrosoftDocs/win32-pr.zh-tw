---
description: CSourceSeeking. GetTimeFormat 方法-GetTimeFormat 方法會抓取目前的時間格式。 這個方法會實 IMediaSeeking：： GetTimeFormat 方法。
ms.assetid: c90804f7-9a0a-423c-8b26-87abf15eddc5
title: 'CSourceSeeking. GetTimeFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a56f9a490699d68d7a043e9385ad458562058f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085216"
---
# <a name="csourceseekinggettimeformat-method"></a>CSourceSeeking. GetTimeFormat 方法

方法會抓取 `GetTimeFormat` 目前的時間格式。 這個方法會實 [**IMediaSeeking：： GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pformatetc 架構* 
</dt> <dd>

接收時間格式 GUID 之變數的指標。 請參閱 [**時間格式 guid**](time-format-guids.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所列的其中一個 **HRESULT** 值。



| 傳回碼                                                                               | Description                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | Success<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl> | **Null** 指標值<br/> |



 

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

 

 




