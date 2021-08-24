---
description: RemovePin 方法會從篩選中移除指定的 pin。 方法不會刪除 pin。
ms.assetid: 104eccfa-3fff-4f47-ba1b-3206eab9eef8
title: 'CSource. RemovePin 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.RemovePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 376c2b292b0bdba9a79593c8264ecce17b916a88cfd49407638d637d1fbda6b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767838"
---
# <a name="csourceremovepin-method"></a>CSource. RemovePin 方法

`RemovePin`方法會從篩選中移除指定的 pin。 方法不會刪除 pin。

## <a name="syntax"></a>語法


```C++
HRESULT RemovePin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStream* 
</dt> <dd>

[**CSourceStream**](csourcestream.md)物件的指標，該物件會執行釘選。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                             | 描述                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                              |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 篩選不包含此 pin。<br/> |



 

## <a name="remarks"></a>備註

「析構函數」方法會呼叫這個方法，以從篩選中移除輸出的釘選。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSource 類別**](csource.md)
</dt> </dl>

 

 




