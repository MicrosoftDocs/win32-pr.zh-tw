---
description: 在 \_ Windows 的16位版本中，會使用 WM CTLCOLOR 訊息來變更清單方塊的色彩配置、下拉式方塊的清單方塊、訊息方塊、按鈕控制項、編輯控制項、靜態控制項和對話方塊。請注意，如需此訊息和32位版本之 Windows 的相關資訊，請參閱備註。
ms.assetid: e654cf48-550f-4210-9952-20470b9a397a
title: 'WM_CTLCOLOR 訊息 (WindowsX .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c53f18bc42737e44a2137e0c9763dfc41de44f65661ca4754915f7a21317641
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343288"
---
# <a name="wm_ctlcolor-message"></a>WM \_ CTLCOLOR 訊息

在 Windows 的16位版本中，會使用 **WM \_ CTLCOLOR** 訊息來變更清單方塊的色彩配置、下拉式方塊的清單方塊、訊息方塊、按鈕控制項、編輯控制項、靜態控制項和對話方塊。

> [!Note]  
> 如需此訊息和32位版本之 Windows 的相關資訊，請參閱備註。

 


```C++
  WM_CTLCOLOR

  WPARAM wParam;
  LPARAM lParam;
    
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

目的地視窗的控制碼。

</dd> <dt>

*wParam* 
</dt> <dd>

 (DC) 的顯示內容控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

子視窗的控制碼 (控制項) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則會傳回筆刷的控制碼。 系統會使用筆刷來繪製控制項的背景。

## <a name="remarks"></a>備註

來自16位 Windows 的 **WM \_ CTLCOLOR** 訊息已由更明確的通知取代。 這些取代包括下列各項：

-   [**WM \_ CTLCOLORBTN**](../controls/wm-ctlcolorbtn.md)
-   [**WM \_ CTLCOLOREDIT**](../controls/wm-ctlcoloredit.md)
-   [**WM \_ CTLCOLORDLG**](../dlgbox/wm-ctlcolordlg.md)
-   [**WM \_ CTLCOLORLISTBOX**](../controls/wm-ctlcolorlistbox.md)
-   [**WM \_ CTLCOLORSCROLLBAR**](../controls/wm-ctlcolorscrollbar.md)
-   [**WM \_ CTLCOLORSTATIC**](../controls/wm-ctlcolorstatic.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>WindowsX。h</dt> </dl> |



 

 
