---
description: 從 TAPI 2.1 開始，您可以使用電話語音服務提供者的使用者介面 Dll 來管理和顯示對話方塊。 TAPI 會將 DLL 載入至應用程式的進程，此應用程式會叫用任何可顯示對話方塊的服務提供者函數。
ms.assetid: 0a0320d1-fb75-405e-8074-b37cef956c9f
title: TSPI 2.1 版的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51642fb9ac960732f8e4a56805652333d0c32468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987649"
---
# <a name="whats-new-for-tspi-version-21"></a><span data-ttu-id="6a9dc-104">TSPI 2.1 版的新功能</span><span class="sxs-lookup"><span data-stu-id="6a9dc-104">What's New for TSPI Version 2.1</span></span>

<span data-ttu-id="6a9dc-105">從 TAPI 2.1 開始，您可以使用電話語音服務提供者的使用者介面 Dll 來管理和顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6a9dc-105">Starting with TAPI 2.1, the telephony service provider user interface DLLs can be used to manage and display dialog boxes.</span></span> <span data-ttu-id="6a9dc-106">TAPI 會將 DLL 載入至應用程式的進程，此應用程式會叫用任何可顯示對話方塊的服務提供者函數。</span><span class="sxs-lookup"><span data-stu-id="6a9dc-106">TAPI loads the DLL into the process of an application that invokes any of the service provider functions that can display a dialog.</span></span>

<span data-ttu-id="6a9dc-107">從 TAPI 2.1 開始，可以實作為 proxy 要求處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a9dc-107">Starting with TAPI 2.1, proxy request handlers can be implemented.</span></span> <span data-ttu-id="6a9dc-108">處理常式是一種完整的電話語音應用程式，通常會在電話語音伺服器上執行，並提供比驅動程式更適當地在應用程式中執行的服務。</span><span class="sxs-lookup"><span data-stu-id="6a9dc-108">A handler is a full telephony application that normally executes on a telephony server and provides services that are more appropriately implemented in an application than a driver.</span></span>

<span data-ttu-id="6a9dc-109">針對 TSPI 2.1 版新增或變更的函式和訊息如下所示：</span><span class="sxs-lookup"><span data-stu-id="6a9dc-109">Functions and messages that were new or changed for TSPI version 2.1 are as follows:</span></span>

-   [<span data-ttu-id="6a9dc-110">**TSPI_lineConditionalMediaDetection**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-110">**TSPI_lineConditionalMediaDetection**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   <span data-ttu-id="6a9dc-111">**TSPI_lineDropNoOwner**-**淘汰**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-111">**TSPI_lineDropNoOwner**—**obsolete**</span></span>
-   <span data-ttu-id="6a9dc-112">**TSPI_lineDropOnClose**-**淘汰**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-112">**TSPI_lineDropOnClose**—**obsolete**</span></span>
-   [<span data-ttu-id="6a9dc-113">**TSPI_lineGetID**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-113">**TSPI_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [<span data-ttu-id="6a9dc-114">**TSPI_lineSetCallData**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-114">**TSPI_lineSetCallData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [<span data-ttu-id="6a9dc-115">**TSPI_lineSetCallQualityOfService**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-115">**TSPI_lineSetCallQualityOfService**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [<span data-ttu-id="6a9dc-116">**TSPI_lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-116">**TSPI_lineSetCallTreatment**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [<span data-ttu-id="6a9dc-117">**TSPI_lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-117">**TSPI_lineSetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [<span data-ttu-id="6a9dc-118">**TSPI_phoneGetID**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-118">**TSPI_phoneGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonegetid)
-   [<span data-ttu-id="6a9dc-119">**TSPI_providerInit**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-119">**TSPI_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)
-   [<span data-ttu-id="6a9dc-120">**TSPI_providerShutdown**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-120">**TSPI_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)
-   <span data-ttu-id="6a9dc-121">[**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a9dc-121">[**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))</span></span>
-   <span data-ttu-id="6a9dc-122">[**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a9dc-122">[**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))</span></span>
-   <span data-ttu-id="6a9dc-123">[**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a9dc-123">[**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))</span></span>
-   <span data-ttu-id="6a9dc-124">[**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a9dc-124">[**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))</span></span>
-   <span data-ttu-id="6a9dc-125">[**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a9dc-125">[**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))</span></span>
-   <span data-ttu-id="6a9dc-126">[**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a9dc-126">[**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))</span></span>
-   <span data-ttu-id="6a9dc-127">[**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a9dc-127">[**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))</span></span>

<span data-ttu-id="6a9dc-128">電話語音服務提供者使用者介面 DLL 提供了一種方法，可讓使用者在應用程式的內容中進行互動，而不是服務提供者本身。</span><span class="sxs-lookup"><span data-stu-id="6a9dc-128">The Telephony service provider user interface DLL provides a means of allowing user interaction within the context of the application rather than the service provider itself.</span></span> <span data-ttu-id="6a9dc-129">TSPI 2.1 版提供了下列新的函式、訊息和結構來執行：</span><span class="sxs-lookup"><span data-stu-id="6a9dc-129">TSPI version 2.1 delivered the following new functions, messages, and structures for implementation:</span></span>

-   [<span data-ttu-id="6a9dc-130">**TSPI_providerFreeDialogInstance**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-130">**TSPI_providerFreeDialogInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance)
-   [<span data-ttu-id="6a9dc-131">**TSPI_providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-131">**TSPI_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata)
-   [<span data-ttu-id="6a9dc-132">**TSPI_providerUIIdentify**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-132">**TSPI_providerUIIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify)
-   [<span data-ttu-id="6a9dc-133">**TUISPI_lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-133">**TUISPI_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)
-   [<span data-ttu-id="6a9dc-134">**TUISPI_lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-134">**TUISPI_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit)
-   [<span data-ttu-id="6a9dc-135">**TUISPI_phoneConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-135">**TUISPI_phoneConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog)
-   [<span data-ttu-id="6a9dc-136">**TUISPI_providerConfig**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-136">**TUISPI_providerConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig)
-   [<span data-ttu-id="6a9dc-137">**TUISPI_providerGenericDialog**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-137">**TUISPI_providerGenericDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog)
-   [<span data-ttu-id="6a9dc-138">**TUISPI_providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-138">**TUISPI_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
-   [<span data-ttu-id="6a9dc-139">**TUISPI_providerInstall**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-139">**TUISPI_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)
-   [<span data-ttu-id="6a9dc-140">**TUISPI_providerRemove**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-140">**TUISPI_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)
-   [<span data-ttu-id="6a9dc-141">**TUISPICREATEDIALOGINSTANCEPARAMS**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-141">**TUISPICREATEDIALOGINSTANCEPARAMS**</span></span>](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
-   [<span data-ttu-id="6a9dc-142">**TUISPIDLLCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-142">**TUISPIDLLCALLBACK**</span></span>](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
-   [<span data-ttu-id="6a9dc-143">**LINE_CREATEDIALOGINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-143">**LINE_CREATEDIALOGINSTANCE**</span></span>](line-createdialoginstance.md)
-   [<span data-ttu-id="6a9dc-144">**LINE_SENDDIALOGINSTANCEDATA**</span><span class="sxs-lookup"><span data-stu-id="6a9dc-144">**LINE_SENDDIALOGINSTANCEDATA**</span></span>](line-senddialoginstancedata.md)

 

 
