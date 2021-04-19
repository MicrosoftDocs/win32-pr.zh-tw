---
description: PerformanceAlignWindow 方法會將視窗位置對齊 DWORD 界限，以獲得最大效能。
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: 'CBaseWindow. PerformanceAlignWindow 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PerformanceAlignWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e6e7a54372743d430cd904f47c79414d149cf033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979566"
---
# <a name="cbasewindowperformancealignwindow-method"></a>CBaseWindow. PerformanceAlignWindow 方法

方法會將 `PerformanceAlignWindow` 視窗位置對齊 **DWORD** 界限，以獲得最大效能。

## <a name="syntax"></a>語法


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會將視窗的左邊和上邊緣對齊 DWORD 界限，以改善效能。 如果視窗有父代，則此方法會傳回 \_ [確定]，但會執行對齊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




