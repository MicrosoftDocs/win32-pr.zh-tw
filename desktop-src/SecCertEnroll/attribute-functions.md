---
description: 您可以將屬性新增至憑證要求，以提供憑證授權單位單位 (CA) 以及可在建立和發行憑證時使用的其他資訊。
ms.assetid: 3eba5a2f-eeac-4e38-8705-b12bc183b7eb
title: 屬性函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6413da0d43c142373e6f3cabe3d8e31636b82ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192617"
---
# <a name="attribute-functions"></a><span data-ttu-id="e6619-103">屬性函式</span><span class="sxs-lookup"><span data-stu-id="e6619-103">Attribute Functions</span></span>

<span data-ttu-id="e6619-104">您可以將屬性新增至憑證要求，以提供證書 [*頒發機構*](/windows/desktop/SecGloss/c-gly) 單位 (CA) 以及可在建立和發行憑證時使用的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="e6619-104">Attributes can be added to a certificate request to provide a [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA) with additional information that it can use when creating and issuing a certificate.</span></span>

<span data-ttu-id="e6619-105">CertEnroll.dll 會執行下列介面來定義屬性和屬性集合：</span><span class="sxs-lookup"><span data-stu-id="e6619-105">CertEnroll.dll implements the following interfaces to define attributes and attribute collections:</span></span>

-   [<span data-ttu-id="e6619-106">**ICryptAttribute**</span><span class="sxs-lookup"><span data-stu-id="e6619-106">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [<span data-ttu-id="e6619-107">**ICryptAttributes**</span><span class="sxs-lookup"><span data-stu-id="e6619-107">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [<span data-ttu-id="e6619-108">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="e6619-108">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [<span data-ttu-id="e6619-109">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="e6619-109">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
-   [<span data-ttu-id="e6619-110">**IX509AttributeClientId**</span><span class="sxs-lookup"><span data-stu-id="e6619-110">**IX509AttributeClientId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [<span data-ttu-id="e6619-111">**IX509AttributeExtensions**</span><span class="sxs-lookup"><span data-stu-id="e6619-111">**IX509AttributeExtensions**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [<span data-ttu-id="e6619-112">**IX509AttributeArchiveKey**</span><span class="sxs-lookup"><span data-stu-id="e6619-112">**IX509AttributeArchiveKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [<span data-ttu-id="e6619-113">**IX509AttributeArchiveKeyHash**</span><span class="sxs-lookup"><span data-stu-id="e6619-113">**IX509AttributeArchiveKeyHash**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [<span data-ttu-id="e6619-114">**IX509AttributeCspProvider**</span><span class="sxs-lookup"><span data-stu-id="e6619-114">**IX509AttributeCspProvider**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [<span data-ttu-id="e6619-115">**IX509AttributeOSVersion**</span><span class="sxs-lookup"><span data-stu-id="e6619-115">**IX509AttributeOSVersion**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [<span data-ttu-id="e6619-116">**IX509AttributeRenewalCertificate**</span><span class="sxs-lookup"><span data-stu-id="e6619-116">**IX509AttributeRenewalCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

<span data-ttu-id="e6619-117">下列各節會識別 Xenroll.dll 所匯出的函式，以將密碼編譯屬性與憑證要求產生關聯，並討論如何使用 CertEnroll.dll 來取代函式，或指出兩個程式庫之間沒有對應存在：</span><span class="sxs-lookup"><span data-stu-id="e6619-117">The following sections identify functions exported by Xenroll.dll to associate cryptographic attributes with certificate requests and discuss how to use CertEnroll.dll to replace the function or indicate that no mapping between the two libraries exists:</span></span>

-   [<span data-ttu-id="e6619-118">addAttributeToRequestWStr</span><span class="sxs-lookup"><span data-stu-id="e6619-118">addAttributeToRequestWStr</span></span>](#addattributetorequestwstr)
-   [<span data-ttu-id="e6619-119">AddAuthenticatedAttributesToPKCS7Request</span><span class="sxs-lookup"><span data-stu-id="e6619-119">AddAuthenticatedAttributesToPKCS7Request</span></span>](#addauthenticatedattributestopkcs7request)
-   [<span data-ttu-id="e6619-120">addNameValuePairToRequestWStr</span><span class="sxs-lookup"><span data-stu-id="e6619-120">addNameValuePairToRequestWStr</span></span>](#addnamevaluepairtorequestwstr)
-   [<span data-ttu-id="e6619-121">AddNameValuePairToSignatureWStr</span><span class="sxs-lookup"><span data-stu-id="e6619-121">AddNameValuePairToSignatureWStr</span></span>](#addnamevaluepairtosignaturewstr)
-   [<span data-ttu-id="e6619-122">ClientId</span><span class="sxs-lookup"><span data-stu-id="e6619-122">ClientId</span></span>](#clientid)
-   [<span data-ttu-id="e6619-123">RenewalCertificate</span><span class="sxs-lookup"><span data-stu-id="e6619-123">RenewalCertificate</span></span>](#renewalcertificate)
-   [<span data-ttu-id="e6619-124">resetAttributes</span><span class="sxs-lookup"><span data-stu-id="e6619-124">resetAttributes</span></span>](#resetattributes)
-   [<span data-ttu-id="e6619-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6619-125">Related topics</span></span>](#related-topics)

## <a name="addattributetorequestwstr"></a><span data-ttu-id="e6619-126">addAttributeToRequestWStr</span><span class="sxs-lookup"><span data-stu-id="e6619-126">addAttributeToRequestWStr</span></span>

<span data-ttu-id="e6619-127">Xenroll.dll 中的 [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) 函數會將屬性新增至憑證要求。</span><span class="sxs-lookup"><span data-stu-id="e6619-127">The [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) function in Xenroll.dll adds an attribute to a certificate request.</span></span>

<span data-ttu-id="e6619-128">一般而言，若要使用在 CertEnroll.dll 中執行的物件，將屬性新增至要求，您可以執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e6619-128">In general, to add an attribute to a request by using the objects implemented in CertEnroll.dll, you can perform the following actions:</span></span>

1.  <span data-ttu-id="e6619-129">建立 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) 集合物件。</span><span class="sxs-lookup"><span data-stu-id="e6619-129">Create an [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection object.</span></span>
2.  <span data-ttu-id="e6619-130">建立 [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) 物件，並呼叫 [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attribute-initialize) 方法，從物件識別碼和屬性值建立屬性，或使用先前所列的任何介面來定義一個更常見的屬性。</span><span class="sxs-lookup"><span data-stu-id="e6619-130">Create an [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) object and call the [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attribute-initialize) method to create an attribute from an object identifier and attribute value or use any of the interfaces listed earlier to define one of the more common attributes.</span></span>
3.  <span data-ttu-id="e6619-131">使用 [**add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-add)方法，將在上一個步驟中建立的每個新屬性加入至 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)集合。</span><span class="sxs-lookup"><span data-stu-id="e6619-131">Add each new attribute created in the preceding step to the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection by using the [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-add) method.</span></span>
4.  <span data-ttu-id="e6619-132">建立 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) 物件，並呼叫 [**InitializeFromValues**](/windows/desktop/api/CertEnroll/nf-certenroll-icryptattribute-initializefromvalues) 方法將它初始化，並在輸入上指定 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) 集合。</span><span class="sxs-lookup"><span data-stu-id="e6619-132">Create an [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object and initialize it by calling the [**InitializeFromValues**](/windows/desktop/api/CertEnroll/nf-certenroll-icryptattribute-initializefromvalues) method and specifying the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection on input.</span></span>
5.  <span data-ttu-id="e6619-133">藉由呼叫現有 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)或 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)要求物件上的 [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes)屬性，來取出 [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)集合物件。</span><span class="sxs-lookup"><span data-stu-id="e6619-133">Retrieve an [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) collection object by calling the [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) property on an existing [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) or [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) request object.</span></span>
6.  <span data-ttu-id="e6619-134">將 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) 物件加入至 [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) 集合。</span><span class="sxs-lookup"><span data-stu-id="e6619-134">Add the [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object to the [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) collection.</span></span>

## <a name="addauthenticatedattributestopkcs7request"></a><span data-ttu-id="e6619-135">AddAuthenticatedAttributesToPKCS7Request</span><span class="sxs-lookup"><span data-stu-id="e6619-135">AddAuthenticatedAttributesToPKCS7Request</span></span>

<span data-ttu-id="e6619-136">驗證的屬性是名稱/值組，已簽署並加入至簽章。</span><span class="sxs-lookup"><span data-stu-id="e6619-136">Authenticated attributes are name-value pairs that are signed by and added to a signature.</span></span> <span data-ttu-id="e6619-137">Xenroll.dll 中的 [**AddAuthenticatedAttributesToPKCS7Request**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addauthenticatedattributestopkcs7request) 函數會將經過驗證的屬性陣列新增至 [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) 要求。</span><span class="sxs-lookup"><span data-stu-id="e6619-137">The [**AddAuthenticatedAttributesToPKCS7Request**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addauthenticatedattributestopkcs7request) function in Xenroll.dll adds an array of authenticated attributes to a [*PKCS \#7*](/windows/desktop/SecGloss/p-gly) request.</span></span>

<span data-ttu-id="e6619-138">如上所述， [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) 函式所述，您可以使用 CertEnroll.dll 輕鬆地定義屬性集合，並將其新增至憑證要求。</span><span class="sxs-lookup"><span data-stu-id="e6619-138">As discussed above for the [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) function, you can use CertEnroll.dll to easily define and add a collection of attributes to a certificate request.</span></span> <span data-ttu-id="e6619-139">但是，您無法選擇是否要驗證屬性。</span><span class="sxs-lookup"><span data-stu-id="e6619-139">You cannot, however, choose whether the attribute is authenticated.</span></span> <span data-ttu-id="e6619-140">註冊程式會自動進行此決策。</span><span class="sxs-lookup"><span data-stu-id="e6619-140">The enrollment process automatically makes this decision.</span></span>

## <a name="addnamevaluepairtorequestwstr"></a><span data-ttu-id="e6619-141">addNameValuePairToRequestWStr</span><span class="sxs-lookup"><span data-stu-id="e6619-141">addNameValuePairToRequestWStr</span></span>

<span data-ttu-id="e6619-142">Xenroll.dll 中的 [**addNameValuePairToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addnamevaluepairtorequestwstr) 函數會將未經驗證的名稱/值組加入至要求。</span><span class="sxs-lookup"><span data-stu-id="e6619-142">The [**addNameValuePairToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addnamevaluepairtorequestwstr) function in Xenroll.dll adds an unauthenticated name-value pair to a request.</span></span>

<span data-ttu-id="e6619-143">您可以使用 CertEnroll.dll 中的 [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) 介面來定義名稱/值組，也可以執行下列動作，將名稱/值組的集合新增至 CMC 要求物件：</span><span class="sxs-lookup"><span data-stu-id="e6619-143">You can use the [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) interface in CertEnroll.dll to define a name-value pair, and you can add a collection of name-value pairs to a CMC request object by performing the following actions:</span></span>

1.  <span data-ttu-id="e6619-144">建立並初始化 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件。</span><span class="sxs-lookup"><span data-stu-id="e6619-144">Create and initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span> <span data-ttu-id="e6619-145">初始化進程會建立空的 [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) 集合。</span><span class="sxs-lookup"><span data-stu-id="e6619-145">The initialization process creates an empty [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) collection.</span></span>
2.  <span data-ttu-id="e6619-146">呼叫現有 CMC 要求物件上的 [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) 屬性，以取出集合。</span><span class="sxs-lookup"><span data-stu-id="e6619-146">Call the [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) property on an existing CMC request object to retrieve the collection.</span></span>
3.  <span data-ttu-id="e6619-147">建立並初始化 [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) 物件。</span><span class="sxs-lookup"><span data-stu-id="e6619-147">Create and initialize an [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) object.</span></span>
4.  <span data-ttu-id="e6619-148">藉由呼叫 [**add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509namevaluepairs-add)方法，將每個新的名稱/值組新增至 [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)集合。</span><span class="sxs-lookup"><span data-stu-id="e6619-148">Add each new name-value pair to the [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) collection by calling the [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509namevaluepairs-add) method.</span></span>

<span data-ttu-id="e6619-149">註冊程式會將名稱-值組的集合放在 CMC 要求的 **TaggedAttribute** 結構中。</span><span class="sxs-lookup"><span data-stu-id="e6619-149">The enrollment process places the collection of name-value pairs in the **TaggedAttribute** structure of the CMC request.</span></span>

## <a name="addnamevaluepairtosignaturewstr"></a><span data-ttu-id="e6619-150">AddNameValuePairToSignatureWStr</span><span class="sxs-lookup"><span data-stu-id="e6619-150">AddNameValuePairToSignatureWStr</span></span>

<span data-ttu-id="e6619-151">Xenroll.dll 中的 [**AddNameValuePairToSignatureWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addnamevaluepairtosignaturewstr) 函數會將經過驗證的名稱/值組加入至要求。</span><span class="sxs-lookup"><span data-stu-id="e6619-151">The [**AddNameValuePairToSignatureWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addnamevaluepairtosignaturewstr) function in Xenroll.dll adds an authenticated name-value pair to a request.</span></span> <span data-ttu-id="e6619-152">這通常用來指定以註冊 (EOBO) 要求中的要求者名稱。</span><span class="sxs-lookup"><span data-stu-id="e6619-152">This is typically used to specify the requester name in an enroll-on-behalf-of (EOBO) request.</span></span>

<span data-ttu-id="e6619-153">在 CertEnroll.dll 中，使用 [**RequesterName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_requestername) 屬性來指定 EOBO 要求中的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6619-153">In CertEnroll.dll, use the [**RequesterName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_requestername) property to specify the name in an EOBO request.</span></span>

## <a name="clientid"></a><span data-ttu-id="e6619-154">ClientId</span><span class="sxs-lookup"><span data-stu-id="e6619-154">ClientId</span></span>

<span data-ttu-id="e6619-155">Xenroll.dll 中的 [**clientid**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_clientid) 函數會指定或抓取 **clientid** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e6619-155">The [**ClientId**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_clientid) function in Xenroll.dll specifies or retrieves a **ClientId** attribute.</span></span>

<span data-ttu-id="e6619-156">使用 CertEnroll.dll 中的 [**ClientId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_clientid) 屬性，將此屬性新增至 CMC 或 PKCS \# 10 要求。</span><span class="sxs-lookup"><span data-stu-id="e6619-156">Use the [**ClientId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_clientid) property in CertEnroll.dll to add this attribute to a CMC or PKCS \#10 request.</span></span>

## <a name="renewalcertificate"></a><span data-ttu-id="e6619-157">RenewalCertificate</span><span class="sxs-lookup"><span data-stu-id="e6619-157">RenewalCertificate</span></span>

<span data-ttu-id="e6619-158">Xenroll.dll 中的 [**RenewalCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate) 函數會指定或抓取 **RenewalCertificate** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e6619-158">The [**RenewalCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate) function in Xenroll.dll specifies or retrieves a **RenewalCertificate** attribute.</span></span>

<span data-ttu-id="e6619-159">在 CertEnroll.dll 中，當您在 PKCS 7 或 PKCS ) 物件上呼叫 [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) 時，會 \# 自動建立。</span><span class="sxs-lookup"><span data-stu-id="e6619-159">In CertEnroll.dll, when you call [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) on a PKCS \#7 or PKCS ) object is automatically created.</span></span>

## <a name="resetattributes"></a><span data-ttu-id="e6619-160">resetAttributes</span><span class="sxs-lookup"><span data-stu-id="e6619-160">resetAttributes</span></span>

<span data-ttu-id="e6619-161">Xenroll.dll 中的 [**resetAttributes**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetattributes) 函數會從要求中移除屬性集合。</span><span class="sxs-lookup"><span data-stu-id="e6619-161">The [**resetAttributes**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetattributes) function in Xenroll.dll removes the attribute collection from a request.</span></span>

<span data-ttu-id="e6619-162">若要使用 CertEnroll.dll 從索引中移除要求的屬性，請在 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)集合上呼叫 [**remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="e6619-162">To remove an attribute from a request by index using CertEnroll.dll, call the [**Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-remove) method on the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection.</span></span> <span data-ttu-id="e6619-163">若要從要求中移除所有屬性，請呼叫 [**Clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-clear) 方法。</span><span class="sxs-lookup"><span data-stu-id="e6619-163">To remove all attributes from a request, call the [**Clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-clear) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6619-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6619-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6619-165">將 Xenroll.dll 對應至 CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="e6619-165">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="e6619-166">**ICryptAttribute**</span><span class="sxs-lookup"><span data-stu-id="e6619-166">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[<span data-ttu-id="e6619-167">**ICryptAttributes**</span><span class="sxs-lookup"><span data-stu-id="e6619-167">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[<span data-ttu-id="e6619-168">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="e6619-168">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[<span data-ttu-id="e6619-169">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="e6619-169">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> <dt>

[<span data-ttu-id="e6619-170">**IX509NameValuePair**</span><span class="sxs-lookup"><span data-stu-id="e6619-170">**IX509NameValuePair**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)
</dt> <dt>

[<span data-ttu-id="e6619-171">**IX509NameValuePairs**</span><span class="sxs-lookup"><span data-stu-id="e6619-171">**IX509NameValuePairs**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)
</dt> </dl>

 

 
