---
title: 'TBN_DROPDOWN (Commctrl 的通知碼) '
description: 當使用者按一下下拉式按鈕時，由工具列控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 85360f74-4b43-4d0a-8c89-22b0741fe96a
keywords:
- TBN_DROPDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7adbb9e0e2ed3d77f8ca8bfb6b09dedd2265be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934191"
---
# <a name="tbn_dropdown-notification-code"></a>TBN \_ 下拉式通知碼

當使用者按一下下拉式按鈕時，由工具列控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_DROPDOWN

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)結構的指標，其中包含此通知碼的相關資訊。 針對此通知碼，只有此結構的 **hdr** 和 **iItem** 成員有效。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一值：



| 傳回碼                                                                                          | Description                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**TBDDRET \_ 預設值**</dt> </dl>      | 已處理下拉式清單。<br/>                                             |
| <dl> <dt>**TBDDRET \_ NODEFAULT**</dt> </dl>    | 未處理下拉式清單。<br/>                                         |
| <dl> <dt>**TBDDRET \_ TREATPRESSED**</dt> </dl> | 已處理下拉式清單，但是將按鈕視為一般按鈕。<br/> |



 

## <a name="remarks"></a>備註

> [!Note]  
> 下拉式按鈕可以是純 ([**BTNS \_ 下拉式**](toolbar-control-and-button-styles.md) 樣式) 、在按鈕影像旁邊顯示箭號 ([**BTNS \_ WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) style) ，或是顯示與影像 ([**TBSTYLE 範例 \_ \_ DRAWDDARROWS**](toolbar-extended-styles.md) 樣式) 分開的箭號。 如果使用分隔箭號， \_ 只有當使用者按一下按鈕的箭號部分時，才會傳送 TBN 下拉式清單。 如果使用者按一下按鈕的主要部分，則會傳送具有按鈕識別碼的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息，就像使用標準按鈕一樣。 針對其他兩個下拉式按鈕樣式， \_ 當使用者按一下按鈕的任一個部分時，就會傳送 TBN 下拉式清單。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

