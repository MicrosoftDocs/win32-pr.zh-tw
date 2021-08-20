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
ms.openlocfilehash: a3c077b6cf00f61565124f3d79ad905f6d34a3d8da50d58396e2df1bd35b0d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016466"
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

 

 




