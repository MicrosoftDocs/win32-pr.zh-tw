---
title: 中繼資料匯入
description: WWSAPI 包含的 API 元素可用來處理端點的 WSDL 和原則，其目標為解壓縮可用於與端點通訊的資訊。
ms.assetid: 77738bf1-ef8b-4fd6-a36a-43f1932868dd
keywords:
- 適用于 Windows 的中繼資料匯入 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c36ffdf9bcbf0d63bdef473cc52cd4d545e5a3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103684280"
---
# <a name="metadata-import"></a><span data-ttu-id="e7e22-106">中繼資料匯入</span><span class="sxs-lookup"><span data-stu-id="e7e22-106">Metadata Import</span></span>

<span data-ttu-id="e7e22-107">WWSAPI 包含的 API 元素可用來處理端點的 WSDL 和原則，其目標為解壓縮可用於與端點通訊的資訊。</span><span class="sxs-lookup"><span data-stu-id="e7e22-107">The WWSAPI includes API elements that can be used to process WSDL and Policy from an endpoint with the goal of extracting information that can be used to communicate with the endpoint.</span></span> <span data-ttu-id="e7e22-108">當端點所支援的通訊協定尚未已知時，通常會使用這些 Api。</span><span class="sxs-lookup"><span data-stu-id="e7e22-108">These APIs are typically used when the communication protocol supported by the endpoint is not already known.</span></span>


<span data-ttu-id="e7e22-109">使用下列順序來處理中繼資料：</span><span class="sxs-lookup"><span data-stu-id="e7e22-109">Use the following sequence to process metadata:</span></span>

``` syntax
WsCreateMetadata    // create a metadata object

while there are metadata documents to add
{
    // retrieve the metadata document from it's location
    // (download, read from file, etc)

    // add the document to the metadata object
    WsReadMetadata

    // optionally query the metadata object for any missing documents
    WsGetMissingMetadataDocumentAddress?
}

// get the endpoints from the metadata object
WsGetMetadataEndpoints

for each endpoint
{            
    // examine the endpoint information to see if 
    // the endpoint is relevant for the particular scenario

    if the endpoint is relevant
    {
        // get the policy object from the endpoint

        // get the number of policy alternatives in the policy
        WsGetPolicyAlternativeCount

        for each policy alternative
        {
            // construct a policy constraints structure that specifies
            // what policy is acceptable and what information to extract
            // from the policy

            // see if the policy alternative matches the constraints
            WsMatchPolicyAlternative

            // if there is a match, then use it

            // if there is not a match, then it is also possible to 
            // try with a different constraint structure
        }
    }
}

// If reusing the metadata object for a different set of documents
WsResetMetadata? // reset metadata object, which removes all documents

WsFreeMetadata // free the metadata object
```

<span data-ttu-id="e7e22-110">如需 WSDL 和 WS-Policy 判斷提示如何對應至 API 的詳細資訊，請參閱 [中繼資料](metadata-mapping.md) 對應主題。</span><span class="sxs-lookup"><span data-stu-id="e7e22-110">for information about how WSDL and WS-Policy assertions correspond to the API, see the [Metadata Mapping](metadata-mapping.md) topic.</span></span>

## <a name="security"></a><span data-ttu-id="e7e22-111">安全性</span><span class="sxs-lookup"><span data-stu-id="e7e22-111">Security</span></span>

<span data-ttu-id="e7e22-112">下載的中繼資料只會與用來下載的位址一樣好。</span><span class="sxs-lookup"><span data-stu-id="e7e22-112">The metadata downloaded is only as good as the address used to download it.</span></span> <span data-ttu-id="e7e22-113">應用程式應該確保信任位址。</span><span class="sxs-lookup"><span data-stu-id="e7e22-113">An application should ensure that is trusts the address.</span></span> <span data-ttu-id="e7e22-114">此外，應用程式應該確保它使用安全性通訊協定來下載不允許篡改中繼資料的元資料檔案。</span><span class="sxs-lookup"><span data-stu-id="e7e22-114">Also, an application should ensure that it uses a security protocol to download the metadata documents that does not allow tampering with the metadata.</span></span>

<span data-ttu-id="e7e22-115">應用程式應該檢查中繼資料所公開的服務位址。</span><span class="sxs-lookup"><span data-stu-id="e7e22-115">An application should inspect the addresses of the services exposed by the metadata.</span></span> <span data-ttu-id="e7e22-116">依預設，執行時間會確保服務的主機名稱符合用來下載中繼資料的原始 URL，但應用程式可能會想要執行額外的檢查。</span><span class="sxs-lookup"><span data-stu-id="e7e22-116">By default, the runtime ensures that the host name of the service matches that of the original URL used to download the metadata, but the application may want to perform additional checks.</span></span> <span data-ttu-id="e7e22-117">應用程式可以覆寫 [**WS \_ 中繼資料 \_ 屬性 [ \_ 驗證 \_ 主機 \_ 名**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) ] 屬性，以停用主機名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="e7e22-117">An application can disable the host name verification by overwriting [**WS\_METADATA\_PROPERTY\_VERIFY\_HOST\_NAMES**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) property.</span></span> <span data-ttu-id="e7e22-118">如果預設已停用的主機名稱檢查已停用，應用程式就必須針對包含服務位址的元資料檔案，保護它本身不信任的不同合作物件。</span><span class="sxs-lookup"><span data-stu-id="e7e22-118">If the hostname check that is done by default is disabled, the application will need to protect itself against the metadata documents containing the address of a service from a different party that it does not trust in some other way.</span></span>

<span data-ttu-id="e7e22-119">根據預設，中繼資料執行時間用來還原序列化和處理中繼資料的最大記憶體數量為256k，而且可能加入的檔數目上限為32。</span><span class="sxs-lookup"><span data-stu-id="e7e22-119">By default, the maximum amount of memory used by the metadata runtime to deserialize and process the metadata is 256k, and the maximum number of documents that may be added is 32.</span></span> <span data-ttu-id="e7e22-120">這些預設值可由 [**ws \_ 中繼資料 \_ 屬性 \_ 堆積要求 \_ 的 \_ 大小**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) 和 **ws \_ 中繼資料 \_ 屬性的 \_ 最大 \_ 檔** 屬性覆寫。</span><span class="sxs-lookup"><span data-stu-id="e7e22-120">These default values can be overwritten by [**WS\_METADATA\_PROPERTY\_HEAP\_REQUESTED\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) and **WS\_METADATA\_PROPERTY\_MAX\_DOCUMENTS** properties.</span></span> <span data-ttu-id="e7e22-121">這些界限是設計用來限制下載數量，並限制為了累積中繼資料所配置的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="e7e22-121">These bounds are designed to limit the amount of downloads and limit the amount of memory allocated in order to accumulate the metadata.</span></span> <span data-ttu-id="e7e22-122">增加這些值可能會導致記憶體使用量過高、CPU 使用量或網路頻寬耗用量。</span><span class="sxs-lookup"><span data-stu-id="e7e22-122">Increasing these values may lead to excessive memory usage, CPU usage, or network bandwidth consumption.</span></span> <span data-ttu-id="e7e22-123">請注意，由於會以二進位格式擴充字典字串，因此小型訊息可能會導致更大的還原序列化格式，因此依賴小型訊息來限制中繼資料記憶體配置在使用二進位格式時並不夠。</span><span class="sxs-lookup"><span data-stu-id="e7e22-123">Note that due to expansion of dictionary strings in the binary format, a small message may lead to a much larger deserialized form, so relying on small messages to limit metadata memory allocation is not sufficient when using the binary format.</span></span>

<span data-ttu-id="e7e22-124">根據預設，原則替代專案的最大數目是32，不過可以透過 [**WS \_ 原則屬性的 \_ \_ 最大 \_ 替代**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) 專案屬性來覆寫。</span><span class="sxs-lookup"><span data-stu-id="e7e22-124">By default, the maximum number of policy alternatives is 32, though it can be overwritten by [**WS\_POLICY\_PROPERTY\_MAX\_ALTERNATIVES**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) property.</span></span> <span data-ttu-id="e7e22-125">如果應用程式在尋找相符專案的每個替代專案之間進行迴圈，則可能需要在尋找相符專案之前，先搜尋所有替代專案。</span><span class="sxs-lookup"><span data-stu-id="e7e22-125">If an application loops through each alternative looking for a match, it may need to search all alternatives before finding a match.</span></span> <span data-ttu-id="e7e22-126">增加最大的替代專案數目可能會導致 CPU 使用率過高。</span><span class="sxs-lookup"><span data-stu-id="e7e22-126">Increasing the maximum number of alternatives may lead to excessive CPU utilization.</span></span>

<span data-ttu-id="e7e22-127">下列列舉是中繼資料匯入的一部分：</span><span class="sxs-lookup"><span data-stu-id="e7e22-127">The following enumerations are part of metadata import:</span></span>

-   [<span data-ttu-id="e7e22-128">**WS \_ 中繼資料 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="e7e22-128">**WS\_METADATA\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id)
-   [<span data-ttu-id="e7e22-129">**WS \_ 中繼資料 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="e7e22-129">**WS\_METADATA\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_state)
-   [<span data-ttu-id="e7e22-130">**WS \_ 原則 \_ 延伸 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="e7e22-130">**WS\_POLICY\_EXTENSION\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_extension_type)
-   [<span data-ttu-id="e7e22-131">**WS \_ 原則 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="e7e22-131">**WS\_POLICY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id)
-   [<span data-ttu-id="e7e22-132">**WS \_ 原則 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="e7e22-132">**WS\_POLICY\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_state)
-   [<span data-ttu-id="e7e22-133">**WS \_ 安全性系結 \_ \_ 條件約束 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="e7e22-133">**WS\_SECURITY\_BINDING\_CONSTRAINT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_constraint_type)

<span data-ttu-id="e7e22-134">下列函數是中繼資料匯入的一部分：</span><span class="sxs-lookup"><span data-stu-id="e7e22-134">The following functions are part of metadata import:</span></span>

-   [<span data-ttu-id="e7e22-135">**WsCreateMetadata**</span><span class="sxs-lookup"><span data-stu-id="e7e22-135">**WsCreateMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatemetadata)
-   [<span data-ttu-id="e7e22-136">**WsFreeMetadata**</span><span class="sxs-lookup"><span data-stu-id="e7e22-136">**WsFreeMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreemetadata)
-   [<span data-ttu-id="e7e22-137">**WsGetMetadataEndpoints**</span><span class="sxs-lookup"><span data-stu-id="e7e22-137">**WsGetMetadataEndpoints**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataendpoints)
-   [<span data-ttu-id="e7e22-138">**WsGetMetadataProperty**</span><span class="sxs-lookup"><span data-stu-id="e7e22-138">**WsGetMetadataProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataproperty)
-   [<span data-ttu-id="e7e22-139">**WsGetMissingMetadataDocumentAddress**</span><span class="sxs-lookup"><span data-stu-id="e7e22-139">**WsGetMissingMetadataDocumentAddress**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmissingmetadatadocumentaddress)
-   [<span data-ttu-id="e7e22-140">**WsGetPolicyAlternativeCount**</span><span class="sxs-lookup"><span data-stu-id="e7e22-140">**WsGetPolicyAlternativeCount**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyalternativecount)
-   [<span data-ttu-id="e7e22-141">**WsGetPolicyProperty**</span><span class="sxs-lookup"><span data-stu-id="e7e22-141">**WsGetPolicyProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyproperty)
-   [<span data-ttu-id="e7e22-142">**WsMatchPolicyAlternative**</span><span class="sxs-lookup"><span data-stu-id="e7e22-142">**WsMatchPolicyAlternative**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmatchpolicyalternative)
-   [<span data-ttu-id="e7e22-143">**WsReadMetadata**</span><span class="sxs-lookup"><span data-stu-id="e7e22-143">**WsReadMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadmetadata)
-   [<span data-ttu-id="e7e22-144">**WsResetMetadata**</span><span class="sxs-lookup"><span data-stu-id="e7e22-144">**WsResetMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetmetadata)

<span data-ttu-id="e7e22-145">下列控制碼是中繼資料匯入的一部分：</span><span class="sxs-lookup"><span data-stu-id="e7e22-145">The following handles are part of metadata import:</span></span>

-   [<span data-ttu-id="e7e22-146">WS \_ 中繼資料</span><span class="sxs-lookup"><span data-stu-id="e7e22-146">WS\_METADATA</span></span>](ws-metadata.md)
-   [<span data-ttu-id="e7e22-147">WS \_ 原則</span><span class="sxs-lookup"><span data-stu-id="e7e22-147">WS\_POLICY</span></span>](ws-policy.md)

<span data-ttu-id="e7e22-148">下列結構是中繼資料匯入的一部分：</span><span class="sxs-lookup"><span data-stu-id="e7e22-148">The following structures are part of metadata import:</span></span>

-   [<span data-ttu-id="e7e22-149">**WS \_ CERT \_ MESSAGE \_ SECURITY \_ BINDING \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="e7e22-149">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="e7e22-150">**WS \_ 通道 \_ 屬性 \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="e7e22-150">**WS\_CHANNEL\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property_constraint)
-   [<span data-ttu-id="e7e22-151">**WS \_ 端點 \_ 原則 \_ 擴充功能**</span><span class="sxs-lookup"><span data-stu-id="e7e22-151">**WS\_ENDPOINT\_POLICY\_EXTENSION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_policy_extension)
-   [<span data-ttu-id="e7e22-152">**WS \_ HTTP \_ 標頭 \_ 驗證安全性系結 \_ \_ \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="e7e22-152">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)
-   [<span data-ttu-id="e7e22-153">**WS \_ 發出的 \_ 權杖 \_ 訊息安全性系結 \_ \_ \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="e7e22-153">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)
-   [<span data-ttu-id="e7e22-154">**WS \_ KERBEROS \_ APREQ \_ MESSAGE \_ SECURITY \_ BINDING \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="e7e22-154">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="e7e22-155">**WS \_ 中繼資料 \_ 端點**</span><span class="sxs-lookup"><span data-stu-id="e7e22-155">**WS\_METADATA\_ENDPOINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoint)
-   [<span data-ttu-id="e7e22-156">**WS \_ 中繼資料 \_ 端點**</span><span class="sxs-lookup"><span data-stu-id="e7e22-156">**WS\_METADATA\_ENDPOINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoints)
-   [<span data-ttu-id="e7e22-157">**WS \_ 中繼資料 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="e7e22-157">**WS\_METADATA\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_property)
-   [<span data-ttu-id="e7e22-158">**WS \_ 原則 \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="e7e22-158">**WS\_POLICY\_CONSTRAINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_constraints)
-   [<span data-ttu-id="e7e22-159">**WS \_ 原則 \_ 延伸**</span><span class="sxs-lookup"><span data-stu-id="e7e22-159">**WS\_POLICY\_EXTENSION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_extension)
-   [<span data-ttu-id="e7e22-160">**WS \_ 原則 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="e7e22-160">**WS\_POLICY\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_properties)
-   [<span data-ttu-id="e7e22-161">**WS \_ 原則 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="e7e22-161">**WS\_POLICY\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_property)
-   [<span data-ttu-id="e7e22-162">**WS \_ 要求 \_ 安全性 \_ 權杖 \_ 屬性 \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="e7e22-162">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint)
-   [<span data-ttu-id="e7e22-163">**WS \_ 安全性系結 \_ \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="e7e22-163">**WS\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_constraint)
-   [<span data-ttu-id="e7e22-164">**WS \_ 安全性系結 \_ \_ 屬性 \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="e7e22-164">**WS\_SECURITY\_BINDING\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property_constraint)
-   [<span data-ttu-id="e7e22-165">**WS \_ 安全性 \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="e7e22-165">**WS\_SECURITY\_CONSTRAINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_constraints)
-   [<span data-ttu-id="e7e22-166">**WS \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性系結 \_ \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="e7e22-166">**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)
-   [<span data-ttu-id="e7e22-167">**WS \_ 安全性 \_ 屬性 \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="e7e22-167">**WS\_SECURITY\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_property_constraint)
-   [<span data-ttu-id="e7e22-168">**WS \_ SSL \_ 傳輸 \_ 安全性系結 \_ \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="e7e22-168">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)
-   [<span data-ttu-id="e7e22-169">**WS \_ TCP \_ SSPI \_ 傳輸 \_ 安全性系結 \_ \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="e7e22-169">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)
-   [<span data-ttu-id="e7e22-170">**WS 使用者 \_ 名稱 \_ 訊息安全性系結 \_ \_ \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="e7e22-170">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)

 

 




