---
description: 當控制項或功能表的視覺外觀變更時，傳送至主控描繪控制項或功能表的父視窗。
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: 'DFM_WM_DRAWITEM 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7190d445490b581967c8dda67e170eb5db5665dfa59302313d7af736b275944d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969467"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
