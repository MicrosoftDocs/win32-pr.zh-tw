---
description: GetDefaultRect 方法會抓取工作區的預設大小。
ms.assetid: 9eb9e3a4-0d45-4aa3-a496-1b0bd92d4989
title: 'CBaseWindow. GetDefaultRect 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetDefaultRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e64d13a3fe77370d4b5bbefb7d493738b035c40ceebd13cd7f6f0f5c6d03f783
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074612"
---
# <a name="cbasewindowgetdefaultrect-method"></a>CBaseWindow. GetDefaultRect 方法

方法會抓取 `GetDefaultRect` 工作區的預設大小。

## <a name="syntax"></a>語法


```C++
virtual RECT GetDefaultRect();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回預設的矩形。

## <a name="remarks"></a>備註

當視窗啟動時，物件會呼叫這個方法來判斷視窗的工作區應該要有多大。 在基類中，此方法會傳回其高度和寬度是定義的常數 DEFHEIGHT 和 DEFWIDTH 的矩形。 衍生類別應該覆寫這個方法。 若為影片轉譯器，衍生類別通常會傳回原生影片影像的大小。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




