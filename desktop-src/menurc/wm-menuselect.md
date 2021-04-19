---
title: 'WM_MENUSELECT 訊息 (Winuser .h) '
description: 當使用者選取功能表項目時，傳送至功能表的擁有者視窗。
ms.assetid: 57684a19-dfaa-4e0c-a8ff-010533322cb0
keywords:
- WM_MENUSELECT 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_MENUSELECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdee9187ba2074944b3611fee10f5a22c2cc25ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106973306"
---
# <a name="wm_menuselect-message"></a>WM \_ MENUSELECT 訊息

當使用者選取功能表項目時，傳送至功能表的擁有者視窗。


```C++
#define WM_MENUSELECT                   0x011F
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

低序位字組會指定功能表項目或子功能表索引。 如果選取的專案是命令專案，這個參數會包含功能表項目的識別碼。 如果選取的專案開啟下拉式功能表或子功能表，則此參數包含主功能表中下拉式功能表或子功能表的索引，而 *lParam* 參數包含主 (按一下) 功能表的控制碼;您可以使用 [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) 函式來取得下拉式功能表或子功能表的功能表控制碼。

高序位字組指定一或多個功能表旗標。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                                                                             | 意義                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_BITMAP"></span><span id="mf_bitmap"></span><dl> <dt>**MF \_點陣圖**</dt> <dt>0x00000004L</dt> </dl>                | 專案會顯示點陣圖。<br/>                                                                                                 |
| <span id="MF_CHECKED"></span><span id="mf_checked"></span><dl> <dt>**MF \_已檢查**</dt> <dt>0x00000008L</dt> </dl>             | 已檢查項目。<br/>                                                                                                        |
| <span id="MF_DISABLED"></span><span id="mf_disabled"></span><dl> <dt>**MF \_停用**</dt>的 <dt>0x00000002L</dt> </dl>          | 專案已停用。<br/>                                                                                                       |
| <span id="MF_GRAYED"></span><span id="mf_grayed"></span><dl> <dt>**MF \_灰色**</dt> <dt>0x00000001L</dt> </dl>                | 專案會呈現灰色。<br/>                                                                                                         |
| <span id="MF_HILITE"></span><span id="mf_hilite"></span><dl> <dt>**MF \_HILITE**</dt> <dt>0x00000080L</dt> </dl>                | 專案已反白顯示。<br/>                                                                                                    |
| <span id="MF_MOUSESELECT"></span><span id="mf_mouseselect"></span><dl> <dt>**MF \_MOUSESELECT**</dt> <dt>0x00008000L</dt> </dl> | 使用滑鼠來選取專案。<br/>                                                                                        |
| <span id="MF_OWNERDRAW"></span><span id="mf_ownerdraw"></span><dl> <dt>**MF \_OWNERDRAW**</dt> <dt>0x00000100L</dt> </dl>       | 專案是擁有者繪製的專案。<br/>                                                                                            |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_快顯視窗**</dt> <dt>0x00000010L</dt> </dl>                   | 專案會開啟下拉式功能表或子功能表。<br/>                                                                                 |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_SYSMENU**</dt> <dt>0x00002000L</dt> </dl>             | 專案會包含在 [視窗] 功能表中。 *LParam* 參數包含與訊息相關聯之功能表的控制碼。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

已按下之功能表的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

如果 *wParam* 的高序位字包含0xffff，而 *LParam* 參數包含 **Null**，則系統已關閉功能表。

請勿針對 *wParam* 的高序位字使用值1，因為此值指定為 (**UINT**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) (*wParam*) 。 如果值為0xFFFF，則會將它轉譯為0x0000FFFF，而不是1，因為轉換成 **UINT**。

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

[**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤加速器](keyboard-accelerators.md)
</dt> </dl>

 

