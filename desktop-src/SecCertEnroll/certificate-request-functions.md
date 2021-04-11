---
description: CertEnroll.dll 程式庫會實施五個介面，可用來建立和管理憑證要求。
ms.assetid: f4630095-6ba2-46f7-8825-e7a5b1cb185a
title: 憑證要求功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04191f49949f662a9b9d780726f7ac7a40b370ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026317"
---
# <a name="certificate-request-functions"></a><span data-ttu-id="c60e8-103">憑證要求功能</span><span class="sxs-lookup"><span data-stu-id="c60e8-103">Certificate Request Functions</span></span>

<span data-ttu-id="c60e8-104">CertEnroll.dll 程式庫會實施五個介面，可用來建立和管理憑證要求。</span><span class="sxs-lookup"><span data-stu-id="c60e8-104">The CertEnroll.dll library implements five interfaces that can be used to create and manage a certificate request.</span></span> <span data-ttu-id="c60e8-105">在這些情況下， [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) 介面代表一個抽象基底物件，此物件定義了下列四個介面所繼承的方法簽章。</span><span class="sxs-lookup"><span data-stu-id="c60e8-105">Of these, the [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) interface represents an abstract base object that defines method signatures inherited by the following four interfaces.</span></span>

| <span data-ttu-id="c60e8-106">介面</span><span class="sxs-lookup"><span data-stu-id="c60e8-106">Interface</span></span>                                                                        | <span data-ttu-id="c60e8-107">描述</span><span class="sxs-lookup"><span data-stu-id="c60e8-107">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c60e8-108">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="c60e8-108">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | <span data-ttu-id="c60e8-109">可讓您直接建立憑證，而不需 (CA) 的 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位。</span><span class="sxs-lookup"><span data-stu-id="c60e8-109">Enables you to create a certificate directly without applying to a [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA).</span></span><br/>                                                                                                            |
| [<span data-ttu-id="c60e8-110">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="c60e8-110">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | <span data-ttu-id="c60e8-111">代表透過 [*cms 的憑證管理*](/windows/desktop/SecGloss/c-gly) (CMC)  (憑證管理訊息（透過 cms）) 憑證要求（可包含嵌套的 PKCS \# 10 要求或其他 CMC 要求物件）。</span><span class="sxs-lookup"><span data-stu-id="c60e8-111">Represents a [*Certificate Management over CMS*](/windows/desktop/SecGloss/c-gly) (CMC) (Certificate Management Message over CMS) certificate request that can contain a nested PKCS \#10 request or another CMC request object.</span></span><br/> |
| [<span data-ttu-id="c60e8-112">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="c60e8-112">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | <span data-ttu-id="c60e8-113">表示 [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) 憑證訊息語法 (CMS) 要求物件必須包含嵌套的 PKCS \# 10 要求。</span><span class="sxs-lookup"><span data-stu-id="c60e8-113">Represents a [*PKCS \#7*](/windows/desktop/SecGloss/p-gly) certificate message syntax (CMS) request object that must contain a nested PKCS \#10 request.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="c60e8-114">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="c60e8-114">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | <span data-ttu-id="c60e8-115">表示 PKCS \# 10 憑證要求。</span><span class="sxs-lookup"><span data-stu-id="c60e8-115">Represents a PKCS \#10 certificate request.</span></span> <span data-ttu-id="c60e8-116">PKCS \# 10 要求可以直接傳送至 CA，或可由 pkcs \# 7 或 CMC 要求包裝。</span><span class="sxs-lookup"><span data-stu-id="c60e8-116">A PKCS \#10 request can be sent directly to a CA, or it can be wrapped by a PKCS \#7 or CMC request.</span></span><br/>                                                                                                                                                            |



 

<span data-ttu-id="c60e8-117">您可以使用憑證要求物件來初始化 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件，以在憑證階層中註冊用戶端，並安裝 CA 所傳回的憑證回應。</span><span class="sxs-lookup"><span data-stu-id="c60e8-117">You can use a certificate request object to initialize an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object to enroll a client in a certificate hierarchy and install the certificate response returned by the CA.</span></span>

<span data-ttu-id="c60e8-118">下列各節會識別 Xenroll.dll 所匯出的函式，以建立、列舉或刪除憑證要求。</span><span class="sxs-lookup"><span data-stu-id="c60e8-118">Each of the following sections identifies a function exported by Xenroll.dll to create, enumerate, or delete certificate requests.</span></span> <span data-ttu-id="c60e8-119">每個章節也會討論如何使用 CertEnroll.dll 來取代函式，或指出兩個程式庫之間沒有對應存在：</span><span class="sxs-lookup"><span data-stu-id="c60e8-119">Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists:</span></span>

-   [<span data-ttu-id="c60e8-120">createFilePKCS10WStr</span><span class="sxs-lookup"><span data-stu-id="c60e8-120">createFilePKCS10WStr</span></span>](#createfilepkcs10wstr)
-   [<span data-ttu-id="c60e8-121">createFileRequestWStr</span><span class="sxs-lookup"><span data-stu-id="c60e8-121">createFileRequestWStr</span></span>](#createfilerequestwstr)
-   [<span data-ttu-id="c60e8-122">createPKCS10WStr</span><span class="sxs-lookup"><span data-stu-id="c60e8-122">createPKCS10WStr</span></span>](#createpkcs10wstr)
-   [<span data-ttu-id="c60e8-123">CreatePKCS7RequestFromRequest</span><span class="sxs-lookup"><span data-stu-id="c60e8-123">CreatePKCS7RequestFromRequest</span></span>](#createpkcs7requestfromrequest)
-   [<span data-ttu-id="c60e8-124">createRequestWStr</span><span class="sxs-lookup"><span data-stu-id="c60e8-124">createRequestWStr</span></span>](#createrequestwstr)
-   [<span data-ttu-id="c60e8-125">DeleteRequestCert</span><span class="sxs-lookup"><span data-stu-id="c60e8-125">DeleteRequestCert</span></span>](#deleterequestcert)
-   [<span data-ttu-id="c60e8-126">enumPendingRequestWStr</span><span class="sxs-lookup"><span data-stu-id="c60e8-126">enumPendingRequestWStr</span></span>](#enumpendingrequestwstr)
-   [<span data-ttu-id="c60e8-127">removePendingRequestWStr</span><span class="sxs-lookup"><span data-stu-id="c60e8-127">removePendingRequestWStr</span></span>](#removependingrequestwstr)
-   [<span data-ttu-id="c60e8-128">重設</span><span class="sxs-lookup"><span data-stu-id="c60e8-128">Reset</span></span>](#reset)
-   [<span data-ttu-id="c60e8-129">setPendingRequestInfoWStr</span><span class="sxs-lookup"><span data-stu-id="c60e8-129">setPendingRequestInfoWStr</span></span>](#setpendingrequestinfowstr)
-   [<span data-ttu-id="c60e8-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="c60e8-130">Related topics</span></span>](#related-topics)

## <a name="createfilepkcs10wstr"></a><span data-ttu-id="c60e8-131">createFilePKCS10WStr</span><span class="sxs-lookup"><span data-stu-id="c60e8-131">createFilePKCS10WStr</span></span>

<span data-ttu-id="c60e8-132">Xenroll.dll 中的 [**createFilePKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr) 函數會建立 base64 編碼的 PKCS \# 10 憑證要求，並將它儲存在檔案中。</span><span class="sxs-lookup"><span data-stu-id="c60e8-132">The [**createFilePKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr) function in Xenroll.dll creates a base64-encoded PKCS \#10 certificate request and saves it in a file.</span></span>

<span data-ttu-id="c60e8-133">CertEnroll.dll 程式庫不會直接執行將要求寫入檔案的功能。</span><span class="sxs-lookup"><span data-stu-id="c60e8-133">The CertEnroll.dll library does not directly implement functionality to write a request to a file.</span></span> <span data-ttu-id="c60e8-134">不過，您可以藉由呼叫 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)物件上的 [**RawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata)屬性，並建立自訂函式來將值複製到檔案中，來取得憑證要求。</span><span class="sxs-lookup"><span data-stu-id="c60e8-134">You can, however, retrieve a certificate request by calling the [**RawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) property on the [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) object and creating a custom function to copy the value to a file.</span></span>

## <a name="createfilerequestwstr"></a><span data-ttu-id="c60e8-135">createFileRequestWStr</span><span class="sxs-lookup"><span data-stu-id="c60e8-135">createFileRequestWStr</span></span>

<span data-ttu-id="c60e8-136">Xenroll.dll 中的 [**createFileRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilerequestwstr) 函數會建立 pkcs \# 7、PKCS \# 10 或 CMC 憑證要求，並將它儲存在檔案中。</span><span class="sxs-lookup"><span data-stu-id="c60e8-136">The [**createFileRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilerequestwstr) function in Xenroll.dll creates a PKCS \#7, PKCS \#10, or CMC certificate request and saves it in a file.</span></span>

<span data-ttu-id="c60e8-137">CertEnroll.dll 程式庫不會直接執行將要求寫入檔案的功能。</span><span class="sxs-lookup"><span data-stu-id="c60e8-137">The CertEnroll.dll library does not directly implement functionality to write a request to a file.</span></span> <span data-ttu-id="c60e8-138">不過，您可以藉由呼叫 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)物件上的 [**RawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata)屬性，並建立自訂函式來將值複製到檔案中，來取得憑證要求。</span><span class="sxs-lookup"><span data-stu-id="c60e8-138">You can, however, retrieve a certificate request by calling the [**RawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) property on the [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) object and creating a custom function to copy the value to a file.</span></span>

## <a name="createpkcs10wstr"></a><span data-ttu-id="c60e8-139">createPKCS10WStr</span><span class="sxs-lookup"><span data-stu-id="c60e8-139">createPKCS10WStr</span></span>

<span data-ttu-id="c60e8-140">Xenroll.dll 中的 [**createPKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr) 函數會建立 PKCS \# 10 憑證要求，並將它複製到位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="c60e8-140">The [**createPKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr) function in Xenroll.dll creates a PKCS \#10 certificate request and copies it to a byte array.</span></span>

<span data-ttu-id="c60e8-141">您可以使用 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 物件 \# ，從現有的要求、現有的憑證、 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)、 [*公開金鑰*](/windows/desktop/SecGloss/p-gly)或範本來初始化 PKCS 10 要求。</span><span class="sxs-lookup"><span data-stu-id="c60e8-141">You can use an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object to initialize a PKCS \#10 request from an existing request, an existing certificate, a [*private key*](/windows/desktop/SecGloss/p-gly), a [*public key*](/windows/desktop/SecGloss/p-gly), or a template.</span></span>

## <a name="createpkcs7requestfromrequest"></a><span data-ttu-id="c60e8-142">CreatePKCS7RequestFromRequest</span><span class="sxs-lookup"><span data-stu-id="c60e8-142">CreatePKCS7RequestFromRequest</span></span>

<span data-ttu-id="c60e8-143">Xenroll.dll 中的 [**CreatePKCS7RequestFromRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs7requestfromrequest) 函數會建立 PKCS \# 7 憑證要求，並將它複製到位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="c60e8-143">The [**CreatePKCS7RequestFromRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs7requestfromrequest) function in Xenroll.dll creates a PKCS \#7 certificate request and copies it to a byte array.</span></span>

<span data-ttu-id="c60e8-144">您可以使用 [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) 物件 \# ，從現有的要求、現有的憑證、內部要求物件或範本初始化 PKCS 7 要求。</span><span class="sxs-lookup"><span data-stu-id="c60e8-144">You can use an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object to initialize a PKCS \#7 request from an existing request, an existing certificate, an inner request object, or a template.</span></span>

## <a name="createrequestwstr"></a><span data-ttu-id="c60e8-145">createRequestWStr</span><span class="sxs-lookup"><span data-stu-id="c60e8-145">createRequestWStr</span></span>

<span data-ttu-id="c60e8-146">Xenroll.dll 中的 [**createRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createrequestwstr) 函數會建立 pkcs \# 7、PKCS \# 10 或 CMC 憑證要求，並將它複製到位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="c60e8-146">The [**createRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createrequestwstr) function in Xenroll.dll creates a PKCS \#7, PKCS \#10, or CMC certificate request and copies it to a byte array.</span></span>

<span data-ttu-id="c60e8-147">若要使用 CertEnroll.dll 程式庫來建立 PKCS \# 7、pkcs \# 10 或 CMC 要求，您可以建立及初始化 [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)、 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)或 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="c60e8-147">To use the CertEnroll.dll library to create PKCS \#7, PKCS \#10, or CMC requests, you can create and initialize instances of the [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7), [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10), or [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) objects.</span></span>

## <a name="deleterequestcert"></a><span data-ttu-id="c60e8-148">DeleteRequestCert</span><span class="sxs-lookup"><span data-stu-id="c60e8-148">DeleteRequestCert</span></span>

<span data-ttu-id="c60e8-149">Xenroll.dll 中的 [**DeleteRequestCert**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert) 函式會指定或抓取布林值，指出是否在安裝憑證回應之後移除虛擬憑證。</span><span class="sxs-lookup"><span data-stu-id="c60e8-149">The [**DeleteRequestCert**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert) function in Xenroll.dll specifies or retrieves a Boolean value that indicates whether a dummy certificate is removed after a certificate response has been installed.</span></span>

<span data-ttu-id="c60e8-150">CertEnroll.dll 中的 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件會自動在要求存放區中建立虛擬憑證，以暫時儲存在註冊程式期間初始化的各種憑證屬性。</span><span class="sxs-lookup"><span data-stu-id="c60e8-150">The [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object in CertEnroll.dll automatically creates dummy certificates in the request store to temporarily save various certificate properties that are initialized during the enrollment process.</span></span> <span data-ttu-id="c60e8-151">CA 發行憑證之後，會將屬性複製到新的憑證，並刪除虛擬憑證。</span><span class="sxs-lookup"><span data-stu-id="c60e8-151">After a certificate is issued by a CA, the properties are copied to the new certificate and the dummy certificate is deleted.</span></span> <span data-ttu-id="c60e8-152">CertEnroll.dll 程式庫不允許您在安裝憑證回應之後，強制虛擬憑證維持不變。</span><span class="sxs-lookup"><span data-stu-id="c60e8-152">The CertEnroll.dll library does not allow you to force a dummy certificate to remain after the certificate response has been installed.</span></span>

## <a name="enumpendingrequestwstr"></a><span data-ttu-id="c60e8-153">enumPendingRequestWStr</span><span class="sxs-lookup"><span data-stu-id="c60e8-153">enumPendingRequestWStr</span></span>

<span data-ttu-id="c60e8-154">Xenroll.dll 中的 [**enumPendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-enumpendingrequestwstr) 函式會抓取暫止要求的指定屬性值。</span><span class="sxs-lookup"><span data-stu-id="c60e8-154">The [**enumPendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-enumpendingrequestwstr) function in Xenroll.dll retrieves a specified property value for a pending request.</span></span>

<span data-ttu-id="c60e8-155">CertEnroll.dll 程式庫不會直接執行移除暫止憑證要求的功能。</span><span class="sxs-lookup"><span data-stu-id="c60e8-155">The CertEnroll.dll library does not directly implement functionality to remove a pending certificate request.</span></span>

## <a name="removependingrequestwstr"></a><span data-ttu-id="c60e8-156">removePendingRequestWStr</span><span class="sxs-lookup"><span data-stu-id="c60e8-156">removePendingRequestWStr</span></span>

<span data-ttu-id="c60e8-157">Xenroll.dll 中的 [**removePendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-removependingrequestwstr) 函式會從要求存放區中移除暫止的要求。</span><span class="sxs-lookup"><span data-stu-id="c60e8-157">The [**removePendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-removependingrequestwstr) function in Xenroll.dll removes a pending request from the request store.</span></span>

<span data-ttu-id="c60e8-158">CertEnroll.dll 程式庫不會直接執行移除暫止憑證要求的功能。</span><span class="sxs-lookup"><span data-stu-id="c60e8-158">The CertEnroll.dll library does not directly implement functionality to remove a pending certificate request.</span></span>

## <a name="reset"></a><span data-ttu-id="c60e8-159">重設</span><span class="sxs-lookup"><span data-stu-id="c60e8-159">Reset</span></span>

<span data-ttu-id="c60e8-160">Xenroll.dll 中的 [**Reset**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-reset) 函數會將憑證註冊控制項傳回到初始狀態。</span><span class="sxs-lookup"><span data-stu-id="c60e8-160">The [**Reset**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-reset) function in Xenroll.dll returns the Certificate Enrollment Control to an initial state.</span></span>

<span data-ttu-id="c60e8-161">您可以使用 Certenroll.dll 建立所需類型的新要求物件，以達到相同的結果。</span><span class="sxs-lookup"><span data-stu-id="c60e8-161">You can achieve the same result by using Certenroll.dll to create a new request object of the required type.</span></span>

## <a name="setpendingrequestinfowstr"></a><span data-ttu-id="c60e8-162">setPendingRequestInfoWStr</span><span class="sxs-lookup"><span data-stu-id="c60e8-162">setPendingRequestInfoWStr</span></span>

<span data-ttu-id="c60e8-163">Xenroll.dll 中的 [**setPendingRequestInfoWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setpendingrequestinfowstr) 函數會指定暫止要求的屬性。</span><span class="sxs-lookup"><span data-stu-id="c60e8-163">The [**setPendingRequestInfoWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setpendingrequestinfowstr) function in Xenroll.dll specifies properties for the pending request.</span></span>

<span data-ttu-id="c60e8-164">CertEnroll.dll 程式庫不會直接執行移除暫止憑證要求的功能。</span><span class="sxs-lookup"><span data-stu-id="c60e8-164">The CertEnroll.dll library does not directly implement functionality to remove a pending certificate request.</span></span> <span data-ttu-id="c60e8-165">您可以呼叫 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)物件上的 [**CAConfigString**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_caconfigstring)屬性，以抓取設定字串，但僅適用于使用中的註冊物件。</span><span class="sxs-lookup"><span data-stu-id="c60e8-165">You can call the [**CAConfigString**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_caconfigstring) property on the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object to retrieve a configuration string but only for an active enrollment object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c60e8-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="c60e8-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c60e8-167">將 Xenroll.dll 對應至 CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="c60e8-167">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="c60e8-168">**ISignerCertificate**</span><span class="sxs-lookup"><span data-stu-id="c60e8-168">**ISignerCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)
</dt> <dt>

[<span data-ttu-id="c60e8-169">**IX509CertificateRequest**</span><span class="sxs-lookup"><span data-stu-id="c60e8-169">**IX509CertificateRequest**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)
</dt> <dt>

[<span data-ttu-id="c60e8-170">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="c60e8-170">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[<span data-ttu-id="c60e8-171">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="c60e8-171">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[<span data-ttu-id="c60e8-172">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="c60e8-172">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[<span data-ttu-id="c60e8-173">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="c60e8-173">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> <dt>

[<span data-ttu-id="c60e8-174">**IX509Enrollment**</span><span class="sxs-lookup"><span data-stu-id="c60e8-174">**IX509Enrollment**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

