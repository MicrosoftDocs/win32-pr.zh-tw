---
title: 'TTM_RELAYEVENT 訊息 (Commctrl .h) '
description: 將滑鼠訊息傳遞至工具提示控制項以進行處理。
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- TTM_RELAYEVENT message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_RELAYEVENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8648303a318f1f71eb16e8070235910ecfb8760
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322276"
---
# <a name="ttm_relayevent-message"></a>TTM \_ RELAYEVENT 訊息

將滑鼠訊息傳遞至工具提示控制項以進行處理。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。 **Windows 7 和更新版本：** 如果工具提示的位置是從游標位置位移 (的順序不會被手指或指向裝置) 的阻礙，此參數可能會包含從 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息取得的額外資訊。 使用 [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo)取出此額外資訊。

</dd> <dt>

*lParam* 
</dt> <dd>

訊息 [**結構的**](/windows/win32/api/winuser/ns-winuser-msg) 指標，其中包含要轉送的訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

工具提示控制項只會處理 **TTM \_ RELAYEVENT** 訊息傳遞給它的下列訊息：

-   WM \_ LBUTTONDOWN
-   WM \_ LBUTTONUP
-   WM \_ MBUTTONDOWN
-   WM \_ MBUTTONUP
-   WM \_ MOUSEMOVE
-   WM \_ NCMOUSEMOVE
-   WM \_ RBUTTONDOWN
-   WM \_ RBUTTONUP

所有其他訊息都會被忽略。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

