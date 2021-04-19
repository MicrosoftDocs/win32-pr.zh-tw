---
description: 從秘密衍生工作階段金鑰，並使用該金鑰來加密 Content 屬性值。 它會以編碼字串的形式傳回加密的內容。
ms.assetid: aa6f6e6a-208b-4e9c-b530-08673ab9d794
title: A) 加密方法 (Infocard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 04d7bf8a337c1bcfa0a024b84304fe50c035f9dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985978"
---
# <a name="encrypteddataencrypt-method"></a><span data-ttu-id="7dbc3-104">A 方法</span><span class="sxs-lookup"><span data-stu-id="7dbc3-104">EncryptedData.Encrypt method</span></span>

<span data-ttu-id="7dbc3-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="7dbc3-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7dbc3-106">相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) 和 [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) ，以加密和解密訊息。</span><span class="sxs-lookup"><span data-stu-id="7dbc3-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="7dbc3-107">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="7dbc3-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="7dbc3-108">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="7dbc3-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="7dbc3-109">**Encrypt** 方法會從秘密衍生工作階段金鑰，並使用該金鑰來加密 [**Content**](encrypteddata-content.md)屬性值。</span><span class="sxs-lookup"><span data-stu-id="7dbc3-109">The **Encrypt** method derives a session key from the secret and encrypts the [**Content**](encrypteddata-content.md) property value using that key.</span></span> <span data-ttu-id="7dbc3-110">它會以編碼字串的形式傳回加密的內容。</span><span class="sxs-lookup"><span data-stu-id="7dbc3-110">It returns the encrypted content as an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dbc3-111">語法</span><span class="sxs-lookup"><span data-stu-id="7dbc3-111">Syntax</span></span>


```VB
EncryptedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7dbc3-112">參數</span><span class="sxs-lookup"><span data-stu-id="7dbc3-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dbc3-113">*Edi.encodingtype* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="7dbc3-113">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7dbc3-114">[**CAPICOM \_ 編碼 \_ 類型**](capicom-encoding-type.md)列舉的值，表示用來編碼加密資料的編碼類型。</span><span class="sxs-lookup"><span data-stu-id="7dbc3-114">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the encoding type used to encode the encrypted data.</span></span> <span data-ttu-id="7dbc3-115">預設值為 CAPICOM \_ 編碼 \_ BASE64。</span><span class="sxs-lookup"><span data-stu-id="7dbc3-115">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="7dbc3-116">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7dbc3-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="7dbc3-117">值</span><span class="sxs-lookup"><span data-stu-id="7dbc3-117">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="7dbc3-118">意義</span><span class="sxs-lookup"><span data-stu-id="7dbc3-118">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="7dbc3-119"><dt>**CAPICOM \_ 編碼 \_ 任何**</dt></span><span class="sxs-lookup"><span data-stu-id="7dbc3-119"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="7dbc3-120">只有當輸入資料有未知的編碼類型時，才會使用此編碼類型。</span><span class="sxs-lookup"><span data-stu-id="7dbc3-120">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="7dbc3-121">如果這個值是用來指定輸出的編碼類型，則會 \_ 改用 CAPICOM 編碼 \_ BASE64。</span><span class="sxs-lookup"><span data-stu-id="7dbc3-121">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="7dbc3-122">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="7dbc3-122">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="7dbc3-123"><dt>**CAPICOM \_ 編碼 \_ BASE64**</dt></span><span class="sxs-lookup"><span data-stu-id="7dbc3-123"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="7dbc3-124">資料會儲存為 base64 編碼字串。</span><span class="sxs-lookup"><span data-stu-id="7dbc3-124">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="7dbc3-125"><dt>**CAPICOM \_ 編碼 \_ 二進位**</dt></span><span class="sxs-lookup"><span data-stu-id="7dbc3-125"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="7dbc3-126">資料會儲存為純二進位序列。</span><span class="sxs-lookup"><span data-stu-id="7dbc3-126">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dbc3-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="7dbc3-127">Return value</span></span>

<span data-ttu-id="7dbc3-128">包含已加密之編碼資料的字串。</span><span class="sxs-lookup"><span data-stu-id="7dbc3-128">A string that contains the encrypted, encoded data.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dbc3-129">備註</span><span class="sxs-lookup"><span data-stu-id="7dbc3-129">Remarks</span></span>

<span data-ttu-id="7dbc3-130">在呼叫 **Encrypt** 方法之前，請先設定 [**Content**](encrypteddata-content.md) 屬性，然後呼叫 [**>client.setsecret**](encrypteddata-setsecret.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7dbc3-130">Before calling the **Encrypt** method, set the [**Content**](encrypteddata-content.md) property and call the [**SetSecret**](encrypteddata-setsecret.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dbc3-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="7dbc3-131">Requirements</span></span>



| <span data-ttu-id="7dbc3-132">需求</span><span class="sxs-lookup"><span data-stu-id="7dbc3-132">Requirement</span></span> | <span data-ttu-id="7dbc3-133">值</span><span class="sxs-lookup"><span data-stu-id="7dbc3-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7dbc3-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7dbc3-134">End of client support</span></span><br/> | <span data-ttu-id="7dbc3-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7dbc3-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7dbc3-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="7dbc3-136">End of server support</span></span><br/> | <span data-ttu-id="7dbc3-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7dbc3-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7dbc3-138">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7dbc3-138">Redistributable</span></span><br/>       | <span data-ttu-id="7dbc3-139">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7dbc3-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7dbc3-140">標頭</span><span class="sxs-lookup"><span data-stu-id="7dbc3-140">Header</span></span><br/>                | <dl> <span data-ttu-id="7dbc3-141"><dt>Infocard。h</dt></span><span class="sxs-lookup"><span data-stu-id="7dbc3-141"><dt>Infocard.h</dt></span></span> </dl>  |
| <span data-ttu-id="7dbc3-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7dbc3-142">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7dbc3-143"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dbc3-143"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dbc3-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7dbc3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dbc3-145">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="7dbc3-145">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="7dbc3-146">**A**</span><span class="sxs-lookup"><span data-stu-id="7dbc3-146">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
