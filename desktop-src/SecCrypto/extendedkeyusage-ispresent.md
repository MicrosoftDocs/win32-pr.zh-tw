---
description: 傳回布林值，指出 EKU 延伸是否存在。 這是預設屬性。
ms.assetid: d7568525-1054-47e1-a176-f154792f9589
title: ExtendedKeyUsage. IsPresent 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 785fa3c973e7f90eeab20bd76826b9e5bf612891
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984137"
---
# <a name="extendedkeyusageispresent-property"></a><span data-ttu-id="99203-104">ExtendedKeyUsage. IsPresent 屬性</span><span class="sxs-lookup"><span data-stu-id="99203-104">ExtendedKeyUsage.IsPresent property</span></span>

<span data-ttu-id="99203-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="99203-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="99203-106">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="99203-106">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="99203-107">**IsPresent** 屬性會傳回布林值，指出 EKU 延伸是否存在。</span><span class="sxs-lookup"><span data-stu-id="99203-107">The **IsPresent** property returns a Boolean value that indicates whether the EKU extension is present.</span></span> <span data-ttu-id="99203-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="99203-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="99203-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="99203-109">Syntax</span></span>


```VB
ExtendedKeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="99203-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="99203-110">Property value</span></span>

<span data-ttu-id="99203-111">若 **為 true**，則表示 EKU 延伸模組存在。</span><span class="sxs-lookup"><span data-stu-id="99203-111">If **true**, the EKU extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="99203-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="99203-112">Requirements</span></span>



| <span data-ttu-id="99203-113">需求</span><span class="sxs-lookup"><span data-stu-id="99203-113">Requirement</span></span> | <span data-ttu-id="99203-114">值</span><span class="sxs-lookup"><span data-stu-id="99203-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99203-115">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="99203-115">End of client support</span></span><br/> | <span data-ttu-id="99203-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99203-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="99203-117">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="99203-117">End of server support</span></span><br/> | <span data-ttu-id="99203-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99203-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="99203-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="99203-119">Redistributable</span></span><br/>       | <span data-ttu-id="99203-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="99203-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="99203-121">DLL</span><span class="sxs-lookup"><span data-stu-id="99203-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="99203-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99203-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99203-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99203-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99203-124">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="99203-124">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 
