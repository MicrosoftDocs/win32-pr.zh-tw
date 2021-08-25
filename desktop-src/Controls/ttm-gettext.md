---
title: 'TTM_GETTEXT 訊息 (Commctrl .h) '
description: 抓取工具提示控制項維護工具的相關資訊。
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- TTM_GETTEXT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TTM_GETTEXT
- TTM_GETTEXTA
- TTM_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9efe79105c705eba3dd25c124cf17ff0e4773618608bc7ef86ebbf3d0d9f715e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967888"
---
# <a name="ttm_gettext-message"></a>TTM \_ GETTEXT 訊息

抓取工具提示控制項維護工具的相關資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>要複製到 **lpszText** 所指向之緩衝區的 **TCHARs** 數目，包括終止的 **Null**。 </dd> <dt>

*lParam* 
</dt> <dd>

[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標。 將此結構的 **cbSize** 成員設定為， `sizeof(TOOLINFO)` 然後再傳送此訊息。 設定 **hwnd** 和 **uId** 成員，以識別要取得資訊的工具。 配置 *wParam* 所指定之大小的緩衝區。 設定 **lpszText** 成員指向緩衝區以接收工具文字。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TTM \_GETTEXTW** (Unicode) 和 **TTM \_ GETTEXTA** (ANSI) <br/>                   |



 

 





