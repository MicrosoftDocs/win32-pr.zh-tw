---
description: 安裝程式物件的 FileSignatureInfo 方法會取得檔案的路徑，並傳回代表雜湊或編碼憑證的位元組的 SAFEARRAY。
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: FileSignatureInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSignatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5dbb758118b7612aaef3f7cca744674bca1c768d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992140"
---
# <a name="installerfilesignatureinfo-method"></a><span data-ttu-id="30e11-103">FileSignatureInfo 方法</span><span class="sxs-lookup"><span data-stu-id="30e11-103">Installer.FileSignatureInfo method</span></span>

<span data-ttu-id="30e11-104">[**安裝程式**](installer-object.md)物件的 **FileSignatureInfo** 方法會取得檔案的路徑，並傳回代表雜湊或編碼憑證的位元組的 SAFEARRAY。</span><span class="sxs-lookup"><span data-stu-id="30e11-104">The **FileSignatureInfo** method of the [**Installer**](installer-object.md) object takes the path to a file and returns a SAFEARRAY of bytes that represent the hash or the encoded certificate.</span></span> <span data-ttu-id="30e11-105">然後可以使用這些值來填入 [MsiDigitalSignature](msidigitalsignature-table.md)、 [MsiPatchCertificate](msipatchcertificate-table.md)和 [MsiDigitalCertificate](msidigitalcertificate-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="30e11-105">The values can then be used to populate the [MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md), and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables.</span></span>

<span data-ttu-id="30e11-106">如需詳細資訊，請參閱 [**SAFEARRAY 資料類型**](/windows/win32/api/oaidl/ns-oaidl-safearray)。</span><span class="sxs-lookup"><span data-stu-id="30e11-106">For more information, see the [**SAFEARRAY Data Type**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>

## <a name="syntax"></a><span data-ttu-id="30e11-107">語法</span><span class="sxs-lookup"><span data-stu-id="30e11-107">Syntax</span></span>


```JScript
Installer.FileSignatureInfo(
  FilePath,
  Options,
  Format
)
```



## <a name="parameters"></a><span data-ttu-id="30e11-108">參數</span><span class="sxs-lookup"><span data-stu-id="30e11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30e11-109">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="30e11-109">*FilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="30e11-110">經過數位簽署之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="30e11-110">Full path to a file that is digitally signed.</span></span>

<span data-ttu-id="30e11-111">填入 [MsiDigitalSignature](msidigitalsignature-table.md) 和 [MsiDigitalCertificate](msidigitalcertificate-table.md) 資料表時， *FilePath* 會指向數位簽署的封包。</span><span class="sxs-lookup"><span data-stu-id="30e11-111">When populating the [MsiDigitalSignature](msidigitalsignature-table.md) and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables, *FilePath* points to a digitally signed cabinet.</span></span> <span data-ttu-id="30e11-112">填入 [MsiPatchCertificate](msipatchcertificate-table.md) 和 MsiDigitalCertificate 資料表時， *FilePath* 會指向經過數位簽署的修補程式。</span><span class="sxs-lookup"><span data-stu-id="30e11-112">When populating the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables, *FilePath* points to a digitally signed patch.</span></span>

</dd> <dt>

<span data-ttu-id="30e11-113">*選項*</span><span class="sxs-lookup"><span data-stu-id="30e11-113">*Options*</span></span> 
</dt> <dd>

<span data-ttu-id="30e11-114">特殊的錯誤案例旗標。</span><span class="sxs-lookup"><span data-stu-id="30e11-114">Special error case flags.</span></span>



| <span data-ttu-id="30e11-115">旗標</span><span class="sxs-lookup"><span data-stu-id="30e11-115">Flag</span></span>                                                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="30e11-116">意義</span><span class="sxs-lookup"><span data-stu-id="30e11-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <span data-ttu-id="30e11-117"><dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="30e11-117"><dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="30e11-118">當 *選項* 設定為 msiSignatureOptionInvalidHashFatal 時， **FileSignatureInfo** 一律會傳回無效雜湊的嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="30e11-118">With *Options* set to msiSignatureOptionInvalidHashFatal, **FileSignatureInfo** always returns a fatal error for an invalid hash.</span></span> <br/> <span data-ttu-id="30e11-119">如果 *選項* 未設定為 msiSignatureOptionInvalidHashFatal，而且 *Format* 設定為 msiSignatureInfoCertificate，則 **FileSignatureInfo** 不會針對不正確雜湊傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="30e11-119">If *Options* is not set to msiSignatureOptionInvalidHashFatal and *Format* is set to msiSignatureInfoCertificate, **FileSignatureInfo** does not return an error for an invalid hash.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="30e11-120">*格式*</span><span class="sxs-lookup"><span data-stu-id="30e11-120">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="30e11-121">要求的簽章資訊。</span><span class="sxs-lookup"><span data-stu-id="30e11-121">The requested signature information.</span></span>



| <span data-ttu-id="30e11-122">旗標</span><span class="sxs-lookup"><span data-stu-id="30e11-122">Flag</span></span>                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="30e11-123">意義</span><span class="sxs-lookup"><span data-stu-id="30e11-123">Meaning</span></span>                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <span data-ttu-id="30e11-124"><dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="30e11-124"><dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="30e11-125">傳回代表編碼憑證的位元組的 SAFEARRAY。</span><span class="sxs-lookup"><span data-stu-id="30e11-125">Returns a SAFEARRAY of bytes that represent the encoded certificate.</span></span><br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <span data-ttu-id="30e11-126"><dt>**msiSignatureInfoHash**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="30e11-126"><dt>**msiSignatureInfoHash**</dt> <dt>1</dt></span></span> </dl>                             | <span data-ttu-id="30e11-127">傳回表示雜湊的位元組的 SAFEARRAY。</span><span class="sxs-lookup"><span data-stu-id="30e11-127">Returns a SAFEARRAY of bytes that represent the hash.</span></span><br/>                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30e11-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="30e11-128">Return value</span></span>

<span data-ttu-id="30e11-129">如果成功，方法會傳回包含雜湊或編碼憑證的位元組的 [SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) 。</span><span class="sxs-lookup"><span data-stu-id="30e11-129">If successful, the method returns a [SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) of bytes that contain either the hash or encoded certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="30e11-130">備註</span><span class="sxs-lookup"><span data-stu-id="30e11-130">Remarks</span></span>

<span data-ttu-id="30e11-131">若要使用 automation 來撰寫經過完整驗證的已簽署安裝，請使用 **FileSignatureInfo** 方法來填入 [MsiDigitalCertificate](msidigitalcertificate-table.md)、 [MsiPatchCertificate](msipatchcertificate-table.md)和 [MsiDigitalSignature](msidigitalsignature-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="30e11-131">To author a fully verified signed installation by using automation, use the **FileSignatureInfo** method to populate the [MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md), and [MsiDigitalSignature](msidigitalsignature-table.md) tables.</span></span> <span data-ttu-id="30e11-132">如需詳細資訊，請參閱 [使用自動化撰寫經過完整驗證的已簽署安裝](authoring-a-fully-verified-signed-installation-using-automation.md)。</span><span class="sxs-lookup"><span data-stu-id="30e11-132">For more information, see [Authoring a Fully Verified Signed Installation Using Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30e11-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="30e11-133">Requirements</span></span>



| <span data-ttu-id="30e11-134">需求</span><span class="sxs-lookup"><span data-stu-id="30e11-134">Requirement</span></span> | <span data-ttu-id="30e11-135">值</span><span class="sxs-lookup"><span data-stu-id="30e11-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30e11-136">版本</span><span class="sxs-lookup"><span data-stu-id="30e11-136">Version</span></span><br/> | <span data-ttu-id="30e11-137">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="30e11-137">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="30e11-138">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="30e11-138">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="30e11-139">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="30e11-139">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="30e11-140">DLL</span><span class="sxs-lookup"><span data-stu-id="30e11-140">DLL</span></span><br/>     | <dl> <span data-ttu-id="30e11-141"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30e11-141"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="30e11-142">IID</span><span class="sxs-lookup"><span data-stu-id="30e11-142">IID</span></span><br/>     | <span data-ttu-id="30e11-143">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="30e11-143">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="30e11-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30e11-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30e11-145">使用自動化撰寫經過完整驗證的已簽署安裝</span><span class="sxs-lookup"><span data-stu-id="30e11-145">Authoring a Fully Verified Signed Installation Using Automation</span></span>](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[<span data-ttu-id="30e11-146">數位簽章和 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="30e11-146">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> <dt>

[<span data-ttu-id="30e11-147">**MsiGetFileSignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="30e11-147">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
