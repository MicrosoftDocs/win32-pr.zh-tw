---
title: 編輯內容
description: 編輯內容
ms.assetid: cf8bbe66-d2ad-49b3-9e7c-246e4ca50149
keywords:
- 文字服務架構 (TSF) 編輯內容
- TSF (文字服務架構) 、編輯內容
- 文字服務，編輯內容
- 啟用 TSF 的應用程式，編輯內容
- 編輯內容
- 文字服務架構 (TSF) 、編輯 cookie
- TSF (文字服務架構) 、編輯 cookie
- 文字服務，編輯 cookie
- 啟用 TSF 的應用程式，編輯 cookie
- 編輯 cookie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020ca8713d66d9d14e387381fc21157db8bdedf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839827"
---
# <a name="edit-contexts"></a><span data-ttu-id="23bff-113">編輯內容</span><span class="sxs-lookup"><span data-stu-id="23bff-113">Edit Contexts</span></span>

## <a name="applications"></a><span data-ttu-id="23bff-114">應用程式</span><span class="sxs-lookup"><span data-stu-id="23bff-114">Applications</span></span>

<span data-ttu-id="23bff-115">若要建立編輯內容，應用程式會呼叫 [ITfDocumentMgr：： CreateCoNtext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)。</span><span class="sxs-lookup"><span data-stu-id="23bff-115">To create an edit context, an application calls [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span></span>

## <a name="text-services"></a><span data-ttu-id="23bff-116">文字服務</span><span class="sxs-lookup"><span data-stu-id="23bff-116">Text Services</span></span>

<span data-ttu-id="23bff-117">文字服務通常會使用目前現用的編輯內容。</span><span class="sxs-lookup"><span data-stu-id="23bff-117">A text service often uses the currently active edit context.</span></span> <span data-ttu-id="23bff-118">目前作用中的編輯內容是活動文件管理員堆疊頂端的編輯內容。</span><span class="sxs-lookup"><span data-stu-id="23bff-118">The currently active edit context is the edit context at the top of the stack of the active document manager.</span></span> <span data-ttu-id="23bff-119">為了取得目前使用中的內容，文字服務會呼叫 [ITfThreadMgr：： GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) 來取得使用中的檔管理員，然後呼叫 [ITfDocumentMgr：： vemap.gettop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) ，以取得堆疊頂端的編輯內容。</span><span class="sxs-lookup"><span data-stu-id="23bff-119">To obtain the currently active context, a text service calls [ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) to obtain the active document manager and then calls [ITfDocumentMgr::GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) to obtain the edit context at the top of the stack.</span></span>

<span data-ttu-id="23bff-120">在某些情況下，文字服務需要自己的編輯內容。</span><span class="sxs-lookup"><span data-stu-id="23bff-120">In some cases, a text service requires its own edit context.</span></span> <span data-ttu-id="23bff-121">若要建立編輯內容，文字服務會呼叫 **ITfDocumentMgr：： CreateCoNtext**。</span><span class="sxs-lookup"><span data-stu-id="23bff-121">To create an edit context, a text service calls **ITfDocumentMgr::CreateContext**.</span></span>

## <a name="edit-cookies"></a><span data-ttu-id="23bff-122">編輯 Cookie</span><span class="sxs-lookup"><span data-stu-id="23bff-122">Edit Cookies</span></span>

<span data-ttu-id="23bff-123">許多方法（例如 [ITfRange：： SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)）都需要一種方法來識別具有唯讀或讀取/寫入 [檔鎖定](document-locks.md)的編輯內容。</span><span class="sxs-lookup"><span data-stu-id="23bff-123">Many methods, such as [ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), require a way to identify an edit context that has a read-only or read/write [document lock](document-locks.md).</span></span> <span data-ttu-id="23bff-124">您可以透過 TSF 管理員和應用程式之間的協商來取得檔鎖定。</span><span class="sxs-lookup"><span data-stu-id="23bff-124">A document lock is obtained through a negotiation between the TSF manager and the application.</span></span> <span data-ttu-id="23bff-125">文字服務無法直接執行此協商。</span><span class="sxs-lookup"><span data-stu-id="23bff-125">A text service cannot perform this negotiation directly.</span></span> <span data-ttu-id="23bff-126">文字服務只能藉由要求具有特定內容和唯讀或讀取/寫入存取權的 [編輯會話](edit-sessions.md) 來取得鎖定。</span><span class="sxs-lookup"><span data-stu-id="23bff-126">A text service can only obtain a lock by requesting an [edit session](edit-sessions.md) with a specific context and read-only or read/write access.</span></span> <span data-ttu-id="23bff-127">當授與編輯會話時，系統會提供文字服務與 *編輯 cookie* ，以使用所要求的存取權來識別編輯內容。</span><span class="sxs-lookup"><span data-stu-id="23bff-127">When the edit session is granted, the text service is supplied with an *edit cookie* that identifies the edit context with the requested access.</span></span> <span data-ttu-id="23bff-128">此 cookie 接著會傳遞至方法，以適當的存取權識別編輯內容。</span><span class="sxs-lookup"><span data-stu-id="23bff-128">This cookie is then passed to the method to identify the edit context with the proper access.</span></span>

<span data-ttu-id="23bff-129">**ITfDocumentMgr：： CreateCoNtext** 也會提供編輯 cookie 給內容建立者。</span><span class="sxs-lookup"><span data-stu-id="23bff-129">**ITfDocumentMgr::CreateContext** also supplies an edit cookie to the context creator.</span></span> <span data-ttu-id="23bff-130">此 cookie 具有唯讀存取權，且沒有任何方法可修改存取層級。</span><span class="sxs-lookup"><span data-stu-id="23bff-130">This cookie has read-only access and there is no way to modify the access level.</span></span> <span data-ttu-id="23bff-131">老實說，TSF manager 不會協調此編輯 cookie 的檔鎖定。</span><span class="sxs-lookup"><span data-stu-id="23bff-131">In truth, the TSF manager does not negotiate a document lock for this edit cookie.</span></span> <span data-ttu-id="23bff-132">Cookie 會在內部標示為唯讀，但檔並未實際鎖定。</span><span class="sxs-lookup"><span data-stu-id="23bff-132">The cookie is internally marked read-only, but the document is not actually locked.</span></span> <span data-ttu-id="23bff-133">例如，如果內容建立者使用 **ITfDocumentMgr：： CreateCoNtext** 傳回的編輯 cookie 來呼叫 [ITfCoNtext：： GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) ，這會導致呼叫應用程式的 [ITextStoreACP：： GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)或 [ITextStoreAnchor：： GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) 。</span><span class="sxs-lookup"><span data-stu-id="23bff-133">For example, if the context creator calls [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) with the edit cookie returned by **ITfDocumentMgr::CreateContext** , this results in the application's [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) or [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) being called.</span></span> <span data-ttu-id="23bff-134">取得選取專案之前，應用程式會判斷檔鎖定是否存在。</span><span class="sxs-lookup"><span data-stu-id="23bff-134">Before obtaining the selection, the application will determine if a document lock exists.</span></span> <span data-ttu-id="23bff-135">因為沒有鎖定存在，應用程式將會失敗，並出現 TS \_ E \_ NOLOCK。</span><span class="sxs-lookup"><span data-stu-id="23bff-135">Because no lock exists, the application will fail with TS\_E\_NOLOCK.</span></span> <span data-ttu-id="23bff-136">也就是，如果應用程式使用這個 cookie 來呼叫方法，而此 cookie 會導致呼叫其中一個應用程式的文字存放區方法，它就必須在內部處理此案例，因為應用程式實際上並不會有檔鎖定。</span><span class="sxs-lookup"><span data-stu-id="23bff-136">That is, if an application calls a method with this cookie that results in one of the application's text store methods being called, it must handle this case internally because the application will not actually have a document lock.</span></span>

<span data-ttu-id="23bff-137">如果內容建立者需要具有讀取/寫入存取權的編輯 cookie，它必須建立自己的編輯會話。</span><span class="sxs-lookup"><span data-stu-id="23bff-137">If the context creator requires an edit cookie with read/write access, it must establish its own edit session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23bff-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="23bff-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23bff-139">ITfCoNtext</span><span class="sxs-lookup"><span data-stu-id="23bff-139">ITfContext</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcontext)
</dt> <dt>

[<span data-ttu-id="23bff-140">ITfDocumentMgr：： CreateCoNtext</span><span class="sxs-lookup"><span data-stu-id="23bff-140">ITfDocumentMgr::CreateContext</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[<span data-ttu-id="23bff-141">ITfThreadMgr：： GetFocus</span><span class="sxs-lookup"><span data-stu-id="23bff-141">ITfThreadMgr::GetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> <dt>

[<span data-ttu-id="23bff-142">ITfDocumentMgr：： Vemap.gettop</span><span class="sxs-lookup"><span data-stu-id="23bff-142">ITfDocumentMgr::GetTop</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop)
</dt> <dt>

[<span data-ttu-id="23bff-143">ITfRange：： SetText</span><span class="sxs-lookup"><span data-stu-id="23bff-143">ITfRange::SetText</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[<span data-ttu-id="23bff-144">檔鎖定</span><span class="sxs-lookup"><span data-stu-id="23bff-144">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="23bff-145">編輯工作階段</span><span class="sxs-lookup"><span data-stu-id="23bff-145">Edit Sessions</span></span>](edit-sessions.md)
</dt> <dt>

[<span data-ttu-id="23bff-146">ITfCoNtext：： GetSelection</span><span class="sxs-lookup"><span data-stu-id="23bff-146">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="23bff-147">ITextStoreACP：： GetSelection</span><span class="sxs-lookup"><span data-stu-id="23bff-147">ITextStoreACP::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[<span data-ttu-id="23bff-148">ITextStoreAnchor::GetSelection</span><span class="sxs-lookup"><span data-stu-id="23bff-148">ITextStoreAnchor::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> </dl>

 

 




