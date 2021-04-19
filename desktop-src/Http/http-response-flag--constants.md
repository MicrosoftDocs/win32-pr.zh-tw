---
title: 'HTTP_RESPONSE_FLAG_ 常數 (Http.sys) '
description: 定義在 HTTP 伺服器 API 中設定回應的選項。
ms.assetid: bcb59457-fd22-4166-8a72-ba85209ec8c7
topic_type:
- apiref
api_name:
- HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96b7c34d453c1b9bbe45cf2c85ad268b414f3439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966918"
---
# <a name="http_response_flag_-constants"></a><span data-ttu-id="8ccb2-103">HTTP \_ 回應 \_ 旗標 \_ 常數</span><span class="sxs-lookup"><span data-stu-id="8ccb2-103">HTTP\_RESPONSE\_FLAG\_ Constants</span></span>

<span data-ttu-id="8ccb2-104">**Http \_ 回應 \_ 旗 \_** 標常數定義了在 HTTP 伺服器 API 中設定回應的選項。</span><span class="sxs-lookup"><span data-stu-id="8ccb2-104">The **HTTP\_RESPONSE\_FLAG\_** constants define options to configure responses in the HTTP Server API.</span></span>

<span data-ttu-id="8ccb2-105">這些常數會在 [**HTTP \_ 回應 \_ V1**](/windows/desktop/api/Http/ns-http-http_response_v1)結構的 **旗標** 成員中使用。</span><span class="sxs-lookup"><span data-stu-id="8ccb2-105">These constants are used in the **Flags** member of the [**HTTP\_RESPONSE\_V1**](/windows/desktop/api/Http/ns-http-http_response_v1) structure.</span></span>

<dl> <dt>

<span data-ttu-id="8ccb2-106"><span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**HTTP \_ 回應 \_ 旗 \_ 標 \_ 有多個可用的編碼 \_**</span><span class="sxs-lookup"><span data-stu-id="8ccb2-106"><span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**HTTP\_RESPONSE\_FLAG\_MULTIPLE\_ENCODINGS\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8ccb2-107">身分識別表單以外的編碼可用於此資源。</span><span class="sxs-lookup"><span data-stu-id="8ccb2-107">Encodings other than identity form are available for this resource.</span></span> <span data-ttu-id="8ccb2-108">如果應用程式未要求快取回應，則會忽略此旗標。</span><span class="sxs-lookup"><span data-stu-id="8ccb2-108">This flag is ignored if the application has not asked for the response to be cached.</span></span> <span data-ttu-id="8ccb2-109">從核心回應快取提供服務時，它會用來做為 HTTP 伺服器 API 的提示，以進行內容協商。</span><span class="sxs-lookup"><span data-stu-id="8ccb2-109">It's used as a hint to the HTTP Server API for content negotiation when serving from the kernel response cache.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ccb2-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ccb2-110">Requirements</span></span>



| <span data-ttu-id="8ccb2-111">需求</span><span class="sxs-lookup"><span data-stu-id="8ccb2-111">Requirement</span></span> | <span data-ttu-id="8ccb2-112">值</span><span class="sxs-lookup"><span data-stu-id="8ccb2-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8ccb2-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ccb2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="8ccb2-114">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ccb2-114">Windows 7 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8ccb2-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ccb2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="8ccb2-116">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ccb2-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8ccb2-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8ccb2-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ccb2-118"><dt>Http.sys</dt></span><span class="sxs-lookup"><span data-stu-id="8ccb2-118"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ccb2-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ccb2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ccb2-120">HTTP 伺服器 API 版本2.0 常數</span><span class="sxs-lookup"><span data-stu-id="8ccb2-120">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="8ccb2-121">**HTTP \_ 回應 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="8ccb2-121">**HTTP\_RESPONSE\_V1**</span></span>](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 





