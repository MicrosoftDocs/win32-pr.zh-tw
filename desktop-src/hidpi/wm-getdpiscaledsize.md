---
title: 'WM_GETDPISCALEDSIZE 訊息 (Winuser .h) '
description: 這則訊息會告知作業系統，視窗將會調整大小為預設值以外的維度。
ms.assetid: 038CAA21-0944-45D3-8C40-A6498F36D9E4
keywords:
- WM_GETDPISCALEDSIZE 訊息高 DPI
topic_type:
- apiref
api_name:
- WM_GETDPISCALEDSIZE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95631e51247d7919307f36dd0af10c72621a612
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465401"
---
# <a name="wm_getdpiscaledsize-message"></a>WM \_ GETDPISCALEDSIZE 訊息

這則訊息會告知作業系統，視窗將會調整大小為預設值以外的維度。

在傳送 [**WM \_ DPICHANGED**](wm-dpichanged.md)訊息之前，會將此訊息傳送至具有每個監視器 v2 [DPI \_ 感知 \_ 內容](dpi-awareness-context.md)的最上層視窗，並允許視窗計算其所需的大小以進行暫止的 DPI 變更。 因為線性 DPI 縮放比例是預設行為，所以這只適用于視窗想要以非線性方式調整的情節。 如果應用程式回應此訊息，則產生的大小將會是傳送至 **WM \_ DPICHANGED** 的候選矩形。

您可以使用此訊息來改變以 [**WM \_ DPICHANGED**](wm-dpichanged.md)提供的矩形大小。


```C++
#define WM_GETDPISCALEDSIZE       0x02E4
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

WPARAM 包含 DPI 值。 應用程式所設定的縮放視窗大小必須計算，就像視窗要切換到這個 DPI 一樣。

</dd> <dt>

*lParam* 
</dt> <dd>

LPARAM 是大小結構的 in/out 指標。 \_LPARAM 中的 in \_ 值是使用者起始的移動或 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)呼叫之後的視窗暫止大小。 如果正在調整視窗的大小，此大小與接收此訊息時的視窗目前大小不一定相同。

\_ \_ 應用程式應將 LPARAM 中的 Out 值寫入至應用程式，以指定對應到 WPARAM 中所提供之 DPI 值的所需調整視窗大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回 BOOL。 傳回 TRUE 表示已計算新的大小。 傳回 FALSE 表示將不會處理訊息，而預設的線性 DPI 縮放比例將會套用至視窗。

## <a name="remarks"></a>備註

此訊息只會傳送至具有每個監視器 v2 之 DPI 感知內容的最上層視窗。

此事件是加速非線性調整的必要專案，可確保 windows 的位置在與游標之間的關聯性和跨監視器來回移動時保持不變。

此訊息在 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)中沒有特定的預設處理方式。 針對它未明確處理的所有訊息， [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) 會針對此訊息傳回零。 如上面所述，此傳回會告知系統使用預設線性行為。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Winuser。h</dt> </dl> |



 

