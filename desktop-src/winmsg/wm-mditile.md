---
description: 應用程式會將 WM \_ MDITILE 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以磚格式排列所有的 MDI 子視窗。
ms.assetid: a480ba61-807e-4d0e-bda2-f1876e0bb13c
title: 'WM_MDITILE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cf7ee38fbb3622e2d17bf4cea5a28b6b492a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191288"
---
# <a name="wm_mditile-message"></a>WM \_ MDITILE 訊息

應用程式會將 **WM \_ MDITILE** 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以磚格式排列所有的 MDI 子視窗。


```C++
#define WM_MDITILE                      0x0226
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

平鋪選項。 這個參數可以是下列其中一個值，並選擇性地與 **MDITILE \_ SKIPDISABLED** 結合，以防止停用的 MDI 子視窗進行並排顯示。



| 值                                                                                                                                                                                                                                    | 意義                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MDITILE_HORIZONTAL"></span><span id="mditile_horizontal"></span><dl> <dt>**MDITILE \_水準**</dt> <dt>0x0001</dt> </dl> | 水準磚視窗。<br/> |
| <span id="MDITILE_VERTICAL"></span><span id="mditile_vertical"></span><dl> <dt>**MDITILE \_垂直**</dt> <dt>0x0000</dt> </dl>       | 垂直磚視窗。<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **BOOL**

如果訊息成功，則傳回值為 **TRUE**。

如果訊息失敗，則傳回值為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**WM \_ MDICASCADE**](wm-mdicascade.md)
</dt> <dt>

[**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md)
</dt> <dt>

**概念**
</dt> <dt>

[多個檔介面](multiple-document-interface.md)
</dt> </dl>

 

 




