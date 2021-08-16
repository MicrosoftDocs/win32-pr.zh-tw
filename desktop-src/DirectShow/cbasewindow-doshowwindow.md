---
description: DoShowWindow 方法會設定視窗的顯示狀態。
ms.assetid: 4180de9d-ef40-40e3-aa37-be54283b1f97
title: 'CBaseWindow. DoShowWindow 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoShowWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fef63e04d0e04f2fe0daa78cd6b33a22fa7c8fa14c57b1e022703dea0914dab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074624"
---
# <a name="cbasewindowdoshowwindow-method"></a>CBaseWindow. DoShowWindow 方法

**DoShowWindow** 方法會設定視窗的顯示狀態。

## <a name="syntax"></a>語法


```C++
HRESULT DoShowWindow(
   LONG ShowCmd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ShowCmd* 
</dt> <dd>

指定視窗顯示方式的旗標。 值可以是針對 [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow)函數的 *nCmdShow* 參數所定義的任何常數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

