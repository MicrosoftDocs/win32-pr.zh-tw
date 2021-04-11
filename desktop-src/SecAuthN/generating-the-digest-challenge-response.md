---
description: 從伺服器收到挑戰之後，用戶端會藉由呼叫 InitializeSecurityCoNtext (Digest) 函數來建立摘要挑戰回應。
ms.assetid: b26b5676-a614-4017-a4e5-a5395292a667
title: 產生摘要挑戰回應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b577334348745425db23d3de41431ba4e37b7af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851760"
---
# <a name="generating-the-digest-challenge-response"></a><span data-ttu-id="0f2ad-103">產生摘要挑戰回應</span><span class="sxs-lookup"><span data-stu-id="0f2ad-103">Generating the Digest Challenge Response</span></span>

<span data-ttu-id="0f2ad-104">從伺服器收到挑戰之後，用戶端會藉由呼叫 [**InitializeSecurityCoNtext (digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函數來建立摘要挑戰回應。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-104">After receiving a challenge from the server, the client creates the Digest challenge response by calling the [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span> <span data-ttu-id="0f2ad-105">此函式會使用來自挑戰的要求資源和資料的相關資訊來產生 MD5 [*雜湊*](/windows/desktop/SecGloss/h-gly) 指紋，並輸出代表部分 [*安全性內容*](/windows/desktop/SecGloss/s-gly)的安全性權杖。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-105">This function generates an MD5 [*hash*](/windows/desktop/SecGloss/h-gly) fingerprint by using information about the requested resource and data from the challenge, and outputs a security token that represents a partial [*security context*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="0f2ad-106">若要完成驗證，用戶端必須將權杖傳回到發出挑戰的伺服器。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-106">To complete the authentication, the client must return the token to the server that issued the challenge.</span></span>

<span data-ttu-id="0f2ad-107">下表描述 [**InitializeSecurityCoNtext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) [*函數*](/windows/desktop/SecGloss/c-gly)的參數，以及在建立摘要挑戰回應時要提供的值。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-107">The following table describes the parameters of the [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) [*function*](/windows/desktop/SecGloss/c-gly), and the values to supply when constructing a Digest challenge response.</span></span>



| <span data-ttu-id="0f2ad-108">參數</span><span class="sxs-lookup"><span data-stu-id="0f2ad-108">Parameter</span></span>                  | <span data-ttu-id="0f2ad-109">Description</span><span class="sxs-lookup"><span data-stu-id="0f2ad-109">Description</span></span>                                                                                                                                                                                               |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f2ad-110">*fCoNtextReq*</span><span class="sxs-lookup"><span data-stu-id="0f2ad-110">*fContextReq*</span></span><br/>   | <span data-ttu-id="0f2ad-111">用戶端要求的安全性內容屬性。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-111">The security context attributes requested by the client.</span></span> <span data-ttu-id="0f2ad-112">如需詳細資訊，請參閱摘要挑戰回應內容需求。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-112">For more information, see Digest Challenge Response Context Requirements.</span></span><br/>                                                             |
| <span data-ttu-id="0f2ad-113">*pszTargetName*</span><span class="sxs-lookup"><span data-stu-id="0f2ad-113">*pszTargetName*</span></span><br/> | <span data-ttu-id="0f2ad-114">HTTP：以 Null 終止的字串，指定目標 URL。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-114">HTTP: Null-terminated string that specifies the target URL.</span></span><br/> <span data-ttu-id="0f2ad-115">SASL：指定 DNS/SPN 目標的以 Null 結束的字串。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-115">SASL: Null-terminated string that specifies the DNS/SPN target.</span></span><br/>                                                         |
| <span data-ttu-id="0f2ad-116">*pInput*</span><span class="sxs-lookup"><span data-stu-id="0f2ad-116">*pInput*</span></span><br/>        | <span data-ttu-id="0f2ad-117">包含摘要 SSP 所需資訊的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-117">Buffers that contain information required by the Digest SSP.</span></span> <span data-ttu-id="0f2ad-118">如需詳細資訊，請參閱 [摘要挑戰回應的輸入緩衝區](input-buffers-for-the-digest-challenge-response.md)。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-118">For more information, see [Input Buffers for the Digest Challenge Response](input-buffers-for-the-digest-challenge-response.md).</span></span><br/> |
| <span data-ttu-id="0f2ad-119">*pfCoNtextAttr*</span><span class="sxs-lookup"><span data-stu-id="0f2ad-119">*pfContextAttr*</span></span><br/> | <span data-ttu-id="0f2ad-120">接收傳回的安全性內容所支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-120">Receives the attributes supported by the returned security context.</span></span> <span data-ttu-id="0f2ad-121">如需詳細資訊，請參閱摘要挑戰回應內容需求。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-121">For more information, see Digest Challenge Response Context Requirements.</span></span><br/>                                                  |
| <span data-ttu-id="0f2ad-122">*pOutput*</span><span class="sxs-lookup"><span data-stu-id="0f2ad-122">*pOutput*</span></span><br/>       | <span data-ttu-id="0f2ad-123">\_接收要傳回給伺服器之安全性權杖的之 secbuffer TOKEN 類型緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-123">Address of a SECBUFFER\_TOKEN type buffer that receives a security token to send back to the server.</span></span><br/>                                                                                           |



 

## <a name="digest-challenge-response-context-requirements"></a><span data-ttu-id="0f2ad-124">摘要挑戰回應內容需求</span><span class="sxs-lookup"><span data-stu-id="0f2ad-124">Digest Challenge Response Context Requirements</span></span>

<span data-ttu-id="0f2ad-125">內容需求是決定下列事項的旗標：</span><span class="sxs-lookup"><span data-stu-id="0f2ad-125">Context requirements are flags that determine:</span></span>

-   <span data-ttu-id="0f2ad-126">Microsoft Digest 是否做為 SASL 機制或 HTTP 驗證通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-126">Whether Microsoft Digest functions as a SASL mechanism or HTTP authentication protocol.</span></span>
-   <span data-ttu-id="0f2ad-127">用戶端和伺服器所共用的 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 所支援的保護品質。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-127">The quality of protection supported by the [*security context*](/windows/desktop/SecGloss/s-gly) shared by the client and server.</span></span>

<span data-ttu-id="0f2ad-128">根據預設，Microsoft Digest 會作為 SASL 機制。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-128">By default, Microsoft Digest functions as a SASL mechanism.</span></span>

<span data-ttu-id="0f2ad-129">內容需求會指定為傳遞給 [**InitializeSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)函數之 *fCoNtextReq* 參數的旗標。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-129">Context requirements are specified as flags passed to the *fContextReq* parameter of the [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span> <span data-ttu-id="0f2ad-130">旗標會藉由控制挑戰回應中的 qop 指示詞，來影響安全性內容的保護品質。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-130">The flags affect the security context's quality of protection by controlling the qop directive in the challenge response.</span></span>

<span data-ttu-id="0f2ad-131">根據預設，qop 指示詞會設定為 "auth"。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-131">By default, the qop directive is set to "auth".</span></span> <span data-ttu-id="0f2ad-132">若要產生將 qop 設定為 "auth-int" 的挑戰回應，必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="0f2ad-132">To generate a challenge response that sets qop to "auth-int", the following must occur:</span></span>

1.  <span data-ttu-id="0f2ad-133">摘要挑戰必須將 qop 指示詞設為 "auth-int"。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-133">The Digest challenge must have had a qop directive set to "auth-int".</span></span>
2.  <span data-ttu-id="0f2ad-134">用戶端必須指定下列一或多個旗標：</span><span class="sxs-lookup"><span data-stu-id="0f2ad-134">The client must specify one or more of the following flags:</span></span>

    -   <span data-ttu-id="0f2ad-135">ISC \_ 需求 \_ 完整性</span><span class="sxs-lookup"><span data-stu-id="0f2ad-135">ISC\_REQ\_INTEGRITY</span></span>
    -   <span data-ttu-id="0f2ad-136">ISC 要求重新執行偵測 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="0f2ad-136">ISC\_REQ\_REPLAY\_DETECT</span></span>
    -   <span data-ttu-id="0f2ad-137">會偵測 \_ 到 ISC 需求 \_ 順序 \_</span><span class="sxs-lookup"><span data-stu-id="0f2ad-137">ISC\_REQ\_SEQUENCE\_DETECT</span></span>

<span data-ttu-id="0f2ad-138">僅限 SASL：藉由指定 ISC 要求機密性旗標，以將 qop 指示詞設定為 "auth" 來產生挑戰回應 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-138">For SASL only: Generate a challenge response with the qop directive set to "auth-conf" by specifying the ISC\_REQ\_CONFIDENTIALITY flag.</span></span> <span data-ttu-id="0f2ad-139">因為此旗標對 HTTP 驗證無效，所以無法與 ISC 要求 HTTP 旗標一起使用 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-139">Because this flag is not valid for HTTP authentication, it cannot be used with the ISC\_REQ\_HTTP flag.</span></span>

## <a name="verifying-the-quality-of-protection"></a><span data-ttu-id="0f2ad-140">確認保護品質</span><span class="sxs-lookup"><span data-stu-id="0f2ad-140">Verifying the Quality of Protection</span></span>

<span data-ttu-id="0f2ad-141">用戶端必須檢查 [**InitializeSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函式的 *pfCoNtextAttr* 參數中所傳回的安全性內容屬性旗標。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-141">The client must examine the security context attributes flags returned in the [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function's *pfContextAttr* parameter.</span></span> <span data-ttu-id="0f2ad-142">只有當旗標所指出的保護品質足以滿足其用途時，用戶端才應該將挑戰回應傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-142">The client should send the challenge response to the server only if the quality of protection indicated by the flags is sufficient for its purposes.</span></span> <span data-ttu-id="0f2ad-143">相關的旗標可以是下列各項的任意組合：</span><span class="sxs-lookup"><span data-stu-id="0f2ad-143">The relevant flags can be any combination of the following:</span></span>

-   <span data-ttu-id="0f2ad-144">ISC \_ RET \_ 完整性</span><span class="sxs-lookup"><span data-stu-id="0f2ad-144">ISC\_RET\_INTEGRITY</span></span>
-   <span data-ttu-id="0f2ad-145">ISC RET 重新執行偵測 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="0f2ad-145">ISC\_RET\_REPLAY\_DETECT</span></span>
-   <span data-ttu-id="0f2ad-146">ISC \_ RET \_ 序列 \_ 偵測</span><span class="sxs-lookup"><span data-stu-id="0f2ad-146">ISC\_RET\_SEQUENCE\_DETECT</span></span>
-   <span data-ttu-id="0f2ad-147">ISC \_ RET \_ 機密性僅 (SASL 內容) </span><span class="sxs-lookup"><span data-stu-id="0f2ad-147">ISC\_RET\_CONFIDENTIALITY (SASL contexts only)</span></span>

<span data-ttu-id="0f2ad-148">如需 qop 指示詞的詳細資訊，請參閱 [保護品質和密碼](quality-of-protection-and-ciphers.md)。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-148">For more information about the qop directive, see [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).</span></span>

<span data-ttu-id="0f2ad-149">如需挑戰回應指示詞的詳細資訊，請參閱 [摘要挑戰回應的內容](contents-of-a-digest-challenge-response.md)。</span><span class="sxs-lookup"><span data-stu-id="0f2ad-149">For more information about challenge response directives, see [Contents of a Digest Challenge Response](contents-of-a-digest-challenge-response.md).</span></span>

 

