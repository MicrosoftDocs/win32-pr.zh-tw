---
description: CheckStreaming 方法會判斷 pin 是否可以接受範例。
ms.assetid: fa063966-4c72-466e-933c-def6a6818621
title: 'CTransformInputPin. CheckStreaming 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e5c49a00054547193e3f492f0731f77af8331a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989631"
---
# <a name="ctransforminputpincheckstreaming-method"></a>CTransformInputPin. CheckStreaming 方法

`CheckStreaming`方法會判斷 pin 是否可以接受範例。

## <a name="syntax"></a>語法


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下表所列的其中一個 **HRESULT** 值。



| 傳回碼                                                                                           | Description                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>                         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>               | Pin 目前正在排清。<br/>       |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | 輸出針腳未連接。<br/> |
| <dl> <dt>**VFW \_ E \_ 運行時 \_ 錯誤**</dt> </dl> | 發生執行階段錯誤。<br/>       |
| <dl> <dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt> </dl>   | 已停止 pin。<br/>              |



 

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBaseInputPin：： CheckStreaming**](cbaseinputpin-checkstreaming.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




