---
description: 解密加密和編碼的資料字串。
ms.assetid: 7601083d-0adb-48e1-98a7-804a49f71206
title: A 解密方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aa702a5cefc46f6d0cbe5d7e0fba17ff03596b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000377"
---
# <a name="encrypteddatadecrypt-method"></a><span data-ttu-id="1b434-103">A 解密方法</span><span class="sxs-lookup"><span data-stu-id="1b434-103">EncryptedData.Decrypt method</span></span>

<span data-ttu-id="1b434-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="1b434-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1b434-105">相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) 和 [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) ，以加密和解密訊息。</span><span class="sxs-lookup"><span data-stu-id="1b434-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="1b434-106">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="1b434-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="1b434-107">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="1b434-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="1b434-108">**解密** 方法會解密加密和編碼的資料字串。</span><span class="sxs-lookup"><span data-stu-id="1b434-108">The **Decrypt** method decrypts an encrypted and encoded data string.</span></span> <span data-ttu-id="1b434-109">產生的純文字資料會變成 [**a**](encrypteddata.md)物件的 [**Content**](encrypteddata-content.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="1b434-109">The resulting plaintext data becomes the [**Content**](encrypteddata-content.md) property of the [**EncryptedData**](encrypteddata.md) object.</span></span> <span data-ttu-id="1b434-110">除非 [**>client.setsecret**](encrypteddata-setsecret.md) 方法所設定的密碼與用來衍生用來加密內容之金鑰的密碼完全相同，否則內容解密會失敗。</span><span class="sxs-lookup"><span data-stu-id="1b434-110">Decryption of the content fails unless the secret, set by the [**SetSecret**](encrypteddata-setsecret.md) method, is exactly the same as the secret used to derive the key used to encrypt the content.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b434-111">語法</span><span class="sxs-lookup"><span data-stu-id="1b434-111">Syntax</span></span>


```VB
EncryptedData.Decrypt( _
  ByVal EncryptedMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="1b434-112">參數</span><span class="sxs-lookup"><span data-stu-id="1b434-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b434-113">*EncryptedMessage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b434-113">*EncryptedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b434-114">字串，包含要解密的已編碼、加密的資料。</span><span class="sxs-lookup"><span data-stu-id="1b434-114">String that contains the encoded, encrypted data to be decrypted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b434-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b434-115">Return value</span></span>

<span data-ttu-id="1b434-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1b434-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b434-117">備註</span><span class="sxs-lookup"><span data-stu-id="1b434-117">Remarks</span></span>

<span data-ttu-id="1b434-118">衍生自目前秘密的工作階段金鑰是用來解密。</span><span class="sxs-lookup"><span data-stu-id="1b434-118">The session key derived from the current secret is used for the decryption.</span></span> <span data-ttu-id="1b434-119">除非目前的密碼完全符合用來加密訊息的秘密，否則此方法不會產生正確的純文字。</span><span class="sxs-lookup"><span data-stu-id="1b434-119">This method will not produce the correct plaintext unless the current secret exactly matches the secret used to encrypt the message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b434-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b434-120">Requirements</span></span>



| <span data-ttu-id="1b434-121">需求</span><span class="sxs-lookup"><span data-stu-id="1b434-121">Requirement</span></span> | <span data-ttu-id="1b434-122">值</span><span class="sxs-lookup"><span data-stu-id="1b434-122">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b434-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1b434-123">End of client support</span></span><br/> | <span data-ttu-id="1b434-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b434-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1b434-125">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="1b434-125">End of server support</span></span><br/> | <span data-ttu-id="1b434-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b434-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1b434-127">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="1b434-127">Redistributable</span></span><br/>       | <span data-ttu-id="1b434-128">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1b434-128">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1b434-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1b434-129">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1b434-130"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b434-130"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b434-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b434-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b434-132">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="1b434-132">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="1b434-133">**A**</span><span class="sxs-lookup"><span data-stu-id="1b434-133">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
