---
title: Create-Session 的 Ack
description: 使用 Create-Session 封包的 Ack 來確認用戶端的 Create-Session 要求。
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Create-Session BITS 的 Ack
topic_type:
- apiref
api_name:
- Ack for Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d978ec4c5693a5087734975c412b999ed7d5890
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "106967933"
---
# <a name="ack-for-create-session"></a><span data-ttu-id="9d0a8-104">Create-Session 的 Ack</span><span class="sxs-lookup"><span data-stu-id="9d0a8-104">Ack for Create-Session</span></span>

<span data-ttu-id="9d0a8-105">使用 **建立會話** 封包的 Ack 來確認用戶端的 [**建立會話**](create-session.md) 要求。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-105">Use the **Ack for Create-Session** packet to acknowledge the client's [**Create-Session**](create-session.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Protocol: {guid}
BITS-Session-Id: {guid}
BITS-Host-Id: PublicHostName
BITS-Host-Id-Fallback-Timeout: Timeout
Accept-Encoding: Identity
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="9d0a8-106">標題</span><span class="sxs-lookup"><span data-stu-id="9d0a8-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="9d0a8-107"><span id="reason-code"></span><span id="REASON-CODE"></span>原因-代碼</span><span class="sxs-lookup"><span data-stu-id="9d0a8-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="9d0a8-108">以 HTTP 原因代碼取代 reason 碼。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-108">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="9d0a8-109">下表顯示回應 [**建立會話**](create-session.md) 要求的一般原因代碼。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-109">The following table shows the typical reason codes for a response to a [**Create-Session**](create-session.md) request.</span></span> <span data-ttu-id="9d0a8-110">如需 HTTP 原因代碼的清單，請參閱 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>



| <span data-ttu-id="9d0a8-111">原因代碼</span><span class="sxs-lookup"><span data-stu-id="9d0a8-111">Reason code</span></span>    | <span data-ttu-id="9d0a8-112">描述</span><span class="sxs-lookup"><span data-stu-id="9d0a8-112">Description</span></span>                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9d0a8-113">200</span><span class="sxs-lookup"><span data-stu-id="9d0a8-113">200</span></span><br/> | <span data-ttu-id="9d0a8-114">正常。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-114">OK.</span></span> <span data-ttu-id="9d0a8-115">要求成功。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-115">The request was successful.</span></span><br/>                                          |
| <span data-ttu-id="9d0a8-116">201</span><span class="sxs-lookup"><span data-stu-id="9d0a8-116">201</span></span><br/> | <span data-ttu-id="9d0a8-117">已建立。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-117">Created.</span></span> <span data-ttu-id="9d0a8-118">已建立會話。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-118">The session was created.</span></span><br/>                                        |
| <span data-ttu-id="9d0a8-119">403</span><span class="sxs-lookup"><span data-stu-id="9d0a8-119">403</span></span><br/> | <span data-ttu-id="9d0a8-120">禁止。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-120">Forbidden.</span></span> <span data-ttu-id="9d0a8-121">不允許使用者將檔案上傳至指定的 URL。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-121">The user is not allowed to upload files to the specified URL.</span></span><br/> |
| <span data-ttu-id="9d0a8-122">404</span><span class="sxs-lookup"><span data-stu-id="9d0a8-122">404</span></span><br/> | <span data-ttu-id="9d0a8-123">找不到。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-123">Not Found.</span></span> <span data-ttu-id="9d0a8-124">指定的 URL 不存在。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-124">The specified URL does not exist.</span></span><br/>                             |
| <span data-ttu-id="9d0a8-125">409</span><span class="sxs-lookup"><span data-stu-id="9d0a8-125">409</span></span><br/> | <span data-ttu-id="9d0a8-126">衝突。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-126">Conflict.</span></span> <span data-ttu-id="9d0a8-127">檔案存在於伺服器上，無法覆寫。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-127">The file exists on the server and cannot be overwritten.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="9d0a8-128"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>原因-描述</span><span class="sxs-lookup"><span data-stu-id="9d0a8-128"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="9d0a8-129">以與原因代碼相關聯的 HTTP 描述取代 reason 描述。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-129">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="9d0a8-130">例如，如果 reason-code 是200，請將 reason 描述設定為 OK。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-130">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="9d0a8-131"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-封包類型</span><span class="sxs-lookup"><span data-stu-id="9d0a8-131"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="9d0a8-132">將此回應封包識別為 Ack 封包。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-132">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="9d0a8-133"><span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-通訊協定</span><span class="sxs-lookup"><span data-stu-id="9d0a8-133"><span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-Protocol</span></span>
</dt> <dd>

<span data-ttu-id="9d0a8-134">字串 GUID，可識別伺服器要用於此會話的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-134">String GUID that identifies the protocol that the server wants to use for this session.</span></span> <span data-ttu-id="9d0a8-135">將 {guid} 取代為用戶端在 [**建立會話**](create-session.md) 要求中包含的通訊協定清單中的通訊協定識別碼;支援 BITS 的通訊協定標頭包含清單。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-135">Replace {guid} with the protocol identifier from the list of protocols the client includes in the [**Create-Session**](create-session.md) request; the BITS-Supported-Protocol header contains the list.</span></span> <span data-ttu-id="9d0a8-136">只有當原因代碼為200或201時，才包含此標頭。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-136">Include this header only if the reason-code is 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="9d0a8-137"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>位-會話識別碼</span><span class="sxs-lookup"><span data-stu-id="9d0a8-137"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="9d0a8-138">識別此會話給用戶端的字串 GUID。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-138">String GUID that identifies this session to the client.</span></span> <span data-ttu-id="9d0a8-139">將 {guid} 取代為用戶端在所有後續要求封包中傳送的會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-139">Replace {guid} with the session identifier that the client sends in all subsequent request packets.</span></span>

<span data-ttu-id="9d0a8-140">BITS 使用 GUID 來識別會話，但您可以使用最多100個字元的任何 HTTP 合法字串。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-140">BITS uses a GUID to identify the session, but you can use any HTTP-legal string up to 100 characters.</span></span>

</dd> <dt>

<span data-ttu-id="9d0a8-141"><span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-主機-識別碼</span><span class="sxs-lookup"><span data-stu-id="9d0a8-141"><span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-Host-Id</span></span>
</dt> <dd>

<span data-ttu-id="9d0a8-142">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-142">Optional.</span></span> <span data-ttu-id="9d0a8-143">只有在設定 [BITS IIS 延伸模組屬性](bits-iis-extension-properties.md)BITSHostId 時，才包含此標頭。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-143">Include this header only if the [BITS IIS extension property](bits-iis-extension-properties.md), BITSHostId, is set.</span></span> <span data-ttu-id="9d0a8-144">將 PublicHostName 取代為 BITSHostId 屬性中的伺服器名稱或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-144">Replace PublicHostName with the server name or IP address from the BITSHostId property.</span></span>

<span data-ttu-id="9d0a8-145">用戶端必須在所有後續的封包上取代遠端 URL 的伺服器部分。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-145">The client must replace the server portion of the remote-URL on all subsequent packets.</span></span> <span data-ttu-id="9d0a8-146">如果用戶端未在後續的封包上指定此主機名稱，則該作業可能會在伺服器陣列中的另一部伺服器上再次開始，而在先前的伺服器上留下部分上傳檔案。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-146">If the client does not specify this host name on subsequent packets, it is possible that the job will begin again on another server in the farm, leaving a partial upload file on the previous server.</span></span>

</dd> <dt>

<span data-ttu-id="9d0a8-147"><span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-主機-識別碼-回溯-Timeout</span><span class="sxs-lookup"><span data-stu-id="9d0a8-147"><span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-Host-Id-Fallback-Timeout</span></span>
</dt> <dd>

<span data-ttu-id="9d0a8-148">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-148">Optional.</span></span> <span data-ttu-id="9d0a8-149">只有在指定 BITS-主機識別碼標頭時，才包含此標頭。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-149">Include this header only if the BITS-Host-Id header is specified.</span></span> <span data-ttu-id="9d0a8-150">將 Timeout 取代為 BITSHostIdFallbackTimeout 屬性的超時值。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-150">Replace Timeout with the time-out value from the BITSHostIdFallbackTimeout property.</span></span> <span data-ttu-id="9d0a8-151">BITSHostIdFallbackTimeout 屬性是其中一個 [BITS IIS 延伸模組屬性](bits-iis-extension-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-151">The BITSHostIdFallbackTimeout property is one of the [BITS IIS extension properties](bits-iis-extension-properties.md).</span></span>

<span data-ttu-id="9d0a8-152">用戶端會使用超時時間來判斷在還原為作業的遠端檔案名中指定的主機名稱之前，嘗試重新連線到位主機識別碼標頭中所指定伺服器名稱的時間長度。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-152">The client uses the time-out period to determine how long it tries to reconnect to the server name specified in the BITS-Host-Id header before reverting to the host name specified in the remote file name of the job.</span></span> <span data-ttu-id="9d0a8-153">當 BITS 無法連線到 BITS 主機識別碼伺服器時，就會開始計時器。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-153">The timer begins when BITS is unable to connect to the BITS-Host-Id server.</span></span> <span data-ttu-id="9d0a8-154">當還原伺服器的連接時，就會重設計時器。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-154">The timer is reset when a connection to the server is restored.</span></span> <span data-ttu-id="9d0a8-155">如果未指定超時期間，用戶端永遠不會還原為遠端檔案名中指定的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-155">If a time-out period is not specified, the client never reverts to the host name specified in the remote file name.</span></span>

</dd> <dt>

<span data-ttu-id="9d0a8-156"><span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>接受編碼</span><span class="sxs-lookup"><span data-stu-id="9d0a8-156"><span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accept-Encoding</span></span>
</dt> <dd>

<span data-ttu-id="9d0a8-157">識別要在傳送至伺服器的片段上使用的編碼配置。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-157">Identifies the encoding scheme to use on the fragments sent to the server.</span></span> <span data-ttu-id="9d0a8-158">片段封包會在封包主體中包含編碼的片段。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-158">The Fragment packet contains the encoded fragment in the body of the packet.</span></span> <span data-ttu-id="9d0a8-159">BITS 伺服器需要 (純文字) 的身分識別編碼。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-159">The BITS server requires Identity encoding (plaintext).</span></span> <span data-ttu-id="9d0a8-160">只有當原因代碼為200或201時，才包含此標頭。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-160">Include this header only if the Reason-code is 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="9d0a8-161"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>內容長度</span><span class="sxs-lookup"><span data-stu-id="9d0a8-161"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="9d0a8-162">以回應主體中包含的位元組數目取代長度。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-162">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="9d0a8-163">即使回應本文不包含內容，也是必要項。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-163">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="9d0a8-164"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span><span class="sxs-lookup"><span data-stu-id="9d0a8-164"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="9d0a8-165">以代表與伺服器端錯誤相關之 HRESULT 值的十六進位數位取代錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-165">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="9d0a8-166">只有在原因-程式碼不是200或201時，才包含此標頭。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-166">Include this header only if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="9d0a8-167"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-CoNtext</span><span class="sxs-lookup"><span data-stu-id="9d0a8-167"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="9d0a8-168">將錯誤內容取代為十六進位數位，代表發生錯誤的內容。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-168">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="9d0a8-169">如果伺服器產生錯誤，請指定 [**BG \_ ERROR \_ CONTEXT \_ REMOTE \_ FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) 的十六進位數位 (0x5) 。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-169">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="9d0a8-170">否則，請為 **BG \_ 錯誤 \_ 內容 \_ 遠端 \_ 應用程式** 指定十六進位數位 (0x7) 是否由傳遞上傳檔案的應用程式產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-170">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="9d0a8-171">只有當原因代碼不是200或201時，才包含此標頭。</span><span class="sxs-lookup"><span data-stu-id="9d0a8-171">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="9d0a8-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d0a8-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d0a8-173">**建立-會話**</span><span class="sxs-lookup"><span data-stu-id="9d0a8-173">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 





