---
description: 在要簽署的內容上建立數位簽章。 數位簽章包含要簽署之內容的雜湊，該內容是使用簽署者的私密金鑰進行加密。
ms.assetid: ee98a36c-f9a9-4247-ae48-7b1a10b92be4
title: SignedData. Sign 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9f885bb110b51264bc6108ca8c0f881cc48f7710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994184"
---
# <a name="signeddatasign-method"></a><span data-ttu-id="b15b4-104">SignedData. Sign 方法</span><span class="sxs-lookup"><span data-stu-id="b15b4-104">SignedData.Sign method</span></span>

<span data-ttu-id="b15b4-105">\[**Sign** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b15b4-105">\[The **Sign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b15b4-106">相反地，請使用 [**SignedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="b15b4-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="b15b4-107">**Sign** 方法會在要簽署的內容上建立 [*數位簽章*](../secgloss/d-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b15b4-107">The **Sign** method creates a [*digital signature*](../secgloss/d-gly.md) on the content to be signed.</span></span> <span data-ttu-id="b15b4-108">數位簽章包含要簽署之內容的 [*雜湊*](../secgloss/h-gly.md) ，該內容是使用簽署者的私密金鑰進行加密。</span><span class="sxs-lookup"><span data-stu-id="b15b4-108">A digital signature consists of a [*hash*](../secgloss/h-gly.md) of the content to be signed that is encrypted by using the private key of the signer.</span></span> <span data-ttu-id="b15b4-109">只有在已初始化 [**SignedData 內容**](signeddata-content.md) 屬性之後，才能使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="b15b4-109">This method can only be used after the [**SignedData.Content**](signeddata-content.md) property has been initialized.</span></span> <span data-ttu-id="b15b4-110">如果在已經有簽章的物件上呼叫 Sign 方法，則會取代舊的 **簽** 章。</span><span class="sxs-lookup"><span data-stu-id="b15b4-110">If the **Sign** method is called on an object that already has a signature, the old signature is replaced.</span></span> <span data-ttu-id="b15b4-111">簽章是使用 SHA1 簽署演算法來建立。</span><span class="sxs-lookup"><span data-stu-id="b15b4-111">The signature is created by using the SHA1 signing algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="b15b4-112">語法</span><span class="sxs-lookup"><span data-stu-id="b15b4-112">Syntax</span></span>


```VB
SignedData.Sign( _
  [ ByVal Signer ], _
  [ ByVal bDetached ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b15b4-113">參數</span><span class="sxs-lookup"><span data-stu-id="b15b4-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b15b4-114">*簽署者* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="b15b4-114">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b15b4-115">資料簽署者之 [**簽署者**](signer.md) 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="b15b4-115">A reference to the [**Signer**](signer.md) object of the signer of the data.</span></span> <span data-ttu-id="b15b4-116">**簽署者** 物件必須能夠存取用來簽署的 [*憑證*](../secgloss/c-gly.md)[*私密金鑰*](../secgloss/p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b15b4-116">The **Signer** object must have access to the [*private key*](../secgloss/p-gly.md) of the [*certificate*](../secgloss/c-gly.md) used to sign.</span></span> <span data-ttu-id="b15b4-117">這個參數可以是 **Null**;如需詳細資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="b15b4-117">This parameter can be **NULL**; for more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b15b4-118">*bDetached* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="b15b4-118">*bDetached* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b15b4-119">若為 **True**，則會卸離要簽署的資料;也就是說，簽署的內容不會包含在簽署的物件中。</span><span class="sxs-lookup"><span data-stu-id="b15b4-119">If **True**, the data to be signed is detached; that is, the content that is signed is not included as part of the signed object.</span></span> <span data-ttu-id="b15b4-120">若要確認卸離內容上的簽章，應用程式必須有原始內容的複本。</span><span class="sxs-lookup"><span data-stu-id="b15b4-120">To verify the signature on detached content, an application must have a copy of the original content.</span></span> <span data-ttu-id="b15b4-121">如果已簽署訊息的收件者具有已簽署資料的原始複本，則通常會使用卸離的內容來減少在 web 上傳送的已簽署物件大小。</span><span class="sxs-lookup"><span data-stu-id="b15b4-121">Detached content is often used to decrease the size of a signed object to be sent across the web, if the recipient of the signed message has an original copy of the signed data.</span></span> <span data-ttu-id="b15b4-122">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="b15b4-122">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="b15b4-123">*Edi.encodingtype* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="b15b4-123">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b15b4-124">[CAPICOM \_ 編碼 \_ 類型](capicom-encoding-type.md)列舉的值，指出簽署的資料如何進行編碼。</span><span class="sxs-lookup"><span data-stu-id="b15b4-124">A value of the [CAPICOM\_ENCODING\_TYPE](capicom-encoding-type.md) enumeration that indicates how the signed data is to be encoded.</span></span> <span data-ttu-id="b15b4-125">預設值為 CAPICOM \_ 編碼 \_ BASE64。</span><span class="sxs-lookup"><span data-stu-id="b15b4-125">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="b15b4-126">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b15b4-126">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b15b4-127">值</span><span class="sxs-lookup"><span data-stu-id="b15b4-127">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="b15b4-128">意義</span><span class="sxs-lookup"><span data-stu-id="b15b4-128">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="b15b4-129"><dt>**CAPICOM \_ 編碼 \_ 任何**</dt></span><span class="sxs-lookup"><span data-stu-id="b15b4-129"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="b15b4-130">只有當輸入資料有未知的編碼類型時，才會使用此編碼類型。</span><span class="sxs-lookup"><span data-stu-id="b15b4-130">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="b15b4-131">如果這個值是用來指定輸出的編碼類型，則會 \_ 改用 CAPICOM 編碼 \_ BASE64。</span><span class="sxs-lookup"><span data-stu-id="b15b4-131">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="b15b4-132">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="b15b4-132">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="b15b4-133"><dt>**CAPICOM \_ 編碼 \_ BASE64**</dt></span><span class="sxs-lookup"><span data-stu-id="b15b4-133"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="b15b4-134">資料會儲存為 base64 編碼字串。</span><span class="sxs-lookup"><span data-stu-id="b15b4-134">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="b15b4-135"><dt>**CAPICOM \_ 編碼 \_ 二進位**</dt></span><span class="sxs-lookup"><span data-stu-id="b15b4-135"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="b15b4-136">資料會儲存為純二進位序列。</span><span class="sxs-lookup"><span data-stu-id="b15b4-136">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b15b4-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="b15b4-137">Return value</span></span>

<span data-ttu-id="b15b4-138">這個方法會傳回字串，其中包含已編碼、已簽署的資料。</span><span class="sxs-lookup"><span data-stu-id="b15b4-138">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="b15b4-139">如果此方法失敗，則會擲回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b15b4-139">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="b15b4-140">**Err** 物件將包含有關錯誤的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="b15b4-140">The **Err** object will contain additional information about the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="b15b4-141">備註</span><span class="sxs-lookup"><span data-stu-id="b15b4-141">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b15b4-142">從 web 腳本呼叫這個方法時，腳本必須使用您的私密金鑰來建立數位簽章。</span><span class="sxs-lookup"><span data-stu-id="b15b4-142">When this method is called from a web script, the script needs to use your private key to create a digital signature.</span></span> <span data-ttu-id="b15b4-143">允許不受信任的網站使用您的私密金鑰會有安全性風險。</span><span class="sxs-lookup"><span data-stu-id="b15b4-143">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="b15b4-144">當第一次呼叫此方法時，會詢問網站是否可以使用您的私密金鑰的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b15b4-144">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="b15b4-145">如果您允許腳本使用您的私密金鑰來建立數位簽章，然後選取 [不要再顯示此對話方塊]，則該網域內使用您的私密金鑰來建立數位簽章的任何腳本將不會再出現此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b15b4-145">If you allow the script to use your private key to create a digital signature and select "Do not show this dialog box again," the dialog box will no longer appear for any script within that domain that uses your private key to create a digital signature.</span></span> <span data-ttu-id="b15b4-146">不過，嘗試使用您的私密金鑰來建立數位簽章的網域以外的腳本仍會出現此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b15b4-146">However, scripts outside that domain that attempt to use your private key to create a digital signature will still cause this dialog box to appear.</span></span> <span data-ttu-id="b15b4-147">如果您不允許腳本使用您的私密金鑰，然後選取 [不要再顯示此對話方塊]，則該網域內的腳本將會自動拒絕使用您私密金鑰來建立數位簽章的能力。</span><span class="sxs-lookup"><span data-stu-id="b15b4-147">If you do not allow the script to use your private key and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to use your private key to create digital signatures.</span></span>

 

<span data-ttu-id="b15b4-148">因為建立 [*數位簽章*](../secgloss/d-gly.md) 需要使用 [*私密金鑰*](../secgloss/p-gly.md)，所以嘗試使用這個方法的 web 應用程式將需要使用者介面提示，讓使用者基於安全性理由核准私密金鑰的使用。</span><span class="sxs-lookup"><span data-stu-id="b15b4-148">Because creating a [*digital signature*](../secgloss/d-gly.md) requires the use of a [*private key*](../secgloss/p-gly.md), web-based applications that attempt to use this method will require user interface prompts that allow the user to approve the use of the private key, for security reasons.</span></span>

<span data-ttu-id="b15b4-149">下列結果適用于 *簽署者* 參數值：</span><span class="sxs-lookup"><span data-stu-id="b15b4-149">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="b15b4-150">如果 *簽署者* 參數不是 **Null**，這個方法會使用相關聯憑證所指向的私密金鑰來加密簽章。</span><span class="sxs-lookup"><span data-stu-id="b15b4-150">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the signature.</span></span> <span data-ttu-id="b15b4-151">如果憑證所指向的私密金鑰無法使用，方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="b15b4-151">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="b15b4-152">如果 *簽署者* 參數為 **Null** ，而且目前的使用者儲存區中只有一個可存取私密金鑰的憑證，則會 \_ 使用該憑證來建立簽章。</span><span class="sxs-lookup"><span data-stu-id="b15b4-152">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key, that certificate is used to create the signature.</span></span>
-   <span data-ttu-id="b15b4-153">如果 *簽署者* 參數為 **Null**， [**EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) 屬性值為 true，而且目前使用者的存放區中有一個以上的憑證 \_ 具有可用的私密金鑰，則會出現一個對話方塊，讓使用者選取要使用的憑證。</span><span class="sxs-lookup"><span data-stu-id="b15b4-153">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="b15b4-154">如果 *簽署者* 參數為 **Null** ，而且 [**EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) 屬性為 false，則方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="b15b4-154">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="b15b4-155">如果 *簽署者* 參數為 **Null** ，而且目前 \_ 使用者的存放區中沒有具有可用私密金鑰的憑證，則該方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="b15b4-155">If the *Signer* parameter is **NULL** and there is no certificate in the CURRENT\_USER MY store with an available private key, the method fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="b15b4-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="b15b4-156">Requirements</span></span>



| <span data-ttu-id="b15b4-157">需求</span><span class="sxs-lookup"><span data-stu-id="b15b4-157">Requirement</span></span> | <span data-ttu-id="b15b4-158">值</span><span class="sxs-lookup"><span data-stu-id="b15b4-158">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b15b4-159">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b15b4-159">Redistributable</span></span><br/> | <span data-ttu-id="b15b4-160">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b15b4-160">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b15b4-161">DLL</span><span class="sxs-lookup"><span data-stu-id="b15b4-161">DLL</span></span><br/>             | <dl> <span data-ttu-id="b15b4-162"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b15b4-162"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b15b4-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b15b4-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b15b4-164">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="b15b4-164">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="b15b4-165">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="b15b4-165">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
