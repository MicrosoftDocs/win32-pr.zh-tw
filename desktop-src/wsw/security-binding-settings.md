---
title: 安全性繫結設定
description: 安全性系結設定可控制取得或使用安全性權杖的方式。
ms.assetid: 4bc03cb4-1ac2-4ad1-a45d-eae8f50f5355
keywords:
- 適用于 Windows 的安全性系結設定 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5a3d27627c3360560a38ef9cb85e3fb5ece434
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103684239"
---
# <a name="security-binding-settings"></a><span data-ttu-id="a2ade-106">安全性繫結設定</span><span class="sxs-lookup"><span data-stu-id="a2ade-106">Security Binding Settings</span></span>

<span data-ttu-id="a2ade-107">安全性系結設定可控制取得或使用安全性權杖的方式。</span><span class="sxs-lookup"><span data-stu-id="a2ade-107">Security binding settings control the way a security token is obtained or used.</span></span> <span data-ttu-id="a2ade-108">它們會表示為屬性值組的集合，以及由列舉 [**WS 安全性系結 \_ \_ \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property)定義的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a2ade-108">They are represented as a collection of property-value pairs, with the property keys defined by the enumeration [**WS\_SECURITY\_BINDING\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property).</span></span> <span data-ttu-id="a2ade-109">集合中的每個屬性都有合理的預設值。</span><span class="sxs-lookup"><span data-stu-id="a2ade-109">Each property in the collection has a reasonable default value.</span></span> <span data-ttu-id="a2ade-110">因此，您可以定義和使用安全性描述，而不需要指定任何安全性系結設定。</span><span class="sxs-lookup"><span data-stu-id="a2ade-110">As a result, it is possible to define and use a security description without specifying any of the security binding settings.</span></span>


<span data-ttu-id="a2ade-111">如需全通道安全性設定的詳細資訊，以及其索引鍵是由 [**WS \_ 安全性 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) 列舉所定義的屬性，請參閱 [安全性通道設定](security-channel-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="a2ade-111">For information on channel-wide security settings, with properties whose keys are defined by the [**WS\_SECURITY\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) enumeration, see[Security Channel Settings](security-channel-settings.md).</span></span>

<span data-ttu-id="a2ade-112">下列 API 元素會搭配安全性系結設定使用。</span><span class="sxs-lookup"><span data-stu-id="a2ade-112">The following API elements are used with security binding settings.</span></span>

| <span data-ttu-id="a2ade-113">列舉型別</span><span class="sxs-lookup"><span data-stu-id="a2ade-113">Enumeration</span></span>                                                                          | <span data-ttu-id="a2ade-114">描述</span><span class="sxs-lookup"><span data-stu-id="a2ade-114">Description</span></span>                                                                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2ade-115">**WS \_ 憑證 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="a2ade-115">**WS\_CERT\_FAILURE**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_value_type)                                         | <span data-ttu-id="a2ade-116">定義與憑證驗證相關的失敗。</span><span class="sxs-lookup"><span data-stu-id="a2ade-116">Defines failures related to certificate validation.</span></span>                                                                                                               |
| <span data-ttu-id="a2ade-117">[**WS \_ HTTP \_ 標頭 \_ 驗證 \_ 配置**](https://technet.microsoft.com/windows/dd401907(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="a2ade-117">[**WS\_HTTP\_HEADER\_AUTH\_SCHEME**](https://technet.microsoft.com/windows/dd401907(v=vs.60))</span></span>                 | <span data-ttu-id="a2ade-118">定義使用 HTTP 驗證標頭執行用戶端驗證的選項。</span><span class="sxs-lookup"><span data-stu-id="a2ade-118">Defines the options for performing client authentication using HTTP authentication headers.</span></span>                                                                       |
| [<span data-ttu-id="a2ade-119">**WS \_ HTTP \_ 標頭 \_ 驗證 \_ 目標**</span><span class="sxs-lookup"><span data-stu-id="a2ade-119">**WS\_HTTP\_HEADER\_AUTH\_TARGET**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_http_header_auth_target)                 | <span data-ttu-id="a2ade-120">定義 HTTP 標頭驗證安全性系結的目標。</span><span class="sxs-lookup"><span data-stu-id="a2ade-120">Defines the target for the HTTP header authentication security binding.</span></span>                                                                                           |
| [<span data-ttu-id="a2ade-121">**WS \_ 要求 \_ 安全性 \_ 權杖 \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="a2ade-121">**WS\_REQUEST\_SECURITY\_TOKEN\_ACTION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_action)     | <span data-ttu-id="a2ade-122">定義使用 WS-TRUST 來協商安全性權杖時要使用的動作集合。</span><span class="sxs-lookup"><span data-stu-id="a2ade-122">Defines which set of actions to use when negotiating security tokens using WS-Trust.</span></span>                                                                              |
| [<span data-ttu-id="a2ade-123">**WS \_ 安全性 \_ 演算法 \_ 套件 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="a2ade-123">**WS\_SECURITY\_ALGORITHM\_SUITE\_NAME**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_suite_name)     | <span data-ttu-id="a2ade-124">用於簽署和 encryting 等工作的安全性演算法套件。</span><span class="sxs-lookup"><span data-stu-id="a2ade-124">A suite of security algorithms used for tasks such as signing and encryting.</span></span>                                                                                      |
| [<span data-ttu-id="a2ade-125">**WS \_ 安全性系結 \_ \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="a2ade-125">**WS\_SECURITY\_BINDING\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id)       | <span data-ttu-id="a2ade-126">識別用來指定安全性系結設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="a2ade-126">Identifies the properties used to specify security binding settings.</span></span>                                                                                              |
| [<span data-ttu-id="a2ade-127">**WS \_ 安全性 \_ 金鑰 \_ 熵 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="a2ade-127">**WS\_SECURITY\_KEY\_ENTROPY\_MODE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode)             | <span data-ttu-id="a2ade-128">定義在使用訊息和混合模式安全性完成安全性權杖協商期間，如何為發出的金鑰貢獻隨機性。</span><span class="sxs-lookup"><span data-stu-id="a2ade-128">Defines how randomness should be contributed to the issued key during a security token negotiation done with message and mixed-mode security.</span></span>                     |
| [<span data-ttu-id="a2ade-129">**WS \_ 安全性 \_ 金鑰 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="a2ade-129">**WS\_SECURITY\_KEY\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_type)                              | <span data-ttu-id="a2ade-130">安全性權杖的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="a2ade-130">The key type of a security token.</span></span>                                                                                                                                 |
| [<span data-ttu-id="a2ade-131">**WS \_ 安全性 \_ 權杖 \_ 參考 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="a2ade-131">**WS\_SECURITY\_TOKEN\_REFERENCE\_MODE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_reference_mode)     | <span data-ttu-id="a2ade-132">在訊息和混合模式安全性系結的內容中，用來參考來自簽章、加密專案和衍生標記之安全性權杖的機制。</span><span class="sxs-lookup"><span data-stu-id="a2ade-132">the mechanism to use to refer to a security token from signatures, encrypted items and derived tokens in the context of message and mixed-mode security bindings.</span></span> |
| [<span data-ttu-id="a2ade-133">**WS \_ 信任 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="a2ade-133">**WS\_TRUST\_VERSION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version)                                       | <span data-ttu-id="a2ade-134">定義要搭配訊息安全性和混合模式安全性使用的 WS-Trust 規格版本。</span><span class="sxs-lookup"><span data-stu-id="a2ade-134">Defines the WS-Trust specification version to be used with message security and mixed-mode security.</span></span>                                                              |
| [<span data-ttu-id="a2ade-135">**WS \_ WINDOWS \_ 整合式 \_ 驗證 \_ 套件**</span><span class="sxs-lookup"><span data-stu-id="a2ade-135">**WS\_WINDOWS\_INTEGRATED\_AUTH\_PACKAGE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_package) | <span data-ttu-id="a2ade-136">定義要用於 Windows 整合式驗證的特定 SSP 套件。</span><span class="sxs-lookup"><span data-stu-id="a2ade-136">Defines the specific SSP package to be used for Windows Integrated Authentication.</span></span>                                                                                |



 



| <span data-ttu-id="a2ade-137">結構</span><span class="sxs-lookup"><span data-stu-id="a2ade-137">Structure</span></span>                                                               | <span data-ttu-id="a2ade-138">Description</span><span class="sxs-lookup"><span data-stu-id="a2ade-138">Description</span></span>                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="a2ade-139">**WS \_ 安全性系結 \_ \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="a2ade-139">**WS\_SECURITY\_BINDING\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) | <span data-ttu-id="a2ade-140">指定安全性系結特定設定。</span><span class="sxs-lookup"><span data-stu-id="a2ade-140">Specifies a security binding specific setting.</span></span> |



 

 

 




