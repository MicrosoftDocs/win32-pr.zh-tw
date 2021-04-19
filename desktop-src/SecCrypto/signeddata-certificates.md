---
description: 抓取與 SignedData 物件相關聯的憑證集合。 在抓取之後，可以列舉集合中的個別憑證物件。
ms.assetid: 94741fee-2462-4a18-bc14-c52e9cac374b
title: SignedData 憑證屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 55c0fe432794289fabe67b37deeedfac43f7a7d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990055"
---
# <a name="signeddatacertificates-property"></a><span data-ttu-id="a12dd-104">SignedData 憑證屬性</span><span class="sxs-lookup"><span data-stu-id="a12dd-104">SignedData.Certificates property</span></span>

<span data-ttu-id="a12dd-105">\[[ **憑證** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a12dd-105">\[The **Certificates** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a12dd-106">相反地，請使用 [**SignedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="a12dd-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="a12dd-107">[**憑證**] 屬性會抓取與 [**SignedData**](signeddata.md)物件相關聯的 [**憑證**](certificates.md)集合。</span><span class="sxs-lookup"><span data-stu-id="a12dd-107">The **Certificates** property retrieves the [**Certificates**](certificates.md) collection that is associated with the [**SignedData**](signeddata.md) object.</span></span> <span data-ttu-id="a12dd-108">在抓取之後，可以列舉集合中的個別 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="a12dd-108">After being retrieved, the individual [**Certificate**](certificate.md) objects in the collection can be enumerated.</span></span>

## <a name="syntax"></a><span data-ttu-id="a12dd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a12dd-109">Syntax</span></span>


```VB
SignedData.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="a12dd-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="a12dd-110">Property value</span></span>

<span data-ttu-id="a12dd-111">與 [**SignedData**](signeddata.md)物件相關聯的 [**憑證**](certificates.md)集合。</span><span class="sxs-lookup"><span data-stu-id="a12dd-111">The [**Certificates**](certificates.md) collection that is associated with the [**SignedData**](signeddata.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="a12dd-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a12dd-112">Requirements</span></span>



| <span data-ttu-id="a12dd-113">需求</span><span class="sxs-lookup"><span data-stu-id="a12dd-113">Requirement</span></span> | <span data-ttu-id="a12dd-114">值</span><span class="sxs-lookup"><span data-stu-id="a12dd-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a12dd-115">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a12dd-115">Redistributable</span></span><br/> | <span data-ttu-id="a12dd-116">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a12dd-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a12dd-117">DLL</span><span class="sxs-lookup"><span data-stu-id="a12dd-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="a12dd-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a12dd-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a12dd-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a12dd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a12dd-120">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="a12dd-120">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
