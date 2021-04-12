---
title: 'WM_ENTERIDLE 訊息 (Winuser .h) '
description: 傳送至進入閒置狀態之強制回應對話方塊或功能表的擁有者視窗。 強制回應對話方塊或功能表在處理一或多個先前的訊息之後，就會進入閒置狀態，當佇列中沒有任何訊息在佇列中等候時。
ms.assetid: 11b1f942-185f-4de4-90a2-e2934bb1394f
keywords:
- WM_ENTERIDLE 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_ENTERIDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99b3150a0dbc1a81b78498c8e295fbf2397c22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385037"
---
# <a name="wm_enteridle-message"></a>WM \_ ENTERIDLE 訊息

傳送至進入閒置狀態之強制回應對話方塊或功能表的擁有者視窗。 強制回應對話方塊或功能表在處理一或多個先前的訊息之後，就會進入閒置狀態，當佇列中沒有任何訊息在佇列中等候時。


```C++
#define WM_ENTERIDLE                    0x0121
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                   | 意義                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="MSGF_DIALOGBOX"></span><span id="msgf_dialogbox"></span><dl> <dt>**MSGF \_對話方塊**</dt> <dt>0</dt> </dl> | 系統閒置，因為顯示對話方塊。<br/> |
| <span id="MSGF_MENU"></span><span id="msgf_menu"></span><dl> <dt>**MSGF \_功能表**</dt> <dt>2</dt> </dl>                | 系統閒置，因為顯示功能表。<br/>       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

對話方塊的控制碼 (如果 *wParam* 是 **MSGF \_ 對話方塊**) 或包含所顯示功能表的視窗 (如果 *wParam* 是 **MSGF \_ 功能表**) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

您可以藉由建立具有 **DS \_ NOIDLEMSG** 樣式的對話方塊來隱藏對話方塊的 **WM \_ ENTERIDLE** 訊息。

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**概念**
</dt> <dt>

[對話方塊](dialog-boxes.md)
</dt> </dl>

 

