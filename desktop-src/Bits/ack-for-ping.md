---
title: Ping 的 Ack
description: 使用 Ping 封包的 Ack 來確認用戶端的 Ping 要求。
ms.assetid: 2e288564-d06f-4b45-b0c0-7aab1897da40
keywords:
- Ping 位的 Ack
topic_type:
- apiref
api_name:
- Ack for Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a3ca765c8bd7758f19abe396ad0449a5895d8e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "103933704"
---
# <a name="ack-for-ping"></a><span data-ttu-id="f0bd7-104">Ping 的 Ack</span><span class="sxs-lookup"><span data-stu-id="f0bd7-104">Ack for Ping</span></span>

<span data-ttu-id="f0bd7-105">使用 Ping 封包的 **Ack** 來確認用戶端的 [**ping**](ping.md) 要求。</span><span class="sxs-lookup"><span data-stu-id="f0bd7-105">Use the **Ack for Ping** packet to acknowledge the client's [**Ping**](ping.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="f0bd7-106">標題</span><span class="sxs-lookup"><span data-stu-id="f0bd7-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="f0bd7-107"><span id="reason-code"></span><span id="REASON-CODE"></span>原因-代碼</span><span class="sxs-lookup"><span data-stu-id="f0bd7-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-108">以 HTTP 原因代碼取代 reason 碼。</span><span class="sxs-lookup"><span data-stu-id="f0bd7-108">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="f0bd7-109">例如，如果成功，請將 reason 碼設定為200。</span><span class="sxs-lookup"><span data-stu-id="f0bd7-109">For example, set reason-code to 200 if success.</span></span> <span data-ttu-id="f0bd7-110">如需 HTTP 原因代碼的清單，請參閱 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)。</span><span class="sxs-lookup"><span data-stu-id="f0bd7-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-111"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>原因-描述</span><span class="sxs-lookup"><span data-stu-id="f0bd7-111"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-112">以與原因代碼相關聯的 HTTP 描述取代 reason 描述。</span><span class="sxs-lookup"><span data-stu-id="f0bd7-112">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="f0bd7-113">例如，如果 reason-code 是200，請將 reason 描述設定為 OK。</span><span class="sxs-lookup"><span data-stu-id="f0bd7-113">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-114"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-封包類型</span><span class="sxs-lookup"><span data-stu-id="f0bd7-114"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-115">將此回應封包識別為 Ack 封包。</span><span class="sxs-lookup"><span data-stu-id="f0bd7-115">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-116"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>內容長度</span><span class="sxs-lookup"><span data-stu-id="f0bd7-116"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-117">以回應主體中包含的位元組數目取代長度。</span><span class="sxs-lookup"><span data-stu-id="f0bd7-117">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="f0bd7-118">即使回應本文不包含內容，也是必要項。</span><span class="sxs-lookup"><span data-stu-id="f0bd7-118">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-119"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span><span class="sxs-lookup"><span data-stu-id="f0bd7-119"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-120">以代表與伺服器端錯誤相關之 HRESULT 值的十六進位數位取代錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f0bd7-120">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="f0bd7-121">只有在原因-程式碼不是200或201時，才包含此標頭。</span><span class="sxs-lookup"><span data-stu-id="f0bd7-121">Include this header only if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-122"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-CoNtext</span><span class="sxs-lookup"><span data-stu-id="f0bd7-122"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-123">將錯誤內容取代為十六進位數位，代表發生錯誤的內容。</span><span class="sxs-lookup"><span data-stu-id="f0bd7-123">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="f0bd7-124">如果伺服器產生錯誤，請指定 [**BG \_ ERROR \_ CONTEXT \_ REMOTE \_ FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) 的十六進位數位 (0x5) 。</span><span class="sxs-lookup"><span data-stu-id="f0bd7-124">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="f0bd7-125">否則，請為 **BG \_ 錯誤 \_ 內容 \_ 遠端 \_ 應用程式** 指定十六進位數位 (0x7) 是否由傳遞上傳檔案的應用程式產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="f0bd7-125">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="f0bd7-126">只有當原因代碼不是200或201時，才包含此標頭。</span><span class="sxs-lookup"><span data-stu-id="f0bd7-126">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="f0bd7-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0bd7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0bd7-128">**坪**</span><span class="sxs-lookup"><span data-stu-id="f0bd7-128">**Ping**</span></span>](ping.md)
</dt> </dl>

 

 




