---
title: 如何建立工作對話方塊
description: 您可以使用 TaskDialog 函數或 TaskDialogIndirect 函數來建立和顯示工作對話方塊。
ms.assetid: CCEFF52F-D501-4145-9799-0A9C529017E1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6f74f1922330cae1550fda1a9ad6d451221452017f3856ae5e859948019828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504018"
---
# <a name="how-to-create-task-dialogs"></a>如何建立工作對話方塊

您可以使用 [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) 函數或 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 函數來建立和顯示工作對話方塊。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="taskdialog"></a>TaskDialog

**TaskDialog** 函式適用于顯示文字資訊並要求標準選擇的簡單對話方塊。 此建立功能不支援進度列、核取方塊、頁尾、展開/折迭按鈕、自訂按鈕或選項按鈕。

### <a name="taskdialogindirect"></a>TaskDialogIndirect

**TaskDialogIndirect** 函式更強大，支援所有可用的介面元素，也可讓您在回呼程式中捕捉事件，讓您的應用程式可以更新進度列或回應按一下超連結或按鈕。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作對話方塊](using-task-dialogs.md)
</dt> </dl>

 

 




