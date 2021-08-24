---
description: InactivateWindow 方法會會視窗。 在基類中，這個方法會隱藏視窗。
ms.assetid: b575d4fd-dee1-4ae5-abb4-e92ae361e82a
title: 'CBaseWindow. InactivateWindow 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InactivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3cf175a55ab5739b0fa171fe4c9553d3691be82d71b38fd5eb480d6e28043440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567458"
---
# <a name="cbasewindowinactivatewindow-method"></a>CBaseWindow. InactivateWindow 方法

`InactivateWindow`方法會會視窗。 在基類中，這個方法會隱藏視窗。

## <a name="syntax"></a>語法


```C++
virtual HRESULT InactivateWindow();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                             | 描述                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                    |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 視窗已經處於非使用中狀態。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




