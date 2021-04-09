---
description: 本主題列出使用 XPS 數位簽章 API 將數位簽章新增至 XPS 檔的考慮。
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: 使用 XPS 數位簽章 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9037a1442a44b082caec21309c94390b3f783e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849209"
---
# <a name="using-xps-digital-signature-api"></a><span data-ttu-id="10478-103">使用 XPS 數位簽章 API</span><span class="sxs-lookup"><span data-stu-id="10478-103">Using XPS Digital Signature API</span></span>

<span data-ttu-id="10478-104">本主題列出使用 XPS 數位簽章 API 將數位簽章新增至 XPS 檔的考慮。</span><span class="sxs-lookup"><span data-stu-id="10478-104">This topic lists considerations for using the XPS Digital Signature API to add digital signatures to an XPS document.</span></span>

<span data-ttu-id="10478-105">XPS 數位簽章 API 可讓應用程式要求使用者簽署 XPS 檔，並驗證 XPS 檔中找到的簽章。</span><span class="sxs-lookup"><span data-stu-id="10478-105">The XPS Digital Signature API enables applications to request users to sign XPS documents and to verify signatures that are found in XPS documents.</span></span> <span data-ttu-id="10478-106">XPS 數位簽章 API 可以套用至 XPS 檔，而不需要將它載入 XPS OM，並且可用於從 XPS OM 序列化的 XPS 檔串流。</span><span class="sxs-lookup"><span data-stu-id="10478-106">The XPS Digital Signature API can be applied to an XPS document without loading it into an XPS OM, and it can be used on XPS document streams that are serialized from an XPS OM.</span></span>

<span data-ttu-id="10478-107">[Xps 數位簽章 API 程式設計](#xps-digital-signature-api-programming-tasks)工作章節包含的主題說明如何使用 XPS 數位簽章 api 進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="10478-107">The [XPS Digital Signature API Programming Tasks](#xps-digital-signature-api-programming-tasks) section contains topics that describe how to program with the XPS Digital Signature API.</span></span> <span data-ttu-id="10478-108">本主題列出在將數位簽章支援新增至應用程式時，使用 XPS 數位簽章 API 的下列考慮。</span><span class="sxs-lookup"><span data-stu-id="10478-108">This topic lists the following considerations for using the XPS Digital Signature API when adding digital signature support to an application.</span></span>

-   [<span data-ttu-id="10478-109">XPS 數位簽章 API 程式設計工作</span><span class="sxs-lookup"><span data-stu-id="10478-109">XPS Digital Signature API Programming Tasks</span></span>](#xps-digital-signature-api-programming-tasks)
-   [<span data-ttu-id="10478-110">XPS 數位簽章 API 程式設計的特殊注意事項</span><span class="sxs-lookup"><span data-stu-id="10478-110">Special Notes about XPS Digital Signature API Programming</span></span>](#special-notes-about-xps-digital-signature-api-programming)
    -   [<span data-ttu-id="10478-111">驗證 XPS 檔中的數位簽章</span><span class="sxs-lookup"><span data-stu-id="10478-111">Verifying Digital Signatures in an XPS Document</span></span>](#verifying-digital-signatures-in-an-xps-document)
    -   [<span data-ttu-id="10478-112">數位簽章簽署原則</span><span class="sxs-lookup"><span data-stu-id="10478-112">Digital Signature Signing Policy</span></span>](#digital-signature-signing-policy)
    -   [<span data-ttu-id="10478-113">內嵌憑證鏈</span><span class="sxs-lookup"><span data-stu-id="10478-113">Embedding a Certificate Chain</span></span>](#embedding-a-certificate-chain)
    -   [<span data-ttu-id="10478-114">使用 CERT \_ 內容結構</span><span class="sxs-lookup"><span data-stu-id="10478-114">Using the CERT\_CONTEXT Structure</span></span>](#using-the-cert\_context-structure)
-   [<span data-ttu-id="10478-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="10478-115">Related topics</span></span>](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a><span data-ttu-id="10478-116">XPS 數位簽章 API 程式設計工作</span><span class="sxs-lookup"><span data-stu-id="10478-116">XPS Digital Signature API Programming Tasks</span></span>

<span data-ttu-id="10478-117">本章節包含的主題說明如何使用 XPS 數位簽章 API 來執行程式設計工作。</span><span class="sxs-lookup"><span data-stu-id="10478-117">This section contains topics that describe how to perform programming tasks by using the XPS Digital Signature API.</span></span>

-   [<span data-ttu-id="10478-118">一般數位簽章程式設計工作</span><span class="sxs-lookup"><span data-stu-id="10478-118">Common Digital Signature Programming Tasks</span></span>](basic-digital-signature-programming-tasks.md)<dl>

[<span data-ttu-id="10478-119">初始化簽章管理員</span><span class="sxs-lookup"><span data-stu-id="10478-119">Initialize the Signature Manager</span></span>](initialize-the-signature-manager.md)  
    [<span data-ttu-id="10478-120">簽署檔</span><span class="sxs-lookup"><span data-stu-id="10478-120">Sign a Document</span></span>](sign-a-document.md)  
    [<span data-ttu-id="10478-121">將簽名要求新增至 XPS 檔</span><span class="sxs-lookup"><span data-stu-id="10478-121">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)  
    [<span data-ttu-id="10478-122">驗證檔簽章</span><span class="sxs-lookup"><span data-stu-id="10478-122">Verify Document Signatures</span></span>](verify-document-signatures.md)  
    </dl>
-   [<span data-ttu-id="10478-123">其他數位簽章程式設計工作</span><span class="sxs-lookup"><span data-stu-id="10478-123">Additional Digital Signature Programming Tasks</span></span>](advanced-digital-signature-programming-tasks.md)<dl>

[<span data-ttu-id="10478-124">從檔案載入憑證</span><span class="sxs-lookup"><span data-stu-id="10478-124">Load a Certificate From a File</span></span>](load-a-certificate-from-a-file.md)  
    [<span data-ttu-id="10478-125">確認憑證支援簽章方法</span><span class="sxs-lookup"><span data-stu-id="10478-125">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)  
    [<span data-ttu-id="10478-126">確認系統支援摘要式方法</span><span class="sxs-lookup"><span data-stu-id="10478-126">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)  
    [<span data-ttu-id="10478-127">在檔中內嵌憑證鏈</span><span class="sxs-lookup"><span data-stu-id="10478-127">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a><span data-ttu-id="10478-128">XPS 數位簽章 API 程式設計的特殊注意事項</span><span class="sxs-lookup"><span data-stu-id="10478-128">Special Notes about XPS Digital Signature API Programming</span></span>

<span data-ttu-id="10478-129">當您使用 XPS 數位簽章 API 時，下列主題需要一些特殊的考慮。</span><span class="sxs-lookup"><span data-stu-id="10478-129">The following topics require some special consideration when you use the XPS Digital Signature API.</span></span>

-   [<span data-ttu-id="10478-130">驗證 XPS 檔中的數位簽章</span><span class="sxs-lookup"><span data-stu-id="10478-130">Verifying Digital Signatures in an XPS Document</span></span>](#verifying-digital-signatures-in-an-xps-document)
-   [<span data-ttu-id="10478-131">數位簽章簽署原則</span><span class="sxs-lookup"><span data-stu-id="10478-131">Digital Signature Signing Policy</span></span>](#digital-signature-signing-policy)
-   [<span data-ttu-id="10478-132">內嵌憑證鏈</span><span class="sxs-lookup"><span data-stu-id="10478-132">Embedding a Certificate Chain</span></span>](#embedding-a-certificate-chain)
-   [<span data-ttu-id="10478-133">使用 CERT \_ 內容結構</span><span class="sxs-lookup"><span data-stu-id="10478-133">Using the CERT\_CONTEXT Structure</span></span>](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a><span data-ttu-id="10478-134">驗證 XPS 檔中的數位簽章</span><span class="sxs-lookup"><span data-stu-id="10478-134">Verifying Digital Signatures in an XPS Document</span></span>

<span data-ttu-id="10478-135">[**IXpsSignature：： Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) 只會檢查已簽署的內容，以判斷它在簽署後尚未變更。</span><span class="sxs-lookup"><span data-stu-id="10478-135">[**IXpsSignature::Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) checks only the signed content to determine that it has not changed since it was signed.</span></span> <span data-ttu-id="10478-136">**IXpsSignature：： verify** 不會驗證用來簽署檔內容的任何憑證。</span><span class="sxs-lookup"><span data-stu-id="10478-136">**IXpsSignature::Verify** does not verify any of the certificates that were used to sign the document content.</span></span>

<span data-ttu-id="10478-137">如需有關憑證和密碼編譯的詳細資訊，請參閱 [關於密碼](/windows/desktop/SecCrypto/about-cryptography)編譯。</span><span class="sxs-lookup"><span data-stu-id="10478-137">For more information about certificates and cryptography, see [About Cryptography](/windows/desktop/SecCrypto/about-cryptography).</span></span>

<span data-ttu-id="10478-138">如需如何在程式中驗證檔簽章的範例，請參閱 [驗證檔](verify-document-signatures.md)簽章和憑證。</span><span class="sxs-lookup"><span data-stu-id="10478-138">For an example of how to verify document signatures in a program, see [Verify Document Signatures and Certificates](verify-document-signatures.md).</span></span>

### <a name="digital-signature-signing-policy"></a><span data-ttu-id="10478-139">數位簽章簽署原則</span><span class="sxs-lookup"><span data-stu-id="10478-139">Digital Signature Signing Policy</span></span>

<span data-ttu-id="10478-140">數位簽章簽署原則會決定要簽署 XPS 檔的哪些部分。</span><span class="sxs-lookup"><span data-stu-id="10478-140">The digital signature signing policy determines which parts of an XPS document are signed.</span></span> <span data-ttu-id="10478-141">其中一個簽署原則選項是簽署從簽章來源部分開始的簽章關聯性。</span><span class="sxs-lookup"><span data-stu-id="10478-141">One signing policy option is to sign the signature relationships that start from the signature origin part.</span></span> <span data-ttu-id="10478-142">因為簽章關聯性會隨著每個新增的簽章而變更，所以在加入新簽章時，在此原則下建立的簽章將會中斷。</span><span class="sxs-lookup"><span data-stu-id="10478-142">Because the signature relationships change with each signature that is added, signatures that are made under this policy will break when new signatures are added.</span></span> <span data-ttu-id="10478-143">請確定您清楚瞭解設定此原則的含意和效果;否則，可能會產生非預期或不想要的行為。</span><span class="sxs-lookup"><span data-stu-id="10478-143">Make sure that you understand clearly the implications and effects of setting this policy; otherwise, unexpected or undesired behavior might result.</span></span>

<span data-ttu-id="10478-144">如需簽署原則的詳細資訊，請參閱 [**XPS \_ 簽署 \_ 原則**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)。</span><span class="sxs-lookup"><span data-stu-id="10478-144">For more information about signing policies, see [**XPS\_SIGN\_POLICY**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy).</span></span>

### <a name="embedding-a-certificate-chain"></a><span data-ttu-id="10478-145">內嵌憑證鏈</span><span class="sxs-lookup"><span data-stu-id="10478-145">Embedding a Certificate Chain</span></span>

<span data-ttu-id="10478-146">組成特定憑證信任鏈的憑證可以新增至 XPS 檔。</span><span class="sxs-lookup"><span data-stu-id="10478-146">The certificates that make up the trust chain of a specific certificate can be added to an XPS document.</span></span> <span data-ttu-id="10478-147">內嵌這些憑證可讓應用程式更輕鬆地在離線案例中，以驗證數位簽章所使用的憑證。</span><span class="sxs-lookup"><span data-stu-id="10478-147">Embedding these certificates can make it easier, in off-line scenarios, for an application to verify the certificates that a digital signature uses.</span></span>

<span data-ttu-id="10478-148">如需有關如何將憑證內嵌至 XPS 檔的詳細資訊，請參閱 [在檔中內嵌憑證鏈](embedding-certificate-trust-chains-in-a-document.md)。</span><span class="sxs-lookup"><span data-stu-id="10478-148">For more information about how to embed certificates in an XPS document, see [Embed Certificate Chains in a Document](embedding-certificate-trust-chains-in-a-document.md).</span></span>

### <a name="using-the-cert_context-structure"></a><span data-ttu-id="10478-149">使用 CERT \_ 內容結構</span><span class="sxs-lookup"><span data-stu-id="10478-149">Using the CERT\_CONTEXT Structure</span></span>

<span data-ttu-id="10478-150">[**Cert \_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)和 [**cert \_ 資訊**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)結構是保存憑證資訊的主要資料結構。</span><span class="sxs-lookup"><span data-stu-id="10478-150">The [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) and [**CERT\_INFO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) structures are the main data structures that hold certificate information.</span></span> <span data-ttu-id="10478-151">如需有關使用這些結構的詳細資訊，請參閱 [使用 CERT \_ 資訊資料結構](/windows/desktop/SecCrypto/using-a-cert-info-data-structure)。</span><span class="sxs-lookup"><span data-stu-id="10478-151">For more information about using these structures, see [Using a CERT\_INFO Data Structure](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).</span></span>

<span data-ttu-id="10478-152">[**CERT \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)當您不再需要密碼編譯 API 函式時，必須釋放它所傳回的內容結構。</span><span class="sxs-lookup"><span data-stu-id="10478-152">[**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structures that are returned by Crypto API functions must be released when they are no longer needed.</span></span> <span data-ttu-id="10478-153">若要釋放 **憑證 \_ 內容** 結構，請呼叫 [**CertFreeCertificateCoNtext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) 函數。</span><span class="sxs-lookup"><span data-stu-id="10478-153">To release a **CERT\_CONTEXT** structure, call the [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10478-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="10478-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10478-155">一般數位簽章程式設計工作</span><span class="sxs-lookup"><span data-stu-id="10478-155">Common Digital Signature Programming Tasks</span></span>](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[<span data-ttu-id="10478-156">其他數位簽章程式設計工作</span><span class="sxs-lookup"><span data-stu-id="10478-156">Additional Digital Signature Programming Tasks</span></span>](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[<span data-ttu-id="10478-157">**憑證 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="10478-157">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="10478-158">**CERT \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="10478-158">**CERT\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[<span data-ttu-id="10478-159">**CertFreeCertificateCoNtext**</span><span class="sxs-lookup"><span data-stu-id="10478-159">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[<span data-ttu-id="10478-160">**XPS \_ 簽署 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="10478-160">**XPS\_SIGN\_POLICY**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[<span data-ttu-id="10478-161">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="10478-161">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
