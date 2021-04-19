---
description: 表示 OID 物件的集合。
ms.assetid: 2c4ff87a-58e1-46aa-9680-29062b05308c
title: Oid 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 894689c214d8b7d352a2453d2d62c847866b9bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990105"
---
# <a name="oids-object"></a><span data-ttu-id="3d009-103">Oid 物件</span><span class="sxs-lookup"><span data-stu-id="3d009-103">OIDs object</span></span>

<span data-ttu-id="3d009-104">\[**Oid** 物件可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="3d009-104">\[The **OIDs** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3d009-105">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**OidCollection 類別**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="3d009-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="3d009-106">**Oid** 物件代表 [**oid**](oid.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="3d009-106">The **OIDs** object represents a collection of [**OID**](oid.md) objects.</span></span> <span data-ttu-id="3d009-107">每個 [**OID**](oid.md) 物件都代表一個物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d009-107">Each [**OID**](oid.md) object represents a single object identifier.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="3d009-108">使用時機</span><span class="sxs-lookup"><span data-stu-id="3d009-108">When to use</span></span>

<span data-ttu-id="3d009-109">**Oid** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="3d009-109">The **OIDs** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="3d009-110">從集合中加入或移除 [**OID**](oid.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3d009-110">Add or remove an [**OID**](oid.md) object from the collection.</span></span>
-   <span data-ttu-id="3d009-111">清除集合中的所有 [**OID**](oid.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3d009-111">Clear all the [**OID**](oid.md) objects from the collection.</span></span>
-   <span data-ttu-id="3d009-112">取得集合中的物件識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="3d009-112">Retrieve the number of object identifiers in the collection.</span></span>
-   <span data-ttu-id="3d009-113">從集合中取出特定的 [**OID**](oid.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3d009-113">Retrieve a specific [**OID**](oid.md) object from the collection.</span></span>
-   <span data-ttu-id="3d009-114">逐一查看集合。</span><span class="sxs-lookup"><span data-stu-id="3d009-114">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="3d009-115">成員</span><span class="sxs-lookup"><span data-stu-id="3d009-115">Members</span></span>

<span data-ttu-id="3d009-116">**Oid** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3d009-116">The **OIDs** object has these types of members:</span></span>

-   [<span data-ttu-id="3d009-117">方法</span><span class="sxs-lookup"><span data-stu-id="3d009-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="3d009-118">屬性</span><span class="sxs-lookup"><span data-stu-id="3d009-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3d009-119">方法</span><span class="sxs-lookup"><span data-stu-id="3d009-119">Methods</span></span>

<span data-ttu-id="3d009-120">**Oid** 物件具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3d009-120">The **OIDs** object has these methods.</span></span>



| <span data-ttu-id="3d009-121">方法</span><span class="sxs-lookup"><span data-stu-id="3d009-121">Method</span></span>                        | <span data-ttu-id="3d009-122">描述</span><span class="sxs-lookup"><span data-stu-id="3d009-122">Description</span></span>                                                                  |
|:------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="3d009-123">**添加**</span><span class="sxs-lookup"><span data-stu-id="3d009-123">**Add**</span></span>](oids-add.md)       | <span data-ttu-id="3d009-124">將 [**OID**](oid.md) 物件加入至集合。</span><span class="sxs-lookup"><span data-stu-id="3d009-124">Adds an [**OID**](oid.md) object to the collection.</span></span><br/>              |
| [<span data-ttu-id="3d009-125">**清楚**</span><span class="sxs-lookup"><span data-stu-id="3d009-125">**Clear**</span></span>](oids-clear.md)   | <span data-ttu-id="3d009-126">從集合中清除所有 [**OID**](oid.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3d009-126">Clears all [**OID**](oid.md) objects from the collection.</span></span><br/>        |
| [<span data-ttu-id="3d009-127">**移除**</span><span class="sxs-lookup"><span data-stu-id="3d009-127">**Remove**</span></span>](oids-remove.md) | <span data-ttu-id="3d009-128">從集合中移除已編制索引的 [**OID**](oid.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3d009-128">Removes an indexed [**OID**](oid.md) object from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3d009-129">屬性</span><span class="sxs-lookup"><span data-stu-id="3d009-129">Properties</span></span>

<span data-ttu-id="3d009-130">**Oid** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3d009-130">The **OIDs** object has these properties.</span></span>



| <span data-ttu-id="3d009-131">屬性</span><span class="sxs-lookup"><span data-stu-id="3d009-131">Property</span></span>                                     | <span data-ttu-id="3d009-132">存取類型</span><span class="sxs-lookup"><span data-stu-id="3d009-132">Access type</span></span>          | <span data-ttu-id="3d009-133">Description</span><span class="sxs-lookup"><span data-stu-id="3d009-133">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d009-134">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="3d009-134">**\_NewEnum**</span></span>](oids-newenum.md)<br/> | <span data-ttu-id="3d009-135">唯讀</span><span class="sxs-lookup"><span data-stu-id="3d009-135">Read-only</span></span><br/> | <span data-ttu-id="3d009-136">在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="3d009-136">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="3d009-137">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="3d009-137">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="3d009-138">**計數**</span><span class="sxs-lookup"><span data-stu-id="3d009-138">**Count**</span></span>](oids-count.md)<br/>       | <span data-ttu-id="3d009-139">唯讀</span><span class="sxs-lookup"><span data-stu-id="3d009-139">Read-only</span></span><br/> | <span data-ttu-id="3d009-140">抓取集合中的 [**OID**](oid.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="3d009-140">Retrieves the number of [**OID**](oid.md) objects in the collection.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="3d009-141">**項目**</span><span class="sxs-lookup"><span data-stu-id="3d009-141">**Item**</span></span>](oids-item.md)<br/>         | <span data-ttu-id="3d009-142">唯讀</span><span class="sxs-lookup"><span data-stu-id="3d009-142">Read-only</span></span><br/> | <span data-ttu-id="3d009-143">從集合中抓取索引的 [**OID**](oid.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3d009-143">Retrieves an indexed [**OID**](oid.md) object from the collection.</span></span> <span data-ttu-id="3d009-144">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="3d009-144">This is the default property.</span></span><br/>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="3d009-145">備註</span><span class="sxs-lookup"><span data-stu-id="3d009-145">Remarks</span></span>

<span data-ttu-id="3d009-146">無法建立 **oid** 物件。</span><span class="sxs-lookup"><span data-stu-id="3d009-146">The **OIDs** object cannot be created.</span></span>

<span data-ttu-id="3d009-147">**Oid** 物件是由下列屬性使用：</span><span class="sxs-lookup"><span data-stu-id="3d009-147">The **OIDs** object is used by the following properties:</span></span>

-   [<span data-ttu-id="3d009-148">**CertificateStatus.ApplicationPolicies**</span><span class="sxs-lookup"><span data-stu-id="3d009-148">**CertificateStatus.ApplicationPolicies**</span></span>](certificatestatus-applicationpolicies.md)
-   [<span data-ttu-id="3d009-149">**CertificateStatus.CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="3d009-149">**CertificateStatus.CertificatePolicies**</span></span>](certificatestatus-certificatepolicies.md)

## <a name="requirements"></a><span data-ttu-id="3d009-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d009-150">Requirements</span></span>



| <span data-ttu-id="3d009-151">需求</span><span class="sxs-lookup"><span data-stu-id="3d009-151">Requirement</span></span> | <span data-ttu-id="3d009-152">值</span><span class="sxs-lookup"><span data-stu-id="3d009-152">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d009-153">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="3d009-153">Redistributable</span></span><br/> | <span data-ttu-id="3d009-154">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="3d009-154">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3d009-155">DLL</span><span class="sxs-lookup"><span data-stu-id="3d009-155">DLL</span></span><br/>             | <dl> <span data-ttu-id="3d009-156"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d009-156"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
