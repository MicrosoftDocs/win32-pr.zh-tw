---
description: 表示擴充物件的集合。
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Extension 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3af518d6f1918c82d5819b04a086195c06b79740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976110"
---
# <a name="extensions-object"></a><span data-ttu-id="e721d-103">Extension 物件</span><span class="sxs-lookup"><span data-stu-id="e721d-103">Extensions object</span></span>

<span data-ttu-id="e721d-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="e721d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e721d-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ExtensionCollection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="e721d-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e721d-106">**Extensions** 物件代表 [**擴充**](extension.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="e721d-106">The **Extensions** object represents a collection of [**Extension**](extension.md) objects.</span></span> <span data-ttu-id="e721d-107">每個 [**擴充**](extension.md) 物件都代表一個憑證延伸。</span><span class="sxs-lookup"><span data-stu-id="e721d-107">Each [**Extension**](extension.md) object represents a single certificate extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="e721d-108">使用時機</span><span class="sxs-lookup"><span data-stu-id="e721d-108">When to use</span></span>

<span data-ttu-id="e721d-109">**擴充** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="e721d-109">The **Extensions** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="e721d-110">取得集合中的憑證擴充功能數目。</span><span class="sxs-lookup"><span data-stu-id="e721d-110">Retrieve the number of certificate extensions in the collection.</span></span>
-   <span data-ttu-id="e721d-111">從集合中取出特定的 [**擴充**](extension.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e721d-111">Retrieve a specific [**Extension**](extension.md) object from the collection.</span></span>
-   <span data-ttu-id="e721d-112">逐一查看集合。</span><span class="sxs-lookup"><span data-stu-id="e721d-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="e721d-113">成員</span><span class="sxs-lookup"><span data-stu-id="e721d-113">Members</span></span>

<span data-ttu-id="e721d-114">**擴充** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e721d-114">The **Extensions** object has these types of members:</span></span>

-   [<span data-ttu-id="e721d-115">屬性</span><span class="sxs-lookup"><span data-stu-id="e721d-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e721d-116">屬性</span><span class="sxs-lookup"><span data-stu-id="e721d-116">Properties</span></span>

<span data-ttu-id="e721d-117">**Extensions** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e721d-117">The **Extensions** object has these properties.</span></span>



| <span data-ttu-id="e721d-118">屬性</span><span class="sxs-lookup"><span data-stu-id="e721d-118">Property</span></span>                                           | <span data-ttu-id="e721d-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="e721d-119">Access type</span></span>          | <span data-ttu-id="e721d-120">Description</span><span class="sxs-lookup"><span data-stu-id="e721d-120">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e721d-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="e721d-121">**\_NewEnum**</span></span>](extensions-newenum.md)<br/> | <span data-ttu-id="e721d-122">唯讀</span><span class="sxs-lookup"><span data-stu-id="e721d-122">Read-only</span></span><br/> | <span data-ttu-id="e721d-123">在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="e721d-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="e721d-124">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="e721d-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="e721d-125">**計數**</span><span class="sxs-lookup"><span data-stu-id="e721d-125">**Count**</span></span>](extensions-count.md)<br/>       | <span data-ttu-id="e721d-126">唯讀</span><span class="sxs-lookup"><span data-stu-id="e721d-126">Read-only</span></span><br/> | <span data-ttu-id="e721d-127">抓取集合中的 [**擴充**](extension.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="e721d-127">Retrieves the number of [**Extension**](extension.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="e721d-128">**項目**</span><span class="sxs-lookup"><span data-stu-id="e721d-128">**Item**</span></span>](extensions-item.md)<br/>         | <span data-ttu-id="e721d-129">唯讀</span><span class="sxs-lookup"><span data-stu-id="e721d-129">Read-only</span></span><br/> | <span data-ttu-id="e721d-130">抓取代表集合之索引憑證延伸的 [**擴充**](extension.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e721d-130">Retrieves the [**Extension**](extension.md) object that represents the indexed certificate extension of the collection.</span></span> <span data-ttu-id="e721d-131">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="e721d-131">This is the default property.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="e721d-132">備註</span><span class="sxs-lookup"><span data-stu-id="e721d-132">Remarks</span></span>

<span data-ttu-id="e721d-133">**Extension** 物件是由 [**Certificate. extension**](certificate-extensions.md)方法傳回。</span><span class="sxs-lookup"><span data-stu-id="e721d-133">The **Extensions** object is returned by the [**Certificate.Extensions**](certificate-extensions.md) method.</span></span>

<span data-ttu-id="e721d-134">無法建立 **擴充** 物件。</span><span class="sxs-lookup"><span data-stu-id="e721d-134">The **Extensions** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="e721d-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="e721d-135">Requirements</span></span>



| <span data-ttu-id="e721d-136">需求</span><span class="sxs-lookup"><span data-stu-id="e721d-136">Requirement</span></span> | <span data-ttu-id="e721d-137">值</span><span class="sxs-lookup"><span data-stu-id="e721d-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e721d-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e721d-138">End of client support</span></span><br/> | <span data-ttu-id="e721d-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e721d-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e721d-140">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="e721d-140">End of server support</span></span><br/> | <span data-ttu-id="e721d-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e721d-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e721d-142">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="e721d-142">Redistributable</span></span><br/>       | <span data-ttu-id="e721d-143">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e721d-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e721d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e721d-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e721d-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e721d-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
