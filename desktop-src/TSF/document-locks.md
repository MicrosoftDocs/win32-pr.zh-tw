---
title: 檔鎖定
description: 檔鎖定
ms.assetid: 3c623c44-b0d3-4b03-8de9-25f1062b5726
keywords:
- 文字服務架構 (TSF) 、檔鎖定
- TSF (文字服務架構) ，檔鎖定
- 啟用 TSF 的應用程式，檔鎖定
- 檔鎖定
- '文字服務架構 (TSF) ，應用程式字元位置 (ACP) '
- 'TSF (文字服務架構) ，應用程式字元位置 (ACP) '
- '啟用 TSF 的應用程式，應用程式字元位置 (ACP) '
- '應用程式字元位置 (ACP) '
- 'ACP (應用程式字元位置) '
- 文字服務架構 (TSF) 、錨點
- TSF (文字服務架構) 、錨點
- 啟用 TSF 的應用程式，錨點
- 錨點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438e22d7c77a45d798dfd6d5d7c43eaafa3e09c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183259"
---
# <a name="document-locks"></a><span data-ttu-id="6a48c-116">檔鎖定</span><span class="sxs-lookup"><span data-stu-id="6a48c-116">Document Locks</span></span>

## <a name="the-document-lock-protocol"></a><span data-ttu-id="6a48c-117">檔鎖定通訊協定</span><span class="sxs-lookup"><span data-stu-id="6a48c-117">The Document Lock Protocol</span></span>

<span data-ttu-id="6a48c-118">若要要求 ACP 型應用程式的檔鎖定，TSF 管理員會呼叫 [ITextStoreACP：： RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)。</span><span class="sxs-lookup"><span data-stu-id="6a48c-118">To request a document lock for ACP-based applications, the TSF manager calls [ITextStoreACP::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock).</span></span> <span data-ttu-id="6a48c-119">針對以錨點為基礎的應用程式，TSF 管理員會呼叫 [ITextStoreAnchor：： RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)。</span><span class="sxs-lookup"><span data-stu-id="6a48c-119">For anchor-based applications, the TSF manager calls [ITextStoreAnchor::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock).</span></span> <span data-ttu-id="6a48c-120">應用程式會藉由呼叫 [ITextStoreACPSink：： OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (ACP 型應用程式) 或 [ITextStoreAnchorSink：： OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (以錨點為基礎的應用程式) **RequestLock** 內，來授與檔鎖定。</span><span class="sxs-lookup"><span data-stu-id="6a48c-120">The application grants the document lock by calling [ITextStoreACPSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (ACP-based applications) or [ITextStoreAnchorSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (anchor-based applications) inside of **RequestLock**.</span></span> <span data-ttu-id="6a48c-121">鎖定只有在 **OnLockGranted** 呼叫期間有效。</span><span class="sxs-lookup"><span data-stu-id="6a48c-121">The lock is only valid during the **OnLockGranted** call.</span></span> <span data-ttu-id="6a48c-122">當 **OnLockGranted** 傳回時，檔會被視為已解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="6a48c-122">When **OnLockGranted** returns, the document is considered unlocked.</span></span>

## <a name="types-of-document-locks"></a><span data-ttu-id="6a48c-123">檔鎖定的類型</span><span class="sxs-lookup"><span data-stu-id="6a48c-123">Types of Document Locks</span></span>

<span data-ttu-id="6a48c-124">檔鎖定有兩種類型：唯讀和讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="6a48c-124">There are two types of document locks, read-only and read/write.</span></span> <span data-ttu-id="6a48c-125">唯讀鎖定可讓管理員讀取文字，但無法修改或插入文字。</span><span class="sxs-lookup"><span data-stu-id="6a48c-125">A read-only lock enables the manager to read the text, but it cannot modify or insert text.</span></span> <span data-ttu-id="6a48c-126">讀取/寫入鎖定可讓管理員讀取、修改和插入文字。</span><span class="sxs-lookup"><span data-stu-id="6a48c-126">A read/write lock enables the manager to read, modify, and insert text.</span></span> <span data-ttu-id="6a48c-127">藉由 \_ \_ 在 *DWFLAGS* 中指定 TS LF read 來要求唯讀鎖定。</span><span class="sxs-lookup"><span data-stu-id="6a48c-127">A read-only lock is requested by specifying TS\_LF\_READ in *dwFlags*.</span></span> <span data-ttu-id="6a48c-128">藉由 \_ \_ 在 *DWFLAGS* 中指定 TS LF READWRITE 來要求讀取/寫入鎖定。</span><span class="sxs-lookup"><span data-stu-id="6a48c-128">A read/write lock is requested by specifying TS\_LF\_READWRITE in *dwFlags*.</span></span>

## <a name="asynchronous-and-synchronous-requests"></a><span data-ttu-id="6a48c-129">非同步和同步要求</span><span class="sxs-lookup"><span data-stu-id="6a48c-129">Asynchronous and Synchronous Requests</span></span>

<span data-ttu-id="6a48c-130">鎖定要求可以是同步或非同步。</span><span class="sxs-lookup"><span data-stu-id="6a48c-130">A lock request can be either synchronous or asynchronous.</span></span> <span data-ttu-id="6a48c-131">管理員會使用 \_ \_ *DWFLAGS* 中的 TS LF 同步旗標來要求同步鎖定。</span><span class="sxs-lookup"><span data-stu-id="6a48c-131">The manager requests a synchronous lock by using the TS\_LF\_SYNC flag in *dwFlags*.</span></span> <span data-ttu-id="6a48c-132">如果不存在此旗標，則要求是非同步。</span><span class="sxs-lookup"><span data-stu-id="6a48c-132">If this flag is not present, the request is asynchronous.</span></span>

## <a name="granting-the-lock"></a><span data-ttu-id="6a48c-133">授與鎖定</span><span class="sxs-lookup"><span data-stu-id="6a48c-133">Granting the Lock</span></span>

<span data-ttu-id="6a48c-134">當呼叫 **RequestLock** 時，應用程式必須判斷檔目前是否已鎖定。</span><span class="sxs-lookup"><span data-stu-id="6a48c-134">When **RequestLock** is called, the application must determine if the document is currently locked.</span></span> <span data-ttu-id="6a48c-135">如果檔未鎖定，而且沒有其他原因要拒絕鎖定，應用程式應該將 *phrSession* 設定為 \_ [確定]，然後返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="6a48c-135">If the document is not locked, and no other reason to deny the lock exists, the application should set *phrSession* to S\_OK and return S\_OK.</span></span>

<span data-ttu-id="6a48c-136">如果檔已鎖定，而且鎖定要求是同步的，應用程式應該將 *phrSession* 設定為 TS \_ E 同步，並傳回「 \_ 確定」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6a48c-136">If the document is locked and the lock request is synchronous, the application should set *phrSession* to TS\_E\_SYNCHRONOUS and return S\_OK.</span></span> <span data-ttu-id="6a48c-137">這表示無法授與同步要求。</span><span class="sxs-lookup"><span data-stu-id="6a48c-137">This indicates that a synchronous request cannot be granted.</span></span>

<span data-ttu-id="6a48c-138">如果檔已鎖定，而且鎖定要求是非同步，則應用程式應該將要求排入佇列，將 *phrSession* 設定為 TS \_ S \_ ASYNC，並傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="6a48c-138">If the document is locked and the lock request is asynchronous, the application should queue the request, set *phrSession* to TS\_S\_ASYNC and return S\_OK.</span></span> <span data-ttu-id="6a48c-139">當檔變成可用時，應用程式應該從佇列中移除要求並呼叫 **OnLockGranted**。</span><span class="sxs-lookup"><span data-stu-id="6a48c-139">When the document becomes available, the application should remove the request from the queue and call **OnLockGranted**.</span></span> <span data-ttu-id="6a48c-140">此鎖定要求佇列是選擇性的;有一個應用程式必須支援的案例。</span><span class="sxs-lookup"><span data-stu-id="6a48c-140">This queuing of lock requests is optional; there is one scenario that an application must support.</span></span> <span data-ttu-id="6a48c-141">如果檔有唯讀鎖定，則新的鎖定要求是讀取/寫入，而且要求是非同步，因此應用程式已呼叫 **OnLockGranted** ，而造成 **RequestLock** 的重新進入呼叫。</span><span class="sxs-lookup"><span data-stu-id="6a48c-141">If the document has a read-only lock, the new lock request is read/write and the request is asynchronous, the application has called into **OnLockGranted** , which has caused a reentrant call to **RequestLock**.</span></span> <span data-ttu-id="6a48c-142">應用程式應該將 *phrSession* 設定為 TS \_ S \_ ASYNC，然後返回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="6a48c-142">The application should set *phrSession* to TS\_S\_ASYNC and return S\_OK.</span></span> <span data-ttu-id="6a48c-143">對 **OnLockGranted** 的呼叫傳回之後，應用程式應該使用 TS LF READWRITE 再次呼叫 **OnLockGranted** 來處理升級 \_ 要求 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6a48c-143">After the call to **OnLockGranted** returns, the application should process the upgrade request by calling **OnLockGranted** again with TS\_LF\_READWRITE.</span></span>

## <a name="lock-enforcement"></a><span data-ttu-id="6a48c-144">鎖定強制</span><span class="sxs-lookup"><span data-stu-id="6a48c-144">Lock Enforcement</span></span>

<span data-ttu-id="6a48c-145">應用程式必須先確認有適當的鎖定類型，才能允許存取檔。</span><span class="sxs-lookup"><span data-stu-id="6a48c-145">The application must ensure that the proper type of lock exists before allowing access to the document.</span></span> <span data-ttu-id="6a48c-146">例如，應用程式應該在允許 [ITextStoreACP：： GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) 或 [ITextStoreAnchor：： GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) 繼續進行之前，先確認檔至少有唯讀鎖定。</span><span class="sxs-lookup"><span data-stu-id="6a48c-146">For example, the application should verify that a document has at least a read-only lock before allowing [ITextStoreACP::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) or [ITextStoreAnchor::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) to proceed.</span></span> <span data-ttu-id="6a48c-147">如果沒有適當的鎖定存在，應用程式應該會傳回 TF \_ E \_ NOLOCK。</span><span class="sxs-lookup"><span data-stu-id="6a48c-147">If the proper lock does not exist, the application should return TF\_E\_NOLOCK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a48c-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="6a48c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a48c-149">文字存放區</span><span class="sxs-lookup"><span data-stu-id="6a48c-149">Text Stores</span></span>](text-stores.md)
</dt> <dt>

[<span data-ttu-id="6a48c-150">ITextStoreACP：： RequestLock</span><span class="sxs-lookup"><span data-stu-id="6a48c-150">ITextStoreACP::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[<span data-ttu-id="6a48c-151">ITextStoreACPSink：： OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="6a48c-151">ITextStoreACPSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="6a48c-152">ITextStoreACP：： GetText</span><span class="sxs-lookup"><span data-stu-id="6a48c-152">ITextStoreACP::GetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext)
</dt> <dt>

[<span data-ttu-id="6a48c-153">ITextStoreAnchor：： RequestLock</span><span class="sxs-lookup"><span data-stu-id="6a48c-153">ITextStoreAnchor::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[<span data-ttu-id="6a48c-154">ITextStoreAnchorSink：： OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="6a48c-154">ITextStoreAnchorSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="6a48c-155">ITextStoreAnchor：： GetText</span><span class="sxs-lookup"><span data-stu-id="6a48c-155">ITextStoreAnchor::GetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext)
</dt> </dl>

 

 




