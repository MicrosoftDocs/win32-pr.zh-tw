---
description: CRenderedInputPin。 CRenderedInputPin 函式-函數方法。
ms.assetid: bf335750-b776-47bc-978d-e84e8b5259f7
title: 'CRenderedInputPin. CRenderedInputPin (Amextra. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b75ce6b5f91f5bd9019a4bf6e46266269b72ac7a5e719f7a58b2f2e702375a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953827"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a>CRenderedInputPin. CRenderedInputPin 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CRenderedInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pObjectName* 
</dt> <dd>

包含物件之偵錯工具名稱的字串。 如需詳細資訊，請參閱 [**CBaseObject 類別**](cbaseobject.md)。

</dd> <dt>

*pFilter* 
</dt> <dd>

建立此釘選之篩選準則的指標。

</dd> <dt>

*pLock* 
</dt> <dd>

[**CCritSec**](ccritsec.md)鎖定的指標，用來序列化狀態變更。 這可以是與 filter lock [**CBaseFilter：： m \_ pLock**](cbasefilter-m-plock.md)相同的重要區段。

</dd> <dt>

*phr* 
</dt> <dd>

變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。

</dd> <dt>

*pName* 
</dt> <dd>

包含 pin 名稱的寬字元字串 (也用來作為 pin 識別碼) 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amextra (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CRenderedInputPin 類別**](crenderedinputpin.md)
</dt> </dl>

 

 




