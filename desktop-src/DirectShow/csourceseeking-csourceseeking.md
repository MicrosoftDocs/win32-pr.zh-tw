---
description: CSourceSeeking。 CSourceSeeking 函式-函數方法。
ms.assetid: a51d90c9-4046-42dc-b7cf-51b904c5f57a
title: 'CSourceSeeking. CSourceSeeking (Ctlutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fcca70408e76466a88c620e3907271d49930973
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098816"
---
# <a name="csourceseekingcsourceseeking-constructor"></a>CSourceSeeking. CSourceSeeking 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CSourceSeeking(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         CCritSec  *pLock
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

包含物件名稱之字串的指標。 如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。

</dd> <dt>

*朋 克* 
</dt> <dd>

這個物件之擁有者的指標。 如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。 否則，請將此參數設定為 **Null**。

</dd> <dt>

*phr* 
</dt> <dd>

**HRESULT** 值的指標。 忽略。

</dd> <dt>

*pLock* 
</dt> <dd>

[**CCritSec**](ccritsec.md)物件的指標。 在您的衍生類別中，宣告 **CCritSec** 成員變數，並針對此參數使用它的位址。 `CSourceSeeking`類別會使用此重要區段來同步處理開始和停止時間、持續時間和播放速率的存取。 當您在衍生類別中存取這些變數時，請保留此鎖定。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




