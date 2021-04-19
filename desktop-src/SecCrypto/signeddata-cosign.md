---
description: 在先前簽署的內容上建立數位簽章。
ms.assetid: c0a3de75-afba-45ba-b701-2729f4495eda
title: SignedData. CoSign 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.CoSign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1ab2a24a20fd65fad9622b775bedc59cfa28301a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984860"
---
# <a name="signeddatacosign-method"></a><span data-ttu-id="7dc5c-103">SignedData. CoSign 方法</span><span class="sxs-lookup"><span data-stu-id="7dc5c-103">SignedData.CoSign method</span></span>

<span data-ttu-id="7dc5c-104">\[**CoSign** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-104">\[The **CoSign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7dc5c-105">相反地，請使用 [**SignedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="7dc5c-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="7dc5c-106">**CoSign** 方法會在先前簽署的內容上建立 [*數位簽章*](../secgloss/d-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-106">The **CoSign** method creates a [*digital signature*](../secgloss/d-gly.md) on previously signed content.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc5c-107">語法</span><span class="sxs-lookup"><span data-stu-id="7dc5c-107">Syntax</span></span>


```VB
SignedData.CoSign( _
  [ ByVal Signer ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7dc5c-108">參數</span><span class="sxs-lookup"><span data-stu-id="7dc5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dc5c-109">*簽署者* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="7dc5c-109">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7dc5c-110">資料簽署者之 [**簽署者**](signer.md) 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-110">A reference to the [**Signer**](signer.md) object of the signer of the data.</span></span> <span data-ttu-id="7dc5c-111">**簽署者** 物件必須能夠存取用來簽署的憑證私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-111">The **Signer** object must have access to the private key of the certificate used to sign.</span></span> <span data-ttu-id="7dc5c-112">這個參數可以是 **Null**;如需詳細資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-112">This parameter can be **NULL**; for more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7dc5c-113">*Edi.encodingtype* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="7dc5c-113">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7dc5c-114">[**CAPICOM \_ 編碼 \_ 類型**](capicom-encoding-type.md)列舉的值，指出簽署的資料如何進行編碼。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-114">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates how the signed data is to be encoded.</span></span> <span data-ttu-id="7dc5c-115">預設值為 CAPICOM \_ 編碼 \_ BASE64。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-115">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="7dc5c-116">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="7dc5c-117">值</span><span class="sxs-lookup"><span data-stu-id="7dc5c-117">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="7dc5c-118">意義</span><span class="sxs-lookup"><span data-stu-id="7dc5c-118">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="7dc5c-119"><dt>**CAPICOM \_ 編碼 \_ 任何**</dt></span><span class="sxs-lookup"><span data-stu-id="7dc5c-119"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="7dc5c-120">只有當輸入資料有未知的編碼類型時，才會使用此編碼類型。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-120">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="7dc5c-121">如果這個值是用來指定輸出的編碼類型，則會 \_ 改用 CAPICOM 編碼 \_ BASE64。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-121">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="7dc5c-122">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-122">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="7dc5c-123"><dt>**CAPICOM \_ 編碼 \_ BASE64**</dt></span><span class="sxs-lookup"><span data-stu-id="7dc5c-123"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="7dc5c-124">資料會儲存為 base64 編碼字串。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-124">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="7dc5c-125"><dt>**CAPICOM \_ 編碼 \_ 二進位**</dt></span><span class="sxs-lookup"><span data-stu-id="7dc5c-125"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="7dc5c-126">資料會儲存為純二進位序列。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-126">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dc5c-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="7dc5c-127">Return value</span></span>

<span data-ttu-id="7dc5c-128">這個方法會傳回字串，其中包含已編碼、已簽署的資料。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-128">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="7dc5c-129">如果此方法失敗，則會擲回錯誤。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-129">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="7dc5c-130">**Err** 物件將包含有關錯誤的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-130">The **Err** object will contain additional information about the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dc5c-131">備註</span><span class="sxs-lookup"><span data-stu-id="7dc5c-131">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7dc5c-132">從 web 腳本呼叫這個方法時，腳本必須使用您的 [*私密金鑰*](../secgloss/p-gly.md) 來建立數位簽章。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-132">When this method is called from a web script, the script needs to use your [*private key*](../secgloss/p-gly.md) to create a digital signature.</span></span> <span data-ttu-id="7dc5c-133">允許不受信任的網站使用您的私密金鑰會有安全性風險。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-133">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="7dc5c-134">當第一次呼叫此方法時，會詢問網站是否可以使用您的私密金鑰的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-134">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="7dc5c-135">如果您允許腳本使用您的私密金鑰來建立數位簽章，然後選取 [不要再顯示此對話方塊]，則該網域內使用您的私密金鑰來建立數位簽章的任何腳本將不會再出現此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-135">If you allow the script to use your private key to create a digital signature and select "Do not show this dialog box again," the dialog box will no longer appear for any script within that domain that uses your private key to create a digital signature.</span></span> <span data-ttu-id="7dc5c-136">不過，嘗試使用您的私密金鑰來建立數位簽章的網域以外的腳本仍會出現此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-136">However, scripts outside that domain that attempt to use your private key to create a digital signature will still cause this dialog box to appear.</span></span> <span data-ttu-id="7dc5c-137">如果您不允許腳本使用您的私密金鑰，然後選取 [不要再顯示此對話方塊]，則該網域內的腳本將會自動拒絕使用您私密金鑰來建立數位簽章的能力。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-137">If you do not allow the script to use your private key and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to use your private key to create digital signatures.</span></span>

 

<span data-ttu-id="7dc5c-138">非人保證會以任何特定順序來進行。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-138">Cosigners are not guaranteed to be in any particular order.</span></span>

<span data-ttu-id="7dc5c-139">下列結果適用于 *簽署者* 參數值：</span><span class="sxs-lookup"><span data-stu-id="7dc5c-139">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="7dc5c-140">如果 *簽署者* 參數不是 **Null**，這個方法會使用相關聯憑證所指向的私密金鑰來加密 cosignature。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-140">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the cosignature.</span></span> <span data-ttu-id="7dc5c-141">如果憑證所指向的私密金鑰無法使用，方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-141">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="7dc5c-142">如果 *簽署者* 參數為 **Null** ，而且目前的使用者儲存區中只有一個可存取私密金鑰的憑證，則會 \_ 使用該憑證來建立 cosignature。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-142">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key, that certificate is used to create the cosignature.</span></span>
-   <span data-ttu-id="7dc5c-143">如果 *簽署者* 參數為 **Null**， [**EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) 屬性值為 true，而且目前使用者的存放區中有一個以上的憑證 \_ 具有可用的私密金鑰，則會出現一個對話方塊，讓使用者選取要使用的憑證。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-143">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="7dc5c-144">如果 *簽署者* 參數為 **Null** ，而且 [**EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) 屬性為 false，則方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-144">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="7dc5c-145">如果 *簽署者* 參數為 **Null** ，而且目前 \_ 使用者的存放區中沒有具有可用私密金鑰的憑證，則該方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="7dc5c-145">If the *Signer* parameter is **NULL** and there is no certificate in the CURRENT\_USER MY store with an available private key, the method fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dc5c-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="7dc5c-146">Requirements</span></span>



| <span data-ttu-id="7dc5c-147">需求</span><span class="sxs-lookup"><span data-stu-id="7dc5c-147">Requirement</span></span> | <span data-ttu-id="7dc5c-148">值</span><span class="sxs-lookup"><span data-stu-id="7dc5c-148">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc5c-149">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7dc5c-149">Redistributable</span></span><br/> | <span data-ttu-id="7dc5c-150">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7dc5c-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7dc5c-151">DLL</span><span class="sxs-lookup"><span data-stu-id="7dc5c-151">DLL</span></span><br/>             | <dl> <span data-ttu-id="7dc5c-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dc5c-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dc5c-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7dc5c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc5c-154">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="7dc5c-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="7dc5c-155">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="7dc5c-155">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
