---
description: EnvelopedData 物件提供屬性和方法，以透過加密波封隱私權的資料。
ms.assetid: 7c5f3e3d-6a70-455d-8921-20495eec4b3e
title: EnvelopedData 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5309061c6ab315a089a1e1d8b9488556cae9f31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983003"
---
# <a name="envelopeddata-object"></a><span data-ttu-id="8d877-103">EnvelopedData 物件</span><span class="sxs-lookup"><span data-stu-id="8d877-103">EnvelopedData object</span></span>

<span data-ttu-id="8d877-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="8d877-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="8d877-105">相反地，請使用 [**EnvelopedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="8d877-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="8d877-106">**EnvelopedData** 物件提供屬性和方法，以透過加密波封隱私權的資料。</span><span class="sxs-lookup"><span data-stu-id="8d877-106">The **EnvelopedData** object provides properties and methods to envelop data for privacy by encryption.</span></span> <span data-ttu-id="8d877-107">若要波封資料，會產生會話密碼編譯金鑰。</span><span class="sxs-lookup"><span data-stu-id="8d877-107">To envelop data, a session cryptographic key is generated.</span></span> <span data-ttu-id="8d877-108">接著，會針對每個預定的收件者，使用來自收件者憑證之收件者的 [*公開金鑰*](../secgloss/p-gly.md)來加密該 [*工作階段金鑰*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="8d877-108">That [*session key*](../secgloss/s-gly.md) is then encrypted for each intended recipient using the [*public key*](../secgloss/p-gly.md) of that intended recipient from the recipient's certificate.</span></span> <span data-ttu-id="8d877-109">加密的資料和加密的工作階段金鑰集可以傳送給所有預定的收件者。</span><span class="sxs-lookup"><span data-stu-id="8d877-109">The encrypted data and the set of encrypted session keys can be sent to all intended recipients.</span></span> <span data-ttu-id="8d877-110">產生的訊息是 PKCS \# 7 格式。</span><span class="sxs-lookup"><span data-stu-id="8d877-110">The message generated is in PKCS \#7 format.</span></span>

## <a name="members"></a><span data-ttu-id="8d877-111">成員</span><span class="sxs-lookup"><span data-stu-id="8d877-111">Members</span></span>

<span data-ttu-id="8d877-112">**EnvelopedData** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8d877-112">The **EnvelopedData** object has these types of members:</span></span>

-   [<span data-ttu-id="8d877-113">方法</span><span class="sxs-lookup"><span data-stu-id="8d877-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="8d877-114">屬性</span><span class="sxs-lookup"><span data-stu-id="8d877-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8d877-115">方法</span><span class="sxs-lookup"><span data-stu-id="8d877-115">Methods</span></span>

<span data-ttu-id="8d877-116">**EnvelopedData** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8d877-116">The **EnvelopedData** object has these methods.</span></span>



| <span data-ttu-id="8d877-117">方法</span><span class="sxs-lookup"><span data-stu-id="8d877-117">Method</span></span>                                   | <span data-ttu-id="8d877-118">描述</span><span class="sxs-lookup"><span data-stu-id="8d877-118">Description</span></span>                                                                                                 |
|:-----------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d877-119">**解密**</span><span class="sxs-lookup"><span data-stu-id="8d877-119">**Decrypt**</span></span>](envelopeddata-decrypt.md) | <span data-ttu-id="8d877-120">解密封裝的內容。</span><span class="sxs-lookup"><span data-stu-id="8d877-120">Decrypts enveloped content.</span></span><br/>                                                                      |
| [<span data-ttu-id="8d877-121">**加密**</span><span class="sxs-lookup"><span data-stu-id="8d877-121">**Encrypt**</span></span>](envelopeddata-encrypt.md) | <span data-ttu-id="8d877-122">加密內容、為每個收件者加密工作階段金鑰，並傳回加密的 BLOB。</span><span class="sxs-lookup"><span data-stu-id="8d877-122">Encrypts the content, encrypts a session key for each recipient, and returns the encrypted BLOB.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8d877-123">屬性</span><span class="sxs-lookup"><span data-stu-id="8d877-123">Properties</span></span>

<span data-ttu-id="8d877-124">**EnvelopedData** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8d877-124">The **EnvelopedData** object has these properties.</span></span>



| <span data-ttu-id="8d877-125">屬性</span><span class="sxs-lookup"><span data-stu-id="8d877-125">Property</span></span>                                                  | <span data-ttu-id="8d877-126">存取類型</span><span class="sxs-lookup"><span data-stu-id="8d877-126">Access type</span></span>           | <span data-ttu-id="8d877-127">Description</span><span class="sxs-lookup"><span data-stu-id="8d877-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d877-128">**演算法**</span><span class="sxs-lookup"><span data-stu-id="8d877-128">**Algorithm**</span></span>](envelopeddata-algorithm.md)<br/>   | <span data-ttu-id="8d877-129">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d877-129">Read/write</span></span><br/> | <span data-ttu-id="8d877-130">加密演算法和 [*金鑰長度*](../secgloss/k-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="8d877-130">Encryption algorithm and [*key length*](../secgloss/k-gly.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="8d877-131">**內容**</span><span class="sxs-lookup"><span data-stu-id="8d877-131">**Content**</span></span>](envelopeddata-content.md)<br/>       | <span data-ttu-id="8d877-132">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d877-132">Read/write</span></span><br/> | <span data-ttu-id="8d877-133">要封裝之訊息的純文字內容。</span><span class="sxs-lookup"><span data-stu-id="8d877-133">The plaintext content of a message to be enveloped.</span></span> <span data-ttu-id="8d877-134">設定此屬性必須在呼叫 [**加密**](envelopeddata-encrypt.md) 方法之前完成。</span><span class="sxs-lookup"><span data-stu-id="8d877-134">Setting this property must be done before the [**Encrypt**](envelopeddata-encrypt.md) method is called.</span></span><br/> <span data-ttu-id="8d877-135">當這個屬性的值是直接或間接重設時，會重設物件的整個 [*狀態*](../secgloss/s-gly.md) ，而且會遺失物件中任何加密的內容。</span><span class="sxs-lookup"><span data-stu-id="8d877-135">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span><br/> <span data-ttu-id="8d877-136">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="8d877-136">This is the default property.</span></span><br/> |
| [<span data-ttu-id="8d877-137">**收件者**</span><span class="sxs-lookup"><span data-stu-id="8d877-137">**Recipients**</span></span>](envelopeddata-recipients.md)<br/> | <span data-ttu-id="8d877-138">唯讀</span><span class="sxs-lookup"><span data-stu-id="8d877-138">Read-only</span></span><br/>  | <span data-ttu-id="8d877-139">接收封包訊息的 [**憑證**](certificate.md) 物件集合。</span><span class="sxs-lookup"><span data-stu-id="8d877-139">Collection of [**Certificate**](certificate.md) objects to receive the enveloped message.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="8d877-140">備註</span><span class="sxs-lookup"><span data-stu-id="8d877-140">Remarks</span></span>

<span data-ttu-id="8d877-141">您可以建立 **EnvelopedData** 物件，而且可以安全地進行腳本處理。</span><span class="sxs-lookup"><span data-stu-id="8d877-141">The **EnvelopedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="8d877-142">**EnvelopedData** 物件的 PROGID 是 CAPICOM。EnvelopedData。1。</span><span class="sxs-lookup"><span data-stu-id="8d877-142">The ProgID for the **EnvelopedData** object is CAPICOM.EnvelopedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d877-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d877-143">Requirements</span></span>



| <span data-ttu-id="8d877-144">需求</span><span class="sxs-lookup"><span data-stu-id="8d877-144">Requirement</span></span> | <span data-ttu-id="8d877-145">值</span><span class="sxs-lookup"><span data-stu-id="8d877-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d877-146">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="8d877-146">End of client support</span></span><br/> | <span data-ttu-id="8d877-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d877-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8d877-148">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="8d877-148">End of server support</span></span><br/> | <span data-ttu-id="8d877-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d877-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8d877-150">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8d877-150">Redistributable</span></span><br/>       | <span data-ttu-id="8d877-151">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="8d877-151">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8d877-152">DLL</span><span class="sxs-lookup"><span data-stu-id="8d877-152">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8d877-153"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d877-153"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d877-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d877-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d877-155">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="8d877-155">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
