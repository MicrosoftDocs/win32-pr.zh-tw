---
description: 表示屬性物件的集合。
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Attributes 物件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2493d4e1bbcbeb2dc7e7b335513beb84c3f28d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978652"
---
# <a name="attributes-object"></a><span data-ttu-id="d3721-103">Attributes 物件</span><span class="sxs-lookup"><span data-stu-id="d3721-103">Attributes object</span></span>

<span data-ttu-id="d3721-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="d3721-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="d3721-105">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**CryptographicAttributeObjectCollection 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true)。\]</span><span class="sxs-lookup"><span data-stu-id="d3721-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="d3721-106">**Attributes** 物件表示 [**屬性**](attribute.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="d3721-106">The **Attributes** object represents a collection of [**Attribute**](attribute.md) objects.</span></span> <span data-ttu-id="d3721-107">每個 [**屬性**](attribute.md) 物件都代表訊息的單一屬性。</span><span class="sxs-lookup"><span data-stu-id="d3721-107">Each [**Attribute**](attribute.md) object represents a single attribute of a message.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="d3721-108">使用時機</span><span class="sxs-lookup"><span data-stu-id="d3721-108">When to use</span></span>

<span data-ttu-id="d3721-109">**Attributes** 物件用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="d3721-109">The **Attributes** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="d3721-110">新增或移除集合中的特定 [**屬性**](attribute.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d3721-110">Add or remove a specific [**Attribute**](attribute.md) object from the collection.</span></span>
-   <span data-ttu-id="d3721-111">清除集合。</span><span class="sxs-lookup"><span data-stu-id="d3721-111">Clear the collection.</span></span>
-   <span data-ttu-id="d3721-112">取得集合中的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="d3721-112">Retrieve the number of attributes in the collection.</span></span>
-   <span data-ttu-id="d3721-113">從集合中取出特定 [**屬性**](attribute.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d3721-113">Retrieve a specific [**Attribute**](attribute.md) object from the collection.</span></span>
-   <span data-ttu-id="d3721-114">逐一查看集合。</span><span class="sxs-lookup"><span data-stu-id="d3721-114">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="d3721-115">成員</span><span class="sxs-lookup"><span data-stu-id="d3721-115">Members</span></span>

<span data-ttu-id="d3721-116">**Attributes** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d3721-116">The **Attributes** object has these types of members:</span></span>

-   [<span data-ttu-id="d3721-117">方法</span><span class="sxs-lookup"><span data-stu-id="d3721-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="d3721-118">屬性</span><span class="sxs-lookup"><span data-stu-id="d3721-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d3721-119">方法</span><span class="sxs-lookup"><span data-stu-id="d3721-119">Methods</span></span>

<span data-ttu-id="d3721-120">**Attributes** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d3721-120">The **Attributes** object has these methods.</span></span>



| <span data-ttu-id="d3721-121">方法</span><span class="sxs-lookup"><span data-stu-id="d3721-121">Method</span></span>                              | <span data-ttu-id="d3721-122">描述</span><span class="sxs-lookup"><span data-stu-id="d3721-122">Description</span></span>                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="d3721-123">**添加**</span><span class="sxs-lookup"><span data-stu-id="d3721-123">**Add**</span></span>](attributes-add.md)       | <span data-ttu-id="d3721-124">將 [**屬性**](attribute.md) 物件加入至集合。</span><span class="sxs-lookup"><span data-stu-id="d3721-124">Adds an [**Attribute**](attribute.md) object to the collection.</span></span><br/>       |
| [<span data-ttu-id="d3721-125">**清楚**</span><span class="sxs-lookup"><span data-stu-id="d3721-125">**Clear**</span></span>](attributes-clear.md)   | <span data-ttu-id="d3721-126">清除集合中的所有 [**屬性**](attribute.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d3721-126">Clears all [**Attribute**](attribute.md) objects from the collection.</span></span><br/> |
| [<span data-ttu-id="d3721-127">**移除**</span><span class="sxs-lookup"><span data-stu-id="d3721-127">**Remove**</span></span>](attributes-remove.md) | <span data-ttu-id="d3721-128">從集合中移除 [**屬性**](attribute.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d3721-128">Removes an [**Attribute**](attribute.md) object from the collection.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="d3721-129">屬性</span><span class="sxs-lookup"><span data-stu-id="d3721-129">Properties</span></span>

<span data-ttu-id="d3721-130">**Attributes** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d3721-130">The **Attributes** object has these properties.</span></span>



| <span data-ttu-id="d3721-131">屬性</span><span class="sxs-lookup"><span data-stu-id="d3721-131">Property</span></span>                                           | <span data-ttu-id="d3721-132">存取類型</span><span class="sxs-lookup"><span data-stu-id="d3721-132">Access type</span></span>          | <span data-ttu-id="d3721-133">Description</span><span class="sxs-lookup"><span data-stu-id="d3721-133">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3721-134">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="d3721-134">**\_NewEnum**</span></span>](attributes-newenum.md)<br/> | <span data-ttu-id="d3721-135">唯讀</span><span class="sxs-lookup"><span data-stu-id="d3721-135">Read-only</span></span><br/> | <span data-ttu-id="d3721-136">在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="d3721-136">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="d3721-137">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="d3721-137">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="d3721-138">**計數**</span><span class="sxs-lookup"><span data-stu-id="d3721-138">**Count**</span></span>](attributes-count.md)<br/>       | <span data-ttu-id="d3721-139">唯讀</span><span class="sxs-lookup"><span data-stu-id="d3721-139">Read-only</span></span><br/> | <span data-ttu-id="d3721-140">抓取集合中的 [**屬性**](attribute.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="d3721-140">Retrieves the number of [**Attribute**](attribute.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="d3721-141">**項目**</span><span class="sxs-lookup"><span data-stu-id="d3721-141">**Item**</span></span>](attributes-item.md)<br/>         | <span data-ttu-id="d3721-142">唯讀</span><span class="sxs-lookup"><span data-stu-id="d3721-142">Read-only</span></span><br/> | <span data-ttu-id="d3721-143">抓取代表索引屬性的 [**屬性**](attribute.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d3721-143">Retrieves the [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span> <span data-ttu-id="d3721-144">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="d3721-144">This is the default property.</span></span><br/>                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="d3721-145">備註</span><span class="sxs-lookup"><span data-stu-id="d3721-145">Remarks</span></span>

<span data-ttu-id="d3721-146">無法建立 **屬性** 物件。</span><span class="sxs-lookup"><span data-stu-id="d3721-146">The **Attributes** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3721-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3721-147">Requirements</span></span>



| <span data-ttu-id="d3721-148">需求</span><span class="sxs-lookup"><span data-stu-id="d3721-148">Requirement</span></span> | <span data-ttu-id="d3721-149">值</span><span class="sxs-lookup"><span data-stu-id="d3721-149">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3721-150">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d3721-150">End of client support</span></span><br/> | <span data-ttu-id="d3721-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3721-151">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d3721-152">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d3721-152">End of server support</span></span><br/> | <span data-ttu-id="d3721-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3721-153">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d3721-154">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d3721-154">Redistributable</span></span><br/>       | <span data-ttu-id="d3721-155">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d3721-155">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d3721-156">DLL</span><span class="sxs-lookup"><span data-stu-id="d3721-156">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d3721-157"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3721-157"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3721-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3721-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3721-159">加密物件</span><span class="sxs-lookup"><span data-stu-id="d3721-159">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
