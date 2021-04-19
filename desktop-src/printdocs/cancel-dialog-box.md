---
description: 本主題說明如何將列印工作進度顯示給使用者，並提供選項來取消目前進行中的列印工作。
ms.assetid: 2b7a0ab7-bf7e-473d-ab43-8b79478d4453
title: 如何：顯示列印工作進度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9effc778f6affaba5b53cbd96a7a428ea5554d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997126"
---
# <a name="how-to-display-the-print-job-progress"></a><span data-ttu-id="789f6-103">如何：顯示列印工作進度</span><span class="sxs-lookup"><span data-stu-id="789f6-103">How To: Display the Print Job Progress</span></span>

<span data-ttu-id="789f6-104">本主題說明如何將列印工作進度顯示給使用者，並提供選項來取消目前進行中的列印工作。</span><span class="sxs-lookup"><span data-stu-id="789f6-104">This topic describes how to display the print job progress to the user and give them the option to cancel a print job that is currently in progress.</span></span>

## <a name="overview"></a><span data-ttu-id="789f6-105">概觀</span><span class="sxs-lookup"><span data-stu-id="789f6-105">Overview</span></span>

<span data-ttu-id="789f6-106">列印進度對話方塊程式通常會執行下列功能。</span><span class="sxs-lookup"><span data-stu-id="789f6-106">A print progress dialog procedure typically performs the following functions.</span></span>

-   <span data-ttu-id="789f6-107">向使用者顯示列印工作進度。</span><span class="sxs-lookup"><span data-stu-id="789f6-107">Display print job progress to the user.</span></span>
-   <span data-ttu-id="789f6-108">啟動列印處理執行緒。</span><span class="sxs-lookup"><span data-stu-id="789f6-108">Start the print processing thread.</span></span>
-   <span data-ttu-id="789f6-109">顯示 [ **取消** ] 按鈕，讓使用者可以在列印工作完成之前予以停止。</span><span class="sxs-lookup"><span data-stu-id="789f6-109">Display a **Cancel** button so the user can stop a print job before it finishes.</span></span>

<span data-ttu-id="789f6-110">嚴格來說，列印進度對話方塊程式必須執行的工作，就是將列印工作進度顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="789f6-110">Strictly speaking, the only thing that the print progress dialog box procedure must do is display the print job progress to the user.</span></span> <span data-ttu-id="789f6-111">不過，因為上述清單中的其他兩個函式是密切相關的，所以也已包含在此課程模組中。</span><span class="sxs-lookup"><span data-stu-id="789f6-111">However, because the other two functions in the preceding list are closely related, they have also been included in this module.</span></span>

## <a name="displaying-print-job-progress"></a><span data-ttu-id="789f6-112">顯示列印工作進度</span><span class="sxs-lookup"><span data-stu-id="789f6-112">Displaying Print Job Progress</span></span>

<span data-ttu-id="789f6-113">列印進度對話方塊程式會處理下列視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="789f6-113">A print progress dialog box procedure handles the following window messages.</span></span>

-   <span data-ttu-id="789f6-114">**WM \_ INITDIALOG**</span><span class="sxs-lookup"><span data-stu-id="789f6-114">**WM\_INITDIALOG**</span></span>

    <span data-ttu-id="789f6-115">初始化對話方塊使用的控制項。</span><span class="sxs-lookup"><span data-stu-id="789f6-115">Initializes the controls that the dialog box uses.</span></span>

-   <span data-ttu-id="789f6-116">**WM \_ SETCURSOR**</span><span class="sxs-lookup"><span data-stu-id="789f6-116">**WM\_SETCURSOR**</span></span>

    <span data-ttu-id="789f6-117">當使用者可以取消列印工作時，將游標設定為指標，而當列印工作處於無法取消的時間點時，則為等候游標。</span><span class="sxs-lookup"><span data-stu-id="789f6-117">Sets the cursor to a pointer when the user is able to cancel a print job, and to the wait cursor when the print job is at a point where it cannot be cancelled.</span></span>

-   <span data-ttu-id="789f6-118">**使用者 \_ 列印 \_ 開始 \_ 列印**</span><span class="sxs-lookup"><span data-stu-id="789f6-118">**USER\_PRINT\_START\_PRINTING**</span></span>

    <span data-ttu-id="789f6-119">設定列印工作的進度列參數，並建立列印執行緒來開始處理列印工作。</span><span class="sxs-lookup"><span data-stu-id="789f6-119">Sets the progress bar parameters for the print job, and creates the printing thread to start processing the print job.</span></span>

    <span data-ttu-id="789f6-120">這是應用程式特定的視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="789f6-120">This is an application-specific window message.</span></span>

-   <span data-ttu-id="789f6-121">**WM \_ 命令-IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="789f6-121">**WM\_COMMAND - IDCANCEL**</span></span>

    <span data-ttu-id="789f6-122">設定取消事件，以指示列印處理執行緒取消列印工作。</span><span class="sxs-lookup"><span data-stu-id="789f6-122">Sets the cancel event to tell the print processing thread to cancel the print job.</span></span>

-   <span data-ttu-id="789f6-123">**使用者 \_ 列印 \_ 狀態 \_ 更新**</span><span class="sxs-lookup"><span data-stu-id="789f6-123">**USER\_PRINT\_STATUS\_UPDATE**</span></span>

    <span data-ttu-id="789f6-124">更新進度列和狀態文字，以顯示列印工作的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="789f6-124">Updates the progress bar and status text to show the current state of the print job.</span></span>

    <span data-ttu-id="789f6-125">這是應用程式特定的視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="789f6-125">This is an application-specific window message.</span></span>

-   <span data-ttu-id="789f6-126">**使用者 \_ 列印 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="789f6-126">**USER\_PRINT\_CLOSING**</span></span>

    <span data-ttu-id="789f6-127">在 [進度] 對話方塊中設定關閉狀態文字，表示列印工作正在關閉。</span><span class="sxs-lookup"><span data-stu-id="789f6-127">Sets the closing status text in the progress dialog box to indicate that the print job is closing.</span></span>

    <span data-ttu-id="789f6-128">這是應用程式特定的視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="789f6-128">This is an application-specific window message.</span></span>

-   <span data-ttu-id="789f6-129">**使用者 \_ 列印 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="789f6-129">**USER\_PRINT\_COMPLETE**</span></span>

    <span data-ttu-id="789f6-130">向使用者顯示「列印工作完成」訊息，並釋放此列印工作中使用的控制碼和事件。</span><span class="sxs-lookup"><span data-stu-id="789f6-130">Displays the "Print job complete" message to the user, and releases handles and events that were used in this print job.</span></span>

    <span data-ttu-id="789f6-131">這是應用程式特定的視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="789f6-131">This is an application-specific window message.</span></span>

 

 



