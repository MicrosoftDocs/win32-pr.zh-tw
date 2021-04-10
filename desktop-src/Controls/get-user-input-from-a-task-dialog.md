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
# <a name="how-to-get-user-input-from-a-task-dialog"></a><span data-ttu-id="da823-103">如何從工作對話方塊取得使用者輸入</span><span class="sxs-lookup"><span data-stu-id="da823-103">How to Get User Input from a Task Dialog</span></span>

<span data-ttu-id="da823-104">若要完成工作，使用者可以藉由設定工作對話方塊內的控制項，將工作詳細資料提交給應用程式，然後按一下命令按鈕 (通常是 **正常** 的) 。</span><span class="sxs-lookup"><span data-stu-id="da823-104">To complete a task, users submit the task details to the application by configuring the controls within the task dialog, and then clicking a command button (usually **OK**).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="da823-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="da823-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="da823-106">技術</span><span class="sxs-lookup"><span data-stu-id="da823-106">Technologies</span></span>

-   [<span data-ttu-id="da823-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="da823-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="da823-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="da823-108">Prerequisites</span></span>

-   <span data-ttu-id="da823-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="da823-109">C/C++</span></span>
-   <span data-ttu-id="da823-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="da823-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="da823-111">指示</span><span class="sxs-lookup"><span data-stu-id="da823-111">Instructions</span></span>

### <a name="getting-user-input-from-a-task-dialog"></a><span data-ttu-id="da823-112">從工作對話方塊取得使用者輸入</span><span class="sxs-lookup"><span data-stu-id="da823-112">Getting User Input from a Task Dialog</span></span>

<span data-ttu-id="da823-113">您可以藉由檢查呼叫函式的 *pnButton* 參數來識別按一下的按鈕。</span><span class="sxs-lookup"><span data-stu-id="da823-113">You can identify the button that was clicked by examining the *pnButton* parameter of the calling function.</span></span> <span data-ttu-id="da823-114">您也可以從 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)的 *pnRadioButton* 參數，以及 *pfVerificationFlagChecked* 參數的 [驗證] 核取方塊的狀態，識別選取的選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="da823-114">You can also identify the selected radio button from the *pnRadioButton* parameter of [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect), and the state of the verification check box from the *pfVerificationFlagChecked* parameter.</span></span>

<span data-ttu-id="da823-115">按一下按鈕和超連結， [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) 函式會以 [TDN \_ 按鈕 \_](tdn-button-clicked.md) 的形式來接收，然後再按一下 [TDN 的 \_ 超連結 \_](tdn-hyperlink-clicked.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="da823-115">Clicks on buttons and hyperlinks are received by the [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) function in the form of [TDN\_BUTTON\_CLICKED](tdn-button-clicked.md) and [TDN\_HYPERLINK\_CLICKED](tdn-hyperlink-clicked.md) notifications.</span></span> <span data-ttu-id="da823-116">如果您的回呼函式 \_ 在處理按鈕通知之後傳回 S OK，工作對話方塊會關閉，而且會在 *pnButton* 中傳回按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="da823-116">If your callback function returns S\_OK after handling a button notification, the task dialog closes and the command identifier of the button is returned in *pnButton*.</span></span> <span data-ttu-id="da823-117">如果您傳回 \_ FALSE，或沒有回呼函式，工作對話方塊會保持開啟。</span><span class="sxs-lookup"><span data-stu-id="da823-117">If you return S\_FALSE, or do not have a callback function, the task dialog remains open.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da823-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="da823-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da823-119">使用工作對話方塊</span><span class="sxs-lookup"><span data-stu-id="da823-119">Using Task Dialogs</span></span>](using-task-dialogs.md)
</dt> </dl>

 

 