---
description: 將憑證儲存至檔案。
ms.assetid: 2012b39b-47fd-4071-9752-98bb10954fc0
title: ICertificate2：： Save 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Save
- ICertificate2.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3427feb86c705f5558d083bc39673fdf77553f58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983004"
---
# <a name="icertificate2save-method"></a><span data-ttu-id="9ede5-103">ICertificate2：： Save 方法</span><span class="sxs-lookup"><span data-stu-id="9ede5-103">ICertificate2::Save method</span></span>

<span data-ttu-id="9ede5-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="9ede5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9ede5-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="9ede5-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="9ede5-106">Save 方法會將憑證 **儲存** 至檔案。</span><span class="sxs-lookup"><span data-stu-id="9ede5-106">The **Save** method saves the certificate to a file.</span></span> <span data-ttu-id="9ede5-107">此方法是在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="9ede5-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ede5-108">語法</span><span class="sxs-lookup"><span data-stu-id="9ede5-108">Syntax</span></span>


```VB
Certificate.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal IncludeOption ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9ede5-109">參數</span><span class="sxs-lookup"><span data-stu-id="9ede5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ede5-110">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9ede5-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ede5-111">字串，其中包含將儲存憑證的輸出檔名稱。</span><span class="sxs-lookup"><span data-stu-id="9ede5-111">A string that contains the name of the output file where the certificate will be saved.</span></span>

</dd> <dt>

<span data-ttu-id="9ede5-112">*密碼* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9ede5-112">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9ede5-113">字串，其中包含 [*私密金鑰*](../secgloss/p-gly.md)檔案的 [*純文字*](../secgloss/p-gly.md)密碼。</span><span class="sxs-lookup"><span data-stu-id="9ede5-113">A string that contains the [*plaintext*](../secgloss/p-gly.md) password for a [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="9ede5-114">密碼最多可包含32個 Unicode 字元，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="9ede5-114">The password can contain up to 32 Unicode characters, including a terminating null character.</span></span> <span data-ttu-id="9ede5-115">如需保護密碼的相關資訊，請參閱 [處理密碼](../secbp/handling-passwords.md)。</span><span class="sxs-lookup"><span data-stu-id="9ede5-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ede5-116">*SaveAs* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9ede5-116">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9ede5-117">指定輸出檔格式之 [**CAPICOM \_ 憑證 \_ 儲存 \_ 為 \_ 類型**](capicom-certificate-save-as-type.md) 列舉的值。</span><span class="sxs-lookup"><span data-stu-id="9ede5-117">A value of the [**CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE**](capicom-certificate-save-as-type.md) enumeration that specifies the format of the output file.</span></span> <span data-ttu-id="9ede5-118">預設值為 **[ \_ 將 CAPICOM 憑證 \_ 另存 \_ 為 \_ CER**]。</span><span class="sxs-lookup"><span data-stu-id="9ede5-118">The default is **CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**.</span></span> <span data-ttu-id="9ede5-119">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="9ede5-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="9ede5-120">值</span><span class="sxs-lookup"><span data-stu-id="9ede5-120">Value</span></span>                                                                                                                                                                                                                  | <span data-ttu-id="9ede5-121">意義</span><span class="sxs-lookup"><span data-stu-id="9ede5-121">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_CER"></span><span id="capicom_certificate_save_as_cer"></span><dl> <span data-ttu-id="9ede5-122"><dt>**\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ CER**</dt></span><span class="sxs-lookup"><span data-stu-id="9ede5-122"><dt>**CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**</dt></span></span> </dl> | <span data-ttu-id="9ede5-123">輸出檔案會格式化為不儲存私密金鑰的 .cer 檔案。</span><span class="sxs-lookup"><span data-stu-id="9ede5-123">The output file will be formatted as a .cer file with no private keys saved.</span></span><br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_PFX"></span><span id="capicom_certificate_save_as_pfx"></span><dl> <span data-ttu-id="9ede5-124"><dt>**\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ PFX**</dt></span><span class="sxs-lookup"><span data-stu-id="9ede5-124"><dt>**CAPICOM\_CERTIFICATE\_SAVE\_AS\_PFX**</dt></span></span> </dl> | <span data-ttu-id="9ede5-125">輸出檔將格式化為 .pfx (PKCS \# 12) 檔案，而且任何可匯出的相關私密金鑰也會儲存。</span><span class="sxs-lookup"><span data-stu-id="9ede5-125">The output file will be formatted as a .pfx (PKCS \#12) file and any associated private keys that are exportable will also be saved.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9ede5-126">*IncludeOption* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9ede5-126">*IncludeOption* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9ede5-127">[**CAPICOM \_ 憑證 \_ 包含 \_ 選項**](capicom-certificate-include-option.md)列舉值，這個值會指定要將鏈中的憑證儲存到輸出檔的數量。</span><span class="sxs-lookup"><span data-stu-id="9ede5-127">A value of the [**CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION**](capicom-certificate-include-option.md) enumeration that specifies how many certificates in the chain are saved to the output file.</span></span> <span data-ttu-id="9ede5-128">預設值為 [ \_ \_ 僅限 CAPICOM 憑證包含 \_ 結束實體] \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="9ede5-128">The default is CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY.</span></span> <span data-ttu-id="9ede5-129">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="9ede5-129">The following table shows the possible values.</span></span>



| <span data-ttu-id="9ede5-130">值</span><span class="sxs-lookup"><span data-stu-id="9ede5-130">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="9ede5-131">意義</span><span class="sxs-lookup"><span data-stu-id="9ede5-131">Meaning</span></span>                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <span data-ttu-id="9ede5-132"><dt>**\_ \_ \_ \_ 除了 \_ 根以外的 CAPICOM 憑證包含鏈**</dt></span><span class="sxs-lookup"><span data-stu-id="9ede5-132"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</dt></span></span> </dl> | <span data-ttu-id="9ede5-133">將所有憑證儲存在鏈中，但根實體除外</span><span class="sxs-lookup"><span data-stu-id="9ede5-133">Saves all certificates in the chain with the exception of the root entity</span></span><br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <span data-ttu-id="9ede5-134"><dt>**CAPICOM \_ 憑證 \_ 包含 \_ 整個 \_ 鏈**</dt></span><span class="sxs-lookup"><span data-stu-id="9ede5-134"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</dt></span></span> </dl>                    | <span data-ttu-id="9ede5-135">儲存完整的憑證鏈</span><span class="sxs-lookup"><span data-stu-id="9ede5-135">Saves the complete certificate chain</span></span><br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <span data-ttu-id="9ede5-136"><dt>**\_ \_ 僅限 CAPICOM 憑證包含 \_ 結束 \_ 實體 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9ede5-136"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</dt></span></span> </dl>       | <span data-ttu-id="9ede5-137">只儲存終端實體憑證</span><span class="sxs-lookup"><span data-stu-id="9ede5-137">Saves only the end entity certificate</span></span><br/>                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ede5-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ede5-138">Return value</span></span>

<span data-ttu-id="9ede5-139">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9ede5-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ede5-140">備註</span><span class="sxs-lookup"><span data-stu-id="9ede5-140">Remarks</span></span>

<span data-ttu-id="9ede5-141">\_ \_ \_ 從 web 應用程式編寫腳本時，此方法不允許引發 CAPICOM E。</span><span class="sxs-lookup"><span data-stu-id="9ede5-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ede5-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ede5-142">Requirements</span></span>



| <span data-ttu-id="9ede5-143">需求</span><span class="sxs-lookup"><span data-stu-id="9ede5-143">Requirement</span></span> | <span data-ttu-id="9ede5-144">值</span><span class="sxs-lookup"><span data-stu-id="9ede5-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ede5-145">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9ede5-145">End of client support</span></span><br/> | <span data-ttu-id="9ede5-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ede5-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9ede5-147">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="9ede5-147">End of server support</span></span><br/> | <span data-ttu-id="9ede5-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ede5-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9ede5-149">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="9ede5-149">Redistributable</span></span><br/>       | <span data-ttu-id="9ede5-150">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9ede5-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9ede5-151">DLL</span><span class="sxs-lookup"><span data-stu-id="9ede5-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9ede5-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ede5-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
