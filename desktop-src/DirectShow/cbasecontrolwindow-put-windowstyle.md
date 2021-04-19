---
description: Put \_ system.windows.window.windowstyle 方法會設定標準的視窗樣式。
ms.assetid: 3b3aa035-6aa1-4f11-80d8-03268fcf98e1
title: 'CBaseControlWindow.put_WindowStyle 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f98e6205a45530a0dbcce09d095dfaa2267ccbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983230"
---
# <a name="cbasecontrolwindowput_windowstyle-method"></a>CBaseControlWindow. put \_ system.windows.window.windowstyle 方法

`put_WindowStyle`方法會設定標準的視窗樣式。

## <a name="syntax"></a>語法


```C++
HRESULT put_WindowStyle(
   long WindowStyle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*WindowStyle* 
</dt> <dd>

新的視窗樣式。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

變更視窗樣式時請小心。 在大部分的情況下，應用程式應該取出目前的樣式，然後新增或移除不適當的位。 此程式可讓 Windows 使用的各種內部視窗樣式保持不變。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




