---
description: DoSetWindowStyle 方法會變更典型或延伸的視窗樣式。
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: 'CBaseControlWindow. DoSetWindowStyle 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoSetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3b1f72ace792f13f88fbf0ce1e0edaf7b08789ecba88aede0b4094e9e75ae52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640878"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a>CBaseControlWindow. DoSetWindowStyle 方法

`DoSetWindowStyle`方法會變更典型或延伸的視窗樣式。

## <a name="syntax"></a>語法


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Style* 
</dt> <dd>

適當的視窗樣式。

</dd> <dt>

*WindowLong* 
</dt> <dd>

值，指定要設定的樣式。 必須是下列其中之一：



| 標籤 | 值 |
|--------------|--------------------------------------|
| GWL \_ 樣式   | 取出視窗樣式。          |
| GWL \_ EXSTYLE | 取出擴充的視窗樣式。 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

這個成員函式會呼叫 Win32 **SetWindowLong** 函式來設定視窗樣式，然後在目前的位置重新配置視窗。 這個成員函式是由 [**CBaseControlWindow：:p 的 \_ System.windows.window.windowstyle**](cbasecontrolwindow-put-windowstyle.md) 和 [**CBaseControlWindow：:p 的工作 \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) 成員函式所呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




