---
description: 應用程式會將 WM \_ MDIMAXIMIZE 訊息傳送至多重文件介面 (mdi) 用戶端視窗，以將 mdi 子視窗最大化。
ms.assetid: 7c5e4157-13f6-40d7-a64a-076bd14aca0d
title: 'WM_MDIMAXIMIZE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8372bcb25f35a52793292de4fd94a4a9dadafe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970798"
---
# <a name="wm_mdimaximize-message"></a>WM \_ MDIMAXIMIZE 訊息

應用程式會將 **WM \_ MDIMAXIMIZE** 訊息傳送至多重文件介面 (mdi) 用戶端視窗，以將 mdi 子視窗最大化。 系統會調整子視窗的大小，使其用戶端區域填滿用戶端視窗。 系統會將子視窗的 [視窗] 功能表圖示放置在框架視窗的功能表列最右邊的位置，並將子視窗的 [還原] 圖示放在最左邊的位置。 系統也會將子視窗的標題列文字附加至框架視窗的標題列文字。


```C++
#define WM_MDIMAXIMIZE                  0x0225
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要最大化的 MDI 子視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **零**

傳回值永遠是零。

## <a name="remarks"></a>備註

如果 MDI 用戶端視窗在目前作用中的 MDI 子視窗最大化時，收到變更其子視窗啟動的任何訊息，系統會還原使用中的子視窗，並將新啟動的子視窗最大化。

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

[**WM \_ MDIRESTORE**](wm-mdirestore.md)
</dt> <dt>

**概念**
</dt> <dt>

[多個檔介面](multiple-document-interface.md)
</dt> </dl>

 

 




