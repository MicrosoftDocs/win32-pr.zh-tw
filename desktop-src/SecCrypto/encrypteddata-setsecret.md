---
description: 設定用來衍生加密和解密資料的密碼編譯工作階段金鑰的秘密值。
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: A. >client.setsecret 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.SetSecret
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c8d30355b022a593ca17519e3ccfa876a5b07b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982920"
---
# <a name="encrypteddatasetsecret-method"></a><span data-ttu-id="19e09-103">A. >client.setsecret 方法</span><span class="sxs-lookup"><span data-stu-id="19e09-103">EncryptedData.SetSecret method</span></span>

<span data-ttu-id="19e09-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="19e09-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="19e09-105">相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) 和 [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) ，以加密和解密訊息。</span><span class="sxs-lookup"><span data-stu-id="19e09-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="19e09-106">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="19e09-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="19e09-107">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="19e09-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="19e09-108">**>client.setsecret** 方法會設定秘密的值，用來衍生用來加密和解密資料的密碼編譯 [*工作階段金鑰*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="19e09-108">The **SetSecret** method sets the value of the secret used to derive the cryptographic [*session key*](../secgloss/s-gly.md) used to encrypt and decrypt data.</span></span>

## <a name="syntax"></a><span data-ttu-id="19e09-109">語法</span><span class="sxs-lookup"><span data-stu-id="19e09-109">Syntax</span></span>


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="19e09-110">參數</span><span class="sxs-lookup"><span data-stu-id="19e09-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19e09-111">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19e09-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e09-112">包含用來建立會話密碼編譯金鑰之密碼的字串。</span><span class="sxs-lookup"><span data-stu-id="19e09-112">A string that contains a secret used to create a session cryptographic key.</span></span>

</dd> <dt>

<span data-ttu-id="19e09-113">*SecretType* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="19e09-113">*SecretType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19e09-114">[**CAPICOM \_ 秘密 \_ 類型**](capicom-secret-type.md)列舉的值，表示用來產生工作階段金鑰的秘密種類。</span><span class="sxs-lookup"><span data-stu-id="19e09-114">A value of the [**CAPICOM\_SECRET\_TYPE**](capicom-secret-type.md) enumeration that indicates the kind of secret used to generate the session key.</span></span> <span data-ttu-id="19e09-115">預設值是 [CAPICOM \_ 秘密 \_ 密碼]。</span><span class="sxs-lookup"><span data-stu-id="19e09-115">The default value is CAPICOM\_SECRET\_PASSWORD.</span></span> <span data-ttu-id="19e09-116">此參數可為下列值。</span><span class="sxs-lookup"><span data-stu-id="19e09-116">This parameter can be the following value.</span></span>



| <span data-ttu-id="19e09-117">值</span><span class="sxs-lookup"><span data-stu-id="19e09-117">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="19e09-118">意義</span><span class="sxs-lookup"><span data-stu-id="19e09-118">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <span data-ttu-id="19e09-119"><dt>**CAPICOM \_ 秘密 \_ 密碼**</dt></span><span class="sxs-lookup"><span data-stu-id="19e09-119"><dt>**CAPICOM\_SECRET\_PASSWORD**</dt></span></span> </dl> | <span data-ttu-id="19e09-120">加密金鑰是衍生自密碼。</span><span class="sxs-lookup"><span data-stu-id="19e09-120">The encryption key is to be derived from a password.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19e09-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="19e09-121">Return value</span></span>

<span data-ttu-id="19e09-122">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="19e09-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="19e09-123">備註</span><span class="sxs-lookup"><span data-stu-id="19e09-123">Remarks</span></span>

<span data-ttu-id="19e09-124">秘密可用來建立用於加密或解密的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="19e09-124">The secret is used to create the session key for encryption or decryption.</span></span> <span data-ttu-id="19e09-125">這兩個作業都必須使用相同的密碼。</span><span class="sxs-lookup"><span data-stu-id="19e09-125">The same secret must be used for both operations.</span></span> <span data-ttu-id="19e09-126">如果用來加密資料的密碼遺失，則無法解密加密的資料。</span><span class="sxs-lookup"><span data-stu-id="19e09-126">If the secret used to encrypt data is lost, the encrypted data cannot be decrypted.</span></span>

<span data-ttu-id="19e09-127">如果適用于您的應用程式，請考慮使用 [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) 或 [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) ，以在使用之前和之後保護秘密。</span><span class="sxs-lookup"><span data-stu-id="19e09-127">If appropriate for your application, consider using [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) or [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) to protect the secret before and after use.</span></span> <span data-ttu-id="19e09-128">完成時清除與秘密相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="19e09-128">Clear the memory associated with the secret when done.</span></span>

## <a name="requirements"></a><span data-ttu-id="19e09-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="19e09-129">Requirements</span></span>



| <span data-ttu-id="19e09-130">需求</span><span class="sxs-lookup"><span data-stu-id="19e09-130">Requirement</span></span> | <span data-ttu-id="19e09-131">值</span><span class="sxs-lookup"><span data-stu-id="19e09-131">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19e09-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="19e09-132">End of client support</span></span><br/> | <span data-ttu-id="19e09-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19e09-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="19e09-134">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="19e09-134">End of server support</span></span><br/> | <span data-ttu-id="19e09-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19e09-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="19e09-136">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="19e09-136">Redistributable</span></span><br/>       | <span data-ttu-id="19e09-137">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="19e09-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="19e09-138">DLL</span><span class="sxs-lookup"><span data-stu-id="19e09-138">DLL</span></span><br/>                   | <dl> <span data-ttu-id="19e09-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19e09-139"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19e09-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19e09-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e09-141">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="19e09-141">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="19e09-142">**A**</span><span class="sxs-lookup"><span data-stu-id="19e09-142">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
