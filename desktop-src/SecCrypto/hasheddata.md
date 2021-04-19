---
description: 提供雜湊字串的功能。
ms.assetid: 893639c2-57b9-48f6-bf60-a21c3368ffeb
title: HashedData 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b6e54d7d2ca52ceafe500615af4063dfc7310b0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989500"
---
# <a name="hasheddata-object"></a><span data-ttu-id="a6df9-103">HashedData 物件</span><span class="sxs-lookup"><span data-stu-id="a6df9-103">HashedData object</span></span>

<span data-ttu-id="a6df9-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="a6df9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a6df9-105">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**HashAlgorithm 類別**](/previous-versions/windows/)。\]</span><span class="sxs-lookup"><span data-stu-id="a6df9-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="a6df9-106">**HashedData** 物件提供雜湊字串的功能。</span><span class="sxs-lookup"><span data-stu-id="a6df9-106">The **HashedData** object provides functionality for hashing a string.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="a6df9-107">使用時機</span><span class="sxs-lookup"><span data-stu-id="a6df9-107">When to use</span></span>

<span data-ttu-id="a6df9-108">**HashedData** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="a6df9-108">The **HashedData** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="a6df9-109">指定包含要雜湊之資料的內容字串。</span><span class="sxs-lookup"><span data-stu-id="a6df9-109">Specify the content string that contains the data to be hashed.</span></span>
-   <span data-ttu-id="a6df9-110">將指定的雜湊演算法套用至內容字串。</span><span class="sxs-lookup"><span data-stu-id="a6df9-110">Apply a specified hash algorithm to the content string.</span></span>

## <a name="members"></a><span data-ttu-id="a6df9-111">成員</span><span class="sxs-lookup"><span data-stu-id="a6df9-111">Members</span></span>

<span data-ttu-id="a6df9-112">**HashedData** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a6df9-112">The **HashedData** object has these types of members:</span></span>

-   [<span data-ttu-id="a6df9-113">方法</span><span class="sxs-lookup"><span data-stu-id="a6df9-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="a6df9-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a6df9-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a6df9-115">方法</span><span class="sxs-lookup"><span data-stu-id="a6df9-115">Methods</span></span>

<span data-ttu-id="a6df9-116">**HashedData** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a6df9-116">The **HashedData** object has these methods.</span></span>



| <span data-ttu-id="a6df9-117">方法</span><span class="sxs-lookup"><span data-stu-id="a6df9-117">Method</span></span>                          | <span data-ttu-id="a6df9-118">描述</span><span class="sxs-lookup"><span data-stu-id="a6df9-118">Description</span></span>                                        |
|:--------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="a6df9-119">**散 列**</span><span class="sxs-lookup"><span data-stu-id="a6df9-119">**Hash**</span></span>](hasheddata-hash.md) | <span data-ttu-id="a6df9-120">建立指定之字串的雜湊。</span><span class="sxs-lookup"><span data-stu-id="a6df9-120">Creates a hash of the specified string.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a6df9-121">屬性</span><span class="sxs-lookup"><span data-stu-id="a6df9-121">Properties</span></span>

<span data-ttu-id="a6df9-122">**HashedData** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a6df9-122">The **HashedData** object has these properties.</span></span>



| <span data-ttu-id="a6df9-123">屬性</span><span class="sxs-lookup"><span data-stu-id="a6df9-123">Property</span></span>                                             | <span data-ttu-id="a6df9-124">存取類型</span><span class="sxs-lookup"><span data-stu-id="a6df9-124">Access type</span></span>           | <span data-ttu-id="a6df9-125">Description</span><span class="sxs-lookup"><span data-stu-id="a6df9-125">Description</span></span>                                                                                                                                                                          |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6df9-126">**演算法**</span><span class="sxs-lookup"><span data-stu-id="a6df9-126">**Algorithm**</span></span>](hasheddata-algorithm.md)<br/> | <span data-ttu-id="a6df9-127">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a6df9-127">Read/write</span></span><br/> | <span data-ttu-id="a6df9-128">設定或抓取所使用的雜湊演算法類型。</span><span class="sxs-lookup"><span data-stu-id="a6df9-128">Sets or retrieves the type of hashing algorithm used.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="a6df9-129">**值**</span><span class="sxs-lookup"><span data-stu-id="a6df9-129">**Value**</span></span>](hasheddata-value.md)<br/>         | <span data-ttu-id="a6df9-130">唯讀</span><span class="sxs-lookup"><span data-stu-id="a6df9-130">Read-only</span></span><br/>  | <span data-ttu-id="a6df9-131">在成功呼叫 [**Hash**](hasheddata-hash.md) 方法之後，取得雜湊的資料。</span><span class="sxs-lookup"><span data-stu-id="a6df9-131">Retrieves the hashed data after successful calls to the [**Hash**](hasheddata-hash.md) method.</span></span> <span data-ttu-id="a6df9-132">雜湊會以十六進位格式傳回。</span><span class="sxs-lookup"><span data-stu-id="a6df9-132">The hash is returned in hexadecimal format.</span></span> <span data-ttu-id="a6df9-133">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="a6df9-133">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a6df9-134">備註</span><span class="sxs-lookup"><span data-stu-id="a6df9-134">Remarks</span></span>

<span data-ttu-id="a6df9-135">若要建立大量資料的雜湊，請呼叫每個資料片段的 [**雜湊**](hasheddata-hash.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a6df9-135">To create the hash of a large amount of data, call the [**Hash**](hasheddata-hash.md) method for each piece of data.</span></span> <span data-ttu-id="a6df9-136">在讀取屬性之前，會將每個資料片段的雜湊串連至 [**Value**](hasheddata-value.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="a6df9-136">The hash of each piece of data is concatenated to the [**Value**](hasheddata-value.md) property until the property is read.</span></span> <span data-ttu-id="a6df9-137">當讀取屬性時，會重設 **Value** 屬性的內容。</span><span class="sxs-lookup"><span data-stu-id="a6df9-137">The contents of the **Value** property are reset when the property is read.</span></span>

<span data-ttu-id="a6df9-138">您可以建立 **HashedData** 物件，而且可以安全地進行腳本處理。</span><span class="sxs-lookup"><span data-stu-id="a6df9-138">The **HashedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="a6df9-139">**HashedData** 物件的 ProgID 是「CAPICOM」。HashedData。 1 "。</span><span class="sxs-lookup"><span data-stu-id="a6df9-139">The ProgID for the **HashedData** object is "CAPICOM.HashedData.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="a6df9-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6df9-140">Requirements</span></span>



| <span data-ttu-id="a6df9-141">需求</span><span class="sxs-lookup"><span data-stu-id="a6df9-141">Requirement</span></span> | <span data-ttu-id="a6df9-142">值</span><span class="sxs-lookup"><span data-stu-id="a6df9-142">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6df9-143">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a6df9-143">End of client support</span></span><br/> | <span data-ttu-id="a6df9-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a6df9-144">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a6df9-145">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="a6df9-145">End of server support</span></span><br/> | <span data-ttu-id="a6df9-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6df9-146">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a6df9-147">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a6df9-147">Redistributable</span></span><br/>       | <span data-ttu-id="a6df9-148">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a6df9-148">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a6df9-149">DLL</span><span class="sxs-lookup"><span data-stu-id="a6df9-149">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a6df9-150"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6df9-150"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
