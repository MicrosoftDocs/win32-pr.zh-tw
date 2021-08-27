---
title: 如何使用 Rich Edit 剪貼簿作業
description: 應用程式可以使用最適合的剪貼簿格式或特定的剪貼簿格式，將剪貼簿的內容貼入 rich edit 控制項。
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdeac2e892716880e4e2971d597c13047dc79cebf2c57888e2fa248c6b0c4beb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132088"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a>如何使用 Rich Edit 剪貼簿作業

應用程式可以使用最適合的剪貼簿格式或特定的剪貼簿格式，將剪貼簿的內容貼入 rich edit 控制項。 您也可以判斷 rich edit 控制項是否能夠貼上剪貼簿格式。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="use-a-rich-edit-clipboard-operation"></a>使用 Rich Edit 剪貼簿操作

如同編輯控制項，您可以使用 [**wm \_ 複製**](/windows/desktop/dataxchg/wm-copy) 或 [**wm \_ 剪**](/windows/desktop/dataxchg/wm-cut) 下訊息來複製或剪下目前選取範圍的內容。 同樣地，您可以使用 [**WM \_ 貼**](/windows/desktop/dataxchg/wm-paste) 上訊息，將剪貼簿的內容貼入 rich edit 控制項。 控制項會先貼上其所辨識的第一個可用的格式，這大概會是最具描述性的格式。

若要貼上特定的剪貼簿格式，您可以使用 [**EM \_ PASTESPECIAL**](em-pastespecial.md) 訊息。 這則訊息適用于具有 [貼上] **特殊** 命令的應用程式，可讓使用者選取 [剪貼簿] 格式。 您可以使用 [**EM \_ CANPASTE**](em-canpaste.md) 訊息來判斷控制項是否能辨識指定的格式。

您也可以使用 [**EM \_ CANPASTE**](em-canpaste.md) 訊息來判斷 rich edit 控制項是否能辨識任何可用的剪貼簿格式。 此訊息在處理 [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) 訊息時很有用。 應用程式可能會根據控制項是否可以貼上任何可用的格式，來啟用或使其 **貼** 上命令變成灰色。

Rich edit 控制項會註冊兩個剪貼簿格式：

-   Rich Text 格式
-   沒有物件的 Rich Text 格式
-   RichEdit 文字和物件

應用程式可以使用 [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) 函式來註冊這些格式，指定 cf \_ RTF、CF \_ RTFNOOBJS 和 cf \_ RETEXTOBJ 值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Rich Edit 控制項](using-rich-edit-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 