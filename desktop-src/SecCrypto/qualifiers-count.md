---
description: 抓取集合中的限定詞物件數目。
ms.assetid: 9dafb83a-ff7f-4317-8ed4-2a46dcebf409
title: 限定詞。 Count 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ffb79941a78602bfda8f5287b0f4df7205d4d86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999527"
---
# <a name="qualifierscount-property"></a><span data-ttu-id="c10d0-103">限定詞。 Count 屬性</span><span class="sxs-lookup"><span data-stu-id="c10d0-103">Qualifiers.Count property</span></span>

<span data-ttu-id="c10d0-104">\[[ **計數** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c10d0-104">\[The **Count** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c10d0-105">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 Oid 來處理憑證原則延伸中屬於原則資訊的限定詞。\]</span><span class="sxs-lookup"><span data-stu-id="c10d0-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="c10d0-106">**Count** 屬性會抓取集合中的 [**限定詞**](qualifier.md)物件數目。</span><span class="sxs-lookup"><span data-stu-id="c10d0-106">The **Count** property retrieves the number of [**Qualifier**](qualifier.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c10d0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c10d0-107">Syntax</span></span>


```VB
Qualifiers.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="c10d0-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="c10d0-108">Property value</span></span>

<span data-ttu-id="c10d0-109">集合中的 [**限定詞**](qualifier.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="c10d0-109">Number of [**Qualifier**](qualifier.md) objects in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="c10d0-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="c10d0-110">Requirements</span></span>



| <span data-ttu-id="c10d0-111">需求</span><span class="sxs-lookup"><span data-stu-id="c10d0-111">Requirement</span></span> | <span data-ttu-id="c10d0-112">值</span><span class="sxs-lookup"><span data-stu-id="c10d0-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c10d0-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="c10d0-113">Redistributable</span></span><br/> | <span data-ttu-id="c10d0-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c10d0-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c10d0-115">DLL</span><span class="sxs-lookup"><span data-stu-id="c10d0-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="c10d0-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c10d0-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c10d0-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c10d0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c10d0-118">**限定詞**</span><span class="sxs-lookup"><span data-stu-id="c10d0-118">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
