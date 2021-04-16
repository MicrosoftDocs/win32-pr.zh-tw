---
description: 下列範例說明如何撰寫會彈出的條件訊息方塊，並警告使用者在使用者提前啟用顯示的控制項時，背景工作仍在執行中。
ms.assetid: 4a99a96b-50c2-42eb-82ad-acdfa186a71f
title: 撰寫「請稍候。 . ." 訊息方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c5f0cb1e4f1a0224c3b71d42d6fc63c1940483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513237"
---
# <a name="authoring-a-conditional-please-wait-message-box"></a><span data-ttu-id="33a30-106">撰寫條件式「請稍候 ...」訊息方塊</span><span class="sxs-lookup"><span data-stu-id="33a30-106">Authoring a Conditional "Please Wait..." Message Box</span></span>

<span data-ttu-id="33a30-107">下列範例說明如何撰寫會彈出的條件訊息方塊，並警告使用者在使用者提前啟用顯示的控制項時，背景工作仍在執行中。</span><span class="sxs-lookup"><span data-stu-id="33a30-107">The following example illustrates how to author a conditional message box that pops up and warns the user that a background task is still running whenever the user activates a displayed control prematurely.</span></span>

<span data-ttu-id="33a30-108">此範例也會說明如何使用 [SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md) 來保護會觸發動作的控制項，而該控制項會根據背景工作完成而觸發動作。</span><span class="sxs-lookup"><span data-stu-id="33a30-108">The example also illustrates how the [SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md) can generally be used to protect a control that triggers an action dependent upon the completion of a background task.</span></span>

<span data-ttu-id="33a30-109">在此範例中，包含三個按鈕控制項的 [選項對話方塊](selection-dialog.md) ，在安裝過程中，會對使用者顯示標示為 [ **立即安裝** **]、[下一步]** 和 [ **磁片費用** ]。</span><span class="sxs-lookup"><span data-stu-id="33a30-109">In this example, a [Selection Dialog](selection-dialog.md) containing three push button controls labeled **Install Now**, **Next**, and **Disk Cost** is displayed to the user during the installation process.</span></span> <span data-ttu-id="33a30-110">但是，安裝程式在顯示此對話方塊時，也會在背景中執行磁碟空間的成本工作。</span><span class="sxs-lookup"><span data-stu-id="33a30-110">However, the installer also carries out a disk space costing task in the background while displaying this dialog box.</span></span> <span data-ttu-id="33a30-111">作者希望從啟用中保護這些按鈕，並希望當使用者在完成成本之前按一下任何按鈕時，想要有 [請等候] 訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="33a30-111">The author wishes to protect these buttons from activation and wants a "Please wait" message box to pop up if the user clicks any of the buttons before the costing has completed.</span></span> <span data-ttu-id="33a30-112">作者也希望這個訊息方塊包含 [ **取消** ] 按鈕，並在背景工作完成時立即消失。</span><span class="sxs-lookup"><span data-stu-id="33a30-112">The author also wants this message box to contain a **Cancel** button and to disappear as soon as the background task is finished.</span></span>

<span data-ttu-id="33a30-113">**顯示對話方塊，要求使用者在背景磁片成本已完成時等候**</span><span class="sxs-lookup"><span data-stu-id="33a30-113">**To display a dialog box asking the user to wait while background disk costing is completed**</span></span>

1.  <span data-ttu-id="33a30-114">您可以使用安裝程式的撰寫功能，將名為 **WaitForCosting** 的新強制回應對話方塊新增至 [對話方塊資料表](dialog-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="33a30-114">Use the authoring capabilities of the installer to add a new modal dialog box, named **WaitForCosting**, into the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="33a30-115">對話方塊應該會顯示文字字串，指出「請稍候，正在完成磁碟空間的成本。」</span><span class="sxs-lookup"><span data-stu-id="33a30-115">The dialog box should display a text string that says "Please wait while disk space costing is completed."</span></span>
2.  <span data-ttu-id="33a30-116">將單一推播按鈕控制項新增至這個對話方塊，並將其撰寫至 [控制項資料表](control-table.md)，以將其標示為 [**取消**]。</span><span class="sxs-lookup"><span data-stu-id="33a30-116">Add a single push button control to this dialog box, labeled **Cancel**, by authoring it into the [Control table](control-table.md).</span></span>
3.  <span data-ttu-id="33a30-117">將 **「取消」** 推播按鈕連結到 ControlEvent，藉由在 [ControlEvent 資料表](controlevent-table.md)中撰寫 [EndDialog ControlEvent](enddialog-controlevent.md)來關閉 [ **WaitForCosting** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="33a30-117">Link the **Cancel** push button to a ControlEvent that closes the **WaitForCosting** dialog box by authoring an [EndDialog ControlEvent](enddialog-controlevent.md) into the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="33a30-118">將 EndDialog 控制項事件的引數設定為 Exit。</span><span class="sxs-lookup"><span data-stu-id="33a30-118">Set the argument of the EndDialog Control event to be Exit.</span></span>
4.  <span data-ttu-id="33a30-119">將 [SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md)連結至 [**立即安裝**]、 **[下一步**]，以及顯示在 [[選取範圍] 對話方塊](selection-dialog.md)中的 [**磁片成本**] 推播按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="33a30-119">Link a [SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md) to the existing **Install Now**, **Next**, and **Disk Cost** push button controls displayed in the [Selection Dialog](selection-dialog.md) box.</span></span> <span data-ttu-id="33a30-120">將 [ControlEvent] 資料表中這個 ControlEvent 的引數設定為 [ **WaitForCosting** ] 對話方塊，並將資料表的 [條件] 資料行中的運算式設為： [**CostingComplete**](costingcomplete.md) = 1。</span><span class="sxs-lookup"><span data-stu-id="33a30-120">Set the argument of this ControlEvent in the ControlEvent table to be the **WaitForCosting** dialog box and set the expression in the Condition column of the table to be: [**CostingComplete**](costingcomplete.md) =1.</span></span>

 

 



