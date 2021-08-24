---
description: Get 自動完成方法會抓取 \_ 目前的自動完成狀態旗標。
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: 'CBaseControlWindow.get_AutoShow 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7a5c16e0b460d07255cae113194f672ca3dace6f46827ac613c9559370284beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158791"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a>CBaseControlWindow。取得自動完成 \_ 方法

方法會抓取 `get_AutoShow` 目前的自動中狀態旗標。

## <a name="syntax"></a>語法


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*自動* 
</dt> <dd>

自動化布林值旗標的指標 (0 是 off，1是) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會實 [**IVideoWindow：： \_ get**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) 自動完成方法。 這個屬性可簡化應用程式的視窗顯示存取。 如果這是在) 上設定為 1 (，則在篩選暫停或執行時，通常會隱藏的視窗（通常會在篩選連接之後隱藏）。 不過，當篩選準則停止時，不應該隱藏視窗。 如果此參數設定為 0 (off) ，則只有當應用程式呼叫 CBaseControlWindow 時，才會顯示此視窗 [**： \_ :p**](cbasecontrolwindow-put-visible.md) 的 Ui 可見或 [**CBaseControlWindow \_ ：:p**](cbasecontrolwindow-put-windowstate.md) 不適當的參數 system.windows.window.windowstate。

此成員函式的目的是要透過 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面呼叫外部物件，因此會鎖定重要區段以與相關聯的篩選進行同步處理。 如果您不是從外部物件呼叫，請呼叫 [**CBaseControlWindow：： IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) 成員函式，以取得此屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




