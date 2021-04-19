---
description: 本主題說明如何將簽章要求新增至 XPS 檔。
ms.assetid: 95eb1887-8754-43e0-8886-1f23653bff26
title: 將簽名要求新增至 XPS 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db0d3a899dd49f141adf5cd23ea8c837c8b12d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994452"
---
# <a name="add-a-signature-request-to-an-xps-document"></a><span data-ttu-id="6d906-103">將簽名要求新增至 XPS 檔</span><span class="sxs-lookup"><span data-stu-id="6d906-103">Add a Signature Request to an XPS Document</span></span>

<span data-ttu-id="6d906-104">本主題說明如何將簽章要求新增至 XPS 檔。</span><span class="sxs-lookup"><span data-stu-id="6d906-104">This topic describes how to add a signature request to an XPS document.</span></span> <span data-ttu-id="6d906-105">簽章要求會在使用者同意簽章意圖時提示使用者簽署檔。</span><span class="sxs-lookup"><span data-stu-id="6d906-105">A signature request prompts a user to sign a document if he or she agrees with the signature intent.</span></span>

<span data-ttu-id="6d906-106">在您的程式中使用下列程式碼範例之前，請閱讀 [一般數位簽章程式設計](basic-digital-signature-programming-tasks.md)工作中的免責聲明。</span><span class="sxs-lookup"><span data-stu-id="6d906-106">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="6d906-107">若要將簽章要求新增至 XPS 檔：</span><span class="sxs-lookup"><span data-stu-id="6d906-107">To add a signature request to an XPS Document:</span></span>

1.  <span data-ttu-id="6d906-108">將 XPS 檔載入到簽章管理員中，如初始化簽章 [管理員](initialize-the-signature-manager.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="6d906-108">Load the XPS document into a signature manager, as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>
2.  <span data-ttu-id="6d906-109">將簽章區塊加入至簽章管理員。</span><span class="sxs-lookup"><span data-stu-id="6d906-109">Add a signature block to the signature manager.</span></span>
3.  <span data-ttu-id="6d906-110">在新的簽章區塊中建立簽章要求。</span><span class="sxs-lookup"><span data-stu-id="6d906-110">Create a signature request in the new signature block.</span></span>
4.  <span data-ttu-id="6d906-111">設定簽章要求的屬性：</span><span class="sxs-lookup"><span data-stu-id="6d906-111">Set the properties of the signature request:</span></span>
    1.  <span data-ttu-id="6d906-112">設定簽章意圖。</span><span class="sxs-lookup"><span data-stu-id="6d906-112">Set the signature intent.</span></span>
    2.  <span data-ttu-id="6d906-113">設定 (要求的簽署者) 要求其簽章的人員名稱。</span><span class="sxs-lookup"><span data-stu-id="6d906-113">Set the name of the person whose signature is requested (the requested signer).</span></span>
    3.  <span data-ttu-id="6d906-114">設定需要簽章的日期。</span><span class="sxs-lookup"><span data-stu-id="6d906-114">Set the date the signature is required.</span></span>
    4.  <span data-ttu-id="6d906-115">視需要設定其他簽章屬性。</span><span class="sxs-lookup"><span data-stu-id="6d906-115">Set other signature properties as required.</span></span>

<span data-ttu-id="6d906-116">下列程式碼範例說明如何將簽章要求加入至 XPS 檔。</span><span class="sxs-lookup"><span data-stu-id="6d906-116">The following code example illustrates how to add a signature request to an XPS document.</span></span>


```C++
HRESULT 
AddSignatureRequestToDocument (
    __in IXpsSignatureManager    *signatureManager,
    __in LPCWSTR                reasonForSignatureRequest,
    __in LPCWSTR                nameOfRequestedSigner,
    __in LPCWSTR                requestSignByDate
)
{
    HRESULT                  hr = S_OK;
    IXpsSignatureBlock       *signatureDefinition = NULL;
    IXpsSignatureRequest     *signatureRequest = NULL;
    
    // Create a new signature block and get a pointer to it
    hr = signatureManager->AddSignatureBlock (NULL, 0, &signatureDefinition);
    
    if (SUCCEEDED(hr)) {
        // Create a new signature request to use for this signature block
        hr = signatureDefinition->CreateRequest(NULL, &signatureRequest);
    }

    if (SUCCEEDED(hr)) {
        // Initialize the properties of the signature request

        //  Set the string that describes the purpose of the signature
        //  to the person who will sign the document.
        hr = signatureRequest->SetIntent(reasonForSignatureRequest);
    }

    if (SUCCEEDED(hr)) {
        //  Set the name of the person whose signature is requested.
        hr = signatureRequest->SetRequestedSigner(nameOfRequestedSigner);
    }

    if (SUCCEEDED(hr)) {
        //  Set the date that the person should sign the document.
        //  The person is requested to sign the document on or before
        //   the date specified in this field. Refer to the help text
        //   for the correct format of this string.
        hr = signatureRequest->SetRequestSignByDate(requestSignByDate);
    }

    if (NULL != signatureDefinition) signatureDefinition->Release();
    if (NULL != signatureRequest) signatureRequest->Release();

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="6d906-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d906-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6d906-118">**在本節中使用**</span><span class="sxs-lookup"><span data-stu-id="6d906-118">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="6d906-119">**IXpsSignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="6d906-119">**IXpsSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)
</dt> <dt>

[<span data-ttu-id="6d906-120">**IXpsSignatureBlock::CreateRequest**</span><span class="sxs-lookup"><span data-stu-id="6d906-120">**IXpsSignatureBlock::CreateRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblock-createrequest)
</dt> <dt>

[<span data-ttu-id="6d906-121">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="6d906-121">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="6d906-122">**IXpsSignatureManager::AddSignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="6d906-122">**IXpsSignatureManager::AddSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-addsignatureblock)
</dt> <dt>

[<span data-ttu-id="6d906-123">**IXpsSignatureRequest**</span><span class="sxs-lookup"><span data-stu-id="6d906-123">**IXpsSignatureRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)
</dt> <dt>

[<span data-ttu-id="6d906-124">**IXpsSignatureRequest::SetIntent**</span><span class="sxs-lookup"><span data-stu-id="6d906-124">**IXpsSignatureRequest::SetIntent**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setintent)
</dt> <dt>

[<span data-ttu-id="6d906-125">**IXpsSignatureRequest::SetRequestedSigner**</span><span class="sxs-lookup"><span data-stu-id="6d906-125">**IXpsSignatureRequest::SetRequestedSigner**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestedsigner)
</dt> <dt>

[<span data-ttu-id="6d906-126">**IXpsSignatureRequest::SetRequestSignByDate**</span><span class="sxs-lookup"><span data-stu-id="6d906-126">**IXpsSignatureRequest::SetRequestSignByDate**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestsignbydate)
</dt> <dt>

<span data-ttu-id="6d906-127">**詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="6d906-127">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="6d906-128">XPS 數位簽章 API 錯誤</span><span class="sxs-lookup"><span data-stu-id="6d906-128">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="6d906-129">XPS 檔錯誤</span><span class="sxs-lookup"><span data-stu-id="6d906-129">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="6d906-130">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="6d906-130">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



