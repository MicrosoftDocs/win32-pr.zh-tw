---
description: 代表 (CPS) 指標或使用者注意事項辨識符號的認證實務聲明。
ms.assetid: 857af3d6-aa7b-429a-a056-72573232f72c
title: 限定詞物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1740e064cac53f93d9c81603477a1230c7fd7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983056"
---
# <a name="qualifier-object"></a><span data-ttu-id="09117-103">限定詞物件</span><span class="sxs-lookup"><span data-stu-id="09117-103">Qualifier object</span></span>

<span data-ttu-id="09117-104">\[**限定詞** 物件可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="09117-104">\[The **Qualifier** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="09117-105">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 Oid 來處理憑證原則延伸中屬於原則資訊的限定詞。\]</span><span class="sxs-lookup"><span data-stu-id="09117-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="09117-106">辨識 **符號** 物件代表 (CPS) 指標或使用者注意事項辨識符號的認證實務聲明。</span><span class="sxs-lookup"><span data-stu-id="09117-106">The **Qualifier** object represents a Certification Practice Statement (CPS) pointer or user notice qualifier.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="09117-107">使用時機</span><span class="sxs-lookup"><span data-stu-id="09117-107">When to use</span></span>

<span data-ttu-id="09117-108">辨識 **符號** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="09117-108">The **Qualifier** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="09117-109">取出辨識符號的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="09117-109">Retrieve the object identifier of the qualifier.</span></span>
-   <span data-ttu-id="09117-110">抓取 (URI) 的統一資源識別項，指向 [*憑證授權單位*](../secgloss/c-gly.md) 單位 (CA) 發佈的 CPS。</span><span class="sxs-lookup"><span data-stu-id="09117-110">Retrieve the Uniform Resource Identifier (URI) that points to a CPS published by the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>
-   <span data-ttu-id="09117-111">取出與辨識符號相關聯的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="09117-111">Retrieve the name of the organization associated with the qualifier.</span></span>
-   <span data-ttu-id="09117-112">取出使用者通知的名稱和內容。</span><span class="sxs-lookup"><span data-stu-id="09117-112">Retrieve the name and content of a user notice.</span></span>

## <a name="members"></a><span data-ttu-id="09117-113">成員</span><span class="sxs-lookup"><span data-stu-id="09117-113">Members</span></span>

<span data-ttu-id="09117-114">**限定詞** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="09117-114">The **Qualifier** object has these types of members:</span></span>

-   [<span data-ttu-id="09117-115">屬性</span><span class="sxs-lookup"><span data-stu-id="09117-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09117-116">屬性</span><span class="sxs-lookup"><span data-stu-id="09117-116">Properties</span></span>

<span data-ttu-id="09117-117">**限定詞** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="09117-117">The **Qualifier** object has these properties.</span></span>



| <span data-ttu-id="09117-118">屬性</span><span class="sxs-lookup"><span data-stu-id="09117-118">Property</span></span>                                                          | <span data-ttu-id="09117-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="09117-119">Access type</span></span>          | <span data-ttu-id="09117-120">Description</span><span class="sxs-lookup"><span data-stu-id="09117-120">Description</span></span>                                                                                                                         |
|:------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09117-121">**CPSPointer**</span><span class="sxs-lookup"><span data-stu-id="09117-121">**CPSPointer**</span></span>](qualifier-cpspointer.md)<br/>             | <span data-ttu-id="09117-122">唯讀</span><span class="sxs-lookup"><span data-stu-id="09117-122">Read-only</span></span><br/> | <span data-ttu-id="09117-123">抓取包含指向 CA 所發佈之 CPS 之 URI 的字串。</span><span class="sxs-lookup"><span data-stu-id="09117-123">Retrieves a string that contains the URI that points to a CPS published by the CA.</span></span><br/>                                       |
| [<span data-ttu-id="09117-124">**ExplicitText**</span><span class="sxs-lookup"><span data-stu-id="09117-124">**ExplicitText**</span></span>](qualifier-explicittext.md)<br/>         | <span data-ttu-id="09117-125">唯讀</span><span class="sxs-lookup"><span data-stu-id="09117-125">Read-only</span></span><br/> | <span data-ttu-id="09117-126">抓取包含使用者通知內容的字串。</span><span class="sxs-lookup"><span data-stu-id="09117-126">Retrieves a string that contains the content of the user notice.</span></span> <span data-ttu-id="09117-127">這個屬性可以是空的。</span><span class="sxs-lookup"><span data-stu-id="09117-127">This property may be empty.</span></span><br/>                             |
| [<span data-ttu-id="09117-128">**NoticeNumbers**</span><span class="sxs-lookup"><span data-stu-id="09117-128">**NoticeNumbers**</span></span>](qualifier-noticenumbers.md)<br/>       | <span data-ttu-id="09117-129">唯讀</span><span class="sxs-lookup"><span data-stu-id="09117-129">Read-only</span></span><br/> | <span data-ttu-id="09117-130">抓取包含使用者聲明編號集合的 **NoticeNumbers** 物件。</span><span class="sxs-lookup"><span data-stu-id="09117-130">Retrieves a **NoticeNumbers** object that contains the collection of user notice numbers.</span></span> <span data-ttu-id="09117-131">這個屬性可以是空的。</span><span class="sxs-lookup"><span data-stu-id="09117-131">This property may be empty.</span></span><br/>    |
| [<span data-ttu-id="09117-132">**老**</span><span class="sxs-lookup"><span data-stu-id="09117-132">**OID**</span></span>](qualifier-oid.md)<br/>                           | <span data-ttu-id="09117-133">唯讀</span><span class="sxs-lookup"><span data-stu-id="09117-133">Read-only</span></span><br/> | <span data-ttu-id="09117-134">抓取識別辨識符號的 [**OID**](oid.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="09117-134">Retrieves an [**OID**](oid.md) object that identifies the qualifier.</span></span> <span data-ttu-id="09117-135">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="09117-135">This is the default property.</span></span><br/>                      |
| [<span data-ttu-id="09117-136">**OrganizationName**</span><span class="sxs-lookup"><span data-stu-id="09117-136">**OrganizationName**</span></span>](qualifier-organizationname.md)<br/> | <span data-ttu-id="09117-137">唯讀</span><span class="sxs-lookup"><span data-stu-id="09117-137">Read-only</span></span><br/> | <span data-ttu-id="09117-138">抓取字串，其中包含與辨識符號相關聯的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="09117-138">Retrieves a string that contains the name of the organization associated with the qualifier.</span></span> <span data-ttu-id="09117-139">這個屬性可以是空的。</span><span class="sxs-lookup"><span data-stu-id="09117-139">This property may be empty.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="09117-140">備註</span><span class="sxs-lookup"><span data-stu-id="09117-140">Remarks</span></span>

<span data-ttu-id="09117-141">無法建立 **限定詞** 物件。</span><span class="sxs-lookup"><span data-stu-id="09117-141">The **Qualifier** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="09117-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="09117-142">Requirements</span></span>



| <span data-ttu-id="09117-143">需求</span><span class="sxs-lookup"><span data-stu-id="09117-143">Requirement</span></span> | <span data-ttu-id="09117-144">值</span><span class="sxs-lookup"><span data-stu-id="09117-144">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09117-145">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="09117-145">Redistributable</span></span><br/> | <span data-ttu-id="09117-146">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="09117-146">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="09117-147">DLL</span><span class="sxs-lookup"><span data-stu-id="09117-147">DLL</span></span><br/>             | <dl> <span data-ttu-id="09117-148"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09117-148"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
