---
description: Get \_ system.windows.window.windowstate 方法會抓取目前的視窗狀態。
ms.assetid: 118b6710-b041-4a7d-8cdb-b96ae3dcbb09
title: 'CBaseControlWindow.get_WindowState 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5603e846fcf3357f01f896e6a0d34e34da6c355e5d41ab5d8f7b0c344c1a16dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586419"
---
# <a name="cbasecontrolwindowget_windowstate-method"></a>CBaseControlWindow. 取得 \_ system.windows.window.windowstate 方法

方法會抓取 `get_WindowState` 目前的視窗狀態。

## <a name="syntax"></a>語法


```C++
HRESULT get_WindowState(
   long *pWindowState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pWindowState* 
</dt> <dd>

視窗狀態的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會傳回 Microsoft Win32 **ShowWindow** 函數的參數子集。 尤其是，它會 \_ 根據目前的視窗可見度，傳回軟體顯示和軟體 \_ 隱藏。 它也會傳回 SW \_ 最小化和 \_ 最大化軟體，取決於視窗是圖示或展開。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




