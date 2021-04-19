---
description: 提供屬性和方法來建立要以數位簽章簽署的內容、以數位方式簽署或 cosign 資料，以及驗證已簽署資料的數位簽章。 簽署的訊息是 PKCS \# 7 格式。
ms.assetid: 500437e8-a637-4e89-9ac9-aa3ea20d437f
title: SignedData 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d0424826f7dc5d041b877ced1cd7f50490d7801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994590"
---
# <a name="signeddata-object"></a><span data-ttu-id="b06be-104">SignedData 物件</span><span class="sxs-lookup"><span data-stu-id="b06be-104">SignedData object</span></span>

<span data-ttu-id="b06be-105">\[**SignedData** 物件可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b06be-105">\[The **SignedData** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b06be-106">相反地，請使用 [**SignedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="b06be-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="b06be-107">**SignedData** 物件提供屬性和方法來建立要以 [*數位簽章*](../secgloss/d-gly.md)簽署的內容、以數位方式簽署或 cosign 資料，以及驗證已簽署資料的數位簽章。</span><span class="sxs-lookup"><span data-stu-id="b06be-107">The **SignedData** object provides properties and methods to establish the content to be signed with a [*digital signature*](../secgloss/d-gly.md), to sign or cosign data digitally, and to verify the digital signature of signed data.</span></span> <span data-ttu-id="b06be-108">簽署的訊息是 PKCS \# 7 格式。</span><span class="sxs-lookup"><span data-stu-id="b06be-108">The signed message is in PKCS \#7 format.</span></span>

<span data-ttu-id="b06be-109">如果資料簽章經過驗證，就會證明簽署者與資料之間的關聯性，並顯示資料在建立簽章之後不會以任何方式變更。</span><span class="sxs-lookup"><span data-stu-id="b06be-109">A data signature, if verified, proves the association between a signer and data and shows that the data was not changed in any way after the signature was created.</span></span>

## <a name="members"></a><span data-ttu-id="b06be-110">成員</span><span class="sxs-lookup"><span data-stu-id="b06be-110">Members</span></span>

<span data-ttu-id="b06be-111">**SignedData** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b06be-111">The **SignedData** object has these types of members:</span></span>

-   [<span data-ttu-id="b06be-112">方法</span><span class="sxs-lookup"><span data-stu-id="b06be-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b06be-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b06be-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b06be-114">方法</span><span class="sxs-lookup"><span data-stu-id="b06be-114">Methods</span></span>

<span data-ttu-id="b06be-115">**SignedData** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b06be-115">The **SignedData** object has these methods.</span></span>



| <span data-ttu-id="b06be-116">方法</span><span class="sxs-lookup"><span data-stu-id="b06be-116">Method</span></span>                              | <span data-ttu-id="b06be-117">描述</span><span class="sxs-lookup"><span data-stu-id="b06be-117">Description</span></span>                                                         |
|:------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="b06be-118">**CoSign**</span><span class="sxs-lookup"><span data-stu-id="b06be-118">**CoSign**</span></span>](signeddata-cosign.md) | <span data-ttu-id="b06be-119">Cosigns 已簽署的訊息。</span><span class="sxs-lookup"><span data-stu-id="b06be-119">Cosigns an already signed message.</span></span><br/>                       |
| [<span data-ttu-id="b06be-120">**標誌**</span><span class="sxs-lookup"><span data-stu-id="b06be-120">**Sign**</span></span>](signeddata-sign.md)     | <span data-ttu-id="b06be-121">在要簽署的內容上建立數位簽章。</span><span class="sxs-lookup"><span data-stu-id="b06be-121">Creates a digital signature on the content to be signed.</span></span><br/> |
| [<span data-ttu-id="b06be-122">**驗證**</span><span class="sxs-lookup"><span data-stu-id="b06be-122">**Verify**</span></span>](signeddata-verify.md) | <span data-ttu-id="b06be-123">判斷簽章或簽章的有效性。</span><span class="sxs-lookup"><span data-stu-id="b06be-123">Determines the validity of a signature or signatures.</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="b06be-124">屬性</span><span class="sxs-lookup"><span data-stu-id="b06be-124">Properties</span></span>

<span data-ttu-id="b06be-125">**SignedData** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b06be-125">The **SignedData** object has these properties.</span></span>



| <span data-ttu-id="b06be-126">屬性</span><span class="sxs-lookup"><span data-stu-id="b06be-126">Property</span></span>                                                   | <span data-ttu-id="b06be-127">存取類型</span><span class="sxs-lookup"><span data-stu-id="b06be-127">Access type</span></span>           | <span data-ttu-id="b06be-128">Description</span><span class="sxs-lookup"><span data-stu-id="b06be-128">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b06be-129">**憑證**</span><span class="sxs-lookup"><span data-stu-id="b06be-129">**Certificates**</span></span>](signeddata-certificates.md)<br/> | <span data-ttu-id="b06be-130">唯讀</span><span class="sxs-lookup"><span data-stu-id="b06be-130">Read-only</span></span><br/>  | <span data-ttu-id="b06be-131">抓取已簽署資料的 [**憑證**](certificates.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="b06be-131">Retrieves the [**Certificates**](certificates.md) collection of the signed data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="b06be-132">**內容**</span><span class="sxs-lookup"><span data-stu-id="b06be-132">**Content**</span></span>](signeddata-content.md)<br/>           | <span data-ttu-id="b06be-133">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b06be-133">Read/write</span></span><br/> | <span data-ttu-id="b06be-134">要簽署的資料。</span><span class="sxs-lookup"><span data-stu-id="b06be-134">Data to be signed.</span></span> <span data-ttu-id="b06be-135">這個屬性必須在呼叫 [**Sign**](signeddata-sign.md) 方法之前初始化。</span><span class="sxs-lookup"><span data-stu-id="b06be-135">This property must be initialized before the [**Sign**](signeddata-sign.md) method is called.</span></span><br/> <span data-ttu-id="b06be-136">當這個屬性的值是直接或間接重設時，會重設物件的整個 [*狀態*](../secgloss/s-gly.md) ，而且在變更屬性之前與物件相關聯的任何簽章都會遺失。</span><span class="sxs-lookup"><span data-stu-id="b06be-136">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any signature that was associated with the object before the property was changed is lost.</span></span><br/> <span data-ttu-id="b06be-137">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="b06be-137">This is the default property.</span></span><br/> |
| [<span data-ttu-id="b06be-138">**簽名**</span><span class="sxs-lookup"><span data-stu-id="b06be-138">**Signers**</span></span>](signeddata-signers.md)<br/>           | <span data-ttu-id="b06be-139">唯讀</span><span class="sxs-lookup"><span data-stu-id="b06be-139">Read-only</span></span><br/>  | <span data-ttu-id="b06be-140">抓取代表資料簽章建立者的 [**簽署**](signers.md) 者集合。</span><span class="sxs-lookup"><span data-stu-id="b06be-140">Retrieves the [**Signers**](signers.md) collection that represents the signature creators of the data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="b06be-141">備註</span><span class="sxs-lookup"><span data-stu-id="b06be-141">Remarks</span></span>

<span data-ttu-id="b06be-142">您可以建立 **SignedData** 物件，而且可以安全地進行腳本處理。</span><span class="sxs-lookup"><span data-stu-id="b06be-142">The **SignedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="b06be-143">**SignedData** 物件的 PROGID 是 CAPICOM。SignedData。1。</span><span class="sxs-lookup"><span data-stu-id="b06be-143">The ProgID for the **SignedData** object is CAPICOM.SignedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="b06be-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="b06be-144">Requirements</span></span>



| <span data-ttu-id="b06be-145">需求</span><span class="sxs-lookup"><span data-stu-id="b06be-145">Requirement</span></span> | <span data-ttu-id="b06be-146">值</span><span class="sxs-lookup"><span data-stu-id="b06be-146">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b06be-147">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b06be-147">Redistributable</span></span><br/> | <span data-ttu-id="b06be-148">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b06be-148">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b06be-149">DLL</span><span class="sxs-lookup"><span data-stu-id="b06be-149">DLL</span></span><br/>             | <dl> <span data-ttu-id="b06be-150"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b06be-150"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b06be-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b06be-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b06be-152">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="b06be-152">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
