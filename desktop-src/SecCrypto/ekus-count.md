---
description: 抓取集合中的 EKU 物件數目。
ms.assetid: a38ac480-4f9b-4d69-a7e6-fae4993fe2cf
title: Eku. Count 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41e77f3803fa65db1573c6619ebf1265b7418924
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979501"
---
# <a name="ekuscount-property"></a><span data-ttu-id="748d4-103">Eku. Count 屬性</span><span class="sxs-lookup"><span data-stu-id="748d4-103">EKUs.Count property</span></span>

<span data-ttu-id="748d4-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="748d4-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="748d4-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ExtensionCollection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="748d4-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="748d4-106">**Count** 屬性會抓取集合中的 [**EKU**](eku.md)物件數目。</span><span class="sxs-lookup"><span data-stu-id="748d4-106">The **Count** property retrieves the number of [**EKU**](eku.md) objects in the collection.</span></span>

<span data-ttu-id="748d4-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="748d4-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="748d4-108">語法</span><span class="sxs-lookup"><span data-stu-id="748d4-108">Syntax</span></span>


```VB
EKUs.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="748d4-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="748d4-109">Property value</span></span>

<span data-ttu-id="748d4-110">集合中的 [**EKU**](eku.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="748d4-110">The number of [**EKU**](eku.md) objects in the collection.</span></span> <span data-ttu-id="748d4-111">每個 **EKU** 物件都代表憑證 (EKU) 屬性的單一擴充金鑰使用方式。</span><span class="sxs-lookup"><span data-stu-id="748d4-111">Each **EKU** object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="748d4-112">備註</span><span class="sxs-lookup"><span data-stu-id="748d4-112">Remarks</span></span>

<span data-ttu-id="748d4-113">您可以使用 [**計數**] 屬性，在使用 [**eku. Item**](ekus-item.md)屬性抓取特定的 **eku** 物件時，指定集合中的最後一個 [**eku**](eku.md)物件。</span><span class="sxs-lookup"><span data-stu-id="748d4-113">The **Count** property can be used to specify the last [**EKU**](eku.md) object in a collection when retrieving a specific **EKU** object using the [**EKUs.Item**](ekus-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="748d4-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="748d4-114">Requirements</span></span>



| <span data-ttu-id="748d4-115">需求</span><span class="sxs-lookup"><span data-stu-id="748d4-115">Requirement</span></span> | <span data-ttu-id="748d4-116">值</span><span class="sxs-lookup"><span data-stu-id="748d4-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="748d4-117">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="748d4-117">End of client support</span></span><br/> | <span data-ttu-id="748d4-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="748d4-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="748d4-119">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="748d4-119">End of server support</span></span><br/> | <span data-ttu-id="748d4-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="748d4-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="748d4-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="748d4-121">Redistributable</span></span><br/>       | <span data-ttu-id="748d4-122">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="748d4-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="748d4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="748d4-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="748d4-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="748d4-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
