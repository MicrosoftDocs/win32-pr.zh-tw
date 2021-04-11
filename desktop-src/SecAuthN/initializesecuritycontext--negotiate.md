---
description: 使用 Negotiate [*限制委派*](../secgloss/s-gly.md)，從認證控制碼起始用戶端輸出 [*安全性內容*](../secgloss/s-gly.md)。
ms.assetid: 031b0e82-f246-4291-aed3-f443ab152e00
title: 'InitializeSecurityCoNtext (Negotiate) function (Sspi) '
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: f4fd8c68896f10627ff1d66c3f576ca06d67e029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848757"
---
# <a name="initializesecuritycontext-negotiate-function"></a><span data-ttu-id="24006-103">InitializeSecurityCoNtext (Negotiate) 函數</span><span class="sxs-lookup"><span data-stu-id="24006-103">InitializeSecurityContext (Negotiate) function</span></span>

<span data-ttu-id="24006-104">**InitializeSecurityCoNtext (Negotiate)** 函數會從認證控制碼起始用戶端的輸出 [*安全性內容*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="24006-104">The **InitializeSecurityContext (Negotiate)** function initiates the client side, outbound [*security context*](../secgloss/s-gly.md) from a credential handle.</span></span> <span data-ttu-id="24006-105">函數是用來建立用戶端應用程式和遠端對等之間的 [*安全性內容*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="24006-105">The function is used to build a [*security context*](../secgloss/s-gly.md) between the client application and a remote peer.</span></span> <span data-ttu-id="24006-106">**InitializeSecurityCoNtext (Negotiate)** 會傳回用戶端必須傳遞給遠端對等的權杖，對等互連接著會透過 [**AcceptSecurityCoNtext (Negotiate)**](acceptsecuritycontext--negotiate.md) 呼叫，提交給本機安全性執行。</span><span class="sxs-lookup"><span data-stu-id="24006-106">**InitializeSecurityContext (Negotiate)** returns a token that the client must pass to the remote peer, which the peer in turn submits to the local security implementation through the [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) call.</span></span> <span data-ttu-id="24006-107">所有呼叫端都應該將產生的 token 視為不透明。</span><span class="sxs-lookup"><span data-stu-id="24006-107">The token generated should be considered opaque by all callers.</span></span>

<span data-ttu-id="24006-108">通常會在迴圈中呼叫 **InitializeSecurityCoNtext (Negotiate)** 函式，直到建立足夠的 [*安全性內容*](../secgloss/s-gly.md) 為止。</span><span class="sxs-lookup"><span data-stu-id="24006-108">Typically, the **InitializeSecurityContext (Negotiate)** function is called in a loop until a sufficient [*security context*](../secgloss/s-gly.md) is established.</span></span>

## <a name="syntax"></a><span data-ttu-id="24006-109">語法</span><span class="sxs-lookup"><span data-stu-id="24006-109">Syntax</span></span>


```C++
SECURITY_STATUS SEC_Entry InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    SEC_CHAR       *pszTargetName,
  _In_        ULONG          fContextReq,
  _In_        ULONG          Reserved1,
  _In_        ULONG          TargetDataRep,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          Reserved2,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       PULONG         pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a><span data-ttu-id="24006-110">參數</span><span class="sxs-lookup"><span data-stu-id="24006-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24006-111">*phCredential* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="24006-111">*phCredential* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24006-112">[**AcquireCredentialsHandle (Negotiate)**](acquirecredentialshandle--negotiate.md)所傳回認證的控制碼。</span><span class="sxs-lookup"><span data-stu-id="24006-112">A handle to the credentials returned by [**AcquireCredentialsHandle (Negotiate)**](acquirecredentialshandle--negotiate.md).</span></span> <span data-ttu-id="24006-113">這個控制碼是用來建立 [*安全性內容*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="24006-113">This handle is used to build the [*security context*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="24006-114">**InitializeSecurityCoNtext (Negotiate)** 函數至少需要輸出認證。</span><span class="sxs-lookup"><span data-stu-id="24006-114">The **InitializeSecurityContext (Negotiate)** function requires at least OUTBOUND credentials.</span></span>

</dd> <dt>

<span data-ttu-id="24006-115">*phCoNtext* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="24006-115">*phContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24006-116">[CtxtHandle](sspi-handles.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="24006-116">A pointer to a [CtxtHandle](sspi-handles.md) structure.</span></span> <span data-ttu-id="24006-117">在第一次呼叫 **InitializeSecurityCoNtext (Negotiate)** 時，此指標為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="24006-117">On the first call to **InitializeSecurityContext (Negotiate)**, this pointer is **NULL**.</span></span> <span data-ttu-id="24006-118">第二次呼叫時，這個參數是第一個呼叫在 *phNewCoNtext* 參數中傳回之部分格式內容的控制碼指標。</span><span class="sxs-lookup"><span data-stu-id="24006-118">On the second call, this parameter is a pointer to the handle to the partially formed context returned in the *phNewContext* parameter by the first call.</span></span>

</dd> <dt>

<span data-ttu-id="24006-119">*pszTargetName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="24006-119">*pszTargetName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24006-120">以 null 結束的字串指標，指出 (SPN) 的服務主體名稱或目的地伺服器的 [*安全性內容*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="24006-120">A pointer to a null-terminated string that indicates the service principal name (SPN) or the [*security context*](../secgloss/s-gly.md) of the destination server.</span></span>

<span data-ttu-id="24006-121">應用程式必須提供有效的 SPN，以協助減輕重新執行攻擊。</span><span class="sxs-lookup"><span data-stu-id="24006-121">Applications must supply a valid SPN to help mitigate replay attacks.</span></span>

</dd> <dt>

<span data-ttu-id="24006-122">*fCoNtextReq* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24006-122">*fContextReq* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24006-123">表示內容要求的位旗標。</span><span class="sxs-lookup"><span data-stu-id="24006-123">Bit flags that indicate requests for the context.</span></span> <span data-ttu-id="24006-124">並非所有封裝都能支援所有的需求。</span><span class="sxs-lookup"><span data-stu-id="24006-124">Not all packages can support all requirements.</span></span> <span data-ttu-id="24006-125">用於此參數的旗標前面會加 \_ 上 isc 需求 \_ ，例如，isc 要求 \_ \_ 委派。</span><span class="sxs-lookup"><span data-stu-id="24006-125">Flags used for this parameter are prefixed with ISC\_REQ\_, for example, ISC\_REQ\_DELEGATE.</span></span> <span data-ttu-id="24006-126">這個參數可以是下列其中一個或多個屬性旗標。</span><span class="sxs-lookup"><span data-stu-id="24006-126">This parameter can be one or more of the following attributes flags.</span></span>



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="24006-127">值</span><span class="sxs-lookup"><span data-stu-id="24006-127">Value</span></span></th><th><span data-ttu-id="24006-128">意義</span><span class="sxs-lookup"><span data-stu-id="24006-128">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <span data-ttu-id="24006-129"><dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="24006-129"><dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt> </span></span></dl></td><td><span data-ttu-id="24006-130">[*安全性套件*](../secgloss/s-gly.md)會為您配置輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="24006-130">The [*security package*](../secgloss/s-gly.md) allocates output buffers for you.</span></span> <span data-ttu-id="24006-131">當您完成使用輸出緩衝區時，請呼叫 [<strong>FreeCoNtextBuffer</strong>] (/windows/win32/api/sspi/nf-sspi-freecoNtextbuffer) 函式釋放它們。</span><span class="sxs-lookup"><span data-stu-id="24006-131">When you have finished using the output buffers, free them by calling the [<strong>FreeContextBuffer</strong>](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) function.</span></span><br/></td></tr><tr class="even"><td><span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl> <span data-ttu-id="24006-132"><dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="24006-132"><dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt> </span></span></dl></td><td><span data-ttu-id="24006-133">使用 [<strong>EncryptMessage</strong>] (encryptmessage--general.md) 函數來加密訊息。</span><span class="sxs-lookup"><span data-stu-id="24006-133">Encrypt messages by using the [<strong>EncryptMessage</strong>](encryptmessage--general.md) function.</span></span><br/></td></tr><tr class="odd"><td><span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <span data-ttu-id="24006-134"><dt><strong>ISC_REQ_CONNECTION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="24006-134"><dt><strong>ISC_REQ_CONNECTION</strong></dt> </span></span></dl></td><td><span data-ttu-id="24006-135">[*安全性內容*](../secgloss/s-gly.md)將不會處理格式化訊息。</span><span class="sxs-lookup"><span data-stu-id="24006-135">The [*security context*](../secgloss/s-gly.md) will not handle formatting messages.</span></span> <span data-ttu-id="24006-136">此值為預設。</span><span class="sxs-lookup"><span data-stu-id="24006-136">This value is the default.</span></span><br/></td></tr><tr class="even"><td><span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <span data-ttu-id="24006-137"><dt><strong>ISC_REQ_DELEGATE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="24006-137"><dt><strong>ISC_REQ_DELEGATE</strong></dt> </span></span></dl></td><td><span data-ttu-id="24006-138">伺服器可以使用內容，以用戶端的身分向其他伺服器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="24006-138">The server can use the context to authenticate to other servers as the client.</span></span> <span data-ttu-id="24006-139">必須設定 ISC_REQ_MUTUAL_AUTH 旗標，此旗標才能運作。</span><span class="sxs-lookup"><span data-stu-id="24006-139">The ISC_REQ_MUTUAL_AUTH flag must be set for this flag to work.</span></span> <span data-ttu-id="24006-140">適用于 Kerberos。</span><span class="sxs-lookup"><span data-stu-id="24006-140">Valid for Kerberos.</span></span> <span data-ttu-id="24006-141">請忽略此旗標以進行 [*限制委派*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="24006-141">Ignore this flag for [*constrained delegation*](../secgloss/c-gly.md).</span></span><br/></td></tr><tr class="odd"><td><span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <span data-ttu-id="24006-142"><dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="24006-142"><dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt> </span></span></dl></td><td><span data-ttu-id="24006-143">發生錯誤時，將會通知遠端方。</span><span class="sxs-lookup"><span data-stu-id="24006-143">When errors occur, the remote party will be notified.</span></span><br/></td></tr><tr class="even"><td><span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl> <span data-ttu-id="24006-144"><dt><strong>ISC_REQ_INTEGRITY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="24006-144"><dt><strong>ISC_REQ_INTEGRITY</strong></dt> </span></span></dl></td><td><span data-ttu-id="24006-145">使用 [<strong>EncryptMessage</strong>] (encryptmessage--general.md) 和 [<strong>MakeSignature</strong>] (makesignature.md) 函數來簽署訊息和驗證簽章。</span><span class="sxs-lookup"><span data-stu-id="24006-145">Sign messages and verify signatures by using the [<strong>EncryptMessage</strong>](encryptmessage--general.md) and [<strong>MakeSignature</strong>](makesignature.md) functions.</span></span><br/></td></tr><tr class="odd"><td><span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <span data-ttu-id="24006-146"><dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="24006-146"><dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt> </span></span></dl></td><td><span data-ttu-id="24006-147">將會滿足服務的相互驗證原則。</span><span class="sxs-lookup"><span data-stu-id="24006-147">The mutual authentication policy of the service will be satisfied.</span></span><br/><blockquote>[!Caution]<br />
<span data-ttu-id="24006-148">這並不代表會執行相互驗證，只會滿足服務的驗證原則。</span><span class="sxs-lookup"><span data-stu-id="24006-148">This does not necessarily mean that mutual authentication is performed, only that the authentication policy of the service is satisfied.</span></span> <span data-ttu-id="24006-149">若要確保執行相互驗證，請呼叫 [<strong>QueryCoNtextAttributes (Negotiate) </strong>] (querycoNtextattributes--negotiate.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="24006-149">To ensure that mutual authentication is performed, call the [<strong>QueryContextAttributes (Negotiate)</strong>](querycontextattributes--negotiate.md) function.</span></span></blockquote><br/></td></tr><tr class="even"><td><span id="ISC_REQ_NO_INTEGRITY"></span><span id="isc_req_no_integrity"></span><dl> <span data-ttu-id="24006-150"><dt><strong>ISC_REQ_NO_INTEGRITY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="24006-150"><dt><strong>ISC_REQ_NO_INTEGRITY</strong></dt> </span></span></dl></td><td><span data-ttu-id="24006-151">如果設定此旗標，則會忽略 <strong>ISC_REQ_INTEGRITY</strong> 旗標。</span><span class="sxs-lookup"><span data-stu-id="24006-151">If this flag is set, the <strong>ISC_REQ_INTEGRITY</strong> flag is ignored.</span></span><br/></td></tr><tr class="odd"><td><span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl> <span data-ttu-id="24006-152"><dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="24006-152"><dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt> </span></span></dl></td><td><span data-ttu-id="24006-153">偵測已使用 [<strong>EncryptMessage</strong>] (encryptmessage--general.md) 或 [<strong>MakeSignature</strong>] (makesignature.md) 函數編碼的重新執行訊息。</span><span class="sxs-lookup"><span data-stu-id="24006-153">Detect replayed messages that have been encoded by using the [<strong>EncryptMessage</strong>](encryptmessage--general.md) or [<strong>MakeSignature</strong>](makesignature.md) functions.</span></span><br/></td></tr><tr class="even"><td><span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <span data-ttu-id="24006-154"><dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="24006-154"><dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt> </span></span></dl></td><td><span data-ttu-id="24006-155">偵測順序中所接收的訊息。</span><span class="sxs-lookup"><span data-stu-id="24006-155">Detect messages received out of sequence.</span></span><br/></td></tr><tr class="odd"><td><span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <span data-ttu-id="24006-156"><dt><strong>ISC_REQ_STREAM</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="24006-156"><dt><strong>ISC_REQ_STREAM</strong></dt> </span></span></dl></td><td><span data-ttu-id="24006-157">支援資料流程導向連接。</span><span class="sxs-lookup"><span data-stu-id="24006-157">Support a stream-oriented connection.</span></span><br/></td></tr></tbody></table>



 

<span data-ttu-id="24006-158">用戶端可能不支援要求的屬性。</span><span class="sxs-lookup"><span data-stu-id="24006-158">The requested attributes may not be supported by the client.</span></span> <span data-ttu-id="24006-159">如需詳細資訊，請參閱 *pfCoNtextAttr* 參數。</span><span class="sxs-lookup"><span data-stu-id="24006-159">For more information, see the *pfContextAttr* parameter.</span></span>

<span data-ttu-id="24006-160">如需各種屬性的進一步說明，請參閱 [內容需求](context-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="24006-160">For further descriptions of the various attributes, see [Context Requirements](context-requirements.md).</span></span>

</dd> <dt>

<span data-ttu-id="24006-161">*Reserved1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24006-161">*Reserved1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24006-162">此參數是保留的，而且必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="24006-162">This parameter is reserved and must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="24006-163">*TargetDataRep* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24006-163">*TargetDataRep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24006-164">目標上的資料標記法，例如位元組順序。</span><span class="sxs-lookup"><span data-stu-id="24006-164">The data representation, such as byte ordering, on the target.</span></span> <span data-ttu-id="24006-165">此參數可以是安全性 \_ 原生 \_ DREP 或安全性 \_ 網路 \_ DREP。</span><span class="sxs-lookup"><span data-stu-id="24006-165">This parameter can be either SECURITY\_NATIVE\_DREP or SECURITY\_NETWORK\_DREP.</span></span>

</dd> <dt>

<span data-ttu-id="24006-166">*pInput* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="24006-166">*pInput* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24006-167">[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標，其中包含提供給封裝輸入的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="24006-167">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure that contains pointers to the buffers supplied as input to the package.</span></span> <span data-ttu-id="24006-168">除非用戶端內容是由伺服器起始，否則這個參數的值在第一次呼叫函式時必須是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="24006-168">Unless the client context was initiated by the server, the value of this parameter must be **NULL** on the first call to the function.</span></span> <span data-ttu-id="24006-169">在後續呼叫函式或由伺服器起始用戶端內容時，此參數的值會是配置有足夠記憶體的緩衝區指標，以保存遠端電腦所傳回的權杖。</span><span class="sxs-lookup"><span data-stu-id="24006-169">On subsequent calls to the function or when the client context was initiated by the server, the value of this parameter is a pointer to a buffer allocated with enough memory to hold the token returned by the remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="24006-170">*Reserved2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24006-170">*Reserved2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24006-171">此參數是保留的，而且必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="24006-171">This parameter is reserved and must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="24006-172">*phNewCoNtext* \[in、out、optional\]</span><span class="sxs-lookup"><span data-stu-id="24006-172">*phNewContext* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24006-173">[CtxtHandle](sspi-handles.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="24006-173">A pointer to a [CtxtHandle](sspi-handles.md) structure.</span></span> <span data-ttu-id="24006-174">第一次呼叫 **InitializeSecurityCoNtext (Negotiate)** 時，此指標會收到新的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="24006-174">On the first call to **InitializeSecurityContext (Negotiate)**, this pointer receives the new context handle.</span></span> <span data-ttu-id="24006-175">第二次呼叫時， *phNewCoNtext* 可以與 *phCoNtext* 參數中指定的控制碼相同。</span><span class="sxs-lookup"><span data-stu-id="24006-175">On the second call, *phNewContext* can be the same as the handle specified in the *phContext* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="24006-176">*pOutput* \[in、out、optional\]</span><span class="sxs-lookup"><span data-stu-id="24006-176">*pOutput* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24006-177">[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標，其中包含接收輸出資料之 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="24006-177">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure that contains pointers to the [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structure that receives the output data.</span></span> <span data-ttu-id="24006-178">如果輸入中的緩衝區輸入為 SEC \_ READWRITE，則輸出中會有該緩衝區。</span><span class="sxs-lookup"><span data-stu-id="24006-178">If a buffer was typed as SEC\_READWRITE in the input, it will be there on output.</span></span> <span data-ttu-id="24006-179">如果要求 (透過 ISC \_ 需求 \_ 配置 \_ 記憶體) ，並在安全性權杖的緩衝區描述項中填入位址，系統將會配置安全性權杖的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="24006-179">The system will allocate a buffer for the security token if requested (through ISC\_REQ\_ALLOCATE\_MEMORY) and fill in the address in the buffer descriptor for the security token.</span></span>

</dd> <dt>

<span data-ttu-id="24006-180">*pfCoNtextAttr* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="24006-180">*pfContextAttr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24006-181">變數的指標，用來接收一組位旗標，以指出已建立內容的 [*屬性*](../secgloss/a-gly.md#_security_attribute_gly) 。</span><span class="sxs-lookup"><span data-stu-id="24006-181">A pointer to a variable to receive a set of bit flags that indicate the [*attributes*](../secgloss/a-gly.md#_security_attribute_gly) of the established context.</span></span> <span data-ttu-id="24006-182">如需各種屬性的說明，請參閱 [內容需求](context-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="24006-182">For a description of the various attributes, see [Context Requirements](context-requirements.md).</span></span>

<span data-ttu-id="24006-183">用於此參數的旗標前面會加 \_ 上 isc ret，例如 isc \_ ret \_ 委派。</span><span class="sxs-lookup"><span data-stu-id="24006-183">Flags used for this parameter are prefixed with ISC\_RET, such as ISC\_RET\_DELEGATE.</span></span> <span data-ttu-id="24006-184">如需有效值的清單，請參閱 *fCoNtextReq* 參數。</span><span class="sxs-lookup"><span data-stu-id="24006-184">For a list of valid values, see the *fContextReq* parameter.</span></span>

<span data-ttu-id="24006-185">在最後一個函式呼叫成功傳回之前，請勿檢查安全性相關屬性。</span><span class="sxs-lookup"><span data-stu-id="24006-185">Do not check for security-related attributes until the final function call returns successfully.</span></span> <span data-ttu-id="24006-186">與安全性無關的屬性旗標（例如 ASC RET 配置的 \_ \_ \_ 記憶體旗標）可以在最後一次傳回前進行檢查。</span><span class="sxs-lookup"><span data-stu-id="24006-186">Attribute flags that are not related to security, such as the ASC\_RET\_ALLOCATED\_MEMORY flag, can be checked before the final return.</span></span>

> [!Note]  
> <span data-ttu-id="24006-187">特定內容屬性在與遠端對等的協商期間可能會變更。</span><span class="sxs-lookup"><span data-stu-id="24006-187">Particular context attributes can change during negotiation with a remote peer.</span></span>

 

</dd> <dt>

<span data-ttu-id="24006-188">*ptsExpiry* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="24006-188">*ptsExpiry* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24006-189">[**時間戳記**](timestamp.md)結構的指標，此結構會接收內容的到期時間。</span><span class="sxs-lookup"><span data-stu-id="24006-189">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the expiration time of the context.</span></span> <span data-ttu-id="24006-190">建議 [*安全套件*](../secgloss/s-gly.md) 在本地時間一律會傳回此值。</span><span class="sxs-lookup"><span data-stu-id="24006-190">It is recommended that the [*security package*](../secgloss/s-gly.md) always return this value in local time.</span></span> <span data-ttu-id="24006-191">這個參數是選擇性的，且應該傳遞給短期用戶端的 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="24006-191">This parameter is optional and **NULL** should be passed for short-lived clients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24006-192">傳回值</span><span class="sxs-lookup"><span data-stu-id="24006-192">Return value</span></span>

<span data-ttu-id="24006-193">如果函式成功，函數會傳回下列其中一個成功碼。</span><span class="sxs-lookup"><span data-stu-id="24006-193">If the function succeeds, the function returns one of the following success codes.</span></span>



| <span data-ttu-id="24006-194">傳回碼</span><span class="sxs-lookup"><span data-stu-id="24006-194">Return code</span></span>                                                                                                    | <span data-ttu-id="24006-195">Description</span><span class="sxs-lookup"><span data-stu-id="24006-195">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="24006-196"><dt>**秒 \_ E \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="24006-196"><dt>**SEC\_E\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="24006-197">已成功初始化 [*安全性內容*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="24006-197">The [*security context*](../secgloss/s-gly.md) was successfully initialized.</span></span> <span data-ttu-id="24006-198">不需要另一個 [**InitializeSecurityCoNtext (協商)**](initializesecuritycontext--negotiate.md) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="24006-198">There is no need for another [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) call.</span></span> <span data-ttu-id="24006-199">如果函式傳回輸出 token，也就是，如果 \_ *pOutput* 中的之 secbuffer token 的長度是非零，則該 token 必須傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="24006-199">If the function returns an output token, that is, if the SECBUFFER\_TOKEN in *pOutput* is of nonzero length, that token must be sent to the server.</span></span><br/> |
| <dl> <span data-ttu-id="24006-200"><dt>**秒 \_ \_ 完成 \_ 並 \_ 繼續**</dt></span><span class="sxs-lookup"><span data-stu-id="24006-200"><dt>**SEC\_I\_COMPLETE\_AND\_CONTINUE**</dt></span></span> </dl> | <span data-ttu-id="24006-201">用戶端必須呼叫 [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) ，然後將輸出傳遞至伺服器。</span><span class="sxs-lookup"><span data-stu-id="24006-201">The client must call [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) and then pass the output to the server.</span></span> <span data-ttu-id="24006-202">然後，用戶端會等候傳回的權杖，並在另一個呼叫中傳遞它，以 [**InitializeSecurityCoNtext (協商)**](initializesecuritycontext--negotiate.md)。</span><span class="sxs-lookup"><span data-stu-id="24006-202">The client then waits for a returned token and passes it, in another call, to [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md).</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="24006-203"><dt>**\_ \_ 需要完成的秒數 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="24006-203"><dt>**SEC\_I\_COMPLETE\_NEEDED**</dt></span></span> </dl>        | <span data-ttu-id="24006-204">用戶端必須完成建立訊息，然後呼叫 [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) 函數。</span><span class="sxs-lookup"><span data-stu-id="24006-204">The client must finish building the message and then call the [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) function.</span></span><br/>                                                                                                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="24006-205"><dt>**每 \_ 秒 \_ 繼續 \_ 需要**</dt></span><span class="sxs-lookup"><span data-stu-id="24006-205"><dt>**SEC\_I\_CONTINUE\_NEEDED**</dt></span></span> </dl>        | <span data-ttu-id="24006-206">用戶端必須將輸出 token 傳送至伺服器，並等候傳回權杖。</span><span class="sxs-lookup"><span data-stu-id="24006-206">The client must send the output token to the server and wait for a return token.</span></span> <span data-ttu-id="24006-207">傳回的權杖接著會傳遞給 [**InitializeSecurityCoNtext (Negotiate)**](initializesecuritycontext--negotiate.md)的另一個呼叫。</span><span class="sxs-lookup"><span data-stu-id="24006-207">The returned token is then passed in another call to [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md).</span></span> <span data-ttu-id="24006-208">輸出 token 可以是空的。</span><span class="sxs-lookup"><span data-stu-id="24006-208">The output token can be empty.</span></span><br/>                                                                                                                                                       |



 

<span data-ttu-id="24006-209">如果函式失敗，函數會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="24006-209">If the function fails, the function returns one of the following error codes.</span></span>



| <span data-ttu-id="24006-210">傳回碼</span><span class="sxs-lookup"><span data-stu-id="24006-210">Return code</span></span>                                                                                                          | <span data-ttu-id="24006-211">Description</span><span class="sxs-lookup"><span data-stu-id="24006-211">Description</span></span>                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="24006-212"><dt>**每 \_ 秒 \_ 沒有足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="24006-212"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl>          | <span data-ttu-id="24006-213">沒有足夠的記憶體可完成要求的動作。</span><span class="sxs-lookup"><span data-stu-id="24006-213">There is not enough memory available to complete the requested action.</span></span><br/>                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="24006-214"><dt>**SEC \_ E \_ 內部 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="24006-214"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>               | <span data-ttu-id="24006-215">發生未對應到 SSPI 錯誤碼的錯誤。</span><span class="sxs-lookup"><span data-stu-id="24006-215">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="24006-216"><dt>**SEC \_ E \_ 不正確 \_ 控制碼**</dt></span><span class="sxs-lookup"><span data-stu-id="24006-216"><dt>**SEC\_E\_INVALID\_HANDLE**</dt></span></span> </dl>               | <span data-ttu-id="24006-217">傳遞給函數的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="24006-217">The handle passed to the function is not valid.</span></span><br/>                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="24006-218"><dt>**SEC \_ E \_ 不正確 \_ 權杖**</dt></span><span class="sxs-lookup"><span data-stu-id="24006-218"><dt>**SEC\_E\_INVALID\_TOKEN**</dt></span></span> </dl>                | <span data-ttu-id="24006-219">此錯誤是因為輸入標記格式不正確，例如傳輸中損毀、不正確大小的權杖，或傳入錯誤 [*限制委派*](../secgloss/s-gly.md)的權杖。</span><span class="sxs-lookup"><span data-stu-id="24006-219">The error is due to a malformed input token, such as a token corrupted in transit, a token of incorrect size, or a token passed into the wrong [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="24006-220">如果用戶端和伺服器未協調適當的 [*限制委派*](../secgloss/s-gly.md)，就可能會發生將權杖傳遞至錯誤的封裝。</span><span class="sxs-lookup"><span data-stu-id="24006-220">Passing a token to the wrong package can happen if the client and server did not negotiate the proper [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="24006-221"><dt>**秒 \_ E \_ 登入 \_ 拒絕**</dt></span><span class="sxs-lookup"><span data-stu-id="24006-221"><dt>**SEC\_E\_LOGON\_DENIED**</dt></span></span> </dl>                 | <span data-ttu-id="24006-222">登入失敗。</span><span class="sxs-lookup"><span data-stu-id="24006-222">The logon failed.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="24006-223"><dt>**SEC \_ E \_ 無 \_ 驗證 \_ 授權單位**</dt></span><span class="sxs-lookup"><span data-stu-id="24006-223"><dt>**SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY**</dt></span></span> </dl> | <span data-ttu-id="24006-224">無法連絡任何授權單位進行驗證。</span><span class="sxs-lookup"><span data-stu-id="24006-224">No authority could be contacted for authentication.</span></span> <span data-ttu-id="24006-225">驗證方的功能變數名稱可能錯誤、無法連線到網域，或可能有信任關係失敗。</span><span class="sxs-lookup"><span data-stu-id="24006-225">The domain name of the authenticating party could be wrong, the domain could be unreachable, or there might have been a trust relationship failure.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="24006-226"><dt>**SEC \_ E \_ 無 \_ 認證**</dt></span><span class="sxs-lookup"><span data-stu-id="24006-226"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>               | <span data-ttu-id="24006-227">[*限制委派*](../secgloss/s-gly.md)中不提供任何認證。</span><span class="sxs-lookup"><span data-stu-id="24006-227">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/>                                                                                                                                                  |
| <dl> <span data-ttu-id="24006-228"><dt>**SEC \_ E \_ 目標 \_ 不明**</dt></span><span class="sxs-lookup"><span data-stu-id="24006-228"><dt>**SEC\_E\_TARGET\_UNKNOWN**</dt></span></span> </dl>               | <span data-ttu-id="24006-229">無法辨識目標。</span><span class="sxs-lookup"><span data-stu-id="24006-229">The target was not recognized.</span></span><br/>                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="24006-230"><dt>**SEC \_ E \_ 不支援的函式 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="24006-230"><dt>**SEC\_E\_UNSUPPORTED\_FUNCTION**</dt></span></span> </dl>         | <span data-ttu-id="24006-231">FCoNtextReq 參數中指定了不正確內容屬性旗標， () 的的 ISC \_ \_ 要求委派或 isc \_ \_ 要求 \_ 的提示 \_ 。 </span><span class="sxs-lookup"><span data-stu-id="24006-231">A context attribute flag that is not valid (ISC\_REQ\_DELEGATE or ISC\_REQ\_PROMPT\_FOR\_CREDS) was specified in the *fContextReq* parameter.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="24006-232"><dt>**SEC \_ E \_ 錯誤的 \_ 主體**</dt></span><span class="sxs-lookup"><span data-stu-id="24006-232"><dt>**SEC\_E\_WRONG\_PRINCIPAL**</dt></span></span> </dl>              | <span data-ttu-id="24006-233">收到驗證要求的主體與傳入 *pszTargetName* 參數的主體不同。</span><span class="sxs-lookup"><span data-stu-id="24006-233">The principal that received the authentication request is not the same as the one passed into the *pszTargetName* parameter.</span></span> <span data-ttu-id="24006-234">這表示相互驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="24006-234">This indicates a failure in mutual authentication.</span></span><br/>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="24006-235">備註</span><span class="sxs-lookup"><span data-stu-id="24006-235">Remarks</span></span>

<span data-ttu-id="24006-236">呼叫端負責判斷最終的內容屬性是否足夠。</span><span class="sxs-lookup"><span data-stu-id="24006-236">The caller is responsible for determining whether the final context attributes are sufficient.</span></span> <span data-ttu-id="24006-237">例如，如果要求了機密性，但無法建立，有些應用程式可能會選擇立即關閉連接。</span><span class="sxs-lookup"><span data-stu-id="24006-237">If, for example, confidentiality was requested, but could not be established, some applications may choose to shut down the connection immediately.</span></span>

<span data-ttu-id="24006-238">如果 [*安全性內容*](../secgloss/s-gly.md) 的屬性不足夠，用戶端必須藉由呼叫 [**DeleteSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) 函式來釋放部分建立的內容。</span><span class="sxs-lookup"><span data-stu-id="24006-238">If attributes of the [*security context*](../secgloss/s-gly.md) are not sufficient, the client must free the partially created context by calling the [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) function.</span></span>

<span data-ttu-id="24006-239">**InitializeSecurityCoNtext (Negotiate)** 函數會由用戶端用來初始化輸出內容。</span><span class="sxs-lookup"><span data-stu-id="24006-239">The **InitializeSecurityContext (Negotiate)** function is used by a client to initialize an outbound context.</span></span>

<span data-ttu-id="24006-240">針對兩階段 [*安全性內容*](../secgloss/s-gly.md)，呼叫順序如下所示：</span><span class="sxs-lookup"><span data-stu-id="24006-240">For a two-leg [*security context*](../secgloss/s-gly.md), the calling sequence is as follows:</span></span>

1.  <span data-ttu-id="24006-241">用戶端會呼叫 *phCoNtext* 設為 **Null** 的函式，並使用輸入訊息填入緩衝區描述項。</span><span class="sxs-lookup"><span data-stu-id="24006-241">The client calls the function with *phContext* set to **NULL** and fills in the buffer descriptor with the input message.</span></span>
2.  <span data-ttu-id="24006-242">[*安全性套件*](../secgloss/s-gly.md)會檢查參數並建立不透明的權杖，並將它放在緩衝區陣列的 token 專案中。</span><span class="sxs-lookup"><span data-stu-id="24006-242">The [*security package*](../secgloss/s-gly.md) examines the parameters and constructs an opaque token, placing it in the TOKEN element in the buffer array.</span></span> <span data-ttu-id="24006-243">如果 *fCoNtextReq* 參數包含「ISC \_ 需求 \_ 配置記憶體」旗標 \_ ，則 [*安全性封裝*](../secgloss/s-gly.md) 會配置記憶體，並傳回 TOKEN 元素中的指標。</span><span class="sxs-lookup"><span data-stu-id="24006-243">If the *fContextReq* parameter includes the ISC\_REQ\_ALLOCATE\_MEMORY flag, the [*security package*](../secgloss/s-gly.md) allocates the memory and returns the pointer in the TOKEN element.</span></span>
3.  <span data-ttu-id="24006-244">用戶端會將 *pOutput* 緩衝區中傳回的權杖傳送至目標伺服器。</span><span class="sxs-lookup"><span data-stu-id="24006-244">The client sends the token returned in the *pOutput* buffer to the target server.</span></span> <span data-ttu-id="24006-245">然後，伺服器會在對 [**AcceptSecurityCoNtext (Negotiate)**](acceptsecuritycontext--negotiate.md) 函式的呼叫中，將權杖傳遞為輸入引數。</span><span class="sxs-lookup"><span data-stu-id="24006-245">The server then passes the token as an input argument in a call to the [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) function.</span></span>
4.  <span data-ttu-id="24006-246">[**AcceptSecurityCoNtext (Negotiate)**](acceptsecuritycontext--negotiate.md) 可能會傳回權杖，而伺服器會將權杖傳送給用戶端，以進行第二次呼叫 **InitializeSecurityCoNtext (Negotiate)** 如果第一次呼叫傳回 \_ 時，我 \_ 需要繼續進行 \_ 。</span><span class="sxs-lookup"><span data-stu-id="24006-246">[**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) may return a token, which the server sends to the client for a second call to **InitializeSecurityContext (Negotiate)** if the first call returned SEC\_I\_CONTINUE\_NEEDED.</span></span>

<span data-ttu-id="24006-247">針對多階段 [*安全性內容*](../secgloss/s-gly.md)，例如相互驗證，呼叫順序如下所示：</span><span class="sxs-lookup"><span data-stu-id="24006-247">For multiple-leg [*security context*](../secgloss/s-gly.md)s, such as mutual authentication, the calling sequence is as follows:</span></span>

1.  <span data-ttu-id="24006-248">用戶端會如先前所述呼叫函式，但封裝會傳回每秒 \_ \_ 繼續 \_ 需要的成功程式碼。</span><span class="sxs-lookup"><span data-stu-id="24006-248">The client calls the function as described earlier, but the package returns the SEC\_I\_CONTINUE\_NEEDED success code.</span></span>
2.  <span data-ttu-id="24006-249">用戶端會將輸出 token 傳送至伺服器，並等候伺服器的回復。</span><span class="sxs-lookup"><span data-stu-id="24006-249">The client sends the output token to the server and waits for the server's reply.</span></span>
3.  <span data-ttu-id="24006-250">當收到伺服器的回應時，用戶端會呼叫 **InitializeSecurityCoNtext (重新協商)** ，並將 *phCoNtext* 設定為上次呼叫所傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="24006-250">Upon receipt of the server's response, the client calls **InitializeSecurityContext (Negotiate)** again, with *phContext* set to the handle that was returned from the last call.</span></span> <span data-ttu-id="24006-251">從伺服器收到的權杖是在 *pInput* 參數中提供。</span><span class="sxs-lookup"><span data-stu-id="24006-251">The token received from the server is supplied in the *pInput* parameter.</span></span>

<span data-ttu-id="24006-252">如果伺服器已順利回應，則 [*安全性封裝*](../secgloss/s-gly.md) 會傳回 SEC \_ E \_ OK，並且會建立安全會話。</span><span class="sxs-lookup"><span data-stu-id="24006-252">If the server has successfully responded, the [*security package*](../secgloss/s-gly.md) returns SEC\_E\_OK and a secure session is established.</span></span>

<span data-ttu-id="24006-253">如果函數傳回其中一個錯誤回應，則不接受伺服器的回應，也不會建立會話。</span><span class="sxs-lookup"><span data-stu-id="24006-253">If the function returns one of the error responses, the server's response is not accepted, and the session is not established.</span></span>

<span data-ttu-id="24006-254">如果函式傳回的秒數 \_ \_ 是我繼續 \_ 需要的，則需要秒完成 \_ \_ \_ ，或每秒 \_ \_ 完成 \_ 並 \_ 繼續進行，步驟2和3會重複執行。</span><span class="sxs-lookup"><span data-stu-id="24006-254">If the function returns SEC\_I\_CONTINUE\_NEEDED, SEC\_I\_COMPLETE\_NEEDED, or SEC\_I\_COMPLETE\_AND\_CONTINUE, steps 2 and 3 are repeated.</span></span>

<span data-ttu-id="24006-255">若要初始化 [*安全性內容*](../secgloss/s-gly.md)，根據基礎驗證機制以及 *fCoNtextReq* 參數中指定的選項而定，可能需要對這個函式進行一個以上的呼叫。</span><span class="sxs-lookup"><span data-stu-id="24006-255">To initialize a [*security context*](../secgloss/s-gly.md), more than one call to this function may be required, depending on the underlying authentication mechanism as well as the choices specified in the *fContextReq* parameter.</span></span>

<span data-ttu-id="24006-256">*FCoNtextReq* 和 *pfCoNtextAttributes* 參數是代表各種內容屬性的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="24006-256">The *fContextReq* and *pfContextAttributes* parameters are bitmasks that represent various context attributes.</span></span> <span data-ttu-id="24006-257">如需各種屬性的說明，請參閱 [內容需求](context-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="24006-257">For a description of the various attributes, see [Context Requirements](context-requirements.md).</span></span> <span data-ttu-id="24006-258">*PfCoNtextAttributes* 參數在任何成功傳回時都有效，但只有在最後成功傳回時，才應該檢查與內容安全性層面相關的旗標。</span><span class="sxs-lookup"><span data-stu-id="24006-258">The *pfContextAttributes* parameter is valid on any successful return, but only on the final successful return should you examine the flags that pertain to security aspects of the context.</span></span> <span data-ttu-id="24006-259">例如，中繼傳回可以設定 ISC RET 配置的 \_ \_ \_ 記憶體旗標。</span><span class="sxs-lookup"><span data-stu-id="24006-259">Intermediate returns can set, for example, the ISC\_RET\_ALLOCATED\_MEMORY flag.</span></span>

<span data-ttu-id="24006-260">如果 \_ \_ 已設定 ISC 需求使用提供的認證旗標 \_ \_ ，則 [*安全性封裝*](../secgloss/s-gly.md) 必須 \_ \_ 在 *pInput* 輸入緩衝區中尋找之 secbuffer PKG PARAMS 緩衝區類型。</span><span class="sxs-lookup"><span data-stu-id="24006-260">If the ISC\_REQ\_USE\_SUPPLIED\_CREDS flag is set, the [*security package*](../secgloss/s-gly.md) must look for a SECBUFFER\_PKG\_PARAMS buffer type in the *pInput* input buffer.</span></span> <span data-ttu-id="24006-261">這不是一般的解決方案，但在適當的情況下允許 [*安全套件*](../secgloss/s-gly.md) 和應用程式的強式配對。</span><span class="sxs-lookup"><span data-stu-id="24006-261">This is not a generic solution, but it allows for a strong pairing of [*security package*](../secgloss/s-gly.md) and application when appropriate.</span></span>

<span data-ttu-id="24006-262">如果 \_ \_ 指定了 ISC 要求配置 \_ 記憶體，呼叫端必須藉由呼叫 [**FreeCoNtextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) 函式來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="24006-262">If ISC\_REQ\_ALLOCATE\_MEMORY was specified, the caller must free the memory by calling the [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) function.</span></span>

<span data-ttu-id="24006-263">例如，輸入權杖可能是 LAN Manager 的挑戰。</span><span class="sxs-lookup"><span data-stu-id="24006-263">For example, the input token could be the challenge from a LAN Manager.</span></span> <span data-ttu-id="24006-264">在此情況下，輸出權杖會是對挑戰的 NTLM 加密回應。</span><span class="sxs-lookup"><span data-stu-id="24006-264">In this case, the output token would be the NTLM-encrypted response to the challenge.</span></span>

<span data-ttu-id="24006-265">用戶端所採取的動作取決於此函式的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="24006-265">The action the client takes depends on the return code from this function.</span></span> <span data-ttu-id="24006-266">如果傳回碼為 SEC \_ E \_ OK，將不會有第二個 **InitializeSecurityCoNtext (協商)** 呼叫，且不會預期伺服器的回應。</span><span class="sxs-lookup"><span data-stu-id="24006-266">If the return code is SEC\_E\_OK, there will be no second **InitializeSecurityContext (Negotiate)** call, and no response from the server is expected.</span></span> <span data-ttu-id="24006-267">如果傳回碼是每秒 \_ \_ 繼續 \_ 需要的，則用戶端會預期權杖以回應伺服器，並在第二次呼叫中傳遞給 **InitializeSecurityCoNtext (Negotiate)**。</span><span class="sxs-lookup"><span data-stu-id="24006-267">If the return code is SEC\_I\_CONTINUE\_NEEDED, the client expects a token in response from the server and passes it in a second call to **InitializeSecurityContext (Negotiate)**.</span></span> <span data-ttu-id="24006-268">當 \_ 我 \_ 完成所需的傳回碼時， \_ 會指出用戶端必須完成建立訊息並呼叫 [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) 函數。</span><span class="sxs-lookup"><span data-stu-id="24006-268">The SEC\_I\_COMPLETE\_NEEDED return code indicates that the client must finish building the message and call the [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) function.</span></span> <span data-ttu-id="24006-269">當 \_ 我 \_ 完成並繼續程式碼時，會 \_ \_ 合併這兩個動作。</span><span class="sxs-lookup"><span data-stu-id="24006-269">The SEC\_I\_COMPLETE\_AND\_CONTINUE code incorporates both of these actions.</span></span>

<span data-ttu-id="24006-270">如果 **InitializeSecurityCoNtext (Negotiate)** 在第一個 (或只有) 呼叫傳回 success，則呼叫端最後必須在傳回的控制碼上呼叫 [**DeleteSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) 函式，即使在驗證交換的後續階段中呼叫失敗也是一樣。</span><span class="sxs-lookup"><span data-stu-id="24006-270">If **InitializeSecurityContext (Negotiate)** returns success on the first (or only) call, then the caller must eventually call the [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) function on the returned handle, even if the call fails on a later leg of the authentication exchange.</span></span>

<span data-ttu-id="24006-271">用戶端可能會在成功完成之後，再次呼叫 **InitializeSecurityCoNtext (協商)** 。</span><span class="sxs-lookup"><span data-stu-id="24006-271">The client may call **InitializeSecurityContext (Negotiate)** again after it has completed successfully.</span></span> <span data-ttu-id="24006-272">這會向 [*安全性封裝*](../secgloss/s-gly.md) 指出需要重新驗證。</span><span class="sxs-lookup"><span data-stu-id="24006-272">This indicates to the [*security package*](../secgloss/s-gly.md) that a reauthentication is wanted.</span></span>

<span data-ttu-id="24006-273">核心模式呼叫端有下列差異：目標名稱是必須使用 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)在虛擬記憶體中配置的 [*Unicode*](../secgloss/u-gly.md)字串;它不得從集區配置。</span><span class="sxs-lookup"><span data-stu-id="24006-273">Kernel mode callers have the following differences: the target name is a [*Unicode*](../secgloss/u-gly.md) string that must be allocated in virtual memory by using [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); it must not be allocated from the pool.</span></span> <span data-ttu-id="24006-274">*PInput* 和 *pOutput* 中傳遞和提供的緩衝區必須在虛擬記憶體中，而不是在集區中。</span><span class="sxs-lookup"><span data-stu-id="24006-274">Buffers passed and supplied in *pInput* and *pOutput* must be in virtual memory, not in the pool.</span></span>

## <a name="requirements"></a><span data-ttu-id="24006-275">規格需求</span><span class="sxs-lookup"><span data-stu-id="24006-275">Requirements</span></span>



| <span data-ttu-id="24006-276">需求</span><span class="sxs-lookup"><span data-stu-id="24006-276">Requirement</span></span> | <span data-ttu-id="24006-277">值</span><span class="sxs-lookup"><span data-stu-id="24006-277">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24006-278">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24006-278">Minimum supported client</span></span><br/> | <span data-ttu-id="24006-279">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24006-279">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="24006-280">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24006-280">Minimum supported server</span></span><br/> | <span data-ttu-id="24006-281">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24006-281">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="24006-282">標頭</span><span class="sxs-lookup"><span data-stu-id="24006-282">Header</span></span><br/>                   | <dl> <span data-ttu-id="24006-283"><dt>Sspi (包含 Security .h) </dt></span><span class="sxs-lookup"><span data-stu-id="24006-283"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="24006-284">程式庫</span><span class="sxs-lookup"><span data-stu-id="24006-284">Library</span></span><br/>                  | <dl> <span data-ttu-id="24006-285"><dt>Secur32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="24006-285"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="24006-286">DLL</span><span class="sxs-lookup"><span data-stu-id="24006-286">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24006-287"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24006-287"><dt>Secur32.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="24006-288">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24006-288">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24006-289">SSPI 函數</span><span class="sxs-lookup"><span data-stu-id="24006-289">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="24006-290">**AcceptSecurityCoNtext (Negotiate)**</span><span class="sxs-lookup"><span data-stu-id="24006-290">**AcceptSecurityContext (Negotiate)**</span></span>](acceptsecuritycontext--negotiate.md)
</dt> <dt>

[<span data-ttu-id="24006-291">**AcquireCredentialsHandle (Negotiate)**</span><span class="sxs-lookup"><span data-stu-id="24006-291">**AcquireCredentialsHandle (Negotiate)**</span></span>](acquirecredentialshandle--negotiate.md)
</dt> <dt>

[<span data-ttu-id="24006-292">**CompleteAuthToken**</span><span class="sxs-lookup"><span data-stu-id="24006-292">**CompleteAuthToken**</span></span>](/windows/win32/api/sspi/nf-sspi-completeauthtoken)
</dt> <dt>

[<span data-ttu-id="24006-293">**DeleteSecurityCoNtext**</span><span class="sxs-lookup"><span data-stu-id="24006-293">**DeleteSecurityContext**</span></span>](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[<span data-ttu-id="24006-294">**FreeCoNtextBuffer**</span><span class="sxs-lookup"><span data-stu-id="24006-294">**FreeContextBuffer**</span></span>](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[<span data-ttu-id="24006-295">**之 secbuffer**</span><span class="sxs-lookup"><span data-stu-id="24006-295">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[<span data-ttu-id="24006-296">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="24006-296">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
