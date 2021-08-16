---
description: 抓取控制項目前用來繪製其文字的字型。
ms.assetid: a6d05ef5-9933-4d03-a677-a8328bf1cb7d
title: 'WM_GETFONT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d3dbd4a34557459fa0f31f6e2a96eba9d0cab36d54cf2bddaa353343a18b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200469"
---
# <a name="wm_getfont-message"></a>WM \_ GETFONT 訊息

抓取控制項目前用來繪製其文字的字型。


```C++
#define WM_GETFONT                      0x0031
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HFONT**

傳回值是控制項所使用之字型的控制碼; 如果控制項使用系統字型，則為 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**WM \_ SETFONT**](wm-setfont.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 




