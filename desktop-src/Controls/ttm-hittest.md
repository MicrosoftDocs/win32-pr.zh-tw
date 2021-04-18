---
title: 'TTM_HITTEST 訊息 (Commctrl .h) '
description: 測試點以判斷它是否在指定之工具的周框矩形內，如果是，則會抓取工具的相關資訊。
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- TTM_HITTEST message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_HITTEST
- TTM_HITTESTA
- TTM_HITTESTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b515ccb5c283b66760f24c02749368e424e6fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465352"
---
# <a name="ttm_hittest-message"></a>TTM \_ system.windows.media.visualtreehelper.hittest 訊息

測試點以判斷它是否在指定之工具的周框矩形內，如果是，則會抓取工具的相關資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa)結構的指標。 傳送訊息時， **hwnd** 成員必須指定工具的控制碼，而 **pt** 成員必須指定點的座標。 如果傳回值為 **TRUE**，則 **Ti** 成員 ([**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構) 接收有關該點之工具的資訊。 傳送此訊息之前，必須先填入 **ti** 結構的 **cbSize** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果工具佔用指定的點，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

當工具已設定 TTF TRACK 旗標時，必須傳送此訊息 \_ 。 如需此旗標的詳細資訊，請參閱 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)。 \_如果未設定 TTF TRACK，TTM system.windows.media.visualtreehelper.hittest 將會失敗 \_ ，不論點擊點是否在 [工具] 矩形中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TTM \_HITTESTW** (Unicode) 和 **TTM \_ HITTESTA** (ANSI) <br/>                   |



 

 





