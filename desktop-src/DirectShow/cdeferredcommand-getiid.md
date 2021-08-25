---
description: GetIID 方法會抓取將在其上執行方法之介面 (IID) 的介面識別碼。
ms.assetid: d6eb7d46-294a-4169-96d3-4bed02c48c08
title: 'CDeferredCommand. GetIID 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetIID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c5d43f04d8331f39e46e3223a64c09ad306585a1e29fd7627a0f50159d74cde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910078"
---
# <a name="cdeferredcommandgetiid-method"></a>CDeferredCommand. GetIID 方法

`GetIID`方法會針對將在其上執行方法的介面， (IID) 來抓取介面識別碼。

## <a name="syntax"></a>語法


```C++
REFIID GetIID();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回將在其上執行方法之介面的 IID。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDeferredCommand 類別**](cdeferredcommand.md)
</dt> </dl>

 

 




