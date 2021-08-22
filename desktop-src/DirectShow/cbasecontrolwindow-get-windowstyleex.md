---
description: Get \_ WindowStyleEx 方法會抓取擴充的視窗樣式。
ms.assetid: 72955958-bbda-4b8f-9c28-6d3f5eb56a82
title: 'CBaseControlWindow.get_WindowStyleEx 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 082b541c9f04122616f4f96548f1b1e58d940a6060fb4af1ac0fe51fa4887bb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331208"
---
# <a name="cbasecontrolwindowget_windowstyleex-method"></a>CBaseControlWindow. 取得 \_ WindowStyleEx 方法

方法會抓取 `get_WindowStyleEx` 擴充的視窗樣式。

## <a name="syntax"></a>語法


```C++
HRESULT get_WindowStyleEx(
   long *pWindowStyleEx
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pWindowStyleEx* 
</dt> <dd>

延伸視窗樣式的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會抓取擴充的視窗樣式。 它會呼叫 [**CBaseControlWindow：:D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) 成員函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




