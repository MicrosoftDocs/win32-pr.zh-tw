---
description: 表示 EKU 物件的集合。
ms.assetid: 04b9f0bf-e1d4-4a2c-be5d-bae7c1090bdb
title: Eku 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 56fd6eaeb5a00549cbb4ee659b99ece391e0ebed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997729"
---
# <a name="ekus-object"></a><span data-ttu-id="8d0e0-103">Eku 物件</span><span class="sxs-lookup"><span data-stu-id="8d0e0-103">EKUs object</span></span>

<span data-ttu-id="8d0e0-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="8d0e0-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ExtensionCollection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="8d0e0-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="8d0e0-106">Eku **物件代表** [**EKU**](eku.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-106">The **EKUs** object represents a collection of [**EKU**](eku.md) objects.</span></span> <span data-ttu-id="8d0e0-107">每個 [**EKU**](eku.md) 物件都代表憑證 (EKU) 屬性的單一擴充金鑰使用方式。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-107">Each [**EKU**](eku.md) object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="8d0e0-108">使用時機</span><span class="sxs-lookup"><span data-stu-id="8d0e0-108">When to use</span></span>

<span data-ttu-id="8d0e0-109">**Eku** 集合是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="8d0e0-109">The **EKUs** collection is used to perform the following tasks:</span></span>

-   <span data-ttu-id="8d0e0-110">取得集合中的 EKU 屬性數目。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-110">Retrieve the number of EKU properties in the collection.</span></span>
-   <span data-ttu-id="8d0e0-111">從集合中取出特定的 [**EKU**](eku.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-111">Retrieve a specific [**EKU**](eku.md) object from the collection.</span></span>
-   <span data-ttu-id="8d0e0-112">逐一查看集合。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="8d0e0-113">成員</span><span class="sxs-lookup"><span data-stu-id="8d0e0-113">Members</span></span>

<span data-ttu-id="8d0e0-114">**Eku** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8d0e0-114">The **EKUs** object has these types of members:</span></span>

-   [<span data-ttu-id="8d0e0-115">屬性</span><span class="sxs-lookup"><span data-stu-id="8d0e0-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d0e0-116">屬性</span><span class="sxs-lookup"><span data-stu-id="8d0e0-116">Properties</span></span>

<span data-ttu-id="8d0e0-117">**Eku** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-117">The **EKUs** object has these properties.</span></span>



| <span data-ttu-id="8d0e0-118">屬性</span><span class="sxs-lookup"><span data-stu-id="8d0e0-118">Property</span></span>                                     | <span data-ttu-id="8d0e0-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="8d0e0-119">Access type</span></span>          | <span data-ttu-id="8d0e0-120">Description</span><span class="sxs-lookup"><span data-stu-id="8d0e0-120">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d0e0-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="8d0e0-121">**\_NewEnum**</span></span>](ekus-newenum.md)<br/> | <span data-ttu-id="8d0e0-122">唯讀</span><span class="sxs-lookup"><span data-stu-id="8d0e0-122">Read-only</span></span><br/> | <span data-ttu-id="8d0e0-123">在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="8d0e0-124">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="8d0e0-125">**計數**</span><span class="sxs-lookup"><span data-stu-id="8d0e0-125">**Count**</span></span>](ekus-count.md)<br/>       | <span data-ttu-id="8d0e0-126">唯讀</span><span class="sxs-lookup"><span data-stu-id="8d0e0-126">Read-only</span></span><br/> | <span data-ttu-id="8d0e0-127">抓取集合中的 [**EKU**](eku.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-127">Retrieves the number of [**EKU**](eku.md) objects in the collection.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="8d0e0-128">**項目**</span><span class="sxs-lookup"><span data-stu-id="8d0e0-128">**Item**</span></span>](ekus-item.md)<br/>         | <span data-ttu-id="8d0e0-129">唯讀</span><span class="sxs-lookup"><span data-stu-id="8d0e0-129">Read-only</span></span><br/> | <span data-ttu-id="8d0e0-130">抓取表示已編制索引之 EKU 屬性的 [**eku**](eku.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-130">Retrieves the [**EKU**](eku.md) object that represents the indexed EKU property.</span></span> <span data-ttu-id="8d0e0-131">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-131">This is the default property.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="8d0e0-132">備註</span><span class="sxs-lookup"><span data-stu-id="8d0e0-132">Remarks</span></span>

<span data-ttu-id="8d0e0-133">這個集合是由 [**ExtendedKeyUsage**](extendedkeyusage-ekus.md) 屬性所抓取。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-133">This collection is retrieved by the [**ExtendedKeyUsage.EKUs**](extendedkeyusage-ekus.md) property.</span></span>

<span data-ttu-id="8d0e0-134">無法建立 **eku** 物件。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-134">The **EKUs** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d0e0-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d0e0-135">Requirements</span></span>



| <span data-ttu-id="8d0e0-136">需求</span><span class="sxs-lookup"><span data-stu-id="8d0e0-136">Requirement</span></span> | <span data-ttu-id="8d0e0-137">值</span><span class="sxs-lookup"><span data-stu-id="8d0e0-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d0e0-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="8d0e0-138">End of client support</span></span><br/> | <span data-ttu-id="8d0e0-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d0e0-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8d0e0-140">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="8d0e0-140">End of server support</span></span><br/> | <span data-ttu-id="8d0e0-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d0e0-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8d0e0-142">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8d0e0-142">Redistributable</span></span><br/>       | <span data-ttu-id="8d0e0-143">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="8d0e0-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8d0e0-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8d0e0-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8d0e0-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d0e0-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
