---
description: '[取消] 對話方塊會確認使用者是否想要結束安裝。 這是強制回應對話方塊。'
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: 取消對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1022a7613f3f5341d8c833b7cbe2645ce871aeb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974239"
---
# <a name="cancel-dialog"></a><span data-ttu-id="389fa-104">取消對話方塊</span><span class="sxs-lookup"><span data-stu-id="389fa-104">Cancel Dialog</span></span>

<span data-ttu-id="389fa-105">[ **取消** ] 對話方塊會確認使用者是否想要結束安裝。</span><span class="sxs-lookup"><span data-stu-id="389fa-105">A **Cancel** dialog box confirms that the user wants to terminate the installation.</span></span> <span data-ttu-id="389fa-106">這是強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="389fa-106">This is a modal dialog box.</span></span>

<span data-ttu-id="389fa-107">這種類型的對話方塊通常包含 [文字控制項](text-control.md) 和兩個 [按鈕](pushbutton-control.md)。</span><span class="sxs-lookup"><span data-stu-id="389fa-107">This type of dialog box commonly contains a [Text control](text-control.md) and two [PushButtons](pushbutton-control.md).</span></span> <span data-ttu-id="389fa-108">這兩個按鈕可讓使用者選擇返回最後一個對話方塊或確認安裝終止。</span><span class="sxs-lookup"><span data-stu-id="389fa-108">The two buttons give the user the choice of either returning to the last dialog box or confirming the termination of the installation.</span></span>

<span data-ttu-id="389fa-109">[EndDialog](enddialog-controlevent.md) ControlEvent 會連結到[ControlEvent 資料表](controlevent-table.md)中的這兩個按鈕。</span><span class="sxs-lookup"><span data-stu-id="389fa-109">The [EndDialog](enddialog-controlevent.md) ControlEvent is linked to these two buttons in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="389fa-110">EndDialog ControlEvent 的 *Return* 參數會連結到其中一個按鈕，並導致 [ **取消** ] 對話方塊終止，並讓焦點回到上一個對話方塊。</span><span class="sxs-lookup"><span data-stu-id="389fa-110">The *Return* parameter of the EndDialog ControlEvent is linked to one of the buttons and causes the **Cancel** dialog box to be terminated and the focus to return to the previous dialog box.</span></span> <span data-ttu-id="389fa-111">*Exit* 參數會連結至另一個按鈕，並讓使用者介面使用適當的程式碼將控制權傳回給安裝程式，表示使用者想要結束。</span><span class="sxs-lookup"><span data-stu-id="389fa-111">The *Exit* parameter is linked to the other button and causes the user interface to return control to the installer with the appropriate code indicating that the user wants to exit.</span></span> <span data-ttu-id="389fa-112">然後，安裝程式就會關閉並顯示 [ [UserExit] 對話方塊](userexit-dialog.md)。</span><span class="sxs-lookup"><span data-stu-id="389fa-112">The installer then shuts down and displays the [UserExit Dialog](userexit-dialog.md).</span></span>

 

 



