---
description: 抓取布林值，指出 KeyUsage 延伸模組是否標記為重大。
ms.assetid: f7d53570-2b89-40a9-ab56-fcae4e4cb70c
title: KeyUsage. IsCritical 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b1829da9c9ddbcf5261f4cc595b72b8596193078
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983943"
---
# <a name="keyusageiscritical-property"></a><span data-ttu-id="d0236-103">KeyUsage. IsCritical 屬性</span><span class="sxs-lookup"><span data-stu-id="d0236-103">KeyUsage.IsCritical property</span></span>

<span data-ttu-id="d0236-104">\[**IsCritical** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d0236-104">\[The **IsCritical** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d0236-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="d0236-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d0236-106">**IsCritical** 屬性會抓取布林值，指出 KeyUsage 延伸模組是否標記為重大。</span><span class="sxs-lookup"><span data-stu-id="d0236-106">The **IsCritical** property retrieves a Boolean value that indicates whether the KeyUsage extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0236-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0236-107">Syntax</span></span>


```VB
KeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="d0236-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="d0236-108">Property value</span></span>

<span data-ttu-id="d0236-109">若 **為 true**，則表示 KeyUsage 延伸模組標示為「重大」。</span><span class="sxs-lookup"><span data-stu-id="d0236-109">If **true**, the KeyUsage extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0236-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0236-110">Requirements</span></span>



| <span data-ttu-id="d0236-111">需求</span><span class="sxs-lookup"><span data-stu-id="d0236-111">Requirement</span></span> | <span data-ttu-id="d0236-112">值</span><span class="sxs-lookup"><span data-stu-id="d0236-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0236-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d0236-113">Redistributable</span></span><br/> | <span data-ttu-id="d0236-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d0236-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d0236-115">DLL</span><span class="sxs-lookup"><span data-stu-id="d0236-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="d0236-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0236-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0236-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0236-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0236-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="d0236-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
