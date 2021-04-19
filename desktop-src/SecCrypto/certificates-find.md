---
description: 傳回憑證物件，其中包含符合指定之搜尋準則的所有憑證。
ms.assetid: a2b8f4d4-dce3-467b-aaa0-a125056a1dd3
title: ICertificates2：： Find 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Find
- ICertificates2.Find
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9ea15891c33a0789e5b6746b55dfd0b0eb602afc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995490"
---
# <a name="icertificates2find-method"></a><span data-ttu-id="a391c-103">ICertificates2：： Find 方法</span><span class="sxs-lookup"><span data-stu-id="a391c-103">ICertificates2::Find method</span></span>

<span data-ttu-id="a391c-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="a391c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a391c-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="a391c-105">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a391c-106">**Find** 方法會傳回包含所有符合指定搜尋準則之憑證的 [**憑證**](certificates.md)物件。</span><span class="sxs-lookup"><span data-stu-id="a391c-106">The **Find** method returns a [**Certificates**](certificates.md) object that contains all certificates that match the specified search criteria.</span></span> <span data-ttu-id="a391c-107">此方法是在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="a391c-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="a391c-108">語法</span><span class="sxs-lookup"><span data-stu-id="a391c-108">Syntax</span></span>


```VB
Certificates.Find( _
  ByVal FindType, _
  [ ByVal varCriteria ], _
  [ ByVal bFindValidOnly ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a391c-109">參數</span><span class="sxs-lookup"><span data-stu-id="a391c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a391c-110">*FindType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a391c-110">*FindType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a391c-111">[**CAPICOM \_ 憑證 \_ 尋找 \_ 類型**](capicom-certificate-find-type.md)列舉值，指定 *varCriteria* 參數中提供的相符準則類型。</span><span class="sxs-lookup"><span data-stu-id="a391c-111">A value of the [**CAPICOM\_CERTIFICATE\_FIND\_TYPE**](capicom-certificate-find-type.md) enumeration that specifies the type of matching criteria supplied in the *varCriteria* parameter.</span></span> <span data-ttu-id="a391c-112">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="a391c-112">The following table shows the possible values.</span></span>



| <span data-ttu-id="a391c-113">值</span><span class="sxs-lookup"><span data-stu-id="a391c-113">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="a391c-114">意義</span><span class="sxs-lookup"><span data-stu-id="a391c-114">Meaning</span></span>                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_FIND_SHA1_HASH"></span><span id="capicom_certificate_find_sha1_hash"></span><dl> <span data-ttu-id="a391c-115"><dt>**CAPICOM \_ 憑證 \_ 尋找 \_ SHA1 \_ 雜湊**</dt></span><span class="sxs-lookup"><span data-stu-id="a391c-115"><dt>**CAPICOM\_CERTIFICATE\_FIND\_SHA1\_HASH**</dt></span></span> </dl>                              | <span data-ttu-id="a391c-116">傳回具有 SHA1 雜湊的憑證，此雜湊符合在 *varCriteria* 參數中指定的 sha1 雜湊。</span><span class="sxs-lookup"><span data-stu-id="a391c-116">Returns certificates with a SHA1 hash that matches the SHA1 hash specified in the *varCriteria* parameter.</span></span><br/>                                                                                                                              |
| <span id="CAPICOM_CERTIFICATE_FIND_SUBJECT_NAME"></span><span id="capicom_certificate_find_subject_name"></span><dl> <span data-ttu-id="a391c-117"><dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 主體 \_ 名稱**</dt></span><span class="sxs-lookup"><span data-stu-id="a391c-117"><dt>**CAPICOM\_CERTIFICATE\_FIND\_SUBJECT\_NAME**</dt></span></span> </dl>                     | <span data-ttu-id="a391c-118">傳回主體名稱完全或部分符合 *varCriteria* 參數中指定之主體名稱的憑證。</span><span class="sxs-lookup"><span data-stu-id="a391c-118">Returns certificates whose subject name exactly or partially matches the subject name specified in the *varCriteria* parameter.</span></span> <span data-ttu-id="a391c-119">此呼叫只會搜尋 [主體名稱] 欄位。</span><span class="sxs-lookup"><span data-stu-id="a391c-119">This call searches the subject name field only.</span></span><br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_FIND_ISSUER_NAME"></span><span id="capicom_certificate_find_issuer_name"></span><dl> <span data-ttu-id="a391c-120"><dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 簽發者 \_ 名稱**</dt></span><span class="sxs-lookup"><span data-stu-id="a391c-120"><dt>**CAPICOM\_CERTIFICATE\_FIND\_ISSUER\_NAME**</dt></span></span> </dl>                        | <span data-ttu-id="a391c-121">傳回其簽發者名稱完全或部分符合 *varCriteria* 參數中所指定之簽發者名稱的憑證。</span><span class="sxs-lookup"><span data-stu-id="a391c-121">Returns certificates whose issuer name exactly or partially matches the issuer name specified in the *varCriteria* parameter.</span></span> <span data-ttu-id="a391c-122">此呼叫只會搜尋 [簽發者名稱] 欄位。</span><span class="sxs-lookup"><span data-stu-id="a391c-122">This call searches the issuer name field only.</span></span><br/>                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_ROOT_NAME"></span><span id="capicom_certificate_find_root_name"></span><dl> <span data-ttu-id="a391c-123"><dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 根 \_ 名稱**</dt></span><span class="sxs-lookup"><span data-stu-id="a391c-123"><dt>**CAPICOM\_CERTIFICATE\_FIND\_ROOT\_NAME**</dt></span></span> </dl>                              | <span data-ttu-id="a391c-124">傳回其根主體名稱完全或部分符合 *varCriteria* 參數中所指定之根主體名稱的憑證。</span><span class="sxs-lookup"><span data-stu-id="a391c-124">Returns certificates whose root subject name exactly or partially matches the root subject name specified in the *varCriteria* parameter.</span></span> <span data-ttu-id="a391c-125">此呼叫會建立鏈。</span><span class="sxs-lookup"><span data-stu-id="a391c-125">This call creates a chain.</span></span> <span data-ttu-id="a391c-126">此呼叫會搜尋根憑證的 [主體名稱] 欄位。</span><span class="sxs-lookup"><span data-stu-id="a391c-126">This call searches the subject name field of the root certificate.</span></span><br/> |
| <span id="CAPICOM_CERTIFICATE_FIND_TEMPLATE_NAME"></span><span id="capicom_certificate_find_template_name"></span><dl> <span data-ttu-id="a391c-127"><dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 範本 \_ 名稱**</dt></span><span class="sxs-lookup"><span data-stu-id="a391c-127"><dt>**CAPICOM\_CERTIFICATE\_FIND\_TEMPLATE\_NAME**</dt></span></span> </dl>                  | <span data-ttu-id="a391c-128">傳回範本名稱符合 *varCriteria* 參數中所指定範本名稱的憑證。</span><span class="sxs-lookup"><span data-stu-id="a391c-128">Returns certificates whose template name matches the template name specified in the *varCriteria* parameter.</span></span><br/>                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENSION"></span><span id="capicom_certificate_find_extension"></span><dl> <span data-ttu-id="a391c-129"><dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 延伸模組**</dt></span><span class="sxs-lookup"><span data-stu-id="a391c-129"><dt>**CAPICOM\_CERTIFICATE\_FIND\_EXTENSION**</dt></span></span> </dl>                               | <span data-ttu-id="a391c-130">傳回副檔名符合 *varCriteria* 參數中指定之副檔名的憑證。</span><span class="sxs-lookup"><span data-stu-id="a391c-130">Returns certificates that have an extension that matches the extension specified in the *varCriteria* parameter.</span></span><br/>                                                                                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENDED_PROPERTY"></span><span id="capicom_certificate_find_extended_property"></span><dl> <span data-ttu-id="a391c-131"><dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 擴充 \_ 屬性**</dt></span><span class="sxs-lookup"><span data-stu-id="a391c-131"><dt>**CAPICOM\_CERTIFICATE\_FIND\_EXTENDED\_PROPERTY**</dt></span></span> </dl>      | <span data-ttu-id="a391c-132">傳回存放區中的憑證，該憑證明確包含具有 *varCriteria* 參數中所指定之值的擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="a391c-132">Returns certificates in the store that explicitly contain an extended property with the value specified in the *varCriteria* parameter.</span></span><br/>                                                                                                 |
| <span id="CAPICOM_CERTIFICATE_FIND_APPLICATION_POLICY"></span><span id="capicom_certificate_find_application_policy"></span><dl> <span data-ttu-id="a391c-133"><dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 應用程式 \_ 原則**</dt></span><span class="sxs-lookup"><span data-stu-id="a391c-133"><dt>**CAPICOM\_CERTIFICATE\_FIND\_APPLICATION\_POLICY**</dt></span></span> </dl>   | <span data-ttu-id="a391c-134">傳回存放區中的憑證，其中具有在 *varCriteria* 參數中指定的增強金鑰使用方法擴充功能、應用程式原則延伸模組或擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="a391c-134">Returns certificates in the store that have either an enhanced key usage extension, application policy extension, or extended property specified in the *varCriteria* parameter.</span></span><br/>                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_CERTIFICATE_POLICY"></span><span id="capicom_certificate_find_certificate_policy"></span><dl> <span data-ttu-id="a391c-135"><dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 憑證 \_ 原則**</dt></span><span class="sxs-lookup"><span data-stu-id="a391c-135"><dt>**CAPICOM\_CERTIFICATE\_FIND\_CERTIFICATE\_POLICY**</dt></span></span> </dl>   | <span data-ttu-id="a391c-136">傳回憑證，其中包含在 *varCriteria* 參數中指定的憑證原則延伸中的原則 OID。</span><span class="sxs-lookup"><span data-stu-id="a391c-136">Returns certificates that contain the policy OID in the Certificate Policy extension specified in the *varCriteria* parameter.</span></span><br/>                                                                                                          |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_VALID"></span><span id="capicom_certificate_find_time_valid"></span><dl> <span data-ttu-id="a391c-137"><dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 時間 \_ 有效**</dt></span><span class="sxs-lookup"><span data-stu-id="a391c-137"><dt>**CAPICOM\_CERTIFICATE\_FIND\_TIME\_VALID**</dt></span></span> </dl>                           | <span data-ttu-id="a391c-138">傳回時間有效的憑證。</span><span class="sxs-lookup"><span data-stu-id="a391c-138">Returns certificates whose time is valid.</span></span><br/>                                                                                                                                                                                               |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_NOT_YET_VALID"></span><span id="capicom_certificate_find_time_not_yet_valid"></span><dl> <span data-ttu-id="a391c-139"><dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 時間 \_ 尚未 \_ \_ 生效**</dt></span><span class="sxs-lookup"><span data-stu-id="a391c-139"><dt>**CAPICOM\_CERTIFICATE\_FIND\_TIME\_NOT\_YET\_VALID**</dt></span></span> </dl> | <span data-ttu-id="a391c-140">傳回時間尚未生效的憑證。</span><span class="sxs-lookup"><span data-stu-id="a391c-140">Returns certificates whose time is not yet valid.</span></span><br/>                                                                                                                                                                                       |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_EXPIRED"></span><span id="capicom_certificate_find_time_expired"></span><dl> <span data-ttu-id="a391c-141"><dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 時間已 \_ 過期**</dt></span><span class="sxs-lookup"><span data-stu-id="a391c-141"><dt>**CAPICOM\_CERTIFICATE\_FIND\_TIME\_EXPIRED**</dt></span></span> </dl>                     | <span data-ttu-id="a391c-142">傳回時間已過期的憑證。</span><span class="sxs-lookup"><span data-stu-id="a391c-142">Returns certificates whose time has expired.</span></span><br/>                                                                                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_KEY_USAGE"></span><span id="capicom_certificate_find_key_usage"></span><dl> <span data-ttu-id="a391c-143"><dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 金鑰 \_ 使用方式**</dt></span><span class="sxs-lookup"><span data-stu-id="a391c-143"><dt>**CAPICOM\_CERTIFICATE\_FIND\_KEY\_USAGE**</dt></span></span> </dl>                              | <span data-ttu-id="a391c-144">傳回憑證，其中包含在 *varCriteria* 參數中指定的 KeyUsage 延伸模組中的金鑰使用方式。</span><span class="sxs-lookup"><span data-stu-id="a391c-144">Returns certificates containing key usages in the KeyUsage extension specified in the *varCriteria* parameter.</span></span> <span data-ttu-id="a391c-145">如果 KeyUsage 延伸模組不存在，就會假設所有的金鑰使用方式都無法使用。</span><span class="sxs-lookup"><span data-stu-id="a391c-145">If the KeyUsage extension is not present, all of the key usages are assumed to be unavailable.</span></span><br/>                           |



 

</dd> <dt>

<span data-ttu-id="a391c-146">*varCriteria* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a391c-146">*varCriteria* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a391c-147">包含搜尋準則的 variant。</span><span class="sxs-lookup"><span data-stu-id="a391c-147">A variant that contains the search criteria.</span></span> <span data-ttu-id="a391c-148">這項資料必須符合 *FindType* 參數中指定的資料類型。</span><span class="sxs-lookup"><span data-stu-id="a391c-148">This data must match the type of data specified in the *FindType* parameter.</span></span> <span data-ttu-id="a391c-149">如果 *FindType* 參數的值為 capicom \_ 憑證 \_ 尋找 \_ 時間 \_ 有效、capicom \_ 憑證尋找時間 \_ \_ \_ 尚未 \_ \_ 生效，或 capicom \_ 憑證 \_ 找 \_ \_ 出時間已過期，且您未將值傳遞給此參數，則會假設為目前時間。</span><span class="sxs-lookup"><span data-stu-id="a391c-149">If the value of the *FindType* parameter is CAPICOM\_CERTIFICATE\_FIND\_TIME\_VALID, CAPICOM\_CERTIFICATE\_FIND\_TIME\_NOT\_YET\_VALID, or CAPICOM\_CERTIFICATE\_FIND\_TIME\_EXPIRED and you do not pass a value into this parameter, the current time is assumed.</span></span> <span data-ttu-id="a391c-150">如需每種資料類型的範例，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="a391c-150">For examples of each data type, see Remarks.</span></span> <span data-ttu-id="a391c-151">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="a391c-151">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a391c-152">*bFindValidOnly* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a391c-152">*bFindValidOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a391c-153">布林值，指出是否只傳回有效的憑證。</span><span class="sxs-lookup"><span data-stu-id="a391c-153">A Boolean value that indicates whether only valid certificates are returned.</span></span> <span data-ttu-id="a391c-154">預設值為 false;這表示會傳回所有符合搜尋準則的憑證。</span><span class="sxs-lookup"><span data-stu-id="a391c-154">The default value is false; this indicates that all certificates that match the search criteria are returned.</span></span>

<span data-ttu-id="a391c-155">若為 true，則搜尋不會傳回下列類型的憑證：</span><span class="sxs-lookup"><span data-stu-id="a391c-155">If true, the search will not return the following types of certificates:</span></span>

-   <span data-ttu-id="a391c-156">其時間已過期或尚未生效的憑證。</span><span class="sxs-lookup"><span data-stu-id="a391c-156">Certificates whose time has expired or is not yet valid.</span></span>
-   <span data-ttu-id="a391c-157">憑證未正確連結。</span><span class="sxs-lookup"><span data-stu-id="a391c-157">Certificates not chained properly.</span></span>
-   <span data-ttu-id="a391c-158">有簽章問題的憑證。</span><span class="sxs-lookup"><span data-stu-id="a391c-158">Certificates that have signature problems.</span></span>
-   <span data-ttu-id="a391c-159">已撤銷的憑證。</span><span class="sxs-lookup"><span data-stu-id="a391c-159">Certificates that are revoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a391c-160">傳回值</span><span class="sxs-lookup"><span data-stu-id="a391c-160">Return value</span></span>

<span data-ttu-id="a391c-161">包含搜尋結果的 [**憑證**](certificates.md)物件。</span><span class="sxs-lookup"><span data-stu-id="a391c-161">[**Certificates**](certificates.md) object that contains the results of the search.</span></span>

<span data-ttu-id="a391c-162">**CAPICOM 2.1：** 傳回的 [**憑證**](certificates.md) 物件包含對集合中執行搜尋的憑證的參考。</span><span class="sxs-lookup"><span data-stu-id="a391c-162">**CAPICOM 2.1:** The [**Certificates**](certificates.md) object that is returned contains references to the certificates in the collection in which the search was done.</span></span> <span data-ttu-id="a391c-163">對傳回的 **憑證** 物件中的憑證所做的任何變更，都會反映在該集合中。</span><span class="sxs-lookup"><span data-stu-id="a391c-163">Any changes made to the certificates in the returned **Certificates** object are reflected in that collection.</span></span>

<span data-ttu-id="a391c-164">**Capicom 2.0、capicom 2.0.0.1、capicom 2.0.0.2 和 capicom 2.0.0.3：** 傳回的 [**憑證**](certificates.md) 物件包含完成搜尋的集合中憑證的複本。</span><span class="sxs-lookup"><span data-stu-id="a391c-164">**CAPICOM 2.0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2, and CAPICOM 2.0.0.3:** The [**Certificates**](certificates.md) object that is returned contains copies of the certificates in the collection in which the search was done.</span></span> <span data-ttu-id="a391c-165">對傳回的 **憑證** 物件中的憑證所做的任何變更都不會反映在該集合中。</span><span class="sxs-lookup"><span data-stu-id="a391c-165">Any changes made to the certificates in the returned **Certificates** object are not reflected in that collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="a391c-166">備註</span><span class="sxs-lookup"><span data-stu-id="a391c-166">Remarks</span></span>

<span data-ttu-id="a391c-167">下列範例會顯示不同搜尋條件類型的可能搜尋準則。</span><span class="sxs-lookup"><span data-stu-id="a391c-167">The following examples show possible search criteria for the different search criteria types.</span></span>



| <span data-ttu-id="a391c-168">*FindType* 參數</span><span class="sxs-lookup"><span data-stu-id="a391c-168">*FindType* parameter</span></span>                              | <span data-ttu-id="a391c-169">*varCriteria* 參數</span><span class="sxs-lookup"><span data-stu-id="a391c-169">*varCriteria* parameter</span></span>                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a391c-170">CAPICOM \_ 憑證 \_ 尋找 \_ SHA1 \_ 雜湊</span><span class="sxs-lookup"><span data-stu-id="a391c-170">CAPICOM\_CERTIFICATE\_FIND\_SHA1\_HASH</span></span>            | <span data-ttu-id="a391c-171">33F362434B577F844BB7226BE36F7D72EF9D9393</span><span class="sxs-lookup"><span data-stu-id="a391c-171">33F362434B577F844BB7226BE36F7D72EF9D9393</span></span>                                                                                           |
| <span data-ttu-id="a391c-172">CAPICOM \_ 憑證 \_ 尋找 \_ 主體 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="a391c-172">CAPICOM\_CERTIFICATE\_FIND\_SUBJECT\_NAME</span></span>         | <span data-ttu-id="a391c-173">"NameOfPerson"</span><span class="sxs-lookup"><span data-stu-id="a391c-173">"NameOfPerson"</span></span>                                                                                                                     |
| <span data-ttu-id="a391c-174">CAPICOM \_ 憑證 \_ 尋找 \_ 簽發者 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="a391c-174">CAPICOM\_CERTIFICATE\_FIND\_ISSUER\_NAME</span></span>          | <span data-ttu-id="a391c-175">頒發</span><span class="sxs-lookup"><span data-stu-id="a391c-175">"VeriSign"</span></span>                                                                                                                         |
| <span data-ttu-id="a391c-176">CAPICOM \_ 憑證 \_ 尋找 \_ 根 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="a391c-176">CAPICOM\_CERTIFICATE\_FIND\_ROOT\_NAME</span></span>            | <span data-ttu-id="a391c-177">「Microsoft 根授權單位」</span><span class="sxs-lookup"><span data-stu-id="a391c-177">"Microsoft Root Authority"</span></span>                                                                                                         |
| <span data-ttu-id="a391c-178">CAPICOM \_ 憑證 \_ 尋找 \_ 範本 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="a391c-178">CAPICOM\_CERTIFICATE\_FIND\_TEMPLATE\_NAME</span></span>        | <span data-ttu-id="a391c-179">"AutoEnrollEFS"</span><span class="sxs-lookup"><span data-stu-id="a391c-179">"AutoEnrollEFS"</span></span><br/> <span data-ttu-id="a391c-180">1.3.6.1.4.1.311.21.8.3692315854.1256661383.1690418588.4201632533.1741915387.2177932052</span><span class="sxs-lookup"><span data-stu-id="a391c-180">1.3.6.1.4.1.311.21.8.3692315854.1256661383.1690418588.4201632533.1741915387.2177932052</span></span><br/>       |
| <span data-ttu-id="a391c-181">CAPICOM \_ 憑證 \_ 尋找 \_ 延伸模組</span><span class="sxs-lookup"><span data-stu-id="a391c-181">CAPICOM\_CERTIFICATE\_FIND\_EXTENSION</span></span>             | <span data-ttu-id="a391c-182">"2.5.29.31"</span><span class="sxs-lookup"><span data-stu-id="a391c-182">"2.5.29.31"</span></span><br/> <span data-ttu-id="a391c-183">CAPICOM \_ OID \_ 金鑰 \_ 使用方法 \_ 擴充功能</span><span class="sxs-lookup"><span data-stu-id="a391c-183">CAPICOM\_OID\_KEY\_USAGE\_EXTENSION</span></span><br/> <span data-ttu-id="a391c-184">「CRL 通訊群組清單」</span><span class="sxs-lookup"><span data-stu-id="a391c-184">"CRL Distribution List"</span></span><br/>                           |
| <span data-ttu-id="a391c-185">CAPICOM \_ 憑證 \_ 尋找 \_ 擴充 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="a391c-185">CAPICOM\_CERTIFICATE\_FIND\_EXTENDED\_PROPERTY</span></span>    | <span data-ttu-id="a391c-186">CAPICOM \_ PROPID \_ 金鑰 \_ >PROV \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="a391c-186">CAPICOM\_PROPID\_KEY\_PROV\_INFO</span></span>                                                                                                   |
| <span data-ttu-id="a391c-187">CAPICOM \_ 憑證 \_ 尋找 \_ 應用程式 \_ 原則</span><span class="sxs-lookup"><span data-stu-id="a391c-187">CAPICOM\_CERTIFICATE\_FIND\_APPLICATION\_POLICY</span></span>   | <span data-ttu-id="a391c-188">1.3.6.1.5.5.7.3.3</span><span class="sxs-lookup"><span data-stu-id="a391c-188">"1.3.6.1.5.5.7.3.3"</span></span><br/> <span data-ttu-id="a391c-189">"1.3.6.1.5.5.7.3.4"</span><span class="sxs-lookup"><span data-stu-id="a391c-189">"1.3.6.1.5.5.7.3.4"</span></span><br/> <span data-ttu-id="a391c-190">CAPICOM \_ OID \_ 伺服器 \_ 驗證 \_ EKU</span><span class="sxs-lookup"><span data-stu-id="a391c-190">CAPICOM\_OID\_SERVER\_AUTH\_EKU</span></span><br/> <span data-ttu-id="a391c-191">「程式碼簽署」</span><span class="sxs-lookup"><span data-stu-id="a391c-191">"Code Signing"</span></span><br/> |
| <span data-ttu-id="a391c-192">CAPICOM \_ 憑證 \_ 尋找 \_ 憑證 \_ 原則</span><span class="sxs-lookup"><span data-stu-id="a391c-192">CAPICOM\_CERTIFICATE\_FIND\_CERTIFICATE\_POLICY</span></span>   | <span data-ttu-id="a391c-193">"1.3.6.1.5.5.7.3.4.3.5"</span><span class="sxs-lookup"><span data-stu-id="a391c-193">"1.3.6.1.5.5.7.3.4.3.5"</span></span><br/> <span data-ttu-id="a391c-194">「公司高保證」</span><span class="sxs-lookup"><span data-stu-id="a391c-194">"Corporate High Assurance"</span></span><br/>                                                           |
| <span data-ttu-id="a391c-195">CAPICOM \_ 憑證 \_ 尋找 \_ 時間 \_ 有效</span><span class="sxs-lookup"><span data-stu-id="a391c-195">CAPICOM\_CERTIFICATE\_FIND\_TIME\_VALID</span></span>           | <span data-ttu-id="a391c-196">\#04/15/2002、6:00 PM\#</span><span class="sxs-lookup"><span data-stu-id="a391c-196">\#04/15/2002, 6:00 PM\#</span></span>                                                                                                            |
| <span data-ttu-id="a391c-197">CAPICOM \_ 憑證 \_ 尋找 \_ 時間 \_ 尚未 \_ \_ 生效</span><span class="sxs-lookup"><span data-stu-id="a391c-197">CAPICOM\_CERTIFICATE\_FIND\_TIME\_NOT\_YET\_VALID</span></span> | <span data-ttu-id="a391c-198">\#04/15/2002、6:00 PM\#</span><span class="sxs-lookup"><span data-stu-id="a391c-198">\#04/15/2002, 6:00 PM\#</span></span>                                                                                                            |
| <span data-ttu-id="a391c-199">CAPICOM \_ 憑證 \_ 尋找 \_ 時間已 \_ 過期</span><span class="sxs-lookup"><span data-stu-id="a391c-199">CAPICOM\_CERTIFICATE\_FIND\_TIME\_EXPIRED</span></span>         | <span data-ttu-id="a391c-200">\#04/15/2002、6:00 PM\#</span><span class="sxs-lookup"><span data-stu-id="a391c-200">\#04/15/2002, 6:00 PM\#</span></span>                                                                                                            |
| <span data-ttu-id="a391c-201">CAPICOM \_ 憑證 \_ 尋找 \_ 金鑰 \_ 使用方式</span><span class="sxs-lookup"><span data-stu-id="a391c-201">CAPICOM\_CERTIFICATE\_FIND\_KEY\_USAGE</span></span>            | <span data-ttu-id="a391c-202">CAPICOM \_ \_ 只加密 \_ 金鑰 \_ 使用方式</span><span class="sxs-lookup"><span data-stu-id="a391c-202">CAPICOM\_ENCIPHER\_ONLY\_KEY\_USAGE</span></span>                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="a391c-203">規格需求</span><span class="sxs-lookup"><span data-stu-id="a391c-203">Requirements</span></span>



| <span data-ttu-id="a391c-204">需求</span><span class="sxs-lookup"><span data-stu-id="a391c-204">Requirement</span></span> | <span data-ttu-id="a391c-205">值</span><span class="sxs-lookup"><span data-stu-id="a391c-205">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a391c-206">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a391c-206">End of client support</span></span><br/> | <span data-ttu-id="a391c-207">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a391c-207">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a391c-208">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="a391c-208">End of server support</span></span><br/> | <span data-ttu-id="a391c-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a391c-209">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a391c-210">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a391c-210">Redistributable</span></span><br/>       | <span data-ttu-id="a391c-211">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a391c-211">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a391c-212">DLL</span><span class="sxs-lookup"><span data-stu-id="a391c-212">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a391c-213"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a391c-213"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a391c-214">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a391c-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a391c-215">**憑證**</span><span class="sxs-lookup"><span data-stu-id="a391c-215">**Certificates**</span></span>](certificates.md)
</dt> <dt>

[<span data-ttu-id="a391c-216">**CAPICOM \_ OID**</span><span class="sxs-lookup"><span data-stu-id="a391c-216">**CAPICOM\_OID**</span></span>](capicom-oid.md)
</dt> </dl>

 

 
