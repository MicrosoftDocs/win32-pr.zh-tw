---
description: 應用程式會將 WM \_ MDICASCADE 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以串聯格式排列其所有子視窗。
ms.assetid: 33d04859-4220-40a6-be46-74a812a44ca8
title: 'WM_MDICASCADE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6208ce924ab6185399f3f673a435e1fbaca2741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318256"
---
# <a name="wm_mdicascade-message"></a>WM \_ MDICASCADE 訊息

應用程式會將 **WM \_ MDICASCADE** 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以串聯格式排列其所有子視窗。


```C++
#define WM_MDICASCADE                   0x0227
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

重疊顯示行為。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                                                                                          | 意義                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="MDITILE_SKIPDISABLED"></span><span id="mditile_skipdisabled"></span><dl> <dt>**MDITILE \_SKIPDISABLED**</dt> <dt>0x0002</dt> </dl> | 防止停用的 MDI 子視窗進行串聯。 <br/> |
| <span id="MDITILE_ZORDER"></span><span id="mditile_zorder"></span><dl> <dt>**MDITILE \_ZORDER**</dt> <dt>0x0004</dt> </dl>                   | 以 Z 順序排列視窗。<br/>                          |



 

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

[**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md)
</dt> <dt>

[**WM \_ MDITILE**](wm-mditile.md)
</dt> <dt>

**概念**
</dt> <dt>

[多個檔介面](multiple-document-interface.md)
</dt> </dl>

 

 




