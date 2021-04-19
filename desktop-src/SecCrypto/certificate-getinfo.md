---
description: 從憑證抓取資訊。
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: ICertificate2：： GetInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.GetInfo
- ICertificate2.GetInfo
- ICertificate.GetInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41b3cb6cde796f64ee3a5953ed848d105a10bc5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985749"
---
# <a name="icertificate2getinfo-method"></a><span data-ttu-id="7dad1-103">ICertificate2：： GetInfo 方法</span><span class="sxs-lookup"><span data-stu-id="7dad1-103">ICertificate2::GetInfo method</span></span>

<span data-ttu-id="7dad1-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="7dad1-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7dad1-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="7dad1-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7dad1-106">**GetInfo** 方法會從 [*憑證*](../secgloss/c-gly.md)中抓取資訊。</span><span class="sxs-lookup"><span data-stu-id="7dad1-106">The **GetInfo** method retrieves information from the [*certificate*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7dad1-107">語法</span><span class="sxs-lookup"><span data-stu-id="7dad1-107">Syntax</span></span>


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a><span data-ttu-id="7dad1-108">參數</span><span class="sxs-lookup"><span data-stu-id="7dad1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dad1-109">*InfoType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7dad1-109">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dad1-110">[**CAPICOM 憑證 \_ \_ 資訊 \_ 類型**](capicom-cert-info-type.md)列舉值，指定要從憑證中取出的資料類型。</span><span class="sxs-lookup"><span data-stu-id="7dad1-110">A value of the [**CAPICOM\_CERT\_INFO\_TYPE**](capicom-cert-info-type.md) enumeration that specifies what type of data is retrieved from the certificate.</span></span> <span data-ttu-id="7dad1-111">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="7dad1-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="7dad1-112">值</span><span class="sxs-lookup"><span data-stu-id="7dad1-112">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="7dad1-113">意義</span><span class="sxs-lookup"><span data-stu-id="7dad1-113">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <span data-ttu-id="7dad1-114"><dt>**CAPICOM \_ CERT \_ 資訊 \_ 主體 \_ 簡單 \_ 名稱**</dt></span><span class="sxs-lookup"><span data-stu-id="7dad1-114"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_SIMPLE\_NAME**</dt></span></span> </dl> | <span data-ttu-id="7dad1-115">傳回憑證主體的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="7dad1-115">Returns the display name from the certificate subject.</span></span><br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <span data-ttu-id="7dad1-116"><dt>**CAPICOM \_ CERT \_ 資訊 \_ 簽發者 \_ 簡單 \_ 名稱**</dt></span><span class="sxs-lookup"><span data-stu-id="7dad1-116"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_SIMPLE\_NAME**</dt></span></span> </dl>    | <span data-ttu-id="7dad1-117">傳回憑證簽發者的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="7dad1-117">Returns the display name of the issuer of the certificate.</span></span><br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <span data-ttu-id="7dad1-118"><dt>**CAPICOM \_ 憑證 \_ 資訊 \_ 主體 \_ 電子郵件 \_ 名稱**</dt></span><span class="sxs-lookup"><span data-stu-id="7dad1-118"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_EMAIL\_NAME**</dt></span></span> </dl>    | <span data-ttu-id="7dad1-119">傳回憑證主體的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="7dad1-119">Returns the email address of the certificate subject.</span></span><br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <span data-ttu-id="7dad1-120"><dt>**CAPICOM \_ 憑證 \_ 資訊 \_ 簽發者 \_ 電子郵件 \_ 名稱**</dt></span><span class="sxs-lookup"><span data-stu-id="7dad1-120"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_EMAIL\_NAME**</dt></span></span> </dl>       | <span data-ttu-id="7dad1-121">傳回憑證簽發者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="7dad1-121">Returns the email address of the issuer of the certificate.</span></span><br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <span data-ttu-id="7dad1-122"><dt>**CAPICOM \_ CERT \_ 資訊 \_ 主體 \_ UPN**</dt></span><span class="sxs-lookup"><span data-stu-id="7dad1-122"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_UPN**</dt></span></span> </dl>                          | <span data-ttu-id="7dad1-123">傳回憑證主體的 UPN。</span><span class="sxs-lookup"><span data-stu-id="7dad1-123">Returns the UPN of the certificate subject.</span></span> <span data-ttu-id="7dad1-124">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="7dad1-124">Introduced in CAPICOM 2.0.</span></span><br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <span data-ttu-id="7dad1-125"><dt>**CAPICOM \_ CERT \_ 資訊 \_ 簽發者 \_ UPN**</dt></span><span class="sxs-lookup"><span data-stu-id="7dad1-125"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_UPN**</dt></span></span> </dl>                             | <span data-ttu-id="7dad1-126">傳回憑證簽發者的 UPN。</span><span class="sxs-lookup"><span data-stu-id="7dad1-126">Returns the UPN of the issuer of the certificate.</span></span> <span data-ttu-id="7dad1-127">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="7dad1-127">Introduced in CAPICOM 2.0.</span></span><br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <span data-ttu-id="7dad1-128"><dt>**CAPICOM \_ CERT \_ 資訊 \_ 主體 \_ DNS \_ 名稱**</dt></span><span class="sxs-lookup"><span data-stu-id="7dad1-128"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_DNS\_NAME**</dt></span></span> </dl>          | <span data-ttu-id="7dad1-129">傳回憑證主體的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="7dad1-129">Returns the DNS name of the certificate subject.</span></span> <span data-ttu-id="7dad1-130">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="7dad1-130">Introduced in CAPICOM 2.0.</span></span><br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <span data-ttu-id="7dad1-131"><dt>**CAPICOM \_ 憑證 \_ 資訊 \_ 簽發者 \_ DNS \_ 名稱**</dt></span><span class="sxs-lookup"><span data-stu-id="7dad1-131"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_DNS\_NAME**</dt></span></span> </dl>             | <span data-ttu-id="7dad1-132">傳回憑證簽發者的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="7dad1-132">Returns the DNS name of the issuer of the certificate.</span></span> <span data-ttu-id="7dad1-133">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="7dad1-133">Introduced in CAPICOM 2.0.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dad1-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="7dad1-134">Return value</span></span>

<span data-ttu-id="7dad1-135">包含要求之資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="7dad1-135">A string that contains the requested information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dad1-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="7dad1-136">Requirements</span></span>



| <span data-ttu-id="7dad1-137">需求</span><span class="sxs-lookup"><span data-stu-id="7dad1-137">Requirement</span></span> | <span data-ttu-id="7dad1-138">值</span><span class="sxs-lookup"><span data-stu-id="7dad1-138">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7dad1-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7dad1-139">End of client support</span></span><br/> | <span data-ttu-id="7dad1-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7dad1-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7dad1-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="7dad1-141">End of server support</span></span><br/> | <span data-ttu-id="7dad1-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7dad1-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7dad1-143">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7dad1-143">Redistributable</span></span><br/>       | <span data-ttu-id="7dad1-144">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7dad1-144">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7dad1-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7dad1-145">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7dad1-146"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dad1-146"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dad1-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7dad1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dad1-148">加密物件</span><span class="sxs-lookup"><span data-stu-id="7dad1-148">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="7dad1-149">**憑證**</span><span class="sxs-lookup"><span data-stu-id="7dad1-149">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
