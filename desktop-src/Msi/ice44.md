---
description: ICE44 會驗證 NewDialog、SpawnDialog 和 SpawnWaitDialog 的事件，會在對話方塊資料表中參考有效的對話方塊。
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16354ac435979d830ff14c33a846e97757b64962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987652"
---
# <a name="ice44"></a><span data-ttu-id="b77f1-103">ICE44</span><span class="sxs-lookup"><span data-stu-id="b77f1-103">ICE44</span></span>

<span data-ttu-id="b77f1-104">ICE44 會驗證 [NewDialog](newdialog-controlevent.md)、 [SpawnDialog](spawndialog-controlevent.md)和 [SpawnWaitDialog](spawnwaitdialog-controlevent.md) 的事件，會在 [對話方塊資料表](dialog-table.md)中參考有效的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b77f1-104">ICE44 validates that the [NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md), and [SpawnWaitDialog](spawnwaitdialog-controlevent.md) ControlEvents reference valid dialog boxes in the [Dialog table](dialog-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="b77f1-105">結果</span><span class="sxs-lookup"><span data-stu-id="b77f1-105">Result</span></span>

<span data-ttu-id="b77f1-106">如果有對話方塊控制項事件未參考對話方塊資料表中所列的對話方塊，ICE44 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="b77f1-106">ICE44 posts an error message if there is a dialog control event that does not reference a dialog box listed in the Dialog table.</span></span>

## <a name="example"></a><span data-ttu-id="b77f1-107">範例</span><span class="sxs-lookup"><span data-stu-id="b77f1-107">Example</span></span>

<span data-ttu-id="b77f1-108">ICE44 會針對所顯示的範例報告下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="b77f1-108">ICE44 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="b77f1-109">ICE44 錯誤</span><span class="sxs-lookup"><span data-stu-id="b77f1-109">ICE44 error</span></span>                                                                                                                               | <span data-ttu-id="b77f1-110">Description</span><span class="sxs-lookup"><span data-stu-id="b77f1-110">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b77f1-111">控制項 ' Dialog1 ' 的控制項事件。Control1 ' 的類型為 SpawnDialog，但其引數 Dialog2 不是對話方塊資料表中的有效專案。</span><span class="sxs-lookup"><span data-stu-id="b77f1-111">Control Event for Control 'Dialog1'.'Control1' is of type SpawnDialog, but its argument Dialog2 is not a valid entry in the Dialog Table.</span></span> | <span data-ttu-id="b77f1-112">有 SpawnDialog、SpawnWaitDialog 或 NewDialog 動作具有未參考對話方塊資料表中對話方塊的引數。</span><span class="sxs-lookup"><span data-stu-id="b77f1-112">There is a SpawnDialog, SpawnWaitDialog, or NewDialog actions that has an argument that does not refer to a dialog box in the Dialog table.</span></span> <span data-ttu-id="b77f1-113">若要修正這個錯誤，請在對話方塊資料表中新增一個索引鍵的引數。</span><span class="sxs-lookup"><span data-stu-id="b77f1-113">To fix this error, add an argument that is a key in the Dialog Table.</span></span><br/> |



 

<span data-ttu-id="b77f1-114">[對話方塊資料表](dialog-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="b77f1-114">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="b77f1-115">對話</span><span class="sxs-lookup"><span data-stu-id="b77f1-115">Dialog</span></span>  | <span data-ttu-id="b77f1-116">標題</span><span class="sxs-lookup"><span data-stu-id="b77f1-116">Title</span></span> |
|---------|-------|
| <span data-ttu-id="b77f1-117">Dialog1</span><span class="sxs-lookup"><span data-stu-id="b77f1-117">Dialog1</span></span> |       |



 

<span data-ttu-id="b77f1-118">[ControlEvent 資料表](controlevent-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="b77f1-118">[ControlEvent Table](controlevent-table.md) (partial)</span></span>



| <span data-ttu-id="b77f1-119">對話\_</span><span class="sxs-lookup"><span data-stu-id="b77f1-119">Dialog\_</span></span> | <span data-ttu-id="b77f1-120">控制項\_</span><span class="sxs-lookup"><span data-stu-id="b77f1-120">Control\_</span></span> | <span data-ttu-id="b77f1-121">類型</span><span class="sxs-lookup"><span data-stu-id="b77f1-121">Type</span></span>        | <span data-ttu-id="b77f1-122">引數</span><span class="sxs-lookup"><span data-stu-id="b77f1-122">Argument</span></span> |
|----------|-----------|-------------|----------|
| <span data-ttu-id="b77f1-123">Dialog1</span><span class="sxs-lookup"><span data-stu-id="b77f1-123">Dialog1</span></span>  | <span data-ttu-id="b77f1-124">Control1</span><span class="sxs-lookup"><span data-stu-id="b77f1-124">Control1</span></span>  | <span data-ttu-id="b77f1-125">SpawnDialog</span><span class="sxs-lookup"><span data-stu-id="b77f1-125">SpawnDialog</span></span> | <span data-ttu-id="b77f1-126">Dialog2</span><span class="sxs-lookup"><span data-stu-id="b77f1-126">Dialog2</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="b77f1-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="b77f1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b77f1-128">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="b77f1-128">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




