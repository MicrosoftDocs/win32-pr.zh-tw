---
title: 安全性通道設定
description: 安全性通道設定可控制在通道上套用和驗證安全性的方式。
ms.assetid: ad964874-0bc7-4f03-8ceb-33627ff99f08
keywords:
- 適用于 Windows 的安全性通道設定 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcd0b42b2d5581a5b7c489e9ada70f32abfefa
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104093531"
---
# <a name="security-channel-settings"></a><span data-ttu-id="71b5e-106">安全性通道設定</span><span class="sxs-lookup"><span data-stu-id="71b5e-106">Security Channel Settings</span></span>

<span data-ttu-id="71b5e-107">安全性通道設定可控制在通道上套用和驗證安全性的方式。</span><span class="sxs-lookup"><span data-stu-id="71b5e-107">Security channel settings control the way security is applied and verified on a channel.</span></span> <span data-ttu-id="71b5e-108">每個安全性通道設定都是以屬性-值組的集合來表示，並以列舉 [**WS \_ 安全性 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)定義屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="71b5e-108">Each security channel setting is represented by a collection of property-value pairs, with the property keys defined by the enumeration [**WS\_SECURITY\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id).</span></span> <span data-ttu-id="71b5e-109">集合中的每個屬性都有合理的預設值。</span><span class="sxs-lookup"><span data-stu-id="71b5e-109">Each property in the collection has a reasonable default value.</span></span> <span data-ttu-id="71b5e-110">由於這些預設值的原因，您可以定義和使用安全性描述，而不需要指定任何安全性通道設定。</span><span class="sxs-lookup"><span data-stu-id="71b5e-110">Because of these default values, it is possible to define and use a security description without specifying any of the security channel settings.</span></span>


<span data-ttu-id="71b5e-111">[安全性](security-binding-settings.md) 系結設定包含屬性值配對的類似集合，其索引鍵是由 [**WS \_ 安全性 \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) 系結屬性結構所定義。</span><span class="sxs-lookup"><span data-stu-id="71b5e-111">[Security binding settings](security-binding-settings.md) contain similar collections of property-value pairs whose keys are defined by the [**WS\_SECURITY\_BINDING\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) structure.</span></span> <span data-ttu-id="71b5e-112">這兩種設定的差異在於安全性通道設定的範圍設定為安全性描述 (也就是說，它們包含全通道的安全性屬性) ，而安全性系結設定的範圍則是其中一個安全性系結，而且可能有許多安全性系結。</span><span class="sxs-lookup"><span data-stu-id="71b5e-112">The difference between these two sorts of settings is that the security channel settings are scoped to a security description (that is, they contain channel-wide security properties), whereas security binding settings are scoped to one of the security bindings, and there may be many security bindings.</span></span> <span data-ttu-id="71b5e-113">因此，例如，包含三個安全性系結的自訂安全性描述將會有一個安全性通道設定包，適用于整個通道和三個安全性系結設定包（每個安全性系結一個）。</span><span class="sxs-lookup"><span data-stu-id="71b5e-113">Consequently, for example, a custom security description that contains three security bindings will have one security channel settings bag for the entire channel and three security binding settings bags, one for each security binding.</span></span>

<span data-ttu-id="71b5e-114">下列列舉會搭配安全性通道設定使用：</span><span class="sxs-lookup"><span data-stu-id="71b5e-114">The following enumerations are used with security channel settings:</span></span>

-   [<span data-ttu-id="71b5e-115">**WS \_ 保護 \_ 等級**</span><span class="sxs-lookup"><span data-stu-id="71b5e-115">**WS\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)
-   [<span data-ttu-id="71b5e-116">**WS \_ 要求 \_ 安全性 \_ 權杖 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="71b5e-116">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)
-   [<span data-ttu-id="71b5e-117">**WS \_ 安全性 \_ 演算法 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="71b5e-117">**WS\_SECURITY\_ALGORITHM\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_id)
-   [<span data-ttu-id="71b5e-118">**WS \_ 安全性 \_ 演算法 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="71b5e-118">**WS\_SECURITY\_ALGORITHM\_PROPERTY\_ID**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_move_to)
-   [<span data-ttu-id="71b5e-119">**WS \_ 安全性 \_ 標頭配置 \_**</span><span class="sxs-lookup"><span data-stu-id="71b5e-119">**WS\_SECURITY\_HEADER\_LAYOUT**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_layout)
-   [<span data-ttu-id="71b5e-120">**WS \_ 安全性 \_ 標頭 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="71b5e-120">**WS\_SECURITY\_HEADER\_VERSION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_version)
-   [<span data-ttu-id="71b5e-121">**WS \_ 安全性 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="71b5e-121">**WS\_SECURITY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [<span data-ttu-id="71b5e-122">**WS \_ 安全性 \_ 時間戳記 \_ 使用量**</span><span class="sxs-lookup"><span data-stu-id="71b5e-122">**WS\_SECURITY\_TIMESTAMP\_USAGE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)
-   [<span data-ttu-id="71b5e-123">**WS \_ XML \_ 安全性 \_ 權杖 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="71b5e-123">**WS\_XML\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_security_token_property_id)

<span data-ttu-id="71b5e-124">下列結構會搭配安全性通道設定使用：</span><span class="sxs-lookup"><span data-stu-id="71b5e-124">The following structures are used with security channel settings:</span></span>

-   [<span data-ttu-id="71b5e-125">**WS \_ 要求 \_ 安全性 \_ 權杖 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="71b5e-125">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property)
-   [<span data-ttu-id="71b5e-126">**WS \_ 安全性 \_ 演算法 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="71b5e-126">**WS\_SECURITY\_ALGORITHM\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_property)
-   [<span data-ttu-id="71b5e-127">**WS \_ 安全性 \_ 演算法 \_ 套件**</span><span class="sxs-lookup"><span data-stu-id="71b5e-127">**WS\_SECURITY\_ALGORITHM\_SUITE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_suite)
-   [<span data-ttu-id="71b5e-128">**WS \_ 安全性 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="71b5e-128">**WS\_SECURITY\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)
-   [<span data-ttu-id="71b5e-129">**WS \_ XML \_ 安全性 \_ 權杖 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="71b5e-129">**WS\_XML\_SECURITY\_TOKEN\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_security_token_property)

 

 




