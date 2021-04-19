---
description: 抓取布林值，指出是否已設定 nonRepudiationEnabled 位。
ms.assetid: d9bcf0fc-8b2d-408c-b587-71903ef5f5f6
title: KeyUsage. IsNonRepudiationEnabled 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsNonRepudiationEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 30e0a532cd39f2150591a3eb74ed9bbba83a7080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999067"
---
# <a name="keyusageisnonrepudiationenabled-property"></a><span data-ttu-id="5dbce-103">KeyUsage. IsNonRepudiationEnabled 屬性</span><span class="sxs-lookup"><span data-stu-id="5dbce-103">KeyUsage.IsNonRepudiationEnabled property</span></span>

<span data-ttu-id="5dbce-104">\[**IsNonRepudiationEnabled** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="5dbce-104">\[The **IsNonRepudiationEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5dbce-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="5dbce-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="5dbce-106">**IsNonRepudiationEnabled** 屬性會抓取布林值，指出是否已設定 nonRepudiationEnabled 位。</span><span class="sxs-lookup"><span data-stu-id="5dbce-106">The **IsNonRepudiationEnabled** property retrieves a Boolean value that indicates whether the nonRepudiationEnabled bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dbce-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dbce-107">Syntax</span></span>


```VB
KeyUsage.IsNonRepudiationEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="5dbce-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="5dbce-108">Property value</span></span>

<span data-ttu-id="5dbce-109">若 **為 true**，則會設定 nonRepudiationEnabled 位。</span><span class="sxs-lookup"><span data-stu-id="5dbce-109">If **true**, the nonRepudiationEnabled bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dbce-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="5dbce-110">Requirements</span></span>



| <span data-ttu-id="5dbce-111">需求</span><span class="sxs-lookup"><span data-stu-id="5dbce-111">Requirement</span></span> | <span data-ttu-id="5dbce-112">值</span><span class="sxs-lookup"><span data-stu-id="5dbce-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dbce-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="5dbce-113">Redistributable</span></span><br/> | <span data-ttu-id="5dbce-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5dbce-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5dbce-115">DLL</span><span class="sxs-lookup"><span data-stu-id="5dbce-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="5dbce-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dbce-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dbce-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5dbce-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dbce-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="5dbce-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
