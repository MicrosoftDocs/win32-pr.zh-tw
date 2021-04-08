---
description: 應用程式會將 WM \_ MDIDESTROY 訊息傳送至多重文件介面 (mdi) 用戶端視窗來關閉 mdi 子視窗。
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: 'WM_MDIDESTROY 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edea8fe8dadc691ca912df4e9ee5d57421124bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690283"
---
# <a name="wm_mdidestroy-message"></a>WM \_ MDIDESTROY 訊息

應用程式會將 **WM \_ MDIDESTROY** 訊息傳送至多重文件介面 (mdi) 用戶端視窗來關閉 mdi 子視窗。


```C++
#define WM_MDIDESTROY                   0x0221
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要關閉之 MDI 子視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **零**

此訊息一律會傳回零。

## <a name="remarks"></a>備註

此訊息會從 MDI 框架視窗移除 MDI 子視窗的標題，並停用子視窗。 應用程式應該使用此訊息來關閉所有 MDI 子視窗。

如果 MDI 用戶端視窗收到的訊息會變更其子視窗的啟用，而且使用中的 MDI 子視窗最大化，系統會還原使用中的子視窗，並將新啟動的子視窗最大化。

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

[**WM \_ MDICREATE**](wm-mdicreate.md)
</dt> <dt>

**概念**
</dt> <dt>

[多個檔介面](multiple-document-interface.md)
</dt> </dl>

 

 




