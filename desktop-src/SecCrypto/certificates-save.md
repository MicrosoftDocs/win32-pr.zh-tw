---
description: 將憑證物件儲存在集合中。
ms.assetid: 1d4b7bd5-3ed3-4ace-9894-4e89c5cf844f
title: Certificate. Save 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36ab04b394bddcd829d9f15e7562b72125388d33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995083"
---
# <a name="certificatessave-method"></a><span data-ttu-id="30891-103">Certificate. Save 方法</span><span class="sxs-lookup"><span data-stu-id="30891-103">Certificates.Save method</span></span>

<span data-ttu-id="30891-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="30891-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="30891-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/previous-versions/windows/embedded/hh424013(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="30891-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="30891-106">Save 方法會將 [**憑證**](certificate.md)物件 **儲存** 在集合中。</span><span class="sxs-lookup"><span data-stu-id="30891-106">The **Save** method saves the [**Certificate**](certificate.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="30891-107">語法</span><span class="sxs-lookup"><span data-stu-id="30891-107">Syntax</span></span>


```VB
Certificates.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal ExportFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="30891-108">參數</span><span class="sxs-lookup"><span data-stu-id="30891-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30891-109">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30891-109">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30891-110">字串，其中包含將儲存憑證的輸出檔名稱。</span><span class="sxs-lookup"><span data-stu-id="30891-110">A string that contains the name of the output file where the certificates will be saved.</span></span>

</dd> <dt>

<span data-ttu-id="30891-111">*密碼* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="30891-111">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30891-112">字串，其中包含 [*私密金鑰*](../secgloss/p-gly.md)檔案的 [*純文字*](../secgloss/p-gly.md)密碼。</span><span class="sxs-lookup"><span data-stu-id="30891-112">A string that contains the [*plaintext*](../secgloss/p-gly.md) password for a [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="30891-113">預設值為空字串 ("")。</span><span class="sxs-lookup"><span data-stu-id="30891-113">The default value is the empty string ("").</span></span> <span data-ttu-id="30891-114">密碼最多可使用32個 Unicode 字元，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="30891-114">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="30891-115">如需保護密碼的相關資訊，請參閱 [處理密碼](../secbp/handling-passwords.md)。</span><span class="sxs-lookup"><span data-stu-id="30891-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="30891-116">*SaveAs* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="30891-116">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30891-117">指定輸出檔格式之 [**CAPICOM \_ 憑證 \_ 儲存 \_ 為 \_ 類型**](capicom-certificates-save-as-type.md) 列舉的值。</span><span class="sxs-lookup"><span data-stu-id="30891-117">A value of the [**CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE**](capicom-certificates-save-as-type.md) enumeration that specifies the format of the output file.</span></span> <span data-ttu-id="30891-118">預設值為 [ \_ 將 CAPICOM 憑證 \_ 另存 \_ 為 \_ PFX]。</span><span class="sxs-lookup"><span data-stu-id="30891-118">The default is CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX.</span></span> <span data-ttu-id="30891-119">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="30891-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="30891-120">值</span><span class="sxs-lookup"><span data-stu-id="30891-120">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="30891-121">意義</span><span class="sxs-lookup"><span data-stu-id="30891-121">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PFX"></span><span id="capicom_certificates_save_as_pfx"></span><dl> <span data-ttu-id="30891-122"><dt>**\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ PFX**</dt></span><span class="sxs-lookup"><span data-stu-id="30891-122"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX**</dt></span></span> </dl>                      | <span data-ttu-id="30891-123">憑證會儲存為 PFX。</span><span class="sxs-lookup"><span data-stu-id="30891-123">The certificates are saved as a PFX.</span></span><br/>      |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PKCS7"></span><span id="capicom_certificates_save_as_pkcs7"></span><dl> <span data-ttu-id="30891-124"><dt>**\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ PKCS7**</dt></span><span class="sxs-lookup"><span data-stu-id="30891-124"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PKCS7**</dt></span></span> </dl>                | <span data-ttu-id="30891-125">憑證會儲存為 PKCS \# 7。</span><span class="sxs-lookup"><span data-stu-id="30891-125">The certificates are saved as a PKCS \#7.</span></span><br/> |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_SERIALIZED"></span><span id="capicom_certificates_save_as_serialized"></span><dl> <span data-ttu-id="30891-126"><dt>**\_將 CAPICOM 憑證 \_ 另存為已 \_ \_ 序列化**</dt></span><span class="sxs-lookup"><span data-stu-id="30891-126"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_SERIALIZED**</dt></span></span> </dl> | <span data-ttu-id="30891-127">憑證會儲存為已序列化。</span><span class="sxs-lookup"><span data-stu-id="30891-127">The certificates are saved as serialized.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="30891-128">*ExportFlag* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="30891-128">*ExportFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30891-129">此為 [**CAPICOM \_ 匯出 \_ 旗**](capicom-export-flag.md) 標列舉值，指定是否忽略任何私用金鑰匯出錯誤。</span><span class="sxs-lookup"><span data-stu-id="30891-129">A value of the [**CAPICOM\_EXPORT\_FLAG**](capicom-export-flag.md) enumeration that specifies whether any private key export errors are ignored.</span></span> <span data-ttu-id="30891-130">預設值是 [CAPICOM \_ 匯出 \_ 預設值]。</span><span class="sxs-lookup"><span data-stu-id="30891-130">The default is CAPICOM\_EXPORT\_DEFAULT.</span></span> <span data-ttu-id="30891-131">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="30891-131">The following table shows the possible values.</span></span>



| <span data-ttu-id="30891-132">值</span><span class="sxs-lookup"><span data-stu-id="30891-132">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="30891-133">意義</span><span class="sxs-lookup"><span data-stu-id="30891-133">Meaning</span></span>                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="CAPICOM_EXPORT_DEFAULT"></span><span id="capicom_export_default"></span><dl> <span data-ttu-id="30891-134"><dt>**CAPICOM \_ 匯出 \_ 預設值**</dt></span><span class="sxs-lookup"><span data-stu-id="30891-134"><dt>**CAPICOM\_EXPORT\_DEFAULT**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="30891-135">不會忽略私密金鑰匯出錯誤。</span><span class="sxs-lookup"><span data-stu-id="30891-135">Private key export errors are not ignored.</span></span><br/> |
| <span id="CAPICOM_EXPORT_IGNORE_PRIVATE_KEY_NOT_EXPORTABLE_ERROR"></span><span id="capicom_export_ignore_private_key_not_exportable_error"></span><dl> <span data-ttu-id="30891-136"><dt>**CAPICOM \_ 匯出 \_ 略 \_ 過 \_ 私密金鑰 \_ 不可 \_ 匯出的 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="30891-136"><dt>**CAPICOM\_EXPORT\_IGNORE\_PRIVATE\_KEY\_NOT\_EXPORTABLE\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="30891-137">私密金鑰匯出錯誤會被忽略。</span><span class="sxs-lookup"><span data-stu-id="30891-137">Private key export errors are ignored.</span></span><br/>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30891-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="30891-138">Return value</span></span>

<span data-ttu-id="30891-139">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="30891-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="30891-140">備註</span><span class="sxs-lookup"><span data-stu-id="30891-140">Remarks</span></span>

<span data-ttu-id="30891-141">\_ \_ \_ 從 web 應用程式編寫腳本時，此方法不允許引發 CAPICOM E。</span><span class="sxs-lookup"><span data-stu-id="30891-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

<span data-ttu-id="30891-142">您可以使用 [**Store. Load**](store-load.md)方法來取出 [**憑證**](certificate.md)物件。</span><span class="sxs-lookup"><span data-stu-id="30891-142">The [**Certificate**](certificate.md) objects can be retrieved by using the [**Store.Load**](store-load.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="30891-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="30891-143">Requirements</span></span>



| <span data-ttu-id="30891-144">需求</span><span class="sxs-lookup"><span data-stu-id="30891-144">Requirement</span></span> | <span data-ttu-id="30891-145">值</span><span class="sxs-lookup"><span data-stu-id="30891-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30891-146">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="30891-146">End of client support</span></span><br/> | <span data-ttu-id="30891-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30891-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="30891-148">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="30891-148">End of server support</span></span><br/> | <span data-ttu-id="30891-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30891-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="30891-150">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="30891-150">Redistributable</span></span><br/>       | <span data-ttu-id="30891-151">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="30891-151">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="30891-152">DLL</span><span class="sxs-lookup"><span data-stu-id="30891-152">DLL</span></span><br/>                   | <dl> <span data-ttu-id="30891-153"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30891-153"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30891-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30891-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30891-155">**憑證**</span><span class="sxs-lookup"><span data-stu-id="30891-155">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
