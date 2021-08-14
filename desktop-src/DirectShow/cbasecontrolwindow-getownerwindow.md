---
description: GetOwnerWindow 方法會抓取擁有的視窗控制碼 m \_ hwndOwner。
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: 'CBaseControlWindow. GetOwnerWindow 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetOwnerWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cdb3073d1dd8055986b905d6e8f50967a304e5f294b0ffcaeddcd50d8c0ee33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432508"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a>CBaseControlWindow. GetOwnerWindow 方法

方法會抓取 `GetOwnerWindow` 擁有的視窗控制碼（ **m \_ hwndOwner**）。

## <a name="syntax"></a>語法


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回擁有者視窗。

## <a name="remarks"></a>備註

在不呼叫介面方法的情況下，抓取擁有視窗。 使用這個成員函式，而不是 [**CBaseControlWindow：： get \_ owner**](cbasecontrolwindow-get-owner.md)，除非您是透過 [**IVideoWindow：： get \_ owner**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) 方法在外部呼叫這個成員函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




