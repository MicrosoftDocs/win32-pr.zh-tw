---
title: 如何從工作對話方塊取得使用者輸入
description: 若要完成工作，使用者可以藉由設定工作對話方塊內的控制項，將工作詳細資料提交給應用程式，然後按一下命令按鈕 (通常是正常的) 。
ms.assetid: 73CD8FBF-95C9-43C8-B9D8-3823840C23A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd53c8051747187123821211ac7e17c9915b5fd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933667"
---
# <a name="how-to-get-user-input-from-a-task-dialog"></a>如何從工作對話方塊取得使用者輸入

若要完成工作，使用者可以藉由設定工作對話方塊內的控制項，將工作詳細資料提交給應用程式，然後按一下命令按鈕 (通常是 **正常** 的) 。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="getting-user-input-from-a-task-dialog"></a>從工作對話方塊取得使用者輸入

您可以藉由檢查呼叫函式的 *pnButton* 參數來識別按一下的按鈕。 您也可以從 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)的 *pnRadioButton* 參數，以及 *pfVerificationFlagChecked* 參數的 [驗證] 核取方塊的狀態，識別選取的選項按鈕。

按一下按鈕和超連結， [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) 函式會以 [TDN \_ 按鈕 \_](tdn-button-clicked.md) 的形式來接收，然後再按一下 [TDN 的 \_ 超連結 \_](tdn-hyperlink-clicked.md) 通知。 如果您的回呼函式 \_ 在處理按鈕通知之後傳回 S OK，工作對話方塊會關閉，而且會在 *pnButton* 中傳回按鈕的命令識別碼。 如果您傳回 \_ FALSE，或沒有回呼函式，工作對話方塊會保持開啟。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作對話方塊](using-task-dialogs.md)
</dt> </dl>

 

 