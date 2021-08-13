---
description: ActivateWindow 方法會根據衍生類別的需求來調整視窗的大小。
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: 'CBaseWindow. ActivateWindow 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.ActivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e00c3ccc43e2583ce8664e62967a22f753148cfa271dd1995e2374c2bfa53c71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658242"
---
# <a name="cbasewindowactivatewindow-method"></a>CBaseWindow. ActivateWindow 方法

`ActivateWindow`方法會根據衍生類別的需求來調整視窗的大小。

## <a name="syntax"></a>語法


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                             | 描述                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 視窗已經啟用。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                      |



 

## <a name="remarks"></a>備註

這個方法會呼叫 [**CBaseWindow：： GetDefaultRect**](cbasewindow-getdefaultrect.md) 方法來判斷視窗大小。 衍生類別應該覆寫 **GetDefaultRect** ，以傳回將顯示之影像的大小。

如果視窗已在使用中，則呼叫 `ActivateWindow` 會將視窗移至 Z 順序的頂端，但不會調整視窗的大小。 如果視窗有父代，也是如此。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




