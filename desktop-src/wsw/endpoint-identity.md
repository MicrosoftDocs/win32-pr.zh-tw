---
title: 端點識別
description: 此區段中定義的類型是用來定義端點位址的安全性識別。
ms.assetid: 39639b9a-32e2-44d2-9bda-a2ad23850de8
keywords:
- 適用于 Windows 的端點身分識別 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7a3f7b95d5fc1b926d8bafb49b06f96c7d68fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371883"
---
# <a name="endpoint-identity"></a><span data-ttu-id="f55eb-106">端點識別</span><span class="sxs-lookup"><span data-stu-id="f55eb-106">Endpoint Identity</span></span>

<span data-ttu-id="f55eb-107">此區段中定義的類型是用來定義端點位址的安全性識別。</span><span class="sxs-lookup"><span data-stu-id="f55eb-107">The types defined in this section are used to define the security identity of an endpoint address.</span></span>

<span data-ttu-id="f55eb-108">下列 API 元素是端點識別的一部分：</span><span class="sxs-lookup"><span data-stu-id="f55eb-108">The following API elements are part of endpoint indentity:</span></span>



| <span data-ttu-id="f55eb-109">列舉型別</span><span class="sxs-lookup"><span data-stu-id="f55eb-109">Enumeration</span></span>                                                       | <span data-ttu-id="f55eb-110">描述</span><span class="sxs-lookup"><span data-stu-id="f55eb-110">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f55eb-111">**WS \_ 端點身分 \_ 識別 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="f55eb-111">**WS\_ENDPOINT\_IDENTITY\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_endpoint_identity_type) | <span data-ttu-id="f55eb-112">端點身分識別的型別，用來做為 [**WS \_ 端點身分 \_ 識別**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity)之子類型的選取器。</span><span class="sxs-lookup"><span data-stu-id="f55eb-112">The type of the endpoint identity, used as a selector for subtypes of [**WS\_ENDPOINT\_IDENTITY**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity).</span></span> |



 



| <span data-ttu-id="f55eb-113">結構</span><span class="sxs-lookup"><span data-stu-id="f55eb-113">Structure</span></span>                                                               | <span data-ttu-id="f55eb-114">Description</span><span class="sxs-lookup"><span data-stu-id="f55eb-114">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f55eb-115">**WS \_ CERT \_ 端點身分 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="f55eb-115">**WS\_CERT\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_endpoint_identity)       | <span data-ttu-id="f55eb-116">憑證端點身分識別的類型。</span><span class="sxs-lookup"><span data-stu-id="f55eb-116">The type for certificate endpoint identity .</span></span>                                                 |
| [<span data-ttu-id="f55eb-117">**WS \_ DNS \_ 端點身分 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="f55eb-117">**WS\_DNS\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_dns_endpoint_identity)         | <span data-ttu-id="f55eb-118">用來指定 DNS 名稱所代表之端點身分識別的型別。</span><span class="sxs-lookup"><span data-stu-id="f55eb-118">The type for specifying an endpoint identity represented by a DNS name.</span></span>                      |
| [<span data-ttu-id="f55eb-119">**WS \_ 端點身分 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="f55eb-119">**WS\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity)                  | <span data-ttu-id="f55eb-120">所有端點身分識別的基底類型。</span><span class="sxs-lookup"><span data-stu-id="f55eb-120">The base type for all endpoint identities.</span></span>                                                   |
| [<span data-ttu-id="f55eb-121">**WS \_ RSA \_ 端點身分 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="f55eb-121">**WS\_RSA\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_rsa_endpoint_identity)         | <span data-ttu-id="f55eb-122">輸入 RSA 端點身分識別。</span><span class="sxs-lookup"><span data-stu-id="f55eb-122">Type for RSA endpoint identity.</span></span>                                                              |
| [<span data-ttu-id="f55eb-123">**WS \_ SPN \_ 端點身分 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="f55eb-123">**WS\_SPN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_spn_endpoint_identity)         | <span data-ttu-id="f55eb-124">型別，用來指定由 SPN 表示的端點識別 (服務主體名稱) 。</span><span class="sxs-lookup"><span data-stu-id="f55eb-124">The type for specifying an endpoint identity represented by an SPN (service principal name).</span></span> |
| [<span data-ttu-id="f55eb-125">**WS \_ 未知的 \_ 端點身分 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="f55eb-125">**WS\_UNKNOWN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_unknown_endpoint_identity) | <span data-ttu-id="f55eb-126">未知端點身分識別的類型。</span><span class="sxs-lookup"><span data-stu-id="f55eb-126">The type for an unknown endpoint identity.</span></span>                                                   |
| [<span data-ttu-id="f55eb-127">**WS \_ UPN \_ 端點身分 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="f55eb-127">**WS\_UPN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_upn_endpoint_identity)         | <span data-ttu-id="f55eb-128">用來指定 UPN 所代表之端點身分識別的型別 (使用者主體名稱) 。</span><span class="sxs-lookup"><span data-stu-id="f55eb-128">The type for specifying an endpoint identity represented by a UPN (user principal name).</span></span>     |



 

 

 




