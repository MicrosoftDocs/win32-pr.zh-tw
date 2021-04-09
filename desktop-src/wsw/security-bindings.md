---
title: 安全性系結
description: 安全性系結是安全性權杖的規格，可告知執行時間如何取得和使用安全性權杖來進行通道安全性。
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- 適用于 Windows 的安全性系結 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a263c1a79212f3438e77c3dca519f6493cf40e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104093519"
---
# <a name="security-bindings"></a><span data-ttu-id="29b11-106">安全性系結</span><span class="sxs-lookup"><span data-stu-id="29b11-106">Security Bindings</span></span>

<span data-ttu-id="29b11-107">安全性系結是安全性權杖的規格，可告知執行時間如何取得和使用安全性權杖來進行通道安全性。</span><span class="sxs-lookup"><span data-stu-id="29b11-107">A security binding is the specification of a security token, and tells the runtime how to obtain and use a security token for channel security.</span></span> <span data-ttu-id="29b11-108">安全性權杖包含的資訊可擔保存取資源的許可權。</span><span class="sxs-lookup"><span data-stu-id="29b11-108">The security token contains information that vouches for the right to access resources.</span></span> <span data-ttu-id="29b11-109">它可能也有相關聯的密碼編譯金鑰可執行簽章和加密。</span><span class="sxs-lookup"><span data-stu-id="29b11-109">It may also have an associated cryptographic key for performing signatures and encryption.</span></span>


<span data-ttu-id="29b11-110">每個安全性系結都包含它自己的選用安全性系結設定集合，其範圍 [設定](security-binding-settings.md) 為其所定義的安全性權杖。</span><span class="sxs-lookup"><span data-stu-id="29b11-110">Each security binding contains its own collection of optional [security binding settings](security-binding-settings.md) that are scoped to the security token it defines.</span></span> <span data-ttu-id="29b11-111">它也包含 [安全性認證](security-credentials.md)，代表安全性辨識項 (例如使用者名稱和密碼，或建立安全性權杖所需) 憑證。</span><span class="sxs-lookup"><span data-stu-id="29b11-111">It also contains [security credentials](security-credentials.md), representing the security evidence (such as username and passwords, or certificates) needed to create security tokens.</span></span>

<span data-ttu-id="29b11-112">下列回呼是安全性系結的一部分：</span><span class="sxs-lookup"><span data-stu-id="29b11-112">The following callbacks are part of the security binding:</span></span>

-   [<span data-ttu-id="29b11-113">**WS \_ 驗證 \_ SAML \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="29b11-113">**WS\_VALIDATE\_SAML\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

<span data-ttu-id="29b11-114">下列列舉是安全性系結的一部分：</span><span class="sxs-lookup"><span data-stu-id="29b11-114">The following enumerations are part of the security binding:</span></span>

-   [<span data-ttu-id="29b11-115">**WS \_ 訊息 \_ 安全性 \_ 使用方式**</span><span class="sxs-lookup"><span data-stu-id="29b11-115">**WS\_MESSAGE\_SECURITY\_USAGE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [<span data-ttu-id="29b11-116">**WS \_ SAML \_ 驗證器 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="29b11-116">**WS\_SAML\_AUTHENTICATOR\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [<span data-ttu-id="29b11-117">**WS \_ 安全性系結 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="29b11-117">**WS\_SECURITY\_BINDING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [<span data-ttu-id="29b11-118">**WS \_ 安全性 \_ 金鑰 \_ 控制碼 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="29b11-118">**WS\_SECURITY\_KEY\_HANDLE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

<span data-ttu-id="29b11-119">下列函數是安全性系結的一部分：</span><span class="sxs-lookup"><span data-stu-id="29b11-119">The following functions are part of the security binding:</span></span>

-   [<span data-ttu-id="29b11-120">**WsCreateXmlSecurityToken**</span><span class="sxs-lookup"><span data-stu-id="29b11-120">**WsCreateXmlSecurityToken**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [<span data-ttu-id="29b11-121">**WsFreeSecurityToken**</span><span class="sxs-lookup"><span data-stu-id="29b11-121">**WsFreeSecurityToken**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

<span data-ttu-id="29b11-122">下列結構是安全性系結的一部分：</span><span class="sxs-lookup"><span data-stu-id="29b11-122">The following structures are part of the security binding:</span></span>

-   [<span data-ttu-id="29b11-123">**WS \_ CAPI \_ 非對稱 \_ 安全性 \_ 金鑰 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="29b11-123">**WS\_CAPI\_ASYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [<span data-ttu-id="29b11-124">**WS \_ CERT \_ 簽署的 \_ SAML \_ 驗證器**</span><span class="sxs-lookup"><span data-stu-id="29b11-124">**WS\_CERT\_SIGNED\_SAML\_AUTHENTICATOR**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [<span data-ttu-id="29b11-125">**WS \_ HTTP \_ 標頭 \_ 驗證 \_ 安全性 \_ 系結**</span><span class="sxs-lookup"><span data-stu-id="29b11-125">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [<span data-ttu-id="29b11-126">**WS \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_ 系結**</span><span class="sxs-lookup"><span data-stu-id="29b11-126">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [<span data-ttu-id="29b11-127">**WS \_ NAMEDPIPE \_ SSPI \_ TRANSPORT \_ SECURITY \_ BINDING**</span><span class="sxs-lookup"><span data-stu-id="29b11-127">**WS\_NAMEDPIPE\_SSPI\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [<span data-ttu-id="29b11-128">**WS \_ NCRYPT \_ 非對稱 \_ 安全性 \_ 金鑰 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="29b11-128">**WS\_NCRYPT\_ASYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [<span data-ttu-id="29b11-129">**WS \_ RAW \_ 對稱 \_ 安全性 \_ 金鑰 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="29b11-129">**WS\_RAW\_SYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [<span data-ttu-id="29b11-130">**WS \_ SAML \_ 驗證器**</span><span class="sxs-lookup"><span data-stu-id="29b11-130">**WS\_SAML\_AUTHENTICATOR**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [<span data-ttu-id="29b11-131">**WS \_ SAML \_ MESSAGE \_ SECURITY \_ BINDING**</span><span class="sxs-lookup"><span data-stu-id="29b11-131">**WS\_SAML\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [<span data-ttu-id="29b11-132">**WS \_ 安全性系結 \_**</span><span class="sxs-lookup"><span data-stu-id="29b11-132">**WS\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [<span data-ttu-id="29b11-133">**WS \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性 \_ 系結**</span><span class="sxs-lookup"><span data-stu-id="29b11-133">**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [<span data-ttu-id="29b11-134">**WS \_ 安全性 \_ 金鑰 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="29b11-134">**WS\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [<span data-ttu-id="29b11-135">**WS \_ SSL \_ 傳輸 \_ 安全性 \_ 系結**</span><span class="sxs-lookup"><span data-stu-id="29b11-135">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [<span data-ttu-id="29b11-136">**WS \_ TCP \_ SSPI \_ 傳輸 \_ 安全性 \_ 系結**</span><span class="sxs-lookup"><span data-stu-id="29b11-136">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [<span data-ttu-id="29b11-137">**WS 使用者 \_ 名稱 \_ 訊息 \_ 安全性 \_ 系結**</span><span class="sxs-lookup"><span data-stu-id="29b11-137">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [<span data-ttu-id="29b11-138">**WS \_ XML \_ 權杖 \_ 訊息 \_ 安全性 \_ 系結**</span><span class="sxs-lookup"><span data-stu-id="29b11-138">**WS\_XML\_TOKEN\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




