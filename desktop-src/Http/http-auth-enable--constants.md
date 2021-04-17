---
title: 'HTTP_AUTH_ENABLE_ 常數 (Http.sys) '
description: 定義可以在 URL 群組上啟用的驗證配置。
ms.assetid: db22645f-c9e4-427e-b3d5-91d568aec7c5
topic_type:
- apiref
api_name:
- HTTP_AUTH_ENABLE_BASIC
- HTTP_AUTH_ENABLE_DIGEST
- HTTP_AUTH_ENABLE_KERBEROS
- HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING
- HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL
- HTTP_AUTH_ENABLE_NTLM
- HTTP_AUTH_ENABLE_NEGOTIATE
- HTTP_AUTH_ENABLE_ALL
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6462a4f9d884244f460c4bf7714b45d3e17600c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466789"
---
# <a name="http_auth_enable_-constants"></a><span data-ttu-id="acc9c-103">HTTP \_ 驗證 \_ 啟用 \_ 常數</span><span class="sxs-lookup"><span data-stu-id="acc9c-103">HTTP\_AUTH\_ENABLE\_ Constants</span></span>

<span data-ttu-id="acc9c-104">**HTTP \_ AUTH \_ ENABLE** 常數定義可以在 URL 群組上啟用的驗證配置。</span><span class="sxs-lookup"><span data-stu-id="acc9c-104">The **HTTP\_AUTH\_ENABLE** constants define authentication schemes that can be enabled on a URL Group.</span></span>

<span data-ttu-id="acc9c-105">這些常數會用於 [**HTTP \_ 伺服器 \_ 驗證 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) 結構中。</span><span class="sxs-lookup"><span data-stu-id="acc9c-105">These constants are used in the [**HTTP\_SERVER\_AUTHENTICATION\_INFO**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="acc9c-106"><span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**HTTP \_ AUTH \_ ENABLE \_ BASIC**</span><span class="sxs-lookup"><span data-stu-id="acc9c-106"><span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**HTTP\_AUTH\_ENABLE\_BASIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="acc9c-107">已啟用基本驗證配置。</span><span class="sxs-lookup"><span data-stu-id="acc9c-107">The Basic authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="acc9c-108"><span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**HTTP \_ 驗證 \_ 啟用 \_ 摘要**</span><span class="sxs-lookup"><span data-stu-id="acc9c-108"><span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**HTTP\_AUTH\_ENABLE\_DIGEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="acc9c-109">摘要式驗證配置已啟用。</span><span class="sxs-lookup"><span data-stu-id="acc9c-109">The Digest authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="acc9c-110"><span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**HTTP \_ 驗證 \_ 啟用 \_ KERBEROS**</span><span class="sxs-lookup"><span data-stu-id="acc9c-110"><span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**HTTP\_AUTH\_ENABLE\_KERBEROS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="acc9c-111">Kerberos 驗證配置已啟用。</span><span class="sxs-lookup"><span data-stu-id="acc9c-111">The Kerberos authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="acc9c-112"><span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**HTTP \_ 驗證（ \_ 例如旗標） \_ \_ 啟用 \_ KERBEROS \_ 認證 \_ 快取**</span><span class="sxs-lookup"><span data-stu-id="acc9c-112"><span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**HTTP\_AUTH\_EX\_FLAG\_ENABLE\_KERBEROS\_CREDENTIAL\_CACHING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="acc9c-113">Kerberos 認證快取已啟用。</span><span class="sxs-lookup"><span data-stu-id="acc9c-113">Kerberos credential caching is enabled.</span></span>

<span data-ttu-id="acc9c-114">**Windows Server 2003 與之前：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="acc9c-114">**Windows Server 2003 and before:** Not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="acc9c-115"><span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**HTTP \_ 驗證（ \_ 例如 \_ 旗標 \_ 捕捉 \_ 認證）**</span><span class="sxs-lookup"><span data-stu-id="acc9c-115"><span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**HTTP\_AUTH\_EX\_FLAG\_CAPTURE\_CREDENTIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="acc9c-116">HTTP 伺服器 API 會捕捉呼叫端身分識別，並只將其用於協商和 Kerberos 配置的驗證。</span><span class="sxs-lookup"><span data-stu-id="acc9c-116">The HTTP Server API captures the caller identity and uses it for authentication for Negotiate and Kerberos schemes only.</span></span>

<span data-ttu-id="acc9c-117">**Windows Server 2003 與之前：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="acc9c-117">**Windows Server 2003 and before:** Not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="acc9c-118"><span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**HTTP \_ AUTH \_ 啟用 \_ NTLM**</span><span class="sxs-lookup"><span data-stu-id="acc9c-118"><span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**HTTP\_AUTH\_ENABLE\_NTLM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="acc9c-119">已啟用 NTLM 驗證配置。</span><span class="sxs-lookup"><span data-stu-id="acc9c-119">The NTLM authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="acc9c-120"><span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**HTTP \_ AUTH \_ ENABLE \_ NEGOTIATE**</span><span class="sxs-lookup"><span data-stu-id="acc9c-120"><span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**HTTP\_AUTH\_ENABLE\_NEGOTIATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="acc9c-121">已啟用 Negotiate 驗證配置。</span><span class="sxs-lookup"><span data-stu-id="acc9c-121">The Negotiate authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="acc9c-122"><span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**HTTP \_ AUTH \_ \_ 全部啟用**</span><span class="sxs-lookup"><span data-stu-id="acc9c-122"><span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**HTTP\_AUTH\_ENABLE\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="acc9c-123">所有驗證配置都會啟用。</span><span class="sxs-lookup"><span data-stu-id="acc9c-123">All authentication schemes are enabled.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="acc9c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="acc9c-124">Requirements</span></span>



| <span data-ttu-id="acc9c-125">需求</span><span class="sxs-lookup"><span data-stu-id="acc9c-125">Requirement</span></span> | <span data-ttu-id="acc9c-126">值</span><span class="sxs-lookup"><span data-stu-id="acc9c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="acc9c-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="acc9c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="acc9c-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acc9c-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="acc9c-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="acc9c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="acc9c-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acc9c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="acc9c-131">標頭</span><span class="sxs-lookup"><span data-stu-id="acc9c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="acc9c-132"><dt>Http.sys</dt></span><span class="sxs-lookup"><span data-stu-id="acc9c-132"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acc9c-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="acc9c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acc9c-134">HTTP 伺服器 API 版本2.0 常數</span><span class="sxs-lookup"><span data-stu-id="acc9c-134">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="acc9c-135">**HTTP \_ 伺服器 \_ 驗證 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="acc9c-135">**HTTP\_SERVER\_AUTHENTICATION\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
</dt> <dt>

[<span data-ttu-id="acc9c-136">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="acc9c-136">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="acc9c-137">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="acc9c-137">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="acc9c-138">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="acc9c-138">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="acc9c-139">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="acc9c-139">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





