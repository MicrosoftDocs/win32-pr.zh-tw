---
description: 判斷 SignedData 物件中已簽署資料的簽章是否有效。
ms.assetid: 920ac235-0c1a-4b15-9cdd-c7e0c3ea6107
title: SignedData Verify 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3cb48943a826296c13df80130171442fc29435f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000685"
---
# <a name="signeddataverify-method"></a><span data-ttu-id="0c408-103">SignedData Verify 方法</span><span class="sxs-lookup"><span data-stu-id="0c408-103">SignedData.Verify method</span></span>

<span data-ttu-id="0c408-104">\[[ **驗證** ] 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="0c408-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0c408-105">相反地，請使用 [**SignedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="0c408-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="0c408-106">**Verify** 方法會判斷 [**SignedData**](signeddata.md)物件中已簽署 [*資料的簽*](../secgloss/d-gly.md)章是否有效。</span><span class="sxs-lookup"><span data-stu-id="0c408-106">The **Verify** method determines whether the [*signatures*](../secgloss/d-gly.md) on signed data in the [**SignedData**](signeddata.md) object are valid.</span></span> <span data-ttu-id="0c408-107">若要驗證簽章，內容的加密 [*雜湊*](../secgloss/h-gly.md) 會使用簽署者憑證的簽署者公開金鑰進行解密。</span><span class="sxs-lookup"><span data-stu-id="0c408-107">To verify a signature, the encrypted [*hash*](../secgloss/h-gly.md) of the contents is decrypted by using the signer's public key from the signer's certificate.</span></span> <span data-ttu-id="0c408-108">解密的雜湊會與新的資料內容雜湊進行比較。</span><span class="sxs-lookup"><span data-stu-id="0c408-108">The decrypted hash is compared to a new hash of the data content.</span></span> <span data-ttu-id="0c408-109">如果雜湊相符，則簽章有效。</span><span class="sxs-lookup"><span data-stu-id="0c408-109">A signature is valid if the hashes match.</span></span> <span data-ttu-id="0c408-110">此外，這個方法也會建立憑證鏈，以判斷憑證的有效性，以提供用來解密雜湊的 [*公開金鑰*](../secgloss/p-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="0c408-110">In addition, this method also builds a certificate chain to determine the validity of the certificate that provides the [*public key*](../secgloss/p-gly.md) used to decrypt the hash.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c408-111">語法</span><span class="sxs-lookup"><span data-stu-id="0c408-111">Syntax</span></span>


```VB
SignedData.Verify( _
  ByVal SignedMessage, _
  [ ByVal bDetached ], _
  [ ByVal VerifyFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="0c408-112">參數</span><span class="sxs-lookup"><span data-stu-id="0c408-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c408-113">*SignedMessage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0c408-113">*SignedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c408-114">包含要驗證之已簽署訊息的字串。</span><span class="sxs-lookup"><span data-stu-id="0c408-114">A string that contains the signed message to be verified.</span></span>

</dd> <dt>

<span data-ttu-id="0c408-115">*bDetached* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="0c408-115">*bDetached* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0c408-116">若為 **True**，則會卸離要簽署的資料;也就是說，簽署的內容不會包含在簽署的物件中。</span><span class="sxs-lookup"><span data-stu-id="0c408-116">If **True**, the data to be signed is detached; that is, the content that is signed is not included as part of the signed object.</span></span> <span data-ttu-id="0c408-117">若要確認卸離內容上的簽章，應用程式必須有原始內容的複本。</span><span class="sxs-lookup"><span data-stu-id="0c408-117">To verify the signature on detached content, an application must have a copy of the original content.</span></span> <span data-ttu-id="0c408-118">如果已簽署訊息的收件者具有已簽署資料的原始複本，則通常會使用卸離的內容來減少在 web 上傳送的已簽署物件大小。</span><span class="sxs-lookup"><span data-stu-id="0c408-118">Detached content is often used to decrease the size of a signed object to be sent across the web, if the recipient of the signed message has an original copy of the signed data.</span></span> <span data-ttu-id="0c408-119">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="0c408-119">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="0c408-120">*VerifyFlag* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="0c408-120">*VerifyFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0c408-121">表示驗證原則的 [CAPICOM \_ 帶正負號 \_ 資料 \_ 驗證 \_ 旗](capicom-signed-data-verify-flag.md) 標列舉值。</span><span class="sxs-lookup"><span data-stu-id="0c408-121">A value of the [CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG](capicom-signed-data-verify-flag.md) enumeration that indicates the verification policy.</span></span> <span data-ttu-id="0c408-122">預設值是 [CAPICOM \_ 驗證簽章 \_ \_ 和 \_ 憑證]。</span><span class="sxs-lookup"><span data-stu-id="0c408-122">The default value is CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE.</span></span> <span data-ttu-id="0c408-123">使用此值，就會檢查憑證的有效性和簽章的有效性。</span><span class="sxs-lookup"><span data-stu-id="0c408-123">Using this value, both the validity of the certificate and the validity of the signature are checked.</span></span> <span data-ttu-id="0c408-124">此參數可設定為驗證簽章，而非憑證。</span><span class="sxs-lookup"><span data-stu-id="0c408-124">This parameter may be set to verify the signature and not the certificate.</span></span> <span data-ttu-id="0c408-125">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0c408-125">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="0c408-126">值</span><span class="sxs-lookup"><span data-stu-id="0c408-126">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="0c408-127">意義</span><span class="sxs-lookup"><span data-stu-id="0c408-127">Meaning</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_VERIFY_SIGNATURE_ONLY"></span><span id="capicom_verify_signature_only"></span><dl> <span data-ttu-id="0c408-128"><dt>**\_ \_ 僅限 CAPICOM 驗證簽章 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c408-128"><dt>**CAPICOM\_VERIFY\_SIGNATURE\_ONLY**</dt></span></span> </dl>                                   | <span data-ttu-id="0c408-129">只會檢查簽章。</span><span class="sxs-lookup"><span data-stu-id="0c408-129">Only the signature is checked.</span></span><br/>                                                                   |
| <span id="CAPICOM_VERIFY_SIGNATURE_AND_CERTIFICATE"></span><span id="capicom_verify_signature_and_certificate"></span><dl> <span data-ttu-id="0c408-130"><dt>**CAPICOM \_ 驗證簽章 \_ \_ 和 \_ 憑證**</dt></span><span class="sxs-lookup"><span data-stu-id="0c408-130"><dt>**CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE**</dt></span></span> </dl> | <span data-ttu-id="0c408-131">檢查簽章和用來建立簽章之憑證的有效性。</span><span class="sxs-lookup"><span data-stu-id="0c408-131">Both the signature and the validity of the certificate used to create the signature are checked.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c408-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c408-132">Return value</span></span>

<span data-ttu-id="0c408-133">這個方法會傳回字串，其中包含已編碼、已簽署的資料。</span><span class="sxs-lookup"><span data-stu-id="0c408-133">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="0c408-134">如果此方法失敗，則會擲回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0c408-134">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="0c408-135">**Err** 物件將包含有關錯誤的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="0c408-135">The **Err** object will contain additional information about the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c408-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c408-136">Requirements</span></span>



| <span data-ttu-id="0c408-137">需求</span><span class="sxs-lookup"><span data-stu-id="0c408-137">Requirement</span></span> | <span data-ttu-id="0c408-138">值</span><span class="sxs-lookup"><span data-stu-id="0c408-138">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c408-139">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="0c408-139">Redistributable</span></span><br/> | <span data-ttu-id="0c408-140">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="0c408-140">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0c408-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0c408-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="0c408-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c408-142"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c408-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c408-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c408-144">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="0c408-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="0c408-145">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="0c408-145">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
