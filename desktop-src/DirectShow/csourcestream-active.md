---
description: 使用中的方法會通知釘選篩選現在為使用中狀態。 這個方法會覆寫 CBasePin：： Active 方法。 如果連接的是連接的，這個方法會啟動串流執行緒。
ms.assetid: ea32b602-2583-4de6-96ec-6ea875c49d14
title: 'CSourceStream 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a161c82621f29b916e03fbc2e59ec762871940b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983069"
---
# <a name="csourcestreamactive-method"></a>CSourceStream 方法

`Active`方法會通知釘選篩選現在已在使用中。 這個方法會覆寫 [**CBasePin：： Active**](cbasepin-active.md) 方法。 如果連接的是連接的，這個方法會啟動串流執行緒。

## <a name="syntax"></a>語法


```C++
HRESULT Active();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                             | Description                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Pin 已在使用中。<br/>  |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                    |
| <dl> <dt>**E \_ 失敗**</dt> </dl>  | 無法啟動執行緒。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 




