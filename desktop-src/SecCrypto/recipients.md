---
description: 代表憑證物件的集合。
ms.assetid: 11d294b5-0a8a-4970-be10-a3b22389d96e
title: 收件者物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c68ca0217631970f35680160b71841f758b13fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985954"
---
# <a name="recipients-object"></a><span data-ttu-id="f22cf-103">收件者物件</span><span class="sxs-lookup"><span data-stu-id="f22cf-103">Recipients object</span></span>

<span data-ttu-id="f22cf-104">\[[收件者 **] 物件可** 用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="f22cf-104">\[The **Recipients** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f22cf-105">相反地，請使用 [**CmsRecipientCollection 類別**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="f22cf-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="f22cf-106">收件者物件代表 [**憑證**](certificate.md)**物件的集合**。</span><span class="sxs-lookup"><span data-stu-id="f22cf-106">The **Recipients** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="f22cf-107">每個物件都代表封包訊息的預定收件者。</span><span class="sxs-lookup"><span data-stu-id="f22cf-107">Each object represents an intended recipient of the enveloped message.</span></span> <span data-ttu-id="f22cf-108">[**EnvelopedData**](envelopeddata.md)物件中的資料會使用 [*對稱*](../secgloss/s-gly.md)工作階段金鑰進行加密，而該對稱工作階段金鑰接著會使用來自該預定收件者憑證的公開金鑰，針對每個收件者進行加密。</span><span class="sxs-lookup"><span data-stu-id="f22cf-108">Data in an [**EnvelopedData**](envelopeddata.md) object is encrypted with a [*symmetric*](../secgloss/s-gly.md) session key, and that symmetric session key is then itself encrypted for each recipient by using the public key from that intended recipient's certificate.</span></span> <span data-ttu-id="f22cf-109">具有與憑證 [*公開金鑰*](../secgloss/p-gly.md)相關聯之 [*私密金鑰*](../secgloss/p-gly.md)存取權的收件者，可以將 [*工作階段金鑰*](../secgloss/s-gly.md)解密，並使用解密的工作階段金鑰來解密實際的資料。</span><span class="sxs-lookup"><span data-stu-id="f22cf-109">A recipient with access to the [*private key*](../secgloss/p-gly.md) associated with a certificate's [*public key*](../secgloss/p-gly.md) can decrypt the [*session key*](../secgloss/s-gly.md) and use the decrypted session key to decrypt the actual data.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="f22cf-110">使用時機</span><span class="sxs-lookup"><span data-stu-id="f22cf-110">When to use</span></span>

<span data-ttu-id="f22cf-111">收件 **者物件是** 用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="f22cf-111">The **Recipients** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="f22cf-112">新增或移除集合中的 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f22cf-112">Add or remove a [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="f22cf-113">取得集合中的憑證數目。</span><span class="sxs-lookup"><span data-stu-id="f22cf-113">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="f22cf-114">從集合中 **取出特定的** 收件者物件。</span><span class="sxs-lookup"><span data-stu-id="f22cf-114">Retrieve a specific **Recipients** object from the collection.</span></span>
-   <span data-ttu-id="f22cf-115">逐一查看集合。</span><span class="sxs-lookup"><span data-stu-id="f22cf-115">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="f22cf-116">成員</span><span class="sxs-lookup"><span data-stu-id="f22cf-116">Members</span></span>

<span data-ttu-id="f22cf-117">收件 **者物件有** 下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f22cf-117">The **Recipients** object has these types of members:</span></span>

-   [<span data-ttu-id="f22cf-118">方法</span><span class="sxs-lookup"><span data-stu-id="f22cf-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="f22cf-119">屬性</span><span class="sxs-lookup"><span data-stu-id="f22cf-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f22cf-120">方法</span><span class="sxs-lookup"><span data-stu-id="f22cf-120">Methods</span></span>

<span data-ttu-id="f22cf-121">收件 **者物件有** 這些方法。</span><span class="sxs-lookup"><span data-stu-id="f22cf-121">The **Recipients** object has these methods.</span></span>



| <span data-ttu-id="f22cf-122">方法</span><span class="sxs-lookup"><span data-stu-id="f22cf-122">Method</span></span>                              | <span data-ttu-id="f22cf-123">描述</span><span class="sxs-lookup"><span data-stu-id="f22cf-123">Description</span></span>                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="f22cf-124">**添加**</span><span class="sxs-lookup"><span data-stu-id="f22cf-124">**Add**</span></span>](recipients-add.md)       | <span data-ttu-id="f22cf-125">將 [**憑證**](certificate.md) 物件加入至集合。</span><span class="sxs-lookup"><span data-stu-id="f22cf-125">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/>         |
| [<span data-ttu-id="f22cf-126">**清楚**</span><span class="sxs-lookup"><span data-stu-id="f22cf-126">**Clear**</span></span>](recipients-clear.md)   | <span data-ttu-id="f22cf-127">從集合中移除所有的 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f22cf-127">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> |
| [<span data-ttu-id="f22cf-128">**移除**</span><span class="sxs-lookup"><span data-stu-id="f22cf-128">**Remove**</span></span>](recipients-remove.md) | <span data-ttu-id="f22cf-129">從集合中移除 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f22cf-129">Removes a [**Certificate**](certificate.md) object from the collection.</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="f22cf-130">屬性</span><span class="sxs-lookup"><span data-stu-id="f22cf-130">Properties</span></span>

<span data-ttu-id="f22cf-131">收件 **者物件具有** 這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f22cf-131">The **Recipients** object has these properties.</span></span>



| <span data-ttu-id="f22cf-132">屬性</span><span class="sxs-lookup"><span data-stu-id="f22cf-132">Property</span></span>                                           | <span data-ttu-id="f22cf-133">存取類型</span><span class="sxs-lookup"><span data-stu-id="f22cf-133">Access type</span></span>          | <span data-ttu-id="f22cf-134">Description</span><span class="sxs-lookup"><span data-stu-id="f22cf-134">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f22cf-135">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="f22cf-135">**\_NewEnum**</span></span>](recipients-newenum.md)<br/> | <span data-ttu-id="f22cf-136">唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cf-136">Read-only</span></span><br/> | <span data-ttu-id="f22cf-137">在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="f22cf-137">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="f22cf-138">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="f22cf-138">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="f22cf-139">**計數**</span><span class="sxs-lookup"><span data-stu-id="f22cf-139">**Count**</span></span>](recipients-count.md)<br/>       |                      | <span data-ttu-id="f22cf-140">收件 **者集合中的物件** 數目。</span><span class="sxs-lookup"><span data-stu-id="f22cf-140">The number of objects in the **Recipients** collection.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="f22cf-141">**項目**</span><span class="sxs-lookup"><span data-stu-id="f22cf-141">**Item**</span></span>](recipients-item.md)<br/>         |                      | <span data-ttu-id="f22cf-142">集合中的索引物件。</span><span class="sxs-lookup"><span data-stu-id="f22cf-142">An indexed object in the collection.</span></span> <span data-ttu-id="f22cf-143">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="f22cf-143">This is the default property.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="f22cf-144">備註</span><span class="sxs-lookup"><span data-stu-id="f22cf-144">Remarks</span></span>

<span data-ttu-id="f22cf-145">無法建立收件 **者物件。**</span><span class="sxs-lookup"><span data-stu-id="f22cf-145">The **Recipients** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="f22cf-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="f22cf-146">Requirements</span></span>



| <span data-ttu-id="f22cf-147">需求</span><span class="sxs-lookup"><span data-stu-id="f22cf-147">Requirement</span></span> | <span data-ttu-id="f22cf-148">值</span><span class="sxs-lookup"><span data-stu-id="f22cf-148">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f22cf-149">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f22cf-149">Redistributable</span></span><br/> | <span data-ttu-id="f22cf-150">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f22cf-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f22cf-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f22cf-151">DLL</span></span><br/>             | <dl> <span data-ttu-id="f22cf-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f22cf-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f22cf-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f22cf-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f22cf-154">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="f22cf-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
