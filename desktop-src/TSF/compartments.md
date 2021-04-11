---
title: 車廂
description: 車廂
ms.assetid: 7bffab6f-be40-4d3a-9342-6f81557a9656
keywords:
- 文字服務架構 (TSF) 、區間
- TSF (文字服務架構) 、區間
- 文字服務，區間
- 啟用 TSF 的應用程式，區間
- 車廂
- 文字服務架構 (TSF) 、區間類型
- TSF (文字服務架構) 、區間類型
- 文字服務、區間類型
- 啟用 TSF 的應用程式，區間類型
- 區間類型
- 文字服務架構 (TSF) 、區間變更通知
- TSF (文字服務架構) ，區間變更通知
- 文字服務，區間變更通知
- 啟用 TSF 的應用程式，區間變更通知
- 區間變更通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76636c684ee74f7e452b5602ebfd59d6d1947b0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183260"
---
# <a name="compartments"></a><span data-ttu-id="4ed7d-118">車廂</span><span class="sxs-lookup"><span data-stu-id="4ed7d-118">Compartments</span></span>

## <a name="compartment-types"></a><span data-ttu-id="4ed7d-119">區間類型</span><span class="sxs-lookup"><span data-stu-id="4ed7d-119">Compartment Types</span></span>

<span data-ttu-id="4ed7d-120">有數種不同類型的區間。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-120">There are several different types of compartments.</span></span> <span data-ttu-id="4ed7d-121">有一個全域區間，而且每個執行緒管理員、檔管理員和內容都可以包含區間。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-121">There is a global compartment, and each thread manager, document manager, and context can contain a compartment.</span></span>

<span data-ttu-id="4ed7d-122">全域區間可讓用戶端跨進程共用資料。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-122">The global compartment enables clients to share data across processes.</span></span> <span data-ttu-id="4ed7d-123">若要取得全域區間管理員，請呼叫 [**ITfThreadMgr：： GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-123">To obtain the global compartment manager, call [**ITfThreadMgr::GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).</span></span>

<span data-ttu-id="4ed7d-124">執行緒管理員包含區間管理員，其中包含每個執行緒的區間。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-124">The thread manager contains a compartment manager that contains compartments on a per-thread basis.</span></span> <span data-ttu-id="4ed7d-125">這可讓您線上程內共用資料。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-125">This allows data to be shared within a thread.</span></span> <span data-ttu-id="4ed7d-126">若要取得執行緒管理員區間管理員，請使用 IID ITfCompartmentMgr 呼叫 **ITfThreadMgr：： QueryInterface** \_ 。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-126">To obtain a thread manager compartment manager, call **ITfThreadMgr::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

<span data-ttu-id="4ed7d-127">每個建立的檔管理員也都包含區間管理員。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-127">Each document manager created also contains a compartment manager.</span></span> <span data-ttu-id="4ed7d-128">這可讓您在特定檔管理員內共用資料。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-128">This allows data to be shared within a specific document manager.</span></span> <span data-ttu-id="4ed7d-129">若要取得檔管理員區間管理員，請使用 IID ITfCompartmentMgr 呼叫 **ITfDocumentMgr：： QueryInterface** \_ 。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-129">To obtain the document manager compartment manager, call **ITfDocumentMgr::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

<span data-ttu-id="4ed7d-130">所建立的每個內容也會包含區間管理員。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-130">Each context created also contains a compartment manager.</span></span> <span data-ttu-id="4ed7d-131">這可讓您在特定內容中共用資料。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-131">This allows data to be shared within a specific context.</span></span> <span data-ttu-id="4ed7d-132">若要取得內容區間管理員，請使用 IID ITfCompartmentMgr 呼叫 **ITfCoNtext：： QueryInterface** \_ 。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-132">To obtain a context compartment manager, call **ITfContext::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

## <a name="creating-and-deleting-a-compartment"></a><span data-ttu-id="4ed7d-133">建立和刪除區間</span><span class="sxs-lookup"><span data-stu-id="4ed7d-133">Creating and Deleting a Compartment</span></span>

<span data-ttu-id="4ed7d-134">第一次使用區間 GUID 呼叫 [**ITfCompartmentMgr：： GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) 時，會建立區間。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-134">A compartment is created the first time [**ITfCompartmentMgr::GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) is called with the compartment GUID.</span></span> <span data-ttu-id="4ed7d-135">安裝用戶端應該使用 [**ITfCompartment：： SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)設定區間的初始值。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-135">The installing client should set the initial value of the compartment using [**ITfCompartment::SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue).</span></span> <span data-ttu-id="4ed7d-136">在設定值之前，區間值是空的。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-136">Until a value is set, the compartment value is empty.</span></span> <span data-ttu-id="4ed7d-137">因此，在呼叫 **GetCompartment** 之前，無法驗證區間是否存在。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-137">Because of this, there is no way to verify that the compartment existed before **GetCompartment** was called.</span></span> <span data-ttu-id="4ed7d-138">為了避免這種情況，安裝用戶端應該將值設定為某個初始值，讓其他用戶端可以判斷區間是否已存在。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-138">To avoid this situation, the installing client should set the value to some initial value so that other clients can determine if the compartment already exists.</span></span>

<span data-ttu-id="4ed7d-139">[**ITfCompartmentMgr：： ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)方法用來移除區間。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-139">The [**ITfCompartmentMgr::ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) method is used to remove a compartment.</span></span> <span data-ttu-id="4ed7d-140">區間的任何現有參考都會標示為無效。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-140">Any existing references to the compartment are marked invalid.</span></span>

## <a name="obtaining-compartments"></a><span data-ttu-id="4ed7d-141">取得區間</span><span class="sxs-lookup"><span data-stu-id="4ed7d-141">Obtaining Compartments</span></span>

<span data-ttu-id="4ed7d-142">用戶端可以使用 [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) 介面，藉由呼叫 [**ITfCompartmentMgr：： EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)來列舉區間。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-142">Using the [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) interface, a client can enumerate compartments by calling [**ITfCompartmentMgr::EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments).</span></span> <span data-ttu-id="4ed7d-143">這個方法會提供 **IEnumGUID** 物件，其中包含所有已安裝之區間的 guid。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-143">This method provides an **IEnumGUID** object that contains the GUIDs of all of the installed compartments.</span></span>

<span data-ttu-id="4ed7d-144">使用區間 GUID， **ITfCompartmentMgr：： GetCompartment** 可用來取得特定區間。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-144">Using the compartment GUID , **ITfCompartmentMgr::GetCompartment** is used to obtain a specific compartment.</span></span> <span data-ttu-id="4ed7d-145">這個方法會為呼叫端提供可取得及設定區間資料的 [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) 物件。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-145">This method provides the caller with an [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) object that can obtain and set the compartment data.</span></span>

## <a name="receiving-compartment-change-notifications"></a><span data-ttu-id="4ed7d-146">接收區間變更通知</span><span class="sxs-lookup"><span data-stu-id="4ed7d-146">Receiving Compartment Change Notifications</span></span>

<span data-ttu-id="4ed7d-147">當區間的值變更時，TSF manager 會通知任何已安裝的通知接收器，區間已變更。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-147">When the value of a compartment changes, the TSF manager notifies any installed advise sinks that the compartment has changed.</span></span> <span data-ttu-id="4ed7d-148">若要安裝區間變更建議接收器，請建立可執行 [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)的物件。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-148">To install a compartment change advise sink, create an object that implements [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink).</span></span> <span data-ttu-id="4ed7d-149">然後，在要監視的區間物件上，對 IID ITfSource 呼叫 **ITfCompartment：： QueryInterface** ， \_ 以取得 [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) 介面。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-149">Then call **ITfCompartment::QueryInterface** with IID\_ITfSource on the compartment object to be monitored to obtain an [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) interface.</span></span> <span data-ttu-id="4ed7d-150">現在呼叫 [**ITfSource：： AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) 搭配 IID \_ ITfCompartmentEventSink 和 **ITfCompartmentEventSink** 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-150">Now call [**ITfSource::AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) with IID\_ITfCompartmentEventSink and the pointer to the **ITfCompartmentEventSink** object.</span></span> <span data-ttu-id="4ed7d-151">當區間的值變更時，會以區間的 GUID 呼叫建議接收器的 [**ITfCompartmentEventSink：： OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) 。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-151">When the value of the compartment changes, the advise sink's [**ITfCompartmentEventSink::OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) is called with the GUID of the compartment.</span></span> <span data-ttu-id="4ed7d-152">建議接收可呼叫 [**ITfCompartment：： GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) 來取得新值。</span><span class="sxs-lookup"><span data-stu-id="4ed7d-152">The advise sink can call [**ITfCompartment::GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) to obtain the new value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ed7d-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="4ed7d-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ed7d-154">**ITfCompartmentMgr**</span><span class="sxs-lookup"><span data-stu-id="4ed7d-154">**ITfCompartmentMgr**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr)
</dt> <dt>

[<span data-ttu-id="4ed7d-155">**ITfCompartment**</span><span class="sxs-lookup"><span data-stu-id="4ed7d-155">**ITfCompartment**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartment)
</dt> <dt>

[<span data-ttu-id="4ed7d-156">**ITfCompartmentEventSink**</span><span class="sxs-lookup"><span data-stu-id="4ed7d-156">**ITfCompartmentEventSink**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)
</dt> <dt>

[<span data-ttu-id="4ed7d-157">**TfClientId**</span><span class="sxs-lookup"><span data-stu-id="4ed7d-157">**TfClientId**</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="4ed7d-158">**ITfThreadMgr：： GetGlobalCompartment**</span><span class="sxs-lookup"><span data-stu-id="4ed7d-158">**ITfThreadMgr::GetGlobalCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)
</dt> <dt>

[<span data-ttu-id="4ed7d-159">**ITfCompartmentMgr::GetCompartment**</span><span class="sxs-lookup"><span data-stu-id="4ed7d-159">**ITfCompartmentMgr::GetCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment)
</dt> <dt>

[<span data-ttu-id="4ed7d-160">**ITfCompartment：： SetValue**</span><span class="sxs-lookup"><span data-stu-id="4ed7d-160">**ITfCompartment::SetValue**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)
</dt> <dt>

[<span data-ttu-id="4ed7d-161">**ITfCompartmentMgr::ClearCompartment**</span><span class="sxs-lookup"><span data-stu-id="4ed7d-161">**ITfCompartmentMgr::ClearCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)
</dt> <dt>

[<span data-ttu-id="4ed7d-162">**ITfCompartmentMgr::EnumCompartments**</span><span class="sxs-lookup"><span data-stu-id="4ed7d-162">**ITfCompartmentMgr::EnumCompartments**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)
</dt> <dt>

[<span data-ttu-id="4ed7d-163">**ITfSource**</span><span class="sxs-lookup"><span data-stu-id="4ed7d-163">**ITfSource**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfsource)
</dt> <dt>

[<span data-ttu-id="4ed7d-164">**ITfSource::AdviseSink**</span><span class="sxs-lookup"><span data-stu-id="4ed7d-164">**ITfSource::AdviseSink**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> <dt>

[<span data-ttu-id="4ed7d-165">**ITfCompartmentEventSink：： OnChange**</span><span class="sxs-lookup"><span data-stu-id="4ed7d-165">**ITfCompartmentEventSink::OnChange**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange)
</dt> </dl>

 

 




