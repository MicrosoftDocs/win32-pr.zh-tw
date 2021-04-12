---
title: 'HTTP_RESPONSE (Http.sys) '
description: HTTP 回應結構的版本 \_ 取決於所使用的要求佇列版本，如下所示： Http SERVER API 1.0 版要求佇列，這是 HTTP \_ 要求 V1 的 \_ 結構。HTTP 伺服器 API 2.0 版要求佇列這是 HTTP \_ 要求 \_ V2 結構。
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8445021aa61b94ae83a55937b1db5ca4e3c577
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384398"
---
# <a name="http_response"></a><span data-ttu-id="abc3a-106">HTTP \_ 回應</span><span class="sxs-lookup"><span data-stu-id="abc3a-106">HTTP\_RESPONSE</span></span>

<span data-ttu-id="abc3a-107">**HTTP \_ 回應** 結構的版本取決於所使用的要求佇列版本，如下所示：</span><span class="sxs-lookup"><span data-stu-id="abc3a-107">The version of the **HTTP\_RESPONSE** structure is dependent on the version of the request queue used as follows:</span></span>

-   <span data-ttu-id="abc3a-108">HTTP 伺服器 API 1.0 版要求佇列：這是 [**HTTP \_ 要求 \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) 結構。</span><span class="sxs-lookup"><span data-stu-id="abc3a-108">HTTP Server API Version 1.0 request queue: This is an [**HTTP\_REQUEST\_V1**](/windows/desktop/api/Http/ns-http-http_request_v1) structure.</span></span>
-   <span data-ttu-id="abc3a-109">HTTP 伺服器 API 2.0 版要求佇列：這是 [**HTTP \_ 要求 \_ V2**](/windows/desktop/api/Http/ns-http-http_request_v2) 結構。</span><span class="sxs-lookup"><span data-stu-id="abc3a-109">HTTP Server API Version 2.0 request queue: This is an [**HTTP\_REQUEST\_V2**](/windows/desktop/api/Http/ns-http-http_request_v2) structure.</span></span>

<span data-ttu-id="abc3a-110">請勿直接在您的程式碼中使用 [**HTTP \_ 要求 \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) 和 [**HTTP \_ 要求 \_ V2**](/windows/desktop/api/Http/ns-http-http_request_v2) ，改為使用 **HTTP \_ 回應** ，根據要求佇列的版本，確保使用正確的結構版本。</span><span class="sxs-lookup"><span data-stu-id="abc3a-110">Do not use [**HTTP\_REQUEST\_V1**](/windows/desktop/api/Http/ns-http-http_request_v1) and [**HTTP\_REQUEST\_V2**](/windows/desktop/api/Http/ns-http-http_request_v2) directly in your code; using **HTTP\_RESPONSE** instead ensures the proper version of the structure is used based on the version of the request queue.</span></span>


```C++
typedef HTTP_REQUEST_V1 HTTP_RESPONSE;
typedef HTTP_REQUEST_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

<span data-ttu-id="abc3a-111">**HTTP \_ 回應**</span><span class="sxs-lookup"><span data-stu-id="abc3a-111">**HTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="abc3a-112">來自 v1 要求佇列的要求。</span><span class="sxs-lookup"><span data-stu-id="abc3a-112">Request was from a v1 request queue.</span></span>

</dd> <dt>

<span data-ttu-id="abc3a-113">**HTTP \_ 回應**</span><span class="sxs-lookup"><span data-stu-id="abc3a-113">**HTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="abc3a-114">來自 v2 要求佇列的要求。</span><span class="sxs-lookup"><span data-stu-id="abc3a-114">Request was from a v2 request queue.</span></span>

</dd> <dt>

<span data-ttu-id="abc3a-115">**PHTTP \_ 回應**</span><span class="sxs-lookup"><span data-stu-id="abc3a-115">**PHTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="abc3a-116">**HTTP \_ 回應** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="abc3a-116">Pointer to an **HTTP\_RESPONSE** structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abc3a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="abc3a-117">Requirements</span></span>



| <span data-ttu-id="abc3a-118">需求</span><span class="sxs-lookup"><span data-stu-id="abc3a-118">Requirement</span></span> | <span data-ttu-id="abc3a-119">值</span><span class="sxs-lookup"><span data-stu-id="abc3a-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="abc3a-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="abc3a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="abc3a-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="abc3a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="abc3a-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="abc3a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="abc3a-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="abc3a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="abc3a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="abc3a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="abc3a-125"><dt>Http.sys</dt></span><span class="sxs-lookup"><span data-stu-id="abc3a-125"><dt>Http.h</dt></span></span> </dl> |



 

 





