---
description: Put \_ WindowStyleEx 方法會設定擴充的視窗樣式。
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: 'CBaseControlWindow.put_WindowStyleEx 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee04cf2d2b2dcaafdaf4e989fd1118abf447698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991244"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a>CBaseControlWindow. put \_ WindowStyleEx 方法

`put_WindowStyleEx`方法會設定擴充的視窗樣式。

## <a name="syntax"></a>語法


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*WindowStyleEx* \[在\]
</dt> <dd>

值，指定控制項視窗的樣式。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR。

## <a name="remarks"></a>備註

這個方法會使用擴充的視窗樣式。 如需延伸視窗樣式的完整清單，請參閱 Microsoft Win32 **CreateWindowEx** 函數。 若要變更視窗樣式，請取出目前的視窗樣式，然後加入或移除必要的位欄位。

請勿使用下列視窗樣式，因為它們不會經過驗證。

-   WS \_ 已停用
-   WS \_ HSCROLL
-   WS \_ ICONIC
-   WS \_ 最大化
-   WS \_ 最小化
-   WS \_ VSCROLL

有一些例外狀況 (記下) ，可接受的旗標與 Win32 **CreateWindow** 函數所允許的旗標相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




