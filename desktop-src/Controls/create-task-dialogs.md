---
title: 如何建立工作對話方塊
description: 您可以使用 TaskDialog 函數或 TaskDialogIndirect 函數來建立和顯示工作對話方塊。
ms.assetid: CCEFF52F-D501-4145-9799-0A9C529017E1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ea8e3097454505acccf60c7cba3ef56c637af0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021022"
---
# <a name="how-to-create-task-dialogs"></a><span data-ttu-id="d2729-103">如何建立工作對話方塊</span><span class="sxs-lookup"><span data-stu-id="d2729-103">How to Create Task Dialogs</span></span>

<span data-ttu-id="d2729-104">您可以使用 [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) 函數或 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 函數來建立和顯示工作對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d2729-104">A task dialog is created and shown by using either the [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) function or the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d2729-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="d2729-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d2729-106">技術</span><span class="sxs-lookup"><span data-stu-id="d2729-106">Technologies</span></span>

-   [<span data-ttu-id="d2729-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="d2729-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d2729-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="d2729-108">Prerequisites</span></span>

-   <span data-ttu-id="d2729-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="d2729-109">C/C++</span></span>
-   <span data-ttu-id="d2729-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="d2729-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d2729-111">指示</span><span class="sxs-lookup"><span data-stu-id="d2729-111">Instructions</span></span>

### <a name="taskdialog"></a><span data-ttu-id="d2729-112">TaskDialog</span><span class="sxs-lookup"><span data-stu-id="d2729-112">TaskDialog</span></span>

<span data-ttu-id="d2729-113">**TaskDialog** 函式適用于顯示文字資訊並要求標準選擇的簡單對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d2729-113">The **TaskDialog** function is suitable for simple dialog boxes that present textual information and ask for a standard choice.</span></span> <span data-ttu-id="d2729-114">此建立功能不支援進度列、核取方塊、頁尾、展開/折迭按鈕、自訂按鈕或選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="d2729-114">This creation function does not support progress bars, check boxes, footers, expand/collapse buttons, custom buttons, or radio buttons.</span></span>

### <a name="taskdialogindirect"></a><span data-ttu-id="d2729-115">TaskDialogIndirect</span><span class="sxs-lookup"><span data-stu-id="d2729-115">TaskDialogIndirect</span></span>

<span data-ttu-id="d2729-116">**TaskDialogIndirect** 函式更強大，支援所有可用的介面元素，也可讓您在回呼程式中捕捉事件，讓您的應用程式可以更新進度列或回應按一下超連結或按鈕。</span><span class="sxs-lookup"><span data-stu-id="d2729-116">The **TaskDialogIndirect** function is more powerful, supporting all available interface elements and also enabling you to capture events in a callback procedure so that your application can update a progress bar or respond to a click of a hyperlink or button.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2729-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2729-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2729-118">使用工作對話方塊</span><span class="sxs-lookup"><span data-stu-id="d2729-118">Using Task Dialogs</span></span>](using-task-dialogs.md)
</dt> </dl>

 

 




