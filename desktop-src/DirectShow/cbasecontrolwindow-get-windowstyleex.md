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
ms.openlocfilehash: c59336ab57e92e99366494a272f2b995191b494b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996461"
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

 

 




