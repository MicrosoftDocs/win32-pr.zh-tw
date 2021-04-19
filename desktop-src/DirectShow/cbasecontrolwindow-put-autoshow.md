---
description: Put 自動輸入 \_ 方法會設定自動建立狀態旗標。
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: 'CBaseControlWindow.put_AutoShow 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda5c0c4055979537c5cc471053715e29a348f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992887"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a>CBaseControlWindow，put 的 \_ 方法

`put_AutoShow`方法會設定自動中的狀態旗標。

## <a name="syntax"></a>語法


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*自動* 
</dt> <dd>

自動化布林值旗標 (0 是 off，1是) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

這個屬性可簡化應用程式的視窗顯示存取。 如果這是在) 上設定為 1 (，則當篩選暫停或執行時，通常會隱藏的視窗（通常是在連接篩選之後隱藏）。 不過，當篩選準則停止時，不應該隱藏視窗。 如果此設定為 0 (關閉) ，只有當應用程式呼叫 CBaseControlWindow 時，才會顯示視窗 [**：:p 的 ui \_ 可見**](cbasecontrolwindow-put-visible.md) 或 [**CBaseControlWindow：:p \_**](cbasecontrolwindow-put-windowstate.md) 不適當的參數 system.windows.window.windowstate。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




