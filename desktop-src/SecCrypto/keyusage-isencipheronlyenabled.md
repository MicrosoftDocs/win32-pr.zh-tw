---
description: 抓取布林值，指出是否已設定 encipherOnly 位。
ms.assetid: 60d79ea4-4968-49e0-8d16-873fbcbd951c
title: KeyUsage. IsEncipherOnlyEnabled 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsEncipherOnlyEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8a473797f989d18e090af33f08274ecede2630b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993931"
---
# <a name="keyusageisencipheronlyenabled-property"></a><span data-ttu-id="05f85-103">KeyUsage. IsEncipherOnlyEnabled 屬性</span><span class="sxs-lookup"><span data-stu-id="05f85-103">KeyUsage.IsEncipherOnlyEnabled property</span></span>

<span data-ttu-id="05f85-104">\[**IsEncipherOnlyEnabled** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="05f85-104">\[The **IsEncipherOnlyEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="05f85-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="05f85-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="05f85-106">**IsEncipherOnlyEnabled** 屬性會抓取布林值，指出是否已設定 encipherOnly 位。</span><span class="sxs-lookup"><span data-stu-id="05f85-106">The **IsEncipherOnlyEnabled** property retrieves a Boolean value that indicates whether the encipherOnly bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f85-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="05f85-107">Syntax</span></span>


```VB
KeyUsage.IsEncipherOnlyEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="05f85-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="05f85-108">Property value</span></span>

<span data-ttu-id="05f85-109">若 **為 true**，則會設定 encipherOnly 位。</span><span class="sxs-lookup"><span data-stu-id="05f85-109">If **true**, the encipherOnly bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="05f85-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="05f85-110">Requirements</span></span>



| <span data-ttu-id="05f85-111">需求</span><span class="sxs-lookup"><span data-stu-id="05f85-111">Requirement</span></span> | <span data-ttu-id="05f85-112">值</span><span class="sxs-lookup"><span data-stu-id="05f85-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05f85-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="05f85-113">Redistributable</span></span><br/> | <span data-ttu-id="05f85-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="05f85-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="05f85-115">DLL</span><span class="sxs-lookup"><span data-stu-id="05f85-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="05f85-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05f85-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05f85-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05f85-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f85-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="05f85-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
