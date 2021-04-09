---
title: 適用于片段的 Ack
description: 使用片段封包的 Ack 來確認用戶端的片段要求。
ms.assetid: f5466489-2d5e-4850-a39c-37bc4923a7ac
keywords:
- 片段位的 Ack
topic_type:
- apiref
api_name:
- Ack for Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef28381313ce00fd6089ebf845ed342ccae455c7
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "103933705"
---
# <a name="ack-for-fragment"></a><span data-ttu-id="2804f-104">適用于片段的 Ack</span><span class="sxs-lookup"><span data-stu-id="2804f-104">Ack for Fragment</span></span>

<span data-ttu-id="2804f-105">使用片段封包的 **Ack** 來確認用戶端的 [**片段**](fragment.md) 要求。</span><span class="sxs-lookup"><span data-stu-id="2804f-105">Use the **Ack for Fragment** packet to acknowledge the client's [**Fragment**](fragment.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
BITS-Received-Content-Range: range
BITS-Reply-URL: url
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="2804f-106">標題</span><span class="sxs-lookup"><span data-stu-id="2804f-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="2804f-107"><span id="reason-code"></span><span id="REASON-CODE"></span>原因-代碼</span><span class="sxs-lookup"><span data-stu-id="2804f-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="2804f-108">以 HTTP 原因代碼取代 reason 碼。</span><span class="sxs-lookup"><span data-stu-id="2804f-108">Replace reason-code with an HTTP reason code.</span></span> <span data-ttu-id="2804f-109">下錶針對 [**片段**](fragment.md) 要求的回應，顯示一般的原因代碼。</span><span class="sxs-lookup"><span data-stu-id="2804f-109">The following table shows the typical reason codes for a response to a [**Fragment**](fragment.md) request.</span></span> <span data-ttu-id="2804f-110">如需 HTTP 原因代碼的清單，請參閱 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)。</span><span class="sxs-lookup"><span data-stu-id="2804f-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>



| <span data-ttu-id="2804f-111">原因代碼</span><span class="sxs-lookup"><span data-stu-id="2804f-111">Reason code</span></span>    | <span data-ttu-id="2804f-112">描述</span><span class="sxs-lookup"><span data-stu-id="2804f-112">Description</span></span>                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2804f-113">200</span><span class="sxs-lookup"><span data-stu-id="2804f-113">200</span></span><br/> | <span data-ttu-id="2804f-114">正常。</span><span class="sxs-lookup"><span data-stu-id="2804f-114">OK.</span></span> <span data-ttu-id="2804f-115">要求成功。</span><span class="sxs-lookup"><span data-stu-id="2804f-115">The request was successful.</span></span><br/>                                                                             |
| <span data-ttu-id="2804f-116">416</span><span class="sxs-lookup"><span data-stu-id="2804f-116">416</span></span><br/> | <span data-ttu-id="2804f-117">範圍-不] 正確。</span><span class="sxs-lookup"><span data-stu-id="2804f-117">Range-Not-Satisfiable.</span></span> <span data-ttu-id="2804f-118">用戶端傳送的片段的範圍與上一個片段不連續。</span><span class="sxs-lookup"><span data-stu-id="2804f-118">The client sent a fragment whose range is not contiguous with the previous fragment.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2804f-119"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>原因-描述</span><span class="sxs-lookup"><span data-stu-id="2804f-119"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="2804f-120">以與原因代碼相關聯的 HTTP 描述取代 reason 描述。</span><span class="sxs-lookup"><span data-stu-id="2804f-120">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="2804f-121">例如，如果 reason-code 是200，請將 reason 描述設定為 OK。</span><span class="sxs-lookup"><span data-stu-id="2804f-121">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="2804f-122"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-封包類型</span><span class="sxs-lookup"><span data-stu-id="2804f-122"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="2804f-123">將此回應封包識別為 Ack 封包。</span><span class="sxs-lookup"><span data-stu-id="2804f-123">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="2804f-124"><span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>位-已接收-內容約制</span><span class="sxs-lookup"><span data-stu-id="2804f-124"><span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-Received-Content-Range</span></span>
</dt> <dd>

<span data-ttu-id="2804f-125">伺服器預期用戶端傳送的下一個位元組以零為基底的位移。</span><span class="sxs-lookup"><span data-stu-id="2804f-125">Zero-based offset to the next byte the server expects the client to send.</span></span> <span data-ttu-id="2804f-126">例如，如果片段包含範圍 128 212，則會將範圍設定為213。</span><span class="sxs-lookup"><span data-stu-id="2804f-126">For example, if the fragment contained the range 128 212, you would set range to 213.</span></span>

</dd> <dt>

<span data-ttu-id="2804f-127"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>位-會話識別碼</span><span class="sxs-lookup"><span data-stu-id="2804f-127"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="2804f-128">識別用戶端會話的字串 GUID。</span><span class="sxs-lookup"><span data-stu-id="2804f-128">String GUID that identifies the session to the client.</span></span> <span data-ttu-id="2804f-129">將 {guid} 取代為用戶端在 [**片段**](fragment.md) 要求封包中傳送的會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="2804f-129">Replace {guid} with the session identifier that the client sent in the [**Fragment**](fragment.md) request packet.</span></span> <span data-ttu-id="2804f-130">如果您無法辨識會話識別碼，請將位-錯誤碼標頭設定為 [找不到 BG \_ E \_ 會話] \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="2804f-130">If you do not recognize the session identifier, set the BITS-Error-Code header to BG\_E\_SESSION\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="2804f-131"><span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>位-回復-URL</span><span class="sxs-lookup"><span data-stu-id="2804f-131"><span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-Reply-URL</span></span>
</dt> <dd>

<span data-ttu-id="2804f-132">包含上傳-回復作業之回復資料的 URL。</span><span class="sxs-lookup"><span data-stu-id="2804f-132">Contains the URL to the reply data of an upload-reply job.</span></span> <span data-ttu-id="2804f-133">上傳完成之後，在最終片段回應中包含此標頭，而且您會收到來自伺服器應用程式的回應（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="2804f-133">Include this header in the final fragment response after the upload is complete and you receive a response from the server application, if applicable.</span></span>

<span data-ttu-id="2804f-134">使用片段要求中的內容約制標頭來判斷上傳是否完成。</span><span class="sxs-lookup"><span data-stu-id="2804f-134">Use the Content-Range header from the Fragment request to determine whether the upload is complete.</span></span> <span data-ttu-id="2804f-135">如果範圍值的結束位移等於總計長度值減一，則上傳已完成。</span><span class="sxs-lookup"><span data-stu-id="2804f-135">The upload is complete if the end offset of the range value equals the total-length value minus one.</span></span>

<span data-ttu-id="2804f-136">BITS 伺服器會在判斷上傳完成之後，將上傳檔案張貼至伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="2804f-136">The BITS server posts the upload file to the server application after it determines the upload is complete.</span></span> <span data-ttu-id="2804f-137">伺服器應用程式會處理檔案並產生回復。</span><span class="sxs-lookup"><span data-stu-id="2804f-137">The server application processes the file and generates the reply.</span></span> <span data-ttu-id="2804f-138">BITS 伺服器會將位-回復 URL 的值，從伺服器應用程式設定為回復檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="2804f-138">The BITS server sets the value of BITS-Reply-URL to the URL of the reply file from the server application.</span></span>

</dd> <dt>

<span data-ttu-id="2804f-139"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>內容長度</span><span class="sxs-lookup"><span data-stu-id="2804f-139"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="2804f-140">以回應主體中包含的位元組數目取代長度。</span><span class="sxs-lookup"><span data-stu-id="2804f-140">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="2804f-141">即使回應本文不包含內容，也需要內容長度。</span><span class="sxs-lookup"><span data-stu-id="2804f-141">Content-Length is required, even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="2804f-142"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span><span class="sxs-lookup"><span data-stu-id="2804f-142"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="2804f-143">以代表與伺服器端錯誤相關之 HRESULT 值的十六進位數位取代錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2804f-143">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="2804f-144">如果原因-代碼不是200或201，則只包含此標頭。</span><span class="sxs-lookup"><span data-stu-id="2804f-144">Only include this header if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="2804f-145"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-CoNtext</span><span class="sxs-lookup"><span data-stu-id="2804f-145"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="2804f-146">將錯誤內容取代為十六進位數位，代表發生錯誤的內容。</span><span class="sxs-lookup"><span data-stu-id="2804f-146">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="2804f-147">如果伺服器產生錯誤，請指定 [**BG \_ ERROR \_ CONTEXT \_ REMOTE \_ FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) 的十六進位數位 (0x5) 。</span><span class="sxs-lookup"><span data-stu-id="2804f-147">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="2804f-148">否則，請為 **BG \_ 錯誤 \_ 內容 \_ 遠端 \_ 應用程式** 指定十六進位數位 (0x7) 是否由傳遞上傳檔案的應用程式產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="2804f-148">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="2804f-149">只有當原因代碼不是200或201時，才包含此標頭。</span><span class="sxs-lookup"><span data-stu-id="2804f-149">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2804f-150">備註</span><span class="sxs-lookup"><span data-stu-id="2804f-150">Remarks</span></span>

<span data-ttu-id="2804f-151">如果會話適用于上傳-回復作業，則可能會在用戶端收到片段回應的最終 **認可** 之前發生延遲。</span><span class="sxs-lookup"><span data-stu-id="2804f-151">If the session is for an upload-reply job, there may be a delay before the client receives the final **Ack for Fragment** response.</span></span> <span data-ttu-id="2804f-152">延遲的長度取決於伺服器應用程式 (應用程式用來將上傳檔案張貼) 用來產生回復的時間量。</span><span class="sxs-lookup"><span data-stu-id="2804f-152">The length of the delay depends on the amount of time the server application (application to which the server posts the upload file) takes to generate the reply.</span></span>

## <a name="see-also"></a><span data-ttu-id="2804f-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2804f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2804f-154">**建立-會話**</span><span class="sxs-lookup"><span data-stu-id="2804f-154">**Create-Session**</span></span>](create-session.md)
</dt> <dt>

[<span data-ttu-id="2804f-155">**片段**</span><span class="sxs-lookup"><span data-stu-id="2804f-155">**Fragment**</span></span>](fragment.md)
</dt> </dl>

 

 





