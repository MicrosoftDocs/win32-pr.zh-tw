---
description: 傳回布林值，指出 EKU 延伸是否標記為重大。
ms.assetid: f6d2a2e0-512b-44f2-a7d9-9ad661398aa8
title: ExtendedKeyUsage. IsCritical 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5331922567af3b9a34517ab5059fa03ad9904270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992876"
---
# <a name="extendedkeyusageiscritical-property"></a><span data-ttu-id="5fa3a-103">ExtendedKeyUsage. IsCritical 屬性</span><span class="sxs-lookup"><span data-stu-id="5fa3a-103">ExtendedKeyUsage.IsCritical property</span></span>

<span data-ttu-id="5fa3a-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="5fa3a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="5fa3a-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="5fa3a-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="5fa3a-106">**IsCritical** 屬性會傳回布林值，指出 EKU 延伸是否標記為重大。</span><span class="sxs-lookup"><span data-stu-id="5fa3a-106">The **IsCritical** property returns a Boolean value that indicates whether the EKU extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fa3a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fa3a-107">Syntax</span></span>


```VB
ExtendedKeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="5fa3a-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="5fa3a-108">Property value</span></span>

<span data-ttu-id="5fa3a-109">若 **為 true**，則會將 EKU 延伸標示為「重大」。</span><span class="sxs-lookup"><span data-stu-id="5fa3a-109">If **true**, the EKU extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fa3a-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="5fa3a-110">Requirements</span></span>



| <span data-ttu-id="5fa3a-111">需求</span><span class="sxs-lookup"><span data-stu-id="5fa3a-111">Requirement</span></span> | <span data-ttu-id="5fa3a-112">值</span><span class="sxs-lookup"><span data-stu-id="5fa3a-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa3a-113">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5fa3a-113">End of client support</span></span><br/> | <span data-ttu-id="5fa3a-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5fa3a-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5fa3a-115">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="5fa3a-115">End of server support</span></span><br/> | <span data-ttu-id="5fa3a-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5fa3a-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5fa3a-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="5fa3a-117">Redistributable</span></span><br/>       | <span data-ttu-id="5fa3a-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5fa3a-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5fa3a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="5fa3a-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5fa3a-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fa3a-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fa3a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5fa3a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fa3a-122">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="5fa3a-122">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 
