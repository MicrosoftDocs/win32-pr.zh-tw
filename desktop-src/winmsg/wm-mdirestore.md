---
description: 應用程式會將 WM \_ MDIRESTORE 訊息傳送至多重文件介面 (mdi) 用戶端視窗，以從最大化或最小化的大小還原 mdi 子視窗。
ms.assetid: bb99fda1-9eb5-4307-9326-9a417a046c22
title: 'WM_MDIRESTORE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2cf36a0b428e1e9003682a5e766f613fd7ba81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973829"
---
# <a name="wm_mdirestore-message"></a>WM \_ MDIRESTORE 訊息

應用程式會將 **WM \_ MDIRESTORE** 訊息傳送至多重文件介面 (mdi) 用戶端視窗，以從最大化或最小化的大小還原 mdi 子視窗。


```C++
#define WM_MDIRESTORE                   0x0223
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要還原的 MDI 子視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **零**

傳回值永遠是零。

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

[**WM \_ MDIMAXIMIZE**](wm-mdimaximize.md)
</dt> <dt>

**概念**
</dt> <dt>

[多個檔介面](multiple-document-interface.md)
</dt> </dl>

 

 




