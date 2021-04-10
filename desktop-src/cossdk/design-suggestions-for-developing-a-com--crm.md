---
description: 開發 COM + CRM 的設計建議
ms.assetid: dde1b978-6d35-4a75-91fd-69dfcc6c43d2
title: 開發 COM + CRM 的設計建議
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dcdb59f0ea23fb6879300d0bacec7df12970d81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187713"
---
# <a name="design-suggestions-for-developing-a-com-crm"></a><span data-ttu-id="68505-103">開發 COM + CRM 的設計建議</span><span class="sxs-lookup"><span data-stu-id="68505-103">Design Suggestions for Developing a COM+ CRM</span></span>

<span data-ttu-id="68505-104">以下是開發 COM + CRM 的建議步驟：</span><span class="sxs-lookup"><span data-stu-id="68505-104">Following are suggested steps for developing a COM+ CRM:</span></span>

1.  <span data-ttu-id="68505-105">開始開發之前，請使用 [元件服務] 系統管理工具) 將交易超時設定為零 (。</span><span class="sxs-lookup"><span data-stu-id="68505-105">Before starting development, set the transaction time-out to zero (using the Component Services administrative tool).</span></span> <span data-ttu-id="68505-106">設定 VTRACE1 登錄旗標 (查看 [Com + CRM 登錄設定](com--crm-registry-settings.md)) ，以查看調試追蹤上的 CRM 警告和錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="68505-106">Set the VTRACE1 registry flag (see [COM+ CRM Registry Settings](com--crm-registry-settings.md)) to see CRM warning and error messages on the debug trace.</span></span>
2.  <span data-ttu-id="68505-107">判斷您需要使用的介面集、結構化 (變異) 或非結構化。</span><span class="sxs-lookup"><span data-stu-id="68505-107">Determine which set of interfaces you need to use, structured (Variants) or non-structured.</span></span> <span data-ttu-id="68505-108"> (請參閱 [Com + CRM 介面](com--crm-interfaces.md)。 ) 這將取決於您用來開發 CRM 的語言，例如 Microsoft Visual C++ 或 Microsoft Visual Basic。</span><span class="sxs-lookup"><span data-stu-id="68505-108">(See [COM+ CRM Interfaces](com--crm-interfaces.md).) This will depend on the language that you use to develop your CRM—for example, Microsoft Visual C++ or Microsoft Visual Basic.</span></span>
3.  <span data-ttu-id="68505-109">先開發 CRM 背景工作角色。</span><span class="sxs-lookup"><span data-stu-id="68505-109">Develop the CRM worker first.</span></span> <span data-ttu-id="68505-110">判斷記錄檔記錄中所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="68505-110">Determine the information that is required in the log records.</span></span> <span data-ttu-id="68505-111">定義所需的記錄檔記錄類型和其格式。</span><span class="sxs-lookup"><span data-stu-id="68505-111">Define the types of log records required and their format.</span></span>
4.  <span data-ttu-id="68505-112">在 Windows SDK) 中，會在 CRM 範例 (中提供 debug CRM 補償器的一部分。</span><span class="sxs-lookup"><span data-stu-id="68505-112">A debug CRM compensator is provided as part of the CRM samples (in the Windows SDK).</span></span> <span data-ttu-id="68505-113">當您將 CRM 工作者取代為實際的 CRM 補償器時，可以暫時使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="68505-113">This can be used temporarily when debugging the CRM worker in place of the real CRM compensator.</span></span>
5.  <span data-ttu-id="68505-114">當 CRM 背景工作正常運作時，開發實際的 CRM 補償器，並將 debug CRM 補償器取代為實際的 CRM 補償器。</span><span class="sxs-lookup"><span data-stu-id="68505-114">When the CRM worker is working correctly, develop the real CRM compensator and replace the debug CRM compensator with the real CRM compensator.</span></span>
6.  <span data-ttu-id="68505-115">建議您一開始不需要測試復原案例。</span><span class="sxs-lookup"><span data-stu-id="68505-115">It may be desirable to initially not test the recovery case.</span></span> <span data-ttu-id="68505-116">若是如此，請在啟動 crm 伺服器應用程式之前，每次都刪除 CRM 伺服器應用程式的 CRM 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="68505-116">If so, delete the CRM log file for the CRM server application each time before starting that CRM server application.</span></span>

## <a name="considerations"></a><span data-ttu-id="68505-117">考量</span><span class="sxs-lookup"><span data-stu-id="68505-117">Considerations</span></span>

1.  <span data-ttu-id="68505-118">**事先撰寫。**</span><span class="sxs-lookup"><span data-stu-id="68505-118">**Write ahead.**</span></span> <span data-ttu-id="68505-119">CRM 背景工作元件必須先行寫入;也就是說，它必須撰寫記錄檔記錄，指出它會在實際執行該動作之前執行動作。</span><span class="sxs-lookup"><span data-stu-id="68505-119">The CRM worker component must write ahead; that is, it must write a log record indicating it is going to perform an action before actually performing that action.</span></span> <span data-ttu-id="68505-120">此外，此記錄檔記錄必須在寫入後和執行動作之前強制寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="68505-120">In addition, this log record must be forced to disk after the write and before the action is performed.</span></span>
2.  <span data-ttu-id="68505-121">**分離。**</span><span class="sxs-lookup"><span data-stu-id="68505-121">**Isolation.**</span></span> <span data-ttu-id="68505-122">CRM 不會強制執行隔離。</span><span class="sxs-lookup"><span data-stu-id="68505-122">The CRM does not enforce isolation.</span></span> <span data-ttu-id="68505-123">CRM 設計必須在不同的交易上提供多個用戶端之間的隔離，而且也必須考慮復原之前的案例。</span><span class="sxs-lookup"><span data-stu-id="68505-123">The CRM design must provide isolation between multiple clients on separate transactions and must also consider the case prior to recovery.</span></span>
3.  <span data-ttu-id="68505-124">**正在復原。**</span><span class="sxs-lookup"><span data-stu-id="68505-124">**Recovery in progress.**</span></span> <span data-ttu-id="68505-125">CRM 工作者必須處理「正在復原」錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="68505-125">The CRM worker must handle the "recovery in progress" error code.</span></span> <span data-ttu-id="68505-126">如需有關此錯誤碼的詳細資訊，請參閱 [COM + CRM 的疑難排解](troubleshooting-the-com--crm.md) 。</span><span class="sxs-lookup"><span data-stu-id="68505-126">See [Troubleshooting the COM+ CRM](troubleshooting-the-com--crm.md) for more information about this error code.</span></span>
4.  <span data-ttu-id="68505-127">**錯誤處理。**</span><span class="sxs-lookup"><span data-stu-id="68505-127">**Error handling.**</span></span> <span data-ttu-id="68505-128">CRM 工作者必須處理交易比預期早中止的情況。</span><span class="sxs-lookup"><span data-stu-id="68505-128">The CRM worker must cope with the case where the transaction is aborted earlier than expected.</span></span> <span data-ttu-id="68505-129">請參閱 [COM + CRM 中的錯誤處理](error-handling-in-the-com--crm.md)一節。</span><span class="sxs-lookup"><span data-stu-id="68505-129">See the section [Error Handling in the COM+ CRM](error-handling-in-the-com--crm.md).</span></span>
5.  <span data-ttu-id="68505-130">**復原時間。**</span><span class="sxs-lookup"><span data-stu-id="68505-130">**Recovery time.**</span></span> <span data-ttu-id="68505-131">CRM 補償器應設計為可快速執行復原，讓該 CRM 伺服器應用程式的新工作不需要等待。</span><span class="sxs-lookup"><span data-stu-id="68505-131">The CRM compensator should be designed to perform recovery quickly so that new work for that CRM server application does not have to wait.</span></span>
6.  <span data-ttu-id="68505-132">**等冪.**</span><span class="sxs-lookup"><span data-stu-id="68505-132">**Idempotence.**</span></span> <span data-ttu-id="68505-133">CRM 補償器可能會再次收到相同的記錄檔記錄，以復原或重做已復原或重做的動作。</span><span class="sxs-lookup"><span data-stu-id="68505-133">It is possible that a CRM compensator might receive the same log record again, to undo or redo an action that has already been undone or redone.</span></span> <span data-ttu-id="68505-134">CRM 補償器可能執行的動作必須具有等冪性，這通常表示應該忽略從這些動作傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="68505-134">Actions that the CRM compensator might perform must be idempotent, which often means that the error codes returned from these actions should be ignored.</span></span>
7.  <span data-ttu-id="68505-135">**復原的初始。**</span><span class="sxs-lookup"><span data-stu-id="68505-135">**Initiation of recovery.**</span></span> <span data-ttu-id="68505-136">當 CRM 伺服器應用程式啟動時，就會執行 CRM 伺服器應用程式的復原。</span><span class="sxs-lookup"><span data-stu-id="68505-136">Recovery of a CRM server application is performed when that CRM server application starts up.</span></span> <span data-ttu-id="68505-137">但是，CRM 伺服器應用程式並不會自動啟動。</span><span class="sxs-lookup"><span data-stu-id="68505-137">However, there is no automatic startup of a CRM server application.</span></span> <span data-ttu-id="68505-138">應用程式開發人員應該考慮啟動和復原的起始方式。</span><span class="sxs-lookup"><span data-stu-id="68505-138">The application developer should consider how both startup and recovery should be initiated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68505-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="68505-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68505-140">COM + 補償 Resource Manager 概念</span><span class="sxs-lookup"><span data-stu-id="68505-140">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



