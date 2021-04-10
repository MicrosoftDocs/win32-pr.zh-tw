---
title: 文字存放區
description: 文字存放區
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- 文字服務架構 (TSF) 、文字存放區
- TSF (文字服務架構) 、文字存放區
- 啟用 TSF 的應用程式，文字存放區
- 文字存放區
- '文字服務架構 (TSF) ，應用程式字元位置 (ACP) '
- 'TSF (文字服務架構) ，應用程式字元位置 (ACP) '
- '啟用 TSF 的應用程式，應用程式字元位置 (ACP) '
- '應用程式字元位置 (ACP) '
- 'ACP (應用程式字元位置) '
- 文字服務架構 (TSF) 、錨點
- TSF (文字服務架構) 、錨點
- 啟用 TSF 的應用程式，錨點
- 錨點
- 文字服務架構 (TSF) 、檔鎖定
- TSF (文字服務架構) ，檔鎖定
- 啟用 TSF 的應用程式，檔鎖定
- 檔鎖定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1234f71fa799cf911ff7ede89915068f69417a00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023666"
---
# <a name="text-stores"></a><span data-ttu-id="c089e-120">文字存放區</span><span class="sxs-lookup"><span data-stu-id="c089e-120">Text Stores</span></span>

## <a name="application-character-position-acp"></a><span data-ttu-id="c089e-121">應用程式字元位置 (ACP) </span><span class="sxs-lookup"><span data-stu-id="c089e-121">Application Character Position (ACP)</span></span>

<span data-ttu-id="c089e-122">ACP 是文字資料流程中字元（或字元）的位置，以文字資料流程開頭的字元數表示。</span><span class="sxs-lookup"><span data-stu-id="c089e-122">An ACP is the location of a character, or characters, in a text stream that is expressed as the number of characters from the start of the text stream.</span></span> <span data-ttu-id="c089e-123">由於 ACP 模型是以零為基底，因此文字資料流程中的第一個字元具有零的 ACP。</span><span class="sxs-lookup"><span data-stu-id="c089e-123">Because the ACP model is zero-based, the first character in a text stream has an ACP of zero.</span></span> <span data-ttu-id="c089e-124">例如：</span><span class="sxs-lookup"><span data-stu-id="c089e-124">For example:</span></span>


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



<span data-ttu-id="c089e-125">文字存放區會執行支援 [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) 介面的物件，此介面可讓文字資料流程以 ACP 表示。</span><span class="sxs-lookup"><span data-stu-id="c089e-125">A text store implements an object that supports the [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) interface, which enables the text stream to be expressed in an ACP.</span></span> <span data-ttu-id="c089e-126">**ITextStoreACP** 介面方法會使用文字資料流程的 ACP 範圍來修改文字。</span><span class="sxs-lookup"><span data-stu-id="c089e-126">The **ITextStoreACP** interface methods use the ACP range of the text stream to modify the text.</span></span>

## <a name="anchor-based-applications"></a><span data-ttu-id="c089e-127">Anchor-Based 應用程式</span><span class="sxs-lookup"><span data-stu-id="c089e-127">Anchor-Based Applications</span></span>

<span data-ttu-id="c089e-128">管理員會以原生方式使用以 ACP 為基礎的方法來操作文字。</span><span class="sxs-lookup"><span data-stu-id="c089e-128">The manager uses the ACP-based methods natively to manipulate text.</span></span> <span data-ttu-id="c089e-129">不過，錨點型方法適用于支援[錨點](ranges.md) [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md)用戶端，因此管理員會使用[ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)和[ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)方法來包裝[ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)和[ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)方法。</span><span class="sxs-lookup"><span data-stu-id="c089e-129">However, an anchor-based approach is available for [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) clients that support [anchors](ranges.md), whereby the manager uses [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) and [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) methods to wrap the [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) and [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) methods.</span></span>

## <a name="document-access-control"></a><span data-ttu-id="c089e-130">檔存取控制</span><span class="sxs-lookup"><span data-stu-id="c089e-130">Document Access Control</span></span>

<span data-ttu-id="c089e-131">文字存放區會使用 [檔鎖定](document-locks.md)來控制文字資料流程的存取。</span><span class="sxs-lookup"><span data-stu-id="c089e-131">The text store controls access to the text stream by using [document locks](document-locks.md).</span></span> <span data-ttu-id="c089e-132">若要讀取或修改文字存放區，管理員必須先安裝支援 [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) 介面的建議接收，方法是呼叫 [ITextStoreACP：： AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) 方法，並將指標傳遞給建議接收器。</span><span class="sxs-lookup"><span data-stu-id="c089e-132">To read or modify the text store, the manager must first install an advise sink that supports the [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) interface by calling the [ITextStoreACP::AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) method and passing a pointer to an advise sink.</span></span> <span data-ttu-id="c089e-133">「建議接收」可讓管理員取得文字存放區的檔鎖定，並在文字存放區由管理員以外的其他內容（例如透過應用程式的使用者輸入）修改時接收通知。</span><span class="sxs-lookup"><span data-stu-id="c089e-133">The advise sink enables the manager to obtain a document locks on the text store and receive notifications when the text store is modified by something other than the manager, such as user input through the application.</span></span> <span data-ttu-id="c089e-134">本主題稍後會討論建議接收器。</span><span class="sxs-lookup"><span data-stu-id="c089e-134">Advise sinks are discussed later in this topic.</span></span>

## <a name="how-to-initialize-the-text-store"></a><span data-ttu-id="c089e-135">如何初始化文字存放區</span><span class="sxs-lookup"><span data-stu-id="c089e-135">How To Initialize the Text Store</span></span>

<span data-ttu-id="c089e-136">應用程式會藉由完成下列步驟來初始化文字存放區：</span><span class="sxs-lookup"><span data-stu-id="c089e-136">An application initializes a text store by completing the following steps:</span></span>

1.  <span data-ttu-id="c089e-137">藉由呼叫[CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)函式和執行緒管理員物件的指標，以根據[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)介面建立執行緒管理員物件。</span><span class="sxs-lookup"><span data-stu-id="c089e-137">Create a thread manager object based on the [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) interface by calling the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function with a pointer to a thread manager object.</span></span> <span data-ttu-id="c089e-138">以下是執行執行緒管理員物件的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="c089e-138">The following is a code example of implementing a thread manager object.</span></span>
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  <span data-ttu-id="c089e-139">藉由呼叫 [ITfThreadMgr：： activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) 方法來啟動執行緒管理員物件。</span><span class="sxs-lookup"><span data-stu-id="c089e-139">Activate the thread manager object by calling the [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) method.</span></span> <span data-ttu-id="c089e-140">這個方法會提供用來建立內容物件的 [用戶端識別碼](tfclientid.md) 指標。</span><span class="sxs-lookup"><span data-stu-id="c089e-140">This method supplies a pointer to a [client identifier](tfclientid.md) used to create a context object.</span></span> <span data-ttu-id="c089e-141">執行緒管理員是用來執行檔管理員物件。</span><span class="sxs-lookup"><span data-stu-id="c089e-141">The thread manager is used to implement a document manager object.</span></span>
3.  <span data-ttu-id="c089e-142">藉由呼叫[ITfThreadMgr：： CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)方法以及檔管理員物件的指標，以建立以[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)介面為基礎的檔管理員物件。</span><span class="sxs-lookup"><span data-stu-id="c089e-142">Create a document manager object based on the [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) interface by calling the [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) method with a pointer to the document manager object.</span></span> <span data-ttu-id="c089e-143">檔案管理員物件是用來執行做為文字存放區的內容物件。</span><span class="sxs-lookup"><span data-stu-id="c089e-143">The document manager object is used to implement a context object that is the text store.</span></span>
4.  <span data-ttu-id="c089e-144">藉由呼叫 [ITfDocumentMgr：： CreateCoNtext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) 方法並搭配文字存放區物件的指標和用戶端識別碼的指標，從啟用執行緒管理員，以從檔管理員建立內容物件。</span><span class="sxs-lookup"><span data-stu-id="c089e-144">Create a context object from the document manager by calling the [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) method with the pointer to the text store object and a pointer to the client identifier from activating the thread manager.</span></span> <span data-ttu-id="c089e-145">以下是建立內容物件的範例：</span><span class="sxs-lookup"><span data-stu-id="c089e-145">The following is an example of creating a context object:</span></span>
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  <span data-ttu-id="c089e-146">使用 [ITfDocumentMgr：:P ush](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) 方法，將內容物件推送至堆疊。</span><span class="sxs-lookup"><span data-stu-id="c089e-146">Push the context object onto the stack with the [ITfDocumentMgr::Push](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) method.</span></span> <span data-ttu-id="c089e-147">以下是將內容物件推送至堆疊的範例：</span><span class="sxs-lookup"><span data-stu-id="c089e-147">The following is an example of pushing the context object onto the stack:</span></span>
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a><span data-ttu-id="c089e-148">如何修改文字存放區</span><span class="sxs-lookup"><span data-stu-id="c089e-148">How To Modify the Text Store</span></span>

<span data-ttu-id="c089e-149">**ITfDocumentMgr：:P ush** 方法會使用建議接收介面的指標來呼叫 **ITextStoreACP：： AdviseSink** ，以安裝新的建議接收或修改現有的建議接收器。</span><span class="sxs-lookup"><span data-stu-id="c089e-149">The **ITfDocumentMgr::Push** method calls **ITextStoreACP::AdviseSink** with a pointer to the advise sink interface to install a new advise sink or modify an existing advise sink.</span></span> <span data-ttu-id="c089e-150">當文字存放區由管理員以外的其他內容（例如應用程式的使用者輸入）進行修改時，「建議接收」會收到通知。</span><span class="sxs-lookup"><span data-stu-id="c089e-150">The advise sink receives notifications when the text store is modified by something other than the manager, such as user input to the application.</span></span> <span data-ttu-id="c089e-151">當輸入方法取得焦點時，應用程式必須呼叫 [ITfThreadMgrEventSink：： OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) 方法。</span><span class="sxs-lookup"><span data-stu-id="c089e-151">Applications must call the [ITfThreadMgrEventSink::OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) method when the input method obtains the focus.</span></span> <span data-ttu-id="c089e-152">呼叫適當的 **ITextStoreACPSink** 介面方法，即可提供執行緒管理員的其他通知。</span><span class="sxs-lookup"><span data-stu-id="c089e-152">Other notifications to the thread manager are provided by calling to the appropriate **ITextStoreACPSink** interface methods.</span></span>

<span data-ttu-id="c089e-153">不過，應用程式不應該呼叫 **ITextStoreACPSink** 介面方法來回應 **ITextStoreACP** 介面方法。</span><span class="sxs-lookup"><span data-stu-id="c089e-153">However, applications should not call the **ITextStoreACPSink** interface methods in response to **ITextStoreACP** interface methods.</span></span> <span data-ttu-id="c089e-154">應用程式應該只在管理員以外的其他內容修改文字存放區時，才呼叫 **ITextStoreACPSink** 介面方法。</span><span class="sxs-lookup"><span data-stu-id="c089e-154">Applications should only call **ITextStoreACPSink** interface methods when the text store is modified by something other than the manager.</span></span>

<span data-ttu-id="c089e-155">您可以使用稱為 [組合](compositions.md)的暫存輸入狀態來修改文字存放區的內容。</span><span class="sxs-lookup"><span data-stu-id="c089e-155">The contents of the text store can be modified with a temporary input state called a [composition](compositions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c089e-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="c089e-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c089e-157">錨點</span><span class="sxs-lookup"><span data-stu-id="c089e-157">Anchors</span></span>](ranges.md)
</dt> <dt>

[<span data-ttu-id="c089e-158">成分</span><span class="sxs-lookup"><span data-stu-id="c089e-158">Compositions</span></span>](compositions.md)
</dt> <dt>

[<span data-ttu-id="c089e-159">檔鎖定</span><span class="sxs-lookup"><span data-stu-id="c089e-159">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="c089e-160">ITextStoreACPSink</span><span class="sxs-lookup"><span data-stu-id="c089e-160">ITextStoreACPSink</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)
</dt> <dt>

[<span data-ttu-id="c089e-161">ITextStoreACP</span><span class="sxs-lookup"><span data-stu-id="c089e-161">ITextStoreACP</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[<span data-ttu-id="c089e-162">ITextStoreAnchor</span><span class="sxs-lookup"><span data-stu-id="c089e-162">ITextStoreAnchor</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)
</dt> <dt>

[<span data-ttu-id="c089e-163">ITextStoreAnchorSink</span><span class="sxs-lookup"><span data-stu-id="c089e-163">ITextStoreAnchorSink</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)
</dt> <dt>

[<span data-ttu-id="c089e-164">ITfDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="c089e-164">ITfDocumentMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[<span data-ttu-id="c089e-165">ITfThreadMgr</span><span class="sxs-lookup"><span data-stu-id="c089e-165">ITfThreadMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[<span data-ttu-id="c089e-166">ITfThreadMgrEventSink::OnSetFocus</span><span class="sxs-lookup"><span data-stu-id="c089e-166">ITfThreadMgrEventSink::OnSetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[<span data-ttu-id="c089e-167">TfClientId</span><span class="sxs-lookup"><span data-stu-id="c089e-167">TfClientId</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="c089e-168">Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="c089e-168">Microsoft Active Accessibility</span></span>](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 