---
description: CTransformInputPin. EndOfStream 方法-EndOfStream 方法會通知 pin，不需要額外的資料。 這個方法會實 IPin：： EndOfStream 方法。
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: 'CTransformInputPin. EndOfStream 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2035d0261447826098162f480ddc959544b101b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084976"
---
# <a name="ctransforminputpinendofstream-method"></a>CTransformInputPin. EndOfStream 方法

`EndOfStream`方法會通知 pin，不需要任何其他資料。 這個方法會實 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                           | Description                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>                         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>               | Pin 目前正在排清。<br/>       |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | 輸出針腳未連接。<br/> |
| <dl> <dt>**VFW \_ E \_ 運行時 \_ 錯誤**</dt> </dl> | 發生執行階段錯誤。<br/>       |
| <dl> <dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt> </dl>   | 已停止 pin。<br/>              |



 

## <a name="remarks"></a>備註

這個方法會呼叫篩選準則的 [**CTransformFilter：： EndOfStream**](ctransformfilter-endofstream.md) 方法，以傳遞下游的結束資料流程通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




