---
description: 您可以將屬性新增至憑證要求，以提供憑證授權單位單位 (CA) 以及可在建立和發行憑證時使用的其他資訊。
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: 憑證註冊 API)  (屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e7a00c30be8bacf5593d78e21fb420c8a899dc7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691419"
---
# <a name="attributes-certificate-enrollment-api"></a><span data-ttu-id="13737-103">憑證註冊 API)  (屬性</span><span class="sxs-lookup"><span data-stu-id="13737-103">Attributes (Certificate Enrollment API)</span></span>

<span data-ttu-id="13737-104">您可以將屬性新增至憑證要求，以提供憑證授權單位單位 (CA) 以及可在建立和發行憑證時使用的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="13737-104">Attributes can be added to a certificate request to provide a certification authority (CA) with additional information that it can use when creating and issuing a certificate.</span></span> <span data-ttu-id="13737-105">每個屬性都是 [*可辨別編碼規則*](/windows/desktop/SecGloss/d-gly) (DER) 編碼 [*抽象語法標記法 (一)*](/windows/desktop/SecGloss/a-gly) (asn.1) 結構，其中包含 (OID) 和零或多個值的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="13737-105">Each attribute is a [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) encoded [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) structure that contains an object identifier (OID) and zero or more values.</span></span> <span data-ttu-id="13737-106">您可以使用憑證註冊 API 隨附的介面來定義屬性。</span><span class="sxs-lookup"><span data-stu-id="13737-106">Attributes are defined by using interfaces included with the Certificate Enrollment API.</span></span> <span data-ttu-id="13737-107">下列主題會更詳細地討論屬性：</span><span class="sxs-lookup"><span data-stu-id="13737-107">The following topics discuss attributes in more detail:</span></span>

-   [<span data-ttu-id="13737-108">支援的屬性</span><span class="sxs-lookup"><span data-stu-id="13737-108">Supported Attributes</span></span>](supported-attributes.md)
-   [<span data-ttu-id="13737-109">屬性架構</span><span class="sxs-lookup"><span data-stu-id="13737-109">Attribute Architecture</span></span>](attribute-architecture.md)
-   [<span data-ttu-id="13737-110">PKCS \# 7 屬性</span><span class="sxs-lookup"><span data-stu-id="13737-110">PKCS \#7 Attributes</span></span>](pkcs--7-attributes.md)
-   [<span data-ttu-id="13737-111">PKCS \# 10 屬性</span><span class="sxs-lookup"><span data-stu-id="13737-111">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
-   [<span data-ttu-id="13737-112">CMC 屬性</span><span class="sxs-lookup"><span data-stu-id="13737-112">CMC Attributes</span></span>](cmc-attributes.md)

 

 
