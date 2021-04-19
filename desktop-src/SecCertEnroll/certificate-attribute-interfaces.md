---
description: 下列介面可以用來建立憑證屬性。
ms.assetid: 3701f9b2-0857-45f0-b3ed-4f1b3db4d6d8
title: 憑證屬性介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 930f427ae6333084c8a180e5d227e4c24daa5426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973472"
---
# <a name="certificate-attribute-interfaces"></a><span data-ttu-id="d43d0-103">憑證屬性介面</span><span class="sxs-lookup"><span data-stu-id="d43d0-103">Certificate Attribute Interfaces</span></span>

<span data-ttu-id="d43d0-104">下列介面可以用來建立憑證屬性。</span><span class="sxs-lookup"><span data-stu-id="d43d0-104">The following interfaces can be used to create certificate attributes.</span></span>



| <span data-ttu-id="d43d0-105">介面</span><span class="sxs-lookup"><span data-stu-id="d43d0-105">Interface</span></span>                                                                    | <span data-ttu-id="d43d0-106">描述</span><span class="sxs-lookup"><span data-stu-id="d43d0-106">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d43d0-107">**ICryptAttribute**</span><span class="sxs-lookup"><span data-stu-id="d43d0-107">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                   | <span data-ttu-id="d43d0-108">代表憑證要求中的密碼編譯屬性。</span><span class="sxs-lookup"><span data-stu-id="d43d0-108">Represents a cryptographic attribute in a certificate request.</span></span>                                                                              |
| [<span data-ttu-id="d43d0-109">**ICryptAttributes**</span><span class="sxs-lookup"><span data-stu-id="d43d0-109">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)                                 | <span data-ttu-id="d43d0-110">管理 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="d43d0-110">Manages a collection of [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) objects.</span></span>                                                                 |
| [<span data-ttu-id="d43d0-111">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="d43d0-111">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                     | <span data-ttu-id="d43d0-112">表示 PKCS \# 7、pkcs \# 10 或 CMC 憑證要求中的屬性。</span><span class="sxs-lookup"><span data-stu-id="d43d0-112">Represents an attribute in a PKCS \#7, PKCS \#10, or CMC certificate request.</span></span>                                                               |
| [<span data-ttu-id="d43d0-113">**IX509AttributeClientId**</span><span class="sxs-lookup"><span data-stu-id="d43d0-113">**IX509AttributeClientId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)                     | <span data-ttu-id="d43d0-114">表示可用於識別產生憑證要求之用戶端的屬性。</span><span class="sxs-lookup"><span data-stu-id="d43d0-114">Represents an attribute that can be used to identify the client that generated a certificate request.</span></span>                                       |
| [<span data-ttu-id="d43d0-115">**IX509AttributeExtensions**</span><span class="sxs-lookup"><span data-stu-id="d43d0-115">**IX509AttributeExtensions**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)                 | <span data-ttu-id="d43d0-116">代表憑證要求中的憑證延伸。</span><span class="sxs-lookup"><span data-stu-id="d43d0-116">Represents the certificate extensions in a certificate request.</span></span>                                                                             |
| [<span data-ttu-id="d43d0-117">**IX509AttributeArchiveKey**</span><span class="sxs-lookup"><span data-stu-id="d43d0-117">**IX509AttributeArchiveKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)                 | <span data-ttu-id="d43d0-118">表示屬性，其中包含要由憑證授權單位單位封存的加密私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="d43d0-118">Represents an attribute that contains an encrypted private key to be archived by a certification authority.</span></span>                                 |
| [<span data-ttu-id="d43d0-119">**IX509AttributeArchiveKeyHash**</span><span class="sxs-lookup"><span data-stu-id="d43d0-119">**IX509AttributeArchiveKeyHash**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)         | <span data-ttu-id="d43d0-120">表示屬性，其中包含要由憑證授權單位單位封存之加密私密金鑰的 SHA-1 雜湊。</span><span class="sxs-lookup"><span data-stu-id="d43d0-120">Represents an attribute that contains a SHA-1 hash of the encrypted private key to be archived by a certification authority.</span></span>                |
| [<span data-ttu-id="d43d0-121">**IX509AttributeCspProvider**</span><span class="sxs-lookup"><span data-stu-id="d43d0-121">**IX509AttributeCspProvider**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)               | <span data-ttu-id="d43d0-122">代表屬性，這個屬性會識別要求憑證之實體所使用的密碼編譯提供者。</span><span class="sxs-lookup"><span data-stu-id="d43d0-122">Represents an attribute that identifies the cryptographic provider used by the entity requesting the certificate.</span></span>                           |
| [<span data-ttu-id="d43d0-123">**IX509AttributeOSVersion**</span><span class="sxs-lookup"><span data-stu-id="d43d0-123">**IX509AttributeOSVersion**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)                   | <span data-ttu-id="d43d0-124">表示屬性，其中包含產生憑證要求之用戶端作業系統的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="d43d0-124">Represents an attribute that contains version information about the client operating system on which the certificate request was generated.</span></span> |
| [<span data-ttu-id="d43d0-125">**IX509AttributeRenewalCertificate**</span><span class="sxs-lookup"><span data-stu-id="d43d0-125">**IX509AttributeRenewalCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) | <span data-ttu-id="d43d0-126">表示包含要更新之憑證的屬性。</span><span class="sxs-lookup"><span data-stu-id="d43d0-126">Represents an attribute that contains the certificate being renewed.</span></span>                                                                        |
| [<span data-ttu-id="d43d0-127">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="d43d0-127">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)                                   | <span data-ttu-id="d43d0-128">管理 [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="d43d0-128">Manages a collection of [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) objects.</span></span>                                                                   |
| [<span data-ttu-id="d43d0-129">**IX509NameValuePair**</span><span class="sxs-lookup"><span data-stu-id="d43d0-129">**IX509NameValuePair**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                             | <span data-ttu-id="d43d0-130">表示泛型名稱/值配對。</span><span class="sxs-lookup"><span data-stu-id="d43d0-130">Represents a generic name-value pair.</span></span>                                                                                                       |
| [<span data-ttu-id="d43d0-131">**IX509NameValuePairs**</span><span class="sxs-lookup"><span data-stu-id="d43d0-131">**IX509NameValuePairs**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)                           | <span data-ttu-id="d43d0-132">管理 [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="d43d0-132">Manages a collection of [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) objects.</span></span>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="d43d0-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="d43d0-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d43d0-134">CertEnroll 介面</span><span class="sxs-lookup"><span data-stu-id="d43d0-134">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



