---
description: Get \_ Visible 方法會抓取目前的視窗可見度。
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: 'CBaseControlWindow.get_Visible 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef75aaf396e8677e9c470239d5dfca747729b534b67f8fef53a065280175f017
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017376"
---
# <a name="cbasecontrolwindowget_visible-method"></a>CBaseControlWindow。取得 \_ Visible 方法

方法會抓取 `get_Visible` 目前的視窗可見度。

## <a name="syntax"></a>語法


```C++
HRESULT get_Visible(
   long *pVisible
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVisible* 
</dt> <dd>

自動化布林值旗標的指標 (0 是 off，1是) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

如果視窗具有 WS 可見樣式，則這個成員函式會傳回 1 \_ ; 否則會傳回0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




