---
description: GetHResult 方法會從叫用的命令抓取 HRESULT 值。
ms.assetid: 7e88a2bd-6b1b-4e59-b185-5dfd501fc37a
title: 'CDeferredCommand. GetHResult 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetHResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b09049bc443991dabe07a7626ffc42097feceee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996508"
---
# <a name="cdeferredcommandgethresult-method"></a>CDeferredCommand. GetHResult 方法

`GetHResult`方法會從叫用的命令抓取 **HRESULT** 值。

## <a name="syntax"></a>語法


```C++
HRESULT GetHResult(
   HRESULT *phrResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*phrResult* 
</dt> <dd>

**HRESULT** 值的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果 **m \_ pQueue** 為 **Null**，則傳回 E ABORT。 否則，會傳回 S \_ OK。

## <a name="remarks"></a>備註

此成員函式會實 [**IDeferredCommand：： GetHResult**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDeferredCommand 類別**](cdeferredcommand.md)
</dt> </dl>

 

 




