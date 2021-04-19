---
description: 傳回憑證的 Eku 集合。
ms.assetid: 64211a00-7d4d-4381-a134-9cd570ed7dbb
title: ExtendedKeyUsage Eku 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 24bcf7b4332e75afad0e21415a7dfe8eb690c32b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000372"
---
# <a name="extendedkeyusageekus-property"></a><span data-ttu-id="81027-103">ExtendedKeyUsage Eku 屬性</span><span class="sxs-lookup"><span data-stu-id="81027-103">ExtendedKeyUsage.EKUs property</span></span>

<span data-ttu-id="81027-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="81027-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="81027-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="81027-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="81027-106">**Eku** 屬性會傳回憑證的 [**eku**](ekus.md)集合。</span><span class="sxs-lookup"><span data-stu-id="81027-106">The **EKUs** property returns the [**EKUs**](ekus.md) collection for the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="81027-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="81027-107">Syntax</span></span>


```VB
ExtendedKeyUsage.EKUs As EKUs
```



## <a name="property-value"></a><span data-ttu-id="81027-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="81027-108">Property value</span></span>

<span data-ttu-id="81027-109">[**Eku**](ekus.md)集合，其中包含憑證的 [**EKU**](eku.md)物件。</span><span class="sxs-lookup"><span data-stu-id="81027-109">The [**EKUs**](ekus.md) collection that contains the [**EKU**](eku.md) objects for the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="81027-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="81027-110">Requirements</span></span>



| <span data-ttu-id="81027-111">需求</span><span class="sxs-lookup"><span data-stu-id="81027-111">Requirement</span></span> | <span data-ttu-id="81027-112">值</span><span class="sxs-lookup"><span data-stu-id="81027-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81027-113">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="81027-113">End of client support</span></span><br/> | <span data-ttu-id="81027-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81027-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="81027-115">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="81027-115">End of server support</span></span><br/> | <span data-ttu-id="81027-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81027-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="81027-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="81027-117">Redistributable</span></span><br/>       | <span data-ttu-id="81027-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="81027-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="81027-119">DLL</span><span class="sxs-lookup"><span data-stu-id="81027-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="81027-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81027-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81027-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81027-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81027-122">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="81027-122">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 
