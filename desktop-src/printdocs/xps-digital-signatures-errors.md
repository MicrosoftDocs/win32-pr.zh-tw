---
description: 下表列出 XPS 數位簽章 API 中的方法可傳回的所有 HRESULT 值。
ms.assetid: d20707b0-55ea-438a-8ce3-972c61678928
title: 'XPS 數位簽章 API 錯誤 (Xpsdigitalsignature .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82c6f5efe7e67d27f7d94b5d1db2732139fa59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320260"
---
# <a name="xps-digital-signature-api-errors"></a><span data-ttu-id="71b99-103">XPS 數位簽章 API 錯誤</span><span class="sxs-lookup"><span data-stu-id="71b99-103">XPS Digital Signature API Errors</span></span>

<span data-ttu-id="71b99-104">下表列出 XPS 數位簽章 API 中的方法可傳回的所有 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="71b99-104">The following table lists all **HRESULT** values that can be returned by the methods in the XPS Digital Signature API.</span></span> <span data-ttu-id="71b99-105">請注意，並非每個方法都可以傳回下表所列的每個傳回值。</span><span class="sxs-lookup"><span data-stu-id="71b99-105">Note that not every method can return every return value listed in this table.</span></span>



| <span data-ttu-id="71b99-106">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="71b99-106">Return code/value</span></span>                                                                                                                                                                                                                                                                                  | <span data-ttu-id="71b99-107">Description</span><span class="sxs-lookup"><span data-stu-id="71b99-107">Description</span></span>                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="71b99-108"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="71b99-108"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                                                                                 | <span data-ttu-id="71b99-109">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="71b99-109">The method succeeded.</span></span><br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <span data-ttu-id="71b99-110"><dt>**XPS \_E \_ \_ SIGNATUREBLOCK \_ 標記**</dt> <dt>0x8052038b</dt>無效</span><span class="sxs-lookup"><span data-stu-id="71b99-110"><dt>**XPS\_E\_INVALID\_SIGNATUREBLOCK\_MARKUP**</dt> <dt>0x8052038b</dt></span></span> </dl> | <span data-ttu-id="71b99-111">讀取簽章標記時，簽章區塊的 XML 標記發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="71b99-111">Encountered an error in the XML markup of the signature block while the signature markup was being read.</span></span><br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <span data-ttu-id="71b99-112"><dt>**XPS \_E \_ 標記 \_ 相容性 \_ 元素**</dt> <dt>0x80520389</dt></span><span class="sxs-lookup"><span data-stu-id="71b99-112"><dt>**XPS\_E\_MARKUP\_COMPATIBILITY\_ELEMENTS**</dt> <dt>0x80520389</dt></span></span> </dl> | <span data-ttu-id="71b99-113">[**XPS \_ 簽署 \_ 旗標**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags)值指定了不預期的標記相容性元素，但找到標記相容性元素。</span><span class="sxs-lookup"><span data-stu-id="71b99-113">The [**XPS\_SIGN\_FLAGS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) value specified that no markup compatibility elements were expected; however, markup compatibility elements were found.</span></span><br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <span data-ttu-id="71b99-114"><dt>**XPS \_E \_ 物件卸 \_ 離**</dt> <dt>0x8052038a</dt></span><span class="sxs-lookup"><span data-stu-id="71b99-114"><dt>**XPS\_E\_OBJECT\_DETACHED**</dt> <dt>0x8052038a</dt></span></span> </dl>                                            | <span data-ttu-id="71b99-115">介面未與簽章管理員相關聯。</span><span class="sxs-lookup"><span data-stu-id="71b99-115">The interface is not associated with the signature manager.</span></span><br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <span data-ttu-id="71b99-116"><dt>**XPS \_E \_ 套件 \_ 已 \_ 開啟**</dt> <dt>0x80520387</dt></span><span class="sxs-lookup"><span data-stu-id="71b99-116"><dt>**XPS\_E\_PACKAGE\_ALREADY\_OPENED**</dt> <dt>0x80520387</dt></span></span> </dl>                      | <span data-ttu-id="71b99-117">已在 [簽章管理員] 中開啟 XPS 套件。</span><span class="sxs-lookup"><span data-stu-id="71b99-117">An XPS package has already been opened in the signature manager.</span></span> <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <span data-ttu-id="71b99-118"><dt>**XPS \_E \_ 套件 \_ 未 \_ 開啟**</dt> <dt>0x80520386</dt></span><span class="sxs-lookup"><span data-stu-id="71b99-118"><dt>**XPS\_E\_PACKAGE\_NOT\_OPENED**</dt> <dt>0x80520386</dt></span></span> </dl>                                  | <span data-ttu-id="71b99-119">尚未在 [簽章管理員] 中開啟 XPS 套件。</span><span class="sxs-lookup"><span data-stu-id="71b99-119">An XPS package has not yet been opened in the signature manager.</span></span> <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <span data-ttu-id="71b99-120"><dt>**XPS \_E \_ SIGNATUREID \_ DUP**</dt> <dt>0x80520388</dt></span><span class="sxs-lookup"><span data-stu-id="71b99-120"><dt>**XPS\_E\_SIGNATUREID\_DUP**</dt> <dt>0x80520388</dt></span></span> </dl>                                            | <span data-ttu-id="71b99-121">有兩個或多個簽章具有相同的識別碼。</span><span class="sxs-lookup"><span data-stu-id="71b99-121">Two or more signatures have the same ID.</span></span><br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <span data-ttu-id="71b99-122"><dt>**XPS \_E \_ SIGREQUESTID \_ DUP**</dt> <dt>0x80520385</dt></span><span class="sxs-lookup"><span data-stu-id="71b99-122"><dt>**XPS\_E\_SIGREQUESTID\_DUP**</dt> <dt>0x80520385</dt></span></span> </dl>                                         | <span data-ttu-id="71b99-123">簽章要求識別碼在簽章區塊內不是唯一的。</span><span class="sxs-lookup"><span data-stu-id="71b99-123">The signature request ID is not unique within the signature block.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="71b99-124">備註</span><span class="sxs-lookup"><span data-stu-id="71b99-124">Remarks</span></span>

<span data-ttu-id="71b99-125">某些 XPS 數位簽章 API 方法會呼叫 [封裝](/previous-versions/windows/desktop/opc/packaging) API。</span><span class="sxs-lookup"><span data-stu-id="71b99-125">Some XPS digital signature API methods make calls to the [Packaging](/previous-versions/windows/desktop/opc/packaging) API.</span></span> <span data-ttu-id="71b99-126">如需封裝 API 傳回值的相關資訊，請參閱 [封裝錯誤](/previous-versions/windows/desktop/opc/packaging-errors)。</span><span class="sxs-lookup"><span data-stu-id="71b99-126">For information about the Packaging API return values, see [Packaging Errors](/previous-versions/windows/desktop/opc/packaging-errors).</span></span>

## <a name="requirements"></a><span data-ttu-id="71b99-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="71b99-127">Requirements</span></span>



| <span data-ttu-id="71b99-128">需求</span><span class="sxs-lookup"><span data-stu-id="71b99-128">Requirement</span></span> | <span data-ttu-id="71b99-129">值</span><span class="sxs-lookup"><span data-stu-id="71b99-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71b99-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71b99-130">Minimum supported client</span></span><br/> | <span data-ttu-id="71b99-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71b99-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="71b99-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71b99-132">Minimum supported server</span></span><br/> | <span data-ttu-id="71b99-133">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71b99-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="71b99-134">標頭</span><span class="sxs-lookup"><span data-stu-id="71b99-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="71b99-135"><dt>Xpsdigitalsignature。h</dt></span><span class="sxs-lookup"><span data-stu-id="71b99-135"><dt>Xpsdigitalsignature.h</dt></span></span> </dl>   |
| <span data-ttu-id="71b99-136">Idl</span><span class="sxs-lookup"><span data-stu-id="71b99-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71b99-137"><dt>XpsDigitalSignature .idl</dt></span><span class="sxs-lookup"><span data-stu-id="71b99-137"><dt>XpsDigitalSignature.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71b99-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71b99-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b99-139">COM 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="71b99-139">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> <dt>

[<span data-ttu-id="71b99-140">封裝錯誤</span><span class="sxs-lookup"><span data-stu-id="71b99-140">Packaging Errors</span></span>](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[<span data-ttu-id="71b99-141">密碼編譯傳回值</span><span class="sxs-lookup"><span data-stu-id="71b99-141">Cryptography Return Values</span></span>](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

