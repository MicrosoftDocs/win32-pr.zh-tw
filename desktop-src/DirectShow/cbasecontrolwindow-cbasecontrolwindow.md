---
description: CBaseControlWindow。 CBaseControlWindow 函式-函數方法。
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: 'CBaseControlWindow. CBaseControlWindow (Ctlutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.CBaseControlWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4944d121c4fe99ee36c893a4d51ca0cd72344dfa47dde17629f5ca2a1ce3fd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660763"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a>CBaseControlWindow. CBaseControlWindow 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFilter* 
</dt> <dd>

擁有媒體篩選物件的指標。

</dd> <dt>

*pInterfaceLock* 
</dt> <dd>

要用於鎖定的重要區段指標。

</dd> <dt>

*pName* 
</dt> <dd>

物件描述的指標。

</dd> <dt>

*朋 克* 
</dt> <dd>

如果物件是匯總的一部分，則為控制 **IUnknown** 介面的指標;否則，必須是 **Null**。

</dd> <dt>

*phr* 
</dt> <dd>

變數的指標，此變數會接收 HRESULT 值，指出函式方法的成功或失敗。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




