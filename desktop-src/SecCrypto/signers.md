---
description: 表示簽署者物件的集合。
ms.assetid: 72e86acd-eb87-4eff-bd4e-327630ebbfc4
title: 簽署者物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 75eba0ecb2592bf7efc27ecdd63288179e306651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990035"
---
# <a name="signers-object"></a><span data-ttu-id="f9b21-103">簽署者物件</span><span class="sxs-lookup"><span data-stu-id="f9b21-103">Signers object</span></span>

<span data-ttu-id="f9b21-104">\[**簽署** 者物件可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="f9b21-104">\[The **Signers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f9b21-105">相反地，請使用 CmsSigner 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="f9b21-105">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="f9b21-106">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span><span class="sxs-lookup"><span data-stu-id="f9b21-106">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="f9b21-107">**簽署** 者物件代表 [**簽署者**](signer.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="f9b21-107">The **Signers** object represents a collection of [**Signer**](signer.md) objects.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="f9b21-108">使用時機</span><span class="sxs-lookup"><span data-stu-id="f9b21-108">When to use</span></span>

<span data-ttu-id="f9b21-109">**簽署** 者物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="f9b21-109">The **Signers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="f9b21-110">取得集合中的憑證數目。</span><span class="sxs-lookup"><span data-stu-id="f9b21-110">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="f9b21-111">從集合中取出特定的 **簽署** 者物件。</span><span class="sxs-lookup"><span data-stu-id="f9b21-111">Retrieve a specific **Signers** object from the collection.</span></span>
-   <span data-ttu-id="f9b21-112">逐一查看集合。</span><span class="sxs-lookup"><span data-stu-id="f9b21-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="f9b21-113">成員</span><span class="sxs-lookup"><span data-stu-id="f9b21-113">Members</span></span>

<span data-ttu-id="f9b21-114">**簽署** 者物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f9b21-114">The **Signers** object has these types of members:</span></span>

-   [<span data-ttu-id="f9b21-115">屬性</span><span class="sxs-lookup"><span data-stu-id="f9b21-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9b21-116">屬性</span><span class="sxs-lookup"><span data-stu-id="f9b21-116">Properties</span></span>

<span data-ttu-id="f9b21-117">**簽署** 者物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f9b21-117">The **Signers** object has these properties.</span></span>



| <span data-ttu-id="f9b21-118">屬性</span><span class="sxs-lookup"><span data-stu-id="f9b21-118">Property</span></span>                                        | <span data-ttu-id="f9b21-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="f9b21-119">Access type</span></span>          | <span data-ttu-id="f9b21-120">Description</span><span class="sxs-lookup"><span data-stu-id="f9b21-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9b21-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="f9b21-121">**\_NewEnum**</span></span>](signers-newenum.md)<br/> | <span data-ttu-id="f9b21-122">唯讀</span><span class="sxs-lookup"><span data-stu-id="f9b21-122">Read-only</span></span><br/> | <span data-ttu-id="f9b21-123">在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="f9b21-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="f9b21-124">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="f9b21-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="f9b21-125">**計數**</span><span class="sxs-lookup"><span data-stu-id="f9b21-125">**Count**</span></span>](signers-count.md)<br/>       | <span data-ttu-id="f9b21-126">唯讀</span><span class="sxs-lookup"><span data-stu-id="f9b21-126">Read-only</span></span><br/> | <span data-ttu-id="f9b21-127">集合中的 [**簽署者**](signer.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="f9b21-127">Number of [**Signer**](signer.md) objects in the collection.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="f9b21-128">**項目**</span><span class="sxs-lookup"><span data-stu-id="f9b21-128">**Item**</span></span>](signers-item.md)<br/>         | <span data-ttu-id="f9b21-129">唯讀</span><span class="sxs-lookup"><span data-stu-id="f9b21-129">Read-only</span></span><br/> | <span data-ttu-id="f9b21-130">抓取代表索引簽署者的 [**簽署者**](signer.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f9b21-130">Retrieves the [**Signer**](signer.md) object that represents the indexed signer.</span></span> <span data-ttu-id="f9b21-131">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="f9b21-131">This is the default property.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="f9b21-132">備註</span><span class="sxs-lookup"><span data-stu-id="f9b21-132">Remarks</span></span>

<span data-ttu-id="f9b21-133">無法建立 **簽署** 者物件。</span><span class="sxs-lookup"><span data-stu-id="f9b21-133">The **Signers** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9b21-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9b21-134">Requirements</span></span>



| <span data-ttu-id="f9b21-135">需求</span><span class="sxs-lookup"><span data-stu-id="f9b21-135">Requirement</span></span> | <span data-ttu-id="f9b21-136">值</span><span class="sxs-lookup"><span data-stu-id="f9b21-136">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b21-137">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f9b21-137">Redistributable</span></span><br/> | <span data-ttu-id="f9b21-138">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f9b21-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f9b21-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f9b21-139">DLL</span></span><br/>             | <dl> <span data-ttu-id="f9b21-140"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9b21-140"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9b21-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9b21-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9b21-142">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="f9b21-142">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
