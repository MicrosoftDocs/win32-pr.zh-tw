---
title: 如何自動調整 Rich Edit 控制項的大小
description: 應用程式可以視需要調整 rich edit 控制項的大小，使其大小一律與內容相同。
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee9ead05c4c04526a9290dc115f7a2fa7741397
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024184"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a>如何自動調整 Rich Edit 控制項的大小

應用程式可以視需要調整 rich edit 控制項的大小，使其大小一律與內容相同。 Rich edit 控制項支援這種所謂的 *無底邊* 功能，方法是在控制項內容的大小變更時，傳送一個 [EN \_ REQUESTRESIZE](en-requestresize.md) 通知碼給其父視窗。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="automatically-resize-a-rich-edit-control"></a>自動調整 Rich Edit 控制項的大小

處理 [EN \_ REQUESTRESIZE](en-requestresize.md) 通知程式碼時，應用程式應該將控制項的大小調整為指定之 [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) 結構中的維度。 應用程式也可能會移動接近控制項的任何資訊，以容納控制項的高度變更。 若要調整控制項的大小，您可以使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) 函數。

您可以使用 [**EM \_ REQUESTRESIZE**](em-requestresize.md)訊息來強制無底邊 rich Edit 控制項傳送 [EN \_ REQUESTRESIZE](en-requestresize.md)通知碼。 此訊息在處理 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 訊息時可能很有用。

## <a name="remarks"></a>備註

若要接收 [EN \_ REQUESTRESIZE](en-requestresize.md) 通知碼，您必須使用 [EM \_ SETEVENTMASK](em-seteventmask.md) 訊息來啟用通知。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Rich Edit 控制項](using-rich-edit-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 