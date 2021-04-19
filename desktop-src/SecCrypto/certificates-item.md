---
description: 抓取代表集合之索引憑證的憑證物件。 這是預設屬性。
ms.assetid: 733f2b93-c059-4041-b7cd-8c20218f1462
title: Certificate. Item 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bbafaf20f74910e8ea5eb525f48374a2807fa030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987842"
---
# <a name="certificatesitem-property"></a><span data-ttu-id="cd515-104">Certificate. Item 屬性</span><span class="sxs-lookup"><span data-stu-id="cd515-104">Certificates.Item property</span></span>

<span data-ttu-id="cd515-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="cd515-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="cd515-106">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="cd515-106">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="cd515-107">**Item** 屬性會抓取代表集合之索引憑證的 [**憑證**](certificate.md)物件。</span><span class="sxs-lookup"><span data-stu-id="cd515-107">The **Item** property retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="cd515-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="cd515-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd515-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd515-109">Syntax</span></span>


```VB
Certificates.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="cd515-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="cd515-110">Property value</span></span>

<span data-ttu-id="cd515-111">表示已編制索引之憑證的 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="cd515-111">A [**Certificate**](certificate.md) object that represents the indexed certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd515-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd515-112">Requirements</span></span>



| <span data-ttu-id="cd515-113">需求</span><span class="sxs-lookup"><span data-stu-id="cd515-113">Requirement</span></span> | <span data-ttu-id="cd515-114">值</span><span class="sxs-lookup"><span data-stu-id="cd515-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd515-115">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="cd515-115">End of client support</span></span><br/> | <span data-ttu-id="cd515-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd515-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cd515-117">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="cd515-117">End of server support</span></span><br/> | <span data-ttu-id="cd515-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd515-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cd515-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="cd515-119">Redistributable</span></span><br/>       | <span data-ttu-id="cd515-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="cd515-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cd515-121">DLL</span><span class="sxs-lookup"><span data-stu-id="cd515-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="cd515-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd515-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd515-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd515-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd515-124">**憑證**</span><span class="sxs-lookup"><span data-stu-id="cd515-124">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
