---
description: 憑證服務提供可用於要求憑證的網頁註冊頁面。
ms.assetid: 1e198bc8-c712-4d0f-9e3a-35a295445acf
title: 自訂憑證服務網頁註冊頁面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb2fbf421eceb1ebf0b15379aca5d0788a992ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852312"
---
# <a name="customizing-certificate-services-web-enrollment-pages"></a><span data-ttu-id="5cbc1-103">自訂憑證服務網頁註冊頁面</span><span class="sxs-lookup"><span data-stu-id="5cbc1-103">Customizing Certificate Services Web Enrollment Pages</span></span>

<span data-ttu-id="5cbc1-104">[*憑證服務*](../secgloss/c-gly.md) 提供可用於要求憑證的網頁註冊頁面。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-104">[*Certificate Services*](../secgloss/c-gly.md) provides web enrollment pages that can be used to request certificates.</span></span> <span data-ttu-id="5cbc1-105">系統管理員可以自訂一些可在網頁註冊頁面中查看的專案;不過，在進行任何變更之前，您應該先熟悉網頁註冊頁面和 web 腳本。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-105">An administrator can customize some of the items that can be viewed in the web enrollment pages; however, you should be familiar with the web enrollment pages and web scripting before making any changes.</span></span> <span data-ttu-id="5cbc1-106">如需 web 腳本的詳細資訊，請參閱 [腳本](/previous-versions/ms950396(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-106">For more information about web scripting, see [Scripting](/previous-versions/ms950396(v=msdn.10)).</span></span>

<span data-ttu-id="5cbc1-107">[組織]、[組織單位]、[位置]、[狀態] 和 [國家/地區] 的 [辨別名稱] 欄位的預設值是安裝憑證服務時， (CA) 的 [*憑證授權單位*](../secgloss/c-gly.md) 單位所指定的值。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-107">The default values for the Distinguished Name fields for Organization, Organizational Unit, Locality, State, and Country/Region are the values specified for the [*certification authority*](../secgloss/c-gly.md) (CA) when Certificate Services is installed.</span></span> <span data-ttu-id="5cbc1-108">這些預設值會出現在網頁中，且使用者可以在憑證註冊程式期間變更這些預設值。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-108">These default values appear in the webpages and can be changed by the user during the certificate enrollment process.</span></span> <span data-ttu-id="5cbc1-109">However, if you want other default values to appear in the webpages, you can edit the Certdat.inc file (in the path \\*WindowsDirectory*\\System32\\Certsrv\\); specifically, you can assign custom values to the following variables provided for customization.</span><span class="sxs-lookup"><span data-stu-id="5cbc1-109">However, if you want other default values to appear in the webpages, you can edit the Certdat.inc file (in the path \\*WindowsDirectory*\\System32\\Certsrv\\); specifically, you can assign custom values to the following variables provided for customization.</span></span>



| <span data-ttu-id="5cbc1-110">變數</span><span class="sxs-lookup"><span data-stu-id="5cbc1-110">Variable</span></span>            | <span data-ttu-id="5cbc1-111">描述</span><span class="sxs-lookup"><span data-stu-id="5cbc1-111">Description</span></span>                                                                                                                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cbc1-112">sDefaultCompany</span><span class="sxs-lookup"><span data-stu-id="5cbc1-112">sDefaultCompany</span></span>     | <span data-ttu-id="5cbc1-113">預設公司 (會在 [*憑證要求*](../secgloss/c-gly.md) 中顯示為 [ [*x.509*](../secgloss/x-gly.md) 組織] 欄位) 。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-113">Default company (appears in the [*certificate request*](../secgloss/c-gly.md) as the [*X.509*](../secgloss/x-gly.md) Organization field).</span></span> |
| <span data-ttu-id="5cbc1-114">sDefaultOrgUnit</span><span class="sxs-lookup"><span data-stu-id="5cbc1-114">sDefaultOrgUnit</span></span>     | <span data-ttu-id="5cbc1-115">預設部門 (在憑證要求中會顯示為 [x.509 組織單位] 欄位) 。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-115">Default department (appears in the certificate request as the X.509 Organizational Unit field).</span></span>                                                                                                                                           |
| <span data-ttu-id="5cbc1-116">sDefaultLocality</span><span class="sxs-lookup"><span data-stu-id="5cbc1-116">sDefaultLocality</span></span>    | <span data-ttu-id="5cbc1-117">預設 city (在憑證要求中會顯示為 [x.509 位置] 欄位) 。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-117">Default city (appears in the certificate request as the X.509 Location field).</span></span>                                                                                                                                                            |
| <span data-ttu-id="5cbc1-118">sDefaultState</span><span class="sxs-lookup"><span data-stu-id="5cbc1-118">sDefaultState</span></span>       | <span data-ttu-id="5cbc1-119">預設的州/省 (在憑證要求中會顯示為 [x.509 狀態] 欄位) 。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-119">Default state/province (appears in the certificate request as the X.509 State field).</span></span>                                                                                                                                                     |
| <span data-ttu-id="5cbc1-120">sDefaultCountry</span><span class="sxs-lookup"><span data-stu-id="5cbc1-120">sDefaultCountry</span></span>     | <span data-ttu-id="5cbc1-121">預設國家/地區 (在憑證要求中會顯示為 [x.509 國家/地區] 欄位) 。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-121">Default country/region (appears in the certificate request as the X.509 Country/Region field).</span></span>                                                                                                                                            |
| <span data-ttu-id="5cbc1-122">nPendingTimeoutDays</span><span class="sxs-lookup"><span data-stu-id="5cbc1-122">nPendingTimeoutDays</span></span> | <span data-ttu-id="5cbc1-123">要求之後，使用者可以取得擱置中憑證的天數。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-123">Number of days in which the user can retrieve a pending certificate after it has been requested.</span></span>                                                                                                                                          |



 

<span data-ttu-id="5cbc1-124">Certdat inc. 檔案中不應變更其他變數。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-124">No other variables should be changed in the Certdat.inc file.</span></span>

<span data-ttu-id="5cbc1-125">下列範例會將預設的組織單位設為「行銷」。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-125">The following example sets the default Organizational Unit to "Marketing".</span></span>


```VB
sDefaultOrgUnit="Marketing"
```



<span data-ttu-id="5cbc1-126">此外，您可以編輯 Certrqtp 檔案，以新增、變更或移除使用者可用的 [*憑證範本*](../secgloss/c-gly.md) 或類型。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-126">Additionally, you can edit the Certrqtp.inc file to add, change, or remove [*certificate templates*](../secgloss/c-gly.md) or types available to the user.</span></span> <span data-ttu-id="5cbc1-127">這些範本和類型以及相關資訊都包含在名為 rgAvailReqTypes (*m*，5) 的維度陣列中。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-127">These templates and types, as well as related information, are contained in a dimensioned array called rgAvailReqTypes(*m*,5).</span></span>

<span data-ttu-id="5cbc1-128">這個陣列（如同所有 Visual Basic Scripting Edition 陣列）是以零為基礎，因此陣列的第一個維度 *m* 會配置 *m*+ 1 個專案的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-128">This array, like all Visual Basic Scripting Edition arrays, is zero based, and as a result, the array's first dimension, *m*, allocates memory for *m*+1 items.</span></span> <span data-ttu-id="5cbc1-129">因此，如果在自訂網頁時，您需要修改 rgAvailReqTypes 陣列中的專案數，請將 *m* 維度設定為小於所需專案總數的1。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-129">Therefore, if in customizing the webpages, you need to modify the number of items in the rgAvailReqTypes array, set the *m* dimension to one less than the total number of items you need.</span></span> <span data-ttu-id="5cbc1-130">例如，如果您將有七個憑證範本，請變更 rgAvailReqTypes 的宣告，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-130">For example, if you will have seven certificate templates, change the declaration of rgAvailReqTypes as shown in the following example.</span></span>


```VB
Dim rgAvailReqTypes(6,5)
```



<span data-ttu-id="5cbc1-131">陣列的第二個維度（一律具有值五個）會配置構成每個專案的六個欄位。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-131">The array's second dimension, which always has the value five, allocates the six fields that compose each item.</span></span> <span data-ttu-id="5cbc1-132">這六個欄位代表憑證範本或類型、與此範本或類型相關聯的顯示名稱，以及範本是否需要 [*安全/多用途網際網路郵件延伸*](../secgloss/s-gly.md) (S/MIME) 。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-132">These six fields represent the certificate template or type, the display name associated with this template or type, and whether the template requires [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME).</span></span>

<span data-ttu-id="5cbc1-133">為了讓您更容易瞭解存取了哪些欄位，Certrqtp 也提供下列常數，可讓您在設定域值時使用。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-133">To make it easier to understand which of these fields is being accessed, Certrqtp.inc also provides the following constants you can use when setting field values.</span></span>



| <span data-ttu-id="5cbc1-134">常數</span><span class="sxs-lookup"><span data-stu-id="5cbc1-134">Constant</span></span>                              | <span data-ttu-id="5cbc1-135">描述</span><span class="sxs-lookup"><span data-stu-id="5cbc1-135">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cbc1-136">**欄位 \_ OID**</span><span class="sxs-lookup"><span data-stu-id="5cbc1-136">**FIELD\_OID**</span></span>                        | <span data-ttu-id="5cbc1-137"> (適用于獨立 Ca) 索引至專案的第一個欄位;代表憑證類型 (OID) 的 [*物件識別碼*](../secgloss/o-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-137">(Applies to stand-alone CAs) Index to the item's first field; represents an [*object identifier*](../secgloss/o-gly.md) (OID) for a certificate type.</span></span><br/>                                                                                                           |
| <span data-ttu-id="5cbc1-138">**欄位 \_ 範本**</span><span class="sxs-lookup"><span data-stu-id="5cbc1-138">**FIELD\_TEMPLATE**</span></span>                   | <span data-ttu-id="5cbc1-139"> (適用于企業 Ca) 索引至專案的第一個欄位;代表憑證範本。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-139">(Applies to enterprise CAs) Index to the item's first field; represents a certificate template.</span></span><br/>                                                                                                                                                                                                                           |
| <span data-ttu-id="5cbc1-140">**欄位 \_ FRIENDLYNAME**</span><span class="sxs-lookup"><span data-stu-id="5cbc1-140">**FIELD\_FRIENDLYNAME**</span></span>               | <span data-ttu-id="5cbc1-141">專案第二個欄位的索引;表示在註冊第一個欄位中的專案) 時，使用者會看到的顯示名稱 (。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-141">Index to the item's second field; represents the display name (which the user will see when enrolling) of the item in the first field.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="5cbc1-142">**欄位 \_ 請 CSPLIST**</span><span class="sxs-lookup"><span data-stu-id="5cbc1-142">**FIELD\_CSPLIST**</span></span>                    | <span data-ttu-id="5cbc1-143">專案第三個欄位的索引。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-143">Index to the item's third field.</span></span> <span data-ttu-id="5cbc1-144">範本允許的 [*密碼編譯服務提供者*](../secgloss/c-gly.md) 名稱清單。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-144">A list of [*Cryptographic Service Provider*](../secgloss/c-gly.md) names allowed by the template.</span></span> <span data-ttu-id="5cbc1-145">清單中的每個名稱都是以問號 (？ ) 分隔。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-145">Each name in the list is separated by a question mark (?).</span></span>                                                    |
| <span data-ttu-id="5cbc1-146">**欄位 \_ CSPLIST2**</span><span class="sxs-lookup"><span data-stu-id="5cbc1-146">**FIELD\_CSPLIST2**</span></span>                   | <span data-ttu-id="5cbc1-147">專案第四個欄位的索引。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-147">Index to the item's fourth field.</span></span> <span data-ttu-id="5cbc1-148">範本允許的 [*密碼編譯服務提供者*](../secgloss/c-gly.md) 名稱的次要清單。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-148">A secondary list of [*Cryptographic Service Provider*](../secgloss/c-gly.md) names allowed by the template.</span></span> <span data-ttu-id="5cbc1-149">清單中的每個名稱都是以問號 (？ ) 分隔。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-149">Each name in the list is separated by a question mark (?).</span></span> <span data-ttu-id="5cbc1-150">此清單提供不同的預設值。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-150">This list provides a different default.</span></span> |
| <span data-ttu-id="5cbc1-151">**欄位可 \_ 匯出**</span><span class="sxs-lookup"><span data-stu-id="5cbc1-151">**FIELD\_EXPORTABLE**</span></span>                 | <span data-ttu-id="5cbc1-152">專案第五個欄位的索引。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-152">Index to the item's fifth field.</span></span> <span data-ttu-id="5cbc1-153">指出範本是否會指定應該可匯出的金鑰。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-153">Indicates whether the template specifies that the key should be exportable.</span></span> <span data-ttu-id="5cbc1-154">如果此欄位包含 "True"，則金鑰可匯出。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-154">If this field contains "True", the key is exportable.</span></span> <span data-ttu-id="5cbc1-155">如果此欄位包含 "False"，則無法匯出金鑰。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-155">If this field contains "False", the key is not exportable.</span></span>                                                                                                        |
| <span data-ttu-id="5cbc1-156">**FIELD \_ 需要 \_ SMIME \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="5cbc1-156">**FIELD\_NEEDS\_SMIME\_CAPABILITIES**</span></span> | <span data-ttu-id="5cbc1-157">不支援這個常數。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-157">This constant is not supported.</span></span>                                                                                                                                                                                                                                                                                                      |



 

<span data-ttu-id="5cbc1-158">例如，下列運算式會將1.3.6.1.5.5.7.3.2 的 OID 指派給第一個專案的第一個欄位，並將「網頁瀏覽器憑證」指派給第一個專案的第二個欄位， (陣列值為零的第一個專案) 索引。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-158">For example, the following expressions assign the OID of 1.3.6.1.5.5.7.3.2 to the first item's first field and assign "Web Browser Certificate" to the first item's second field (the array value of zero indexes the first item).</span></span>


```VB
rgAvailReqTypes(0, FIELD_OID) = "1.3.6.1.5.5.7.3.2"
rgAvailReqTypes(0, FIELD_FRIENDLYNAME) = "Web Browser Certificate"
```



<span data-ttu-id="5cbc1-159">這些指派的結果是使用者會在註冊時看到文字 **Web 瀏覽器憑證** ，如果使用者選取 **網頁瀏覽器憑證**， [*憑證要求*](../secgloss/c-gly.md) 將會包含 OID 1.3.6.1.5.5.7.3.2。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-159">The result of these assignments is that the user will see the text **Web Browser Certificate** when enrolling, and if the user selects **Web Browser Certificate**, the [*certificate request*](../secgloss/c-gly.md) will contain the OID 1.3.6.1.5.5.7.3.2.</span></span>

<span data-ttu-id="5cbc1-160">Certrqtp inc. 檔案也包含用於憑證範本或類型之顯示名稱的常數。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-160">The Certrqtp.inc file also contains constants that are used for the display names of the certificate templates or types.</span></span> <span data-ttu-id="5cbc1-161">下列範例顯示格式。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-161">The following example shows the format.</span></span>


```VB
' Strings for localization.
Const L_WebBrowserCert_Text="Web Browser Certificate"
Const L_EmailProtectionCert_Text="E-Mail Protection Certificate"
Const L_UserTemplateCert_Text="User Certificate"
```



<span data-ttu-id="5cbc1-162">這些常數定義于 Certrqtp inc. 檔案的區塊中，而此群組可讓您更輕鬆地將自訂值指派給每個常數。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-162">These constants are defined in a block in the Certrqtp.inc file, and this grouping makes it easier to assign each of them a custom value.</span></span> <span data-ttu-id="5cbc1-163">當您將國際版網頁的顯示名稱當地語系化時，這會特別有用。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-163">This is particularly helpful when you localize the display names for international versions of the webpages.</span></span>

<span data-ttu-id="5cbc1-164">最後，Certrqtp 檔案包含的變數代表 rgAvailReqTypes 陣列中的憑證範本數目或類型。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-164">Finally, the Certrqtp.inc file contains a variable that represents the number of certificate templates or types in the rgAvailReqTypes array.</span></span> <span data-ttu-id="5cbc1-165">相對於陣列的 *m* 維度，請將 nAvailReqTypes 變數的值設定為您的安裝將會使用的憑證範本或類型的實際數目。此值不能大於 *m*+ 1。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-165">In contrast to the *m* dimension of the array, set the value of the nAvailReqTypes variable to the actual number of certificate templates or types that your installation will use; this value must be no larger than *m*+1.</span></span> <span data-ttu-id="5cbc1-166">雖然在 Certrqtp inc 檔案的頂端附近宣告，但 nAvailReqTypes 會在填入 rgAvailReqTypes 陣列後指派一個值，讓您更輕鬆地查看陣列實際使用的元素數目。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-166">Although declared near the top of the Certrqtp.inc file, nAvailReqTypes is assigned a value after the rgAvailReqTypes array is populated, making it easier to see how many elements are actually used by the array.</span></span> <span data-ttu-id="5cbc1-167">NAvailReqTypes 值用於網頁註冊頁面中其他位置的反復專案中，因此，此變數必須正確地反映您想要讓使用者看到的憑證範本或類型數目。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-167">The nAvailReqTypes value is used in an iteration elsewhere in the web enrollment pages, so it is important that this variable accurately reflect the number of certificate templates or types that you want to be viewable to the user.</span></span>

<span data-ttu-id="5cbc1-168">請注意，只會將 [*憑證範本*](../secgloss/c-gly.md) 和類型新增至 Certrqtp 檔案，並不保證使用者能夠取得具有這些特性的憑證;CA 必須獲得授權，才能針對指定的憑證範本或類型發出憑證。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-168">Note that merely adding [*certificate templates*](../secgloss/c-gly.md) and types to the Certrqtp.inc file does not guarantee that the user will be able to get a certificate with those traits; the CA must be authorized to issue a certificate for the specified certificate template or type.</span></span>

<span data-ttu-id="5cbc1-169">安裝可以建立自己的應用程式或網頁來要求和接收憑證。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-169">Installations can create their own applications or webpages to request and receive a certificate.</span></span> <span data-ttu-id="5cbc1-170">[**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4)和 [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2)物件可讓程式設計人員或腳本撰寫者建立 [*憑證要求*](../secgloss/c-gly.md)應用程式。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-170">The [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4) and [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2) objects allow programmers or scripters to build [*certificate request*](../secgloss/c-gly.md) applications.</span></span>

<span data-ttu-id="5cbc1-171">若要要求在 [*智慧卡*](../secgloss/s-gly.md)上發行憑證，您可以使用智慧卡註冊控制項。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-171">To request a certificate to be issued on a [*smart card*](../secgloss/s-gly.md), you can use the Smart Card Enrollment Control.</span></span> <span data-ttu-id="5cbc1-172">如需詳細資訊和範例程式碼，請參閱 [**ISCrdEnr**](iscrdenr.md)。</span><span class="sxs-lookup"><span data-stu-id="5cbc1-172">For details and example code, see [**ISCrdEnr**](iscrdenr.md).</span></span>

 

 
