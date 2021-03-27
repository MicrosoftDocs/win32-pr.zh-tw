---
description: 當控制項或功能表的視覺外觀變更時，傳送至主控描繪控制項或功能表的父視窗。
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: 'DFM_WM_DRAWITEM 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67255fea5c39bebc995e5c53d90378536b12921b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972005"
---
# <a name="dfm_wm_drawitem-message"></a>DFM \_ WM \_ DRAWITEM 訊息

當控制項或功能表的視覺外觀變更時，傳送至主控描繪控制項或功能表的父視窗。


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

傳送 **DFM \_ WM \_ DRAWITEM** 訊息之控制項的識別碼。 如果訊息是由功能表傳送，此參數為零。

</dd> <dt>

*lpDrawItem* \[擴展\]
</dt> <dd>

[**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的指標，其中包含要繪製之專案的相關資訊，以及所需的繪圖類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回 **TRUE**。

## <a name="remarks"></a>備註

[**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的 **itemAction** 成員會指定應用程式應該執行的繪圖作業。

從處理此訊息傳回之前，應用程式應該確定 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的 **hDC** 成員所識別的裝置內容為預設狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
