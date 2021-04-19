---
description: 代表 ExtendedProperty 物件的集合。
ms.assetid: 9de25994-9f0b-47a0-b4c8-781aec782f88
title: ExtendedProperties 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 512c29e43b9099d9ef577cce61bbcc3a38d68ac6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989654"
---
# <a name="extendedproperties-object"></a><span data-ttu-id="3c9d5-103">ExtendedProperties 物件</span><span class="sxs-lookup"><span data-stu-id="3c9d5-103">ExtendedProperties object</span></span>

<span data-ttu-id="3c9d5-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3c9d5-105">相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CertGetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) 並取得屬性。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="3c9d5-106">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="3c9d5-107">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="3c9d5-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="3c9d5-108">**ExtendedProperties** 物件代表 [**ExtendedProperty**](extendedproperty.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-108">The **ExtendedProperties** object represents a collection of [**ExtendedProperty**](extendedproperty.md) objects.</span></span> <span data-ttu-id="3c9d5-109">每個物件都代表單一的擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-109">Each object represents a single extended property.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="3c9d5-110">使用時機</span><span class="sxs-lookup"><span data-stu-id="3c9d5-110">When to use</span></span>

<span data-ttu-id="3c9d5-111">**ExtendedProperties** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="3c9d5-111">The **ExtendedProperties** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="3c9d5-112">從集合中加入或移除 [**ExtendedProperty**](extendedproperty.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-112">Add or remove an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span>
-   <span data-ttu-id="3c9d5-113">取得集合中的擴充屬性數目。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-113">Retrieve the number of extended properties in the collection.</span></span>
-   <span data-ttu-id="3c9d5-114">從集合中取出特定的 [**ExtendedProperty**](extendedproperty.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-114">Retrieve a specific [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span>
-   <span data-ttu-id="3c9d5-115">逐一查看集合。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-115">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="3c9d5-116">成員</span><span class="sxs-lookup"><span data-stu-id="3c9d5-116">Members</span></span>

<span data-ttu-id="3c9d5-117">**ExtendedProperties** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3c9d5-117">The **ExtendedProperties** object has these types of members:</span></span>

-   [<span data-ttu-id="3c9d5-118">方法</span><span class="sxs-lookup"><span data-stu-id="3c9d5-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="3c9d5-119">屬性</span><span class="sxs-lookup"><span data-stu-id="3c9d5-119">Properties</span></span>](#extendedproperties-object)

### <a name="methods"></a><span data-ttu-id="3c9d5-120">方法</span><span class="sxs-lookup"><span data-stu-id="3c9d5-120">Methods</span></span>

<span data-ttu-id="3c9d5-121">**ExtendedProperties** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-121">The **ExtendedProperties** object has these methods.</span></span>



| <span data-ttu-id="3c9d5-122">方法</span><span class="sxs-lookup"><span data-stu-id="3c9d5-122">Method</span></span>                                      | <span data-ttu-id="3c9d5-123">描述</span><span class="sxs-lookup"><span data-stu-id="3c9d5-123">Description</span></span>                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c9d5-124">**添加**</span><span class="sxs-lookup"><span data-stu-id="3c9d5-124">**Add**</span></span>](extendedproperties-add.md)       | <span data-ttu-id="3c9d5-125">將 [**ExtendedProperty**](extendedproperty.md) 物件加入至集合。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-125">Adds an [**ExtendedProperty**](extendedproperty.md) object to the collection.</span></span><br/>      |
| [<span data-ttu-id="3c9d5-126">**移除**</span><span class="sxs-lookup"><span data-stu-id="3c9d5-126">**Remove**</span></span>](extendedproperties-remove.md) | <span data-ttu-id="3c9d5-127">從集合中移除 [**ExtendedProperty**](extendedproperty.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-127">Removes an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3c9d5-128">屬性</span><span class="sxs-lookup"><span data-stu-id="3c9d5-128">Properties</span></span>

<span data-ttu-id="3c9d5-129">**ExtendedProperties** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-129">The **ExtendedProperties** object has these properties.</span></span>



| <span data-ttu-id="3c9d5-130">屬性</span><span class="sxs-lookup"><span data-stu-id="3c9d5-130">Property</span></span>                                                   | <span data-ttu-id="3c9d5-131">存取類型</span><span class="sxs-lookup"><span data-stu-id="3c9d5-131">Access type</span></span>          | <span data-ttu-id="3c9d5-132">Description</span><span class="sxs-lookup"><span data-stu-id="3c9d5-132">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c9d5-133">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="3c9d5-133">**\_NewEnum**</span></span>](extendedproperties-newenum.md)<br/> | <span data-ttu-id="3c9d5-134">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9d5-134">Read-only</span></span><br/> | <span data-ttu-id="3c9d5-135">在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-135">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="3c9d5-136">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-136">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="3c9d5-137">**計數**</span><span class="sxs-lookup"><span data-stu-id="3c9d5-137">**Count**</span></span>](extendedproperties-count.md)<br/>       | <span data-ttu-id="3c9d5-138">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9d5-138">Read-only</span></span><br/> | <span data-ttu-id="3c9d5-139">抓取集合中的 [**ExtendedProperty**](extendedproperty.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-139">Retrieves the number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="3c9d5-140">**項目**</span><span class="sxs-lookup"><span data-stu-id="3c9d5-140">**Item**</span></span>](extendedproperties-item.md)<br/>         | <span data-ttu-id="3c9d5-141">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9d5-141">Read-only</span></span><br/> | <span data-ttu-id="3c9d5-142">抓取 [**ExtendedProperty**](extendedproperty.md) 物件，該物件代表集合的索引延伸屬性。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-142">Retrieves an [**ExtendedProperty**](extendedproperty.md) object that represents the indexed extended property of the collection.</span></span> <span data-ttu-id="3c9d5-143">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-143">This is the default property.</span></span><br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="3c9d5-144">備註</span><span class="sxs-lookup"><span data-stu-id="3c9d5-144">Remarks</span></span>

<span data-ttu-id="3c9d5-145">無法建立 **ExtendedProperties** 物件。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-145">The **ExtendedProperties** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c9d5-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c9d5-146">Requirements</span></span>



| <span data-ttu-id="3c9d5-147">需求</span><span class="sxs-lookup"><span data-stu-id="3c9d5-147">Requirement</span></span> | <span data-ttu-id="3c9d5-148">值</span><span class="sxs-lookup"><span data-stu-id="3c9d5-148">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c9d5-149">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="3c9d5-149">End of client support</span></span><br/> | <span data-ttu-id="3c9d5-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c9d5-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3c9d5-151">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="3c9d5-151">End of server support</span></span><br/> | <span data-ttu-id="3c9d5-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c9d5-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3c9d5-153">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="3c9d5-153">Redistributable</span></span><br/>       | <span data-ttu-id="3c9d5-154">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="3c9d5-154">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3c9d5-155">DLL</span><span class="sxs-lookup"><span data-stu-id="3c9d5-155">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3c9d5-156"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c9d5-156"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
