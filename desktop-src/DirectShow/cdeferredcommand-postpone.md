---
description: 延期方法會為先前佇列的命令指定新的呈現時間。
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: CDeferredCommand) 延後方法 (Ctlutil
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Postpone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 079b9f1a852ff0b9eb6e1c38cea6e24e3ee00107ac46ca15e738e1ef9e0eb8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074362"
---
# <a name="cdeferredcommandpostpone-method"></a>CDeferredCommand. 延遲方法

`Postpone`方法會為先前已排入佇列的命令指定新的呈現時間。

## <a name="syntax"></a>語法


```C++
HRESULT Postpone(
   REFTIME newtime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*newtime* 
</dt> <dd>

新的呈現時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_ \_ \_ \_ 如果已通過 *newtime* ，則傳回已通過的 VFW E 時間。 否則，從清單中解壓縮時，會傳回 [**CCmdQueue：： Remove**](ccmdqueue-remove.md) (的 **HRESULT** ，) 或 [**CCmdQueue：： Insert**](ccmdqueue-insert.md) (當重新插入時) 的變更時間。

## <a name="remarks"></a>備註

此成員函式會實 [**IDeferredCommand：:P ostpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDeferredCommand 類別**](cdeferredcommand.md)
</dt> </dl>

 

 




