---
title: 如何使用 Rich Edit 控制項通知碼
description: Rich edit 控制項的父視窗可以處理通知碼來監視影響控制項的事件。 Rich edit 控制項支援與編輯控制項搭配使用的所有通知碼，以及數個其他專案。
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6bc730c648e76137db480f14895d540a9142ae6a80ffa58533e38ef513653ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828630"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a>如何使用 Rich Edit 控制項通知碼

Rich edit 控制項的父視窗可以處理通知碼來監視影響控制項的事件。 Rich edit 控制項支援與編輯控制項搭配使用的所有通知碼，以及數個其他專案。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="use-a-rich-edit-control-notification-code"></a>使用 Rich Edit 控制項通知碼

您可以藉由設定其事件遮罩，判斷 rich edit 控制項傳送其父視窗的通知碼。 若要設定 rich edit 控制項的事件遮罩，請使用 [**EM \_ SETEVENTMASK**](em-seteventmask.md) 訊息。 您可以使用 [**EM \_ GETEVENTMASK**](em-geteventmask.md) 訊息來取得 rich edit 控制項的目前事件遮罩。 如需事件遮罩旗標的清單，請參閱 [Rich Edit 控制項事件遮罩旗標](rich-edit-control-event-mask-flags.md)。

Rich edit 控制項的父視窗可以藉由處理 [ \_ MSGFILTER](en-msgfilter.md) 通知程式碼，來篩選控制項的所有鍵盤和滑鼠輸入。 父視窗可以防止鍵盤或滑鼠訊息被處理，或是藉由修改指定的 [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) 結構來變更訊息。

應用程式可以處理 [En-us \_ 受保護](en-protected.md) 的通知碼，以偵測使用者何時嘗試修改受保護的文字。 若要將某個範圍的文字標示為受保護，您可以設定受保護的字元效果。

您可以藉由處理 [ \_ DROPFILES](en-dropfiles.md) 通知程式碼，讓使用者在 rich edit 控制項中放置檔案。 指定的 [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) 結構包含要卸載之檔案的相關資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Rich Edit 控制項](using-rich-edit-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




