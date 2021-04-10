---
title: Close-Session 的 Ack
description: 使用 Close-Session 封包的 Ack 來確認用戶端的 Close-Session 要求。 伺服器會在釋放與上傳會話相關聯的所有資源之後傳送通知。
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Close-Session BITS 的 Ack
topic_type:
- apiref
api_name:
- Ack for Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7142bfd8d1d5d65d1f669a328c75a2c8cdfb036
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104093491"
---
# <a name="ack-for-close-session"></a><span data-ttu-id="84cc3-105">Close-Session 的 Ack</span><span class="sxs-lookup"><span data-stu-id="84cc3-105">Ack for Close-Session</span></span>

<span data-ttu-id="84cc3-106">使用「通知」來確認用戶端的「[**關閉會話**](close-session.md)」要求，以 **取得接近會話** 封包。</span><span class="sxs-lookup"><span data-stu-id="84cc3-106">Use the **Ack for Close-Session** packet to acknowledge the client's [**Close-Session**](close-session.md) request.</span></span> <span data-ttu-id="84cc3-107">伺服器會在釋放與上傳會話相關聯的所有資源之後傳送通知。</span><span class="sxs-lookup"><span data-stu-id="84cc3-107">The server sends the acknowledgment after releasing all resources associated with the upload session.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="84cc3-108">標題</span><span class="sxs-lookup"><span data-stu-id="84cc3-108">Headers</span></span>

<dl> <dt>

<span data-ttu-id="84cc3-109"><span id="reason-code"></span><span id="REASON-CODE"></span>原因-代碼</span><span class="sxs-lookup"><span data-stu-id="84cc3-109"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="84cc3-110">以 HTTP 原因代碼取代 reason 碼。</span><span class="sxs-lookup"><span data-stu-id="84cc3-110">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="84cc3-111">例如，如果成功，請將 reason 碼設定為200。</span><span class="sxs-lookup"><span data-stu-id="84cc3-111">For example, set reason-code to 200 if success.</span></span> <span data-ttu-id="84cc3-112">如需 HTTP 原因代碼的清單，請參閱 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)。</span><span class="sxs-lookup"><span data-stu-id="84cc3-112">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="84cc3-113"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>原因-描述</span><span class="sxs-lookup"><span data-stu-id="84cc3-113"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="84cc3-114">以與原因代碼相關聯的 HTTP 描述取代 reason 描述。</span><span class="sxs-lookup"><span data-stu-id="84cc3-114">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="84cc3-115">例如，如果 reason-code 是200，請將 reason 描述設定為 OK。</span><span class="sxs-lookup"><span data-stu-id="84cc3-115">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="84cc3-116"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-封包類型</span><span class="sxs-lookup"><span data-stu-id="84cc3-116"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="84cc3-117">將此回應封包識別為 Ack 封包。</span><span class="sxs-lookup"><span data-stu-id="84cc3-117">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="84cc3-118"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>位-會話識別碼</span><span class="sxs-lookup"><span data-stu-id="84cc3-118"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="84cc3-119">識別用戶端會話的字串 GUID。</span><span class="sxs-lookup"><span data-stu-id="84cc3-119">String GUID that identifies the session to the client.</span></span> <span data-ttu-id="84cc3-120">將 {guid} 取代為用戶端在「 [**關閉會話**](close-session.md) 」要求封包中傳送的會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="84cc3-120">Replace {guid} with the session identifier that the client sent in the [**Close-Session**](close-session.md) request packet.</span></span> <span data-ttu-id="84cc3-121">如果您無法辨識會話識別碼，請將位-錯誤碼標頭設定為 [找不到 BG \_ E \_ 會話] \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="84cc3-121">If you do not recognize the session identifier, set the BITS-Error-Code header to BG\_E\_SESSION\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="84cc3-122"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>內容長度</span><span class="sxs-lookup"><span data-stu-id="84cc3-122"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="84cc3-123">以回應主體中包含的位元組數目取代長度。</span><span class="sxs-lookup"><span data-stu-id="84cc3-123">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="84cc3-124">即使回應本文不包含內容，也需要內容長度。</span><span class="sxs-lookup"><span data-stu-id="84cc3-124">Content-Length is required, even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="84cc3-125"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span><span class="sxs-lookup"><span data-stu-id="84cc3-125"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="84cc3-126">以代表與伺服器端錯誤相關之 HRESULT 值的十六進位數位取代錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="84cc3-126">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="84cc3-127">如果原因-代碼不是200或201，則只包含此標頭。</span><span class="sxs-lookup"><span data-stu-id="84cc3-127">Only include this header if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="84cc3-128"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-CoNtext</span><span class="sxs-lookup"><span data-stu-id="84cc3-128"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="84cc3-129">將錯誤內容取代為十六進位數位，代表發生錯誤的內容。</span><span class="sxs-lookup"><span data-stu-id="84cc3-129">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="84cc3-130">如果伺服器產生錯誤，請指定 [**BG \_ ERROR \_ CONTEXT \_ REMOTE \_ FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) 的十六進位數位 (0x5) 。</span><span class="sxs-lookup"><span data-stu-id="84cc3-130">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="84cc3-131">否則，請為 **BG \_ 錯誤 \_ 內容 \_ 遠端 \_ 應用程式** 指定十六進位數位 (0x7) 是否由傳遞上傳檔案的應用程式產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="84cc3-131">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="84cc3-132">只有當原因代碼不是200或201時，才包含此標頭。</span><span class="sxs-lookup"><span data-stu-id="84cc3-132">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84cc3-133">備註</span><span class="sxs-lookup"><span data-stu-id="84cc3-133">Remarks</span></span>

<span data-ttu-id="84cc3-134">如果原因代碼是在500到599的範圍內，則 BITS 用戶端會重新傳送 [**關閉會話**](close-session.md) 封包，除非找不到 BITS-錯誤碼標頭，且值為 BG \_ E \_ 會話找不到 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="84cc3-134">The BITS client resends the [**Close-Session**](close-session.md) packet if the reason-code is in the range 500 through 599, unless the BITS-Error-Code header is present with a value of BG\_E\_SESSION\_NOT\_FOUND.</span></span> <span data-ttu-id="84cc3-135">用戶端不會重試，原因代碼為100到499。</span><span class="sxs-lookup"><span data-stu-id="84cc3-135">The client will not retry for reason codes 100 through 499.</span></span>

## <a name="see-also"></a><span data-ttu-id="84cc3-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84cc3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84cc3-137">**Ack 以進行取消-會話**</span><span class="sxs-lookup"><span data-stu-id="84cc3-137">**Ack for Cancel-Session**</span></span>](ack-for-cancel-session.md)
</dt> <dt>

[<span data-ttu-id="84cc3-138">**關閉會話**</span><span class="sxs-lookup"><span data-stu-id="84cc3-138">**Close-Session**</span></span>](close-session.md)
</dt> </dl>

 

 




