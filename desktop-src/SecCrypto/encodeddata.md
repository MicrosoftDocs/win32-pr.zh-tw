---
description: 表示 asn.1 編碼資料的區塊。
ms.assetid: af7acc5f-da0a-4235-8496-05db94664ea5
title: EncodedData 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d05fce31ad4ef08bf9f573c0158a683bdbeba739
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996498"
---
# <a name="encodeddata-object"></a><span data-ttu-id="1568f-103">EncodedData 物件</span><span class="sxs-lookup"><span data-stu-id="1568f-103">EncodedData object</span></span>

<span data-ttu-id="1568f-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="1568f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1568f-105">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**AsnEncodedData 類別**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="1568f-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="1568f-106">**EncodedData** 物件代表一組 asn.1 編碼的資料。</span><span class="sxs-lookup"><span data-stu-id="1568f-106">The **EncodedData** object represents a block of ASN.1 encoded data.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="1568f-107">使用時機</span><span class="sxs-lookup"><span data-stu-id="1568f-107">When to use</span></span>

<span data-ttu-id="1568f-108">**EncodedData** 物件是由數個 CAPICOM 物件屬性所傳回。</span><span class="sxs-lookup"><span data-stu-id="1568f-108">The **EncodedData** object is returned by several CAPICOM object properties.</span></span> <span data-ttu-id="1568f-109">傳回時，這個物件會用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="1568f-109">When returned, this object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="1568f-110">取得編碼資料的字串表示。</span><span class="sxs-lookup"><span data-stu-id="1568f-110">Obtain a string representation of the encoded data.</span></span>
-   <span data-ttu-id="1568f-111">取得與編碼資料相關聯的解碼器物件（如果存在的話）。</span><span class="sxs-lookup"><span data-stu-id="1568f-111">Obtain the decoder object, if it exists, that is associated with the encoded data.</span></span>
-   <span data-ttu-id="1568f-112">決定編碼資料的類型。</span><span class="sxs-lookup"><span data-stu-id="1568f-112">Determine the type of encoded data.</span></span>

## <a name="members"></a><span data-ttu-id="1568f-113">成員</span><span class="sxs-lookup"><span data-stu-id="1568f-113">Members</span></span>

<span data-ttu-id="1568f-114">**EncodedData** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1568f-114">The **EncodedData** object has these types of members:</span></span>

-   [<span data-ttu-id="1568f-115">方法</span><span class="sxs-lookup"><span data-stu-id="1568f-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="1568f-116">屬性</span><span class="sxs-lookup"><span data-stu-id="1568f-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1568f-117">方法</span><span class="sxs-lookup"><span data-stu-id="1568f-117">Methods</span></span>

<span data-ttu-id="1568f-118">**EncodedData** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1568f-118">The **EncodedData** object has these methods.</span></span>



| <span data-ttu-id="1568f-119">方法</span><span class="sxs-lookup"><span data-stu-id="1568f-119">Method</span></span>                                 | <span data-ttu-id="1568f-120">描述</span><span class="sxs-lookup"><span data-stu-id="1568f-120">Description</span></span>                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="1568f-121">**解碼 器**</span><span class="sxs-lookup"><span data-stu-id="1568f-121">**Decoder**</span></span>](encodeddata-decoder.md) | <span data-ttu-id="1568f-122">取得解碼器物件（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="1568f-122">Obtains a decoder object, if one exists.</span></span><br/>             |
| [<span data-ttu-id="1568f-123">**格式**</span><span class="sxs-lookup"><span data-stu-id="1568f-123">**Format**</span></span>](encodeddata-format.md)   | <span data-ttu-id="1568f-124">傳回編碼資料的字串表示。</span><span class="sxs-lookup"><span data-stu-id="1568f-124">Returns a string representation of the encoded data.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1568f-125">屬性</span><span class="sxs-lookup"><span data-stu-id="1568f-125">Properties</span></span>

<span data-ttu-id="1568f-126">**EncodedData** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1568f-126">The **EncodedData** object has these properties.</span></span>



| <span data-ttu-id="1568f-127">屬性</span><span class="sxs-lookup"><span data-stu-id="1568f-127">Property</span></span>                                      | <span data-ttu-id="1568f-128">存取類型</span><span class="sxs-lookup"><span data-stu-id="1568f-128">Access type</span></span>          | <span data-ttu-id="1568f-129">Description</span><span class="sxs-lookup"><span data-stu-id="1568f-129">Description</span></span>                                                          |
|:----------------------------------------------|:---------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="1568f-130">**值**</span><span class="sxs-lookup"><span data-stu-id="1568f-130">**Value**</span></span>](encodeddata-value.md)<br/> | <span data-ttu-id="1568f-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="1568f-131">Read-only</span></span><br/> | <span data-ttu-id="1568f-132">抓取編碼的資料。</span><span class="sxs-lookup"><span data-stu-id="1568f-132">Retrieves the encoded data.</span></span> <span data-ttu-id="1568f-133">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="1568f-133">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1568f-134">備註</span><span class="sxs-lookup"><span data-stu-id="1568f-134">Remarks</span></span>

<span data-ttu-id="1568f-135">唯一支援的編碼資料類型是 [**CertificatePolicies**](certificatepolicies.md)。</span><span class="sxs-lookup"><span data-stu-id="1568f-135">The only supported type of encoded data is [**CertificatePolicies**](certificatepolicies.md).</span></span>

<span data-ttu-id="1568f-136">無法建立 **EncodedData** 物件。</span><span class="sxs-lookup"><span data-stu-id="1568f-136">The **EncodedData** object cannot be created.</span></span>

<span data-ttu-id="1568f-137">下列的 CAPICOM 物件屬性會傳回 **EncodedData** 物件：</span><span class="sxs-lookup"><span data-stu-id="1568f-137">The following CAPICOM object properties return an **EncodedData** object:</span></span>

-   <span data-ttu-id="1568f-138">**PublicKey. EncodedKey**</span><span class="sxs-lookup"><span data-stu-id="1568f-138">**PublicKey.EncodedKey**</span></span>
-   <span data-ttu-id="1568f-139">**PublicKey. EncodedParameters**</span><span class="sxs-lookup"><span data-stu-id="1568f-139">**PublicKey.EncodedParameters**</span></span>
-   <span data-ttu-id="1568f-140">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="1568f-140">**Extension.EncodedData**</span></span>
-   <span data-ttu-id="1568f-141">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="1568f-141">**Policy.EncodedData**</span></span>

## <a name="requirements"></a><span data-ttu-id="1568f-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="1568f-142">Requirements</span></span>



| <span data-ttu-id="1568f-143">需求</span><span class="sxs-lookup"><span data-stu-id="1568f-143">Requirement</span></span> | <span data-ttu-id="1568f-144">值</span><span class="sxs-lookup"><span data-stu-id="1568f-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1568f-145">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1568f-145">End of client support</span></span><br/> | <span data-ttu-id="1568f-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1568f-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1568f-147">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="1568f-147">End of server support</span></span><br/> | <span data-ttu-id="1568f-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1568f-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1568f-149">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="1568f-149">Redistributable</span></span><br/>       | <span data-ttu-id="1568f-150">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1568f-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1568f-151">DLL</span><span class="sxs-lookup"><span data-stu-id="1568f-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1568f-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1568f-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
