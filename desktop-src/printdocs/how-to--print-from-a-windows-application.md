---
description: 本節說明如何從原生 Windows 程式進行列印。
ms.assetid: D0AE8FF8-D02D-43D3-80CA-E13EAA894F87
title: 如何：從 Windows 程式列印
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84229823944d7f7104da359b953e579f1b21cdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978389"
---
# <a name="how-to-print-from-a-windows-program"></a><span data-ttu-id="d1006-103">如何：從 Windows 程式列印</span><span class="sxs-lookup"><span data-stu-id="d1006-103">How To: Print from a Windows Program</span></span>

<span data-ttu-id="d1006-104">本節說明如何從原生 Windows 程式進行列印。</span><span class="sxs-lookup"><span data-stu-id="d1006-104">This section describes how to print from a native Windows program.</span></span>

## <a name="overview"></a><span data-ttu-id="d1006-105">概觀</span><span class="sxs-lookup"><span data-stu-id="d1006-105">Overview</span></span>

<span data-ttu-id="d1006-106">列印通常是原生 Windows 程式不可或缺的一部分。</span><span class="sxs-lookup"><span data-stu-id="d1006-106">Printing is usually an integral part of a native Windows program.</span></span> <span data-ttu-id="d1006-107">因此，它不是您在撰寫程式之後可以輕鬆新增的功能。</span><span class="sxs-lookup"><span data-stu-id="d1006-107">Therefore, it is not a feature that you can add easily after you have written the program.</span></span> <span data-ttu-id="d1006-108">話雖如此，如果程式設計為使用 XPS 檔，則不需要太多額外的程式碼，就能轉譯檔內容以進行列印。</span><span class="sxs-lookup"><span data-stu-id="d1006-108">That being said, if the program is designed to use XPS documents it will not need much, if any, additional code to render the document content for printing.</span></span> <span data-ttu-id="d1006-109">應用程式的 XPS 檔可以直接傳送到具有 XPSDrv 印表機驅動程式的印表機。</span><span class="sxs-lookup"><span data-stu-id="d1006-109">The XPS documents of the application can be sent directly to a printer that has an XPSDrv printer driver.</span></span>

<span data-ttu-id="d1006-110">使用 [Xps 檔 api](/previous-versions/windows/desktop/dd316976(v=vs.85)) 來建立檔內容和 [xps 列印 api](xps-printing.md) ，以將檔內容傳送至印表機。</span><span class="sxs-lookup"><span data-stu-id="d1006-110">Use the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) to create the document content and the [XPS Print API](xps-printing.md) to send the document content to the printer.</span></span> <span data-ttu-id="d1006-111">XPS 列印 API 會處理目的地印表機的檔內容。</span><span class="sxs-lookup"><span data-stu-id="d1006-111">The XPS Print API processes the document content for the destination printer.</span></span> <span data-ttu-id="d1006-112">如果選取的印表機具有 XPSDrv 印表機驅動程式，則會將檔傳送至印表機，而不需要任何額外的轉換。</span><span class="sxs-lookup"><span data-stu-id="d1006-112">If the selected printer has an XPSDrv printer driver, the document will be sent to the printer without any additional conversion.</span></span> <span data-ttu-id="d1006-113">如果選取的印表機有以 GDI 為基礎的印表機驅動程式，則程式也可以將內容傳送至印表機，而且 XPS 列印 API 會轉換檔內容，使其與以 GDI 為基礎的印表機驅動程式相容。</span><span class="sxs-lookup"><span data-stu-id="d1006-113">If the selected printer has a GDI-based printer driver, the program can also send the content to the printer, and the XPS Print API converts the document content so that it will be compatible with the GDI-based printer driver.</span></span> <span data-ttu-id="d1006-114">無論是哪一種情況，應用程式執行的處理方式都相同。</span><span class="sxs-lookup"><span data-stu-id="d1006-114">In either case, the processing that the application performs is the same.</span></span>

## <a name="printing-tasks"></a><span data-ttu-id="d1006-115">列印工作</span><span class="sxs-lookup"><span data-stu-id="d1006-115">Printing tasks</span></span>

<span data-ttu-id="d1006-116">下列主題描述列印程式內容的基本步驟。</span><span class="sxs-lookup"><span data-stu-id="d1006-116">The following topics describe the basic steps of printing program content.</span></span>

1.  <span data-ttu-id="d1006-117">**收集使用者的列印工作資訊。**</span><span class="sxs-lookup"><span data-stu-id="d1006-117">**Collect print job information from user.**</span></span>

    <span data-ttu-id="d1006-118">一般情況下，當使用者從功能表中選取 [列印] 選項，而且程式顯示 [列印] 對話方塊來收集列印工作的詳細資料時，使用者就會起始列印工作。</span><span class="sxs-lookup"><span data-stu-id="d1006-118">Typically, a user initiates a print job when they select the print option from a menu and the program displays a print dialog box to collect the details of the print job.</span></span> <span data-ttu-id="d1006-119">使用者通常會選取印表機、複本數目，以及印表機設定詳細資料，例如雙面列印和裝訂。</span><span class="sxs-lookup"><span data-stu-id="d1006-119">The user typically selects the printer, the number of copies, and printer configuration details such as two-sided printing and stapling.</span></span>

    <span data-ttu-id="d1006-120">如需有關如何執行此動作的詳細資訊，請參閱 [如何：收集使用者的列印工作資訊](preparing-to-print.md)。</span><span class="sxs-lookup"><span data-stu-id="d1006-120">For information about how to do this, see [How To: Collect Print Job Information from the User](preparing-to-print.md).</span></span>

2.  <span data-ttu-id="d1006-121">**建立進度指標。**</span><span class="sxs-lookup"><span data-stu-id="d1006-121">**Create progress indicator.**</span></span>

    <span data-ttu-id="d1006-122">進度指示器可為使用者提供列印工作進度的意見反應。</span><span class="sxs-lookup"><span data-stu-id="d1006-122">A progress indicator provides the user with feedback about how the print job is progressing.</span></span> <span data-ttu-id="d1006-123">進度列指示器可以是包含作業之 [ **取消** ] 按鈕的對話方塊一部分的進度列，也可以是主視窗底部狀態列中的進度列。</span><span class="sxs-lookup"><span data-stu-id="d1006-123">The progress indicator can be a progress bar that is part of a dialog box that includes the **Cancel** button for the job, or it can be a progress bar in the status bar at the bottom of the main window.</span></span>

    <span data-ttu-id="d1006-124">如需進度指示器運作的詳細資訊，請參閱 [如何：顯示列印工作進度](cancel-dialog-box.md)。</span><span class="sxs-lookup"><span data-stu-id="d1006-124">For information about the progress indicator works, see [How To: Display the Print Job Progress](cancel-dialog-box.md).</span></span>

    <span data-ttu-id="d1006-125">如需有關如何顯示列印工作進度的詳細資訊，請參閱 [Windows 應用程式 UI 開發](/windows/desktop/windows-application-ui-development) 指導方針中的資訊。</span><span class="sxs-lookup"><span data-stu-id="d1006-125">For more ideas about how to display the progress of the print job, see the information in the [Windows Application UI Development](/windows/desktop/windows-application-ui-development) guidelines.</span></span>

3.  <span data-ttu-id="d1006-126">**啟動列印執行緒。**</span><span class="sxs-lookup"><span data-stu-id="d1006-126">**Start the printing thread.**</span></span>

    <span data-ttu-id="d1006-127">在程式收集使用者的列印工作資訊之後，就可以啟動列印執行緒來執行檔的實際處理，以進行列印。</span><span class="sxs-lookup"><span data-stu-id="d1006-127">After the program has collected the print job information from the user, it can start the printing thread to perform the actual processing of the document for printing.</span></span>

    <span data-ttu-id="d1006-128">如需列印執行緒的詳細資訊，請參閱 [如何：啟動和停止列印執行緒](how-to--start-and-stop-a-printing-thread.md)。</span><span class="sxs-lookup"><span data-stu-id="d1006-128">For information about the printing thread, see [How To: Start and Stop a Printing Thread](how-to--start-and-stop-a-printing-thread.md).</span></span>

4.  <span data-ttu-id="d1006-129">**轉譯列印工作資料。**</span><span class="sxs-lookup"><span data-stu-id="d1006-129">**Render print job data.**</span></span>

    <span data-ttu-id="d1006-130">列印執行緒會轉譯檔資料以進行列印。</span><span class="sxs-lookup"><span data-stu-id="d1006-130">The printing thread renders the document data for printing.</span></span> <span data-ttu-id="d1006-131">您應該將此處理細分為離散的處理步驟，讓使用者可以中斷處理並取消作業，以及不允許處理執行緒封鎖其他執行緒和進程。</span><span class="sxs-lookup"><span data-stu-id="d1006-131">You should break down this processing into discrete processing steps so that the user can interrupt the processing and cancel the job as well as to not allow the processing thread to block other threads and processes.</span></span>

    <span data-ttu-id="d1006-132">如需如何呈現列印工作資料的詳細資訊，請參閱 [如何：轉譯列印工作資料](how-to--render-the-print-job-data.md)。</span><span class="sxs-lookup"><span data-stu-id="d1006-132">For information about how the renders the print job data, see [How To: Render Print Job Data](how-to--render-the-print-job-data.md).</span></span>

5.  <span data-ttu-id="d1006-133">**監視列印工作進度。**</span><span class="sxs-lookup"><span data-stu-id="d1006-133">**Monitor print job progress.**</span></span>

    <span data-ttu-id="d1006-134">執行每個處理步驟時，請更新進度列以通知使用。</span><span class="sxs-lookup"><span data-stu-id="d1006-134">As each processing step is performed, update the progress bar to inform the use.</span></span> <span data-ttu-id="d1006-135">計算完成所要求作業的處理步驟，然後在執行這些步驟時更新進度列。</span><span class="sxs-lookup"><span data-stu-id="d1006-135">Compute the processing steps to complete the requested job and then updates the progress bar as those steps are performed.</span></span>

6.  <span data-ttu-id="d1006-136">**關閉列印工作，並結束列印執行緒。**</span><span class="sxs-lookup"><span data-stu-id="d1006-136">**Close print job and terminate printing thread.**</span></span>

    <span data-ttu-id="d1006-137">當程式將列印工作傳送至印表機，或使用者已取消列印工作之後，您必須關閉列印工作，並釋放列印工作所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="d1006-137">After the program has sent the print job to the printer, or if the user has cancelled the print job, you must close the print job and release the resources used by the print job.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1006-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="d1006-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1006-139">如何：收集使用者的列印工作資訊</span><span class="sxs-lookup"><span data-stu-id="d1006-139">How To: Collect Print Job Information from the User</span></span>](preparing-to-print.md)
</dt> </dl>

 

 
