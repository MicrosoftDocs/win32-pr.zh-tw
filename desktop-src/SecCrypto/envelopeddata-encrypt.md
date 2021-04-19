---
description: 產生工作階段金鑰，並將資料加密和信封。
ms.assetid: 7ae0c908-207b-4a74-a195-d12e9e7dec76
title: EnvelopedData 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ecdb665a8e70ff329f25398eb855ff3e82c96cfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994040"
---
# <a name="envelopeddataencrypt-method"></a><span data-ttu-id="9550b-103">EnvelopedData 方法</span><span class="sxs-lookup"><span data-stu-id="9550b-103">EnvelopedData.Encrypt method</span></span>

<span data-ttu-id="9550b-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="9550b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9550b-105">相反地，請使用 [**EnvelopedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="9550b-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="9550b-106">**Encrypt** 方法會產生工作階段金鑰、使用該金鑰來加密內容、使用每個收件者的公開金鑰來加密工作階段金鑰，以信封每個收件者的加密內容，然後傳回包含加密內容和加密工作階段金鑰的 [*BLOB*](../secgloss/b-gly.md)做為編碼字串。</span><span class="sxs-lookup"><span data-stu-id="9550b-106">The **Encrypt** method generates a session key, uses that key to encrypt the contents, envelops the encrypted content for each recipient by encrypting the session key with each recipient's public key, and then returns the [*BLOB*](../secgloss/b-gly.md) that contains the encrypted contents and the encrypted session keys as an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9550b-107">語法</span><span class="sxs-lookup"><span data-stu-id="9550b-107">Syntax</span></span>


```VB
EnvelopedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9550b-108">參數</span><span class="sxs-lookup"><span data-stu-id="9550b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9550b-109">*Edi.encodingtype* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9550b-109">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9550b-110">[**CAPICOM \_ 編碼 \_ 類型**](capicom-encoding-type.md)列舉的值，表示用來編碼封包資料的編碼類型。</span><span class="sxs-lookup"><span data-stu-id="9550b-110">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the encoding type used to encode the enveloped data.</span></span> <span data-ttu-id="9550b-111">預設的編碼值為 CAPICOM \_ 編碼 \_ BASE64。</span><span class="sxs-lookup"><span data-stu-id="9550b-111">The default encoding value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="9550b-112">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9550b-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="9550b-113">值</span><span class="sxs-lookup"><span data-stu-id="9550b-113">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="9550b-114">意義</span><span class="sxs-lookup"><span data-stu-id="9550b-114">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="9550b-115"><dt>**CAPICOM \_ 編碼 \_ 任何**</dt></span><span class="sxs-lookup"><span data-stu-id="9550b-115"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="9550b-116">只有當輸入資料有未知的編碼類型時，才會使用此編碼類型。</span><span class="sxs-lookup"><span data-stu-id="9550b-116">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="9550b-117">如果這個值是用來指定輸出的編碼類型，則會 \_ 改用 CAPICOM 編碼 \_ BASE64。</span><span class="sxs-lookup"><span data-stu-id="9550b-117">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="9550b-118">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="9550b-118">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="9550b-119"><dt>**CAPICOM \_ 編碼 \_ BASE64**</dt></span><span class="sxs-lookup"><span data-stu-id="9550b-119"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="9550b-120">資料會儲存為 base64 編碼字串。</span><span class="sxs-lookup"><span data-stu-id="9550b-120">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="9550b-121"><dt>**CAPICOM \_ 編碼 \_ 二進位**</dt></span><span class="sxs-lookup"><span data-stu-id="9550b-121"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="9550b-122">資料會儲存為純二進位序列。</span><span class="sxs-lookup"><span data-stu-id="9550b-122">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9550b-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="9550b-123">Return value</span></span>

<span data-ttu-id="9550b-124">這個方法會傳回 BLOB，其中包含編碼字串中的封包資料。</span><span class="sxs-lookup"><span data-stu-id="9550b-124">This method returns a BLOB that contains the enveloped data in an encoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="9550b-125">備註</span><span class="sxs-lookup"><span data-stu-id="9550b-125">Remarks</span></span>

<span data-ttu-id="9550b-126">傳回的 BLOB 包含加密的內容，以及每個預定收件者的加密工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="9550b-126">The returned BLOB contains the encrypted content and an encrypted session key for each intended recipient.</span></span> <span data-ttu-id="9550b-127">這些工作階段金鑰會使用每個收件者的公開金鑰進行加密。</span><span class="sxs-lookup"><span data-stu-id="9550b-127">These session keys are encrypted using the public key of each recipient.</span></span> <span data-ttu-id="9550b-128">加密的工作階段金鑰只能使用收件者的私密金鑰進行解密。</span><span class="sxs-lookup"><span data-stu-id="9550b-128">The encrypted session keys can be decrypted only with a recipient's private key.</span></span>

<span data-ttu-id="9550b-129">如果收件者屬性不包含任何資訊 [**，則此**](envelopeddata-recipients.md) 方法會搜尋目前使用者的 AddressBook 憑證存放區中是否有潛在的收件者。</span><span class="sxs-lookup"><span data-stu-id="9550b-129">If the [**Recipients**](envelopeddata-recipients.md) property does not contain any information, this method searches the current user's AddressBook certificate store for potential recipients.</span></span> <span data-ttu-id="9550b-130">如果找到多個潛在的收件者，則會提示使用者從選取範圍對話方塊中選取收件者。</span><span class="sxs-lookup"><span data-stu-id="9550b-130">If more than one potential recipient is found, the user is prompted to select a recipient from a selection dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="9550b-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="9550b-131">Requirements</span></span>



| <span data-ttu-id="9550b-132">需求</span><span class="sxs-lookup"><span data-stu-id="9550b-132">Requirement</span></span> | <span data-ttu-id="9550b-133">值</span><span class="sxs-lookup"><span data-stu-id="9550b-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9550b-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9550b-134">End of client support</span></span><br/> | <span data-ttu-id="9550b-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9550b-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9550b-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="9550b-136">End of server support</span></span><br/> | <span data-ttu-id="9550b-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9550b-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9550b-138">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="9550b-138">Redistributable</span></span><br/>       | <span data-ttu-id="9550b-139">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9550b-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9550b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9550b-140">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9550b-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9550b-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9550b-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9550b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9550b-143">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="9550b-143">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="9550b-144">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="9550b-144">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
