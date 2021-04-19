---
description: 提供屬性和方法，以使用衍生自秘密的工作階段金鑰來加密和解密資料。
ms.assetid: 3b9bd0a2-6e15-4d58-a682-588a93895799
title: A 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 123e0973343e4990dd2d49cfb321d739085358f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977411"
---
# <a name="encrypteddata-object"></a><span data-ttu-id="66c73-103">A 物件</span><span class="sxs-lookup"><span data-stu-id="66c73-103">EncryptedData object</span></span>

<span data-ttu-id="66c73-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="66c73-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="66c73-105">相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) 和 [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) ，以加密和解密訊息。</span><span class="sxs-lookup"><span data-stu-id="66c73-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="66c73-106">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="66c73-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="66c73-107">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="66c73-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="66c73-108">**A** 物件提供屬性和方法，以使用衍生自秘密的 [*工作階段金鑰*](../secgloss/s-gly.md)來加密和解密資料。</span><span class="sxs-lookup"><span data-stu-id="66c73-108">The **EncryptedData** object provides properties and methods to encrypt and decrypt data using a [*session key*](../secgloss/s-gly.md) derived from a secret.</span></span>

> [!Note]  
> <span data-ttu-id="66c73-109">CAPICOM 不支援 PKCS \# 7 a 內容類型，但會使用非標準的 ASN 結構來進行 **a**。</span><span class="sxs-lookup"><span data-stu-id="66c73-109">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a nonstandard ASN structure for **EncryptedData**.</span></span> <span data-ttu-id="66c73-110">因此，只有 CAPICOM 才能解密 CAPICOM **a** 物件。</span><span class="sxs-lookup"><span data-stu-id="66c73-110">Therefore, only CAPICOM can decrypt a CAPICOM **EncryptedData** object.</span></span>

 

## <a name="members"></a><span data-ttu-id="66c73-111">成員</span><span class="sxs-lookup"><span data-stu-id="66c73-111">Members</span></span>

<span data-ttu-id="66c73-112">**A** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="66c73-112">The **EncryptedData** object has these types of members:</span></span>

-   [<span data-ttu-id="66c73-113">方法</span><span class="sxs-lookup"><span data-stu-id="66c73-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="66c73-114">屬性</span><span class="sxs-lookup"><span data-stu-id="66c73-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="66c73-115">方法</span><span class="sxs-lookup"><span data-stu-id="66c73-115">Methods</span></span>

<span data-ttu-id="66c73-116">**A** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="66c73-116">The **EncryptedData** object has these methods.</span></span>



| <span data-ttu-id="66c73-117">方法</span><span class="sxs-lookup"><span data-stu-id="66c73-117">Method</span></span>                                       | <span data-ttu-id="66c73-118">描述</span><span class="sxs-lookup"><span data-stu-id="66c73-118">Description</span></span>                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="66c73-119">**解密**</span><span class="sxs-lookup"><span data-stu-id="66c73-119">**Decrypt**</span></span>](encrypteddata-decrypt.md)     | <span data-ttu-id="66c73-120">使用秘密來解密加密的內容。</span><span class="sxs-lookup"><span data-stu-id="66c73-120">Decrypts encrypted content using the secret.</span></span><br/>                                 |
| [<span data-ttu-id="66c73-121">**加密**</span><span class="sxs-lookup"><span data-stu-id="66c73-121">**Encrypt**</span></span>](encrypteddata-encrypt.md)     | <span data-ttu-id="66c73-122">使用目前的密碼和加密演算法來加密內容。</span><span class="sxs-lookup"><span data-stu-id="66c73-122">Encrypts the content using the current secret and encryption algorithm.</span></span><br/>      |
| [<span data-ttu-id="66c73-123">**>client.setsecret**</span><span class="sxs-lookup"><span data-stu-id="66c73-123">**SetSecret**</span></span>](encrypteddata-setsecret.md) | <span data-ttu-id="66c73-124">設定用來衍生加密/解密工作階段金鑰的秘密。</span><span class="sxs-lookup"><span data-stu-id="66c73-124">Sets the secret from which the encryption/decryption session key is derived.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="66c73-125">屬性</span><span class="sxs-lookup"><span data-stu-id="66c73-125">Properties</span></span>

<span data-ttu-id="66c73-126">**A** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="66c73-126">The **EncryptedData** object has these properties.</span></span>



| <span data-ttu-id="66c73-127">屬性</span><span class="sxs-lookup"><span data-stu-id="66c73-127">Property</span></span>                                                | <span data-ttu-id="66c73-128">存取類型</span><span class="sxs-lookup"><span data-stu-id="66c73-128">Access type</span></span>           | <span data-ttu-id="66c73-129">Description</span><span class="sxs-lookup"><span data-stu-id="66c73-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66c73-130">**演算法**</span><span class="sxs-lookup"><span data-stu-id="66c73-130">**Algorithm**</span></span>](encrypteddata-algorithm.md)<br/> | <span data-ttu-id="66c73-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="66c73-131">Read-only</span></span><br/>  | <span data-ttu-id="66c73-132">用於加密/解密的演算法。</span><span class="sxs-lookup"><span data-stu-id="66c73-132">Algorithm used for encryption/decryption.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="66c73-133">**內容**</span><span class="sxs-lookup"><span data-stu-id="66c73-133">**Content**</span></span>](encrypteddata-content.md)<br/>     | <span data-ttu-id="66c73-134">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="66c73-134">Read/write</span></span><br/> | <span data-ttu-id="66c73-135">要加密或解密的內容。</span><span class="sxs-lookup"><span data-stu-id="66c73-135">The content to be encrypted or decrypted.</span></span> <span data-ttu-id="66c73-136">設定此屬性必須在呼叫 [**加密**](encrypteddata-encrypt.md) 方法之前完成。</span><span class="sxs-lookup"><span data-stu-id="66c73-136">Setting this property must be done before the [**Encrypt**](encrypteddata-encrypt.md) method is called.</span></span> <br/> <span data-ttu-id="66c73-137">當這個屬性的值是直接或間接重設時，會重設物件的整個 [*狀態*](../secgloss/s-gly.md) ，而且會遺失物件中任何加密的內容。</span><span class="sxs-lookup"><span data-stu-id="66c73-137">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span><br/> <span data-ttu-id="66c73-138">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="66c73-138">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="66c73-139">備註</span><span class="sxs-lookup"><span data-stu-id="66c73-139">Remarks</span></span>

<span data-ttu-id="66c73-140">您可以建立 **a** 物件，而且可以安全地進行腳本處理。</span><span class="sxs-lookup"><span data-stu-id="66c73-140">The **EncryptedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="66c73-141">**A** 物件的 PROGID 是 CAPICOM。A。1。</span><span class="sxs-lookup"><span data-stu-id="66c73-141">The ProgID for the **EncryptedData** object is CAPICOM.EncryptedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="66c73-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="66c73-142">Requirements</span></span>



| <span data-ttu-id="66c73-143">需求</span><span class="sxs-lookup"><span data-stu-id="66c73-143">Requirement</span></span> | <span data-ttu-id="66c73-144">值</span><span class="sxs-lookup"><span data-stu-id="66c73-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66c73-145">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="66c73-145">End of client support</span></span><br/> | <span data-ttu-id="66c73-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66c73-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="66c73-147">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="66c73-147">End of server support</span></span><br/> | <span data-ttu-id="66c73-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66c73-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="66c73-149">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="66c73-149">Redistributable</span></span><br/>       | <span data-ttu-id="66c73-150">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="66c73-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="66c73-151">DLL</span><span class="sxs-lookup"><span data-stu-id="66c73-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="66c73-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66c73-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66c73-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66c73-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66c73-154">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="66c73-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
