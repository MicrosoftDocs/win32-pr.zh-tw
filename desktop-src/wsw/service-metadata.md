---
title: 服務中繼資料
description: WWSAPI 服務主機支援其端點的 WS-MetadataExchange。
ms.assetid: 5a6feb34-7fff-4000-b3be-63112b22905a
keywords:
- 服務中繼資料原生-Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebf15614ac9e89a4e08fdd19102492d0121e65d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463948"
---
# <a name="service-metadata"></a><span data-ttu-id="473dd-106">服務中繼資料</span><span class="sxs-lookup"><span data-stu-id="473dd-106">Service Metadata</span></span>

<span data-ttu-id="473dd-107">WWSAPI 服務主機支援其端點的 WS-MetadataExchange。</span><span class="sxs-lookup"><span data-stu-id="473dd-107">The WWSAPI service host supports WS-MetadataExchange for its endpoints.</span></span> <span data-ttu-id="473dd-108">您可以使用下列步驟，在服務主機上啟用這類中繼資料交換：</span><span class="sxs-lookup"><span data-stu-id="473dd-108">You enable such metadata exchange on the service host with the following steps:</span></span>

-   <span data-ttu-id="473dd-109">在 [ws 服務 \_ \_ 主機](ws-service-host.md)的 [**ws \_ 服務 \_ 中繼資料**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)屬性中指定元資料檔案。</span><span class="sxs-lookup"><span data-stu-id="473dd-109">Specify metadata documents in the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) property on the [WS\_SERVICE\_HOST](ws-service-host.md).</span></span>
-   <span data-ttu-id="473dd-110">在 [ws 服務 \_ \_ 主機](ws-service-host.md)的 [**ws \_ 服務 \_ 中繼資料**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)屬性中指定服務名稱。</span><span class="sxs-lookup"><span data-stu-id="473dd-110">Specify the service name in the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) property on the [WS\_SERVICE\_HOST](ws-service-host.md).</span></span>
-   <span data-ttu-id="473dd-111">使用 [**ws \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)上的 [**ws \_ 服務 \_ 端點 \_ 屬性 \_ 中繼資料**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)屬性來指定個別端點的埠。</span><span class="sxs-lookup"><span data-stu-id="473dd-111">Specify the port for individual endpoints by using the [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) property on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>
-   <span data-ttu-id="473dd-112">啟用一或多個 [**WS \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) 結構來服務 WS-MetadataExchange 要求。</span><span class="sxs-lookup"><span data-stu-id="473dd-112">Enable one or more [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structures to service the WS-MetadataExchange requests.</span></span>
-   <span data-ttu-id="473dd-113">（選擇性）在 [**ws \_ 服務 \_ 端點 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)列舉中指定 **ws \_ 服務 \_ 端點 \_ 屬性 \_ 中繼資料 \_ 交換 \_ URL \_ 尾碼**，以提供特定位址的服務 Ws-MetadataExchange 要求。</span><span class="sxs-lookup"><span data-stu-id="473dd-113">Optionally, specify **WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA\_EXCHANGE\_URL\_SUFFIX** in the [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) enumeration for servicing Ws-MetadataExchange requests on a specific address.</span></span>


<span data-ttu-id="473dd-114">在服務主機上指定元資料檔案/服務名稱</span><span class="sxs-lookup"><span data-stu-id="473dd-114">Specifying Metadata documents / Service name on the Service Host</span></span>

<span data-ttu-id="473dd-115">第一個步驟是在服務主機上指定元資料檔案。</span><span class="sxs-lookup"><span data-stu-id="473dd-115">The first step is to specify the metadata documents on the service host.</span></span> <span data-ttu-id="473dd-116">做法是將個別檔收集為 WS \_ XML \_ 字串 \* 的陣列。</span><span class="sxs-lookup"><span data-stu-id="473dd-116">Do this by gathering the individual documents as an array of WS\_XML\_STRING\*'s.</span></span> <span data-ttu-id="473dd-117">這些字串可以是 XML 架構、WSDL 或 WS-Policy 檔。</span><span class="sxs-lookup"><span data-stu-id="473dd-117">These strings can be XML Schema, WSDL or WS-Policy document.</span></span> <span data-ttu-id="473dd-118">這是透過 [**WS \_ 服務 \_ 屬性 \_ 中繼資料**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="473dd-118">This is specified through the [**WS\_SERVICE\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property.</span></span>

<span data-ttu-id="473dd-119">或者，應用程式也可以將服務名稱和命名空間指定為 [**WS \_ 服務 \_ 中繼資料**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)的一部分。</span><span class="sxs-lookup"><span data-stu-id="473dd-119">Optionally, an application can also specify the service name and namespace as part of the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata).</span></span> <span data-ttu-id="473dd-120">如果元資料檔案未指定指定服務名稱的服務專案，服務模型會使用服務的對應 WSDL 埠來產生服務元素。</span><span class="sxs-lookup"><span data-stu-id="473dd-120">If the metadata document does not specify the service element for the given service name, the service model will generate a service element with the corresponding WSDL ports for the service.</span></span>

``` syntax
WS_SERVICE_METADATA_DOCUMENT document = {0};
WS_STRING documentName = WS_STRING_VALUE(L&quot;a.wsdl&quot;);
document.name = &documentName;
document.content = &wsdlDocument
WS_SERVICE_METADATA_DOCUMENT** metadataDocuments [] = {&document};
WS_SERVICE_METADATA serviceMetadata = {0};
// Specify Metadata documents
serviceMetadata.count = WsCountOf(metadataDocuments);
serviceMetadata.documents = &metadataDocuments;
// Specify service name
serviceMetadata.serviceName = &serviceName;
serviceMetadata.serviceNs = &serviceNamespace;


WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_METADATA;
serviceProperties[0].value =  &serviceMetadata;
serviceProperties[0].ValueSize = sizeof(serviceMetadata);
```

<span data-ttu-id="473dd-121">請注意，不會對檔執行個別元資料檔案的驗證。</span><span class="sxs-lookup"><span data-stu-id="473dd-121">Note that no verification of the individual metadata documents will be performed on the documents.</span></span> <span data-ttu-id="473dd-122">應用程式必須負責驗證檔的內容，並確保所有的匯入路徑都是相對指定的。</span><span class="sxs-lookup"><span data-stu-id="473dd-122">It is the responsiblity of the application to validate contents of the documents and ensure that all the imports paths are relatively specified.</span></span>

<span data-ttu-id="473dd-123">指定的命名空間是用來尋找服務主機將在其中新增服務專案的檔。</span><span class="sxs-lookup"><span data-stu-id="473dd-123">The namespace specified is used to locate the document in which the service element will be added by the service host.</span></span>

<span data-ttu-id="473dd-124">將服務元素新增至 WSDL 檔案</span><span class="sxs-lookup"><span data-stu-id="473dd-124">Addition of service element to the WSDL document</span></span>

<span data-ttu-id="473dd-125">服務主機會為應用程式提供應用程式的功能，以代表尚未指定的服務元素。</span><span class="sxs-lookup"><span data-stu-id="473dd-125">The service host provides facility for the application to add a service element on its behalf if one is not already specified.</span></span> <span data-ttu-id="473dd-126">為了啟用此行為，應用程式必須在 [**WS \_ 服務 \_ 中繼資料**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) 結構上指定 serivceName 和 serviceNs 欄位。</span><span class="sxs-lookup"><span data-stu-id="473dd-126">In order to enable this behavior an application must specify serivceName and serviceNs fields on the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) structure.</span></span> <span data-ttu-id="473dd-127">如果 serviceName 和 serviceNs 都是 **Null** ，則不會將任何服務專案新增至 WSDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="473dd-127">If serviceName and serviceNs are both **NULL** no service element is added to the WSDL document.</span></span> <span data-ttu-id="473dd-128">這兩種方式都用來識別要加入 serviceElement 的檔。</span><span class="sxs-lookup"><span data-stu-id="473dd-128">Both these are used to identify document in which the serviceElement is going to be added.</span></span>

<span data-ttu-id="473dd-129">如果未指定 [**WS \_ SERVICE \_ PROPERTY \_ METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) 屬性，就不會在服務主機上進行中繼資料 exhange。</span><span class="sxs-lookup"><span data-stu-id="473dd-129">If [**WS\_SERVICE\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property is not specified no metadata exhange will take place on the service host.</span></span>

<span data-ttu-id="473dd-130">指定 WS \_ 服務端點上的埠 \_</span><span class="sxs-lookup"><span data-stu-id="473dd-130">Specifying the port on the WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="473dd-131">若要讓 [**WS \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) 可作為 WSDL 檔案中 SERVICE 元素內的埠，應用程式必須在其上指定 [**ws \_ service \_ endpoint \_ property \_ METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) 屬性。</span><span class="sxs-lookup"><span data-stu-id="473dd-131">For a [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) to be available as a port inside the service element in the WSDL document, the application must specify [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) property on it.</span></span>

``` syntax
WS_SERVICE_ENDPOINT_METADATA endpointPort = {0}
endpointPort.name = &portName;
endpointPort.bindingName = &bindingName;
endpointPort.bindingNs = &bindingNs;

WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA;
serviceProperties[0].value =  &endpointPort;
serviceProperties[0].valueSize = sizeof(endpointPort);
```

<span data-ttu-id="473dd-132">假設系結名稱和命名空間的參考存在於服務主機上指定的檔中，做為 WS \_ 服務 \_ 屬性 \_ 中繼資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="473dd-132">It is assumed that the reference to the binding name and namespace exists in the documents specified on the service host as part of WS\_SERVICE\_PROPERTY\_METADATA.</span></span> <span data-ttu-id="473dd-133">執行時間不會代表應用程式進行驗證。</span><span class="sxs-lookup"><span data-stu-id="473dd-133">The runtime does not verify this on behalf of the application.</span></span>

<span data-ttu-id="473dd-134">在 WS \_ 服務端點上啟用 WS-MetadataExchange 服務 \_</span><span class="sxs-lookup"><span data-stu-id="473dd-134">Enable WS-MetadataExchange servicing on WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="473dd-135">為了服務 WS-MetadataExchange 要求，服務主機必須至少有一個端點啟用服務 WS-MetadataExchange 要求。</span><span class="sxs-lookup"><span data-stu-id="473dd-135">In order to service WS-MetadataExchange requests,the service host must have at least one endpoint enabled for servicing WS-MetadataExchange requests.</span></span> <span data-ttu-id="473dd-136">這是藉由為 [**WS \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)上的 WS-MetadataExchange 設定適當的版本來完成。</span><span class="sxs-lookup"><span data-stu-id="473dd-136">This is done by setting the appropriate version for WS-MetadataExchange on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_MEX;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

<span data-ttu-id="473dd-137">在 WS \_ 服務端點上啟用 HTTP GET 服務 \_</span><span class="sxs-lookup"><span data-stu-id="473dd-137">Enable HTTP GET servicing on WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="473dd-138">為了 serviceHTTP GET 要求，服務主機必須至少有一個端點啟用服務 WS-MetadataExchange 要求。</span><span class="sxs-lookup"><span data-stu-id="473dd-138">In order to serviceHTTP GET requests, the service host must have at least one endpoint enabled for servicing WS-MetadataExchange requests.</span></span> <span data-ttu-id="473dd-139">這是藉由為 [**WS \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)上的 WS-MetadataExchange 設定適當的版本來完成。</span><span class="sxs-lookup"><span data-stu-id="473dd-139">This is done by setting the appropriate version for WS-MetadataExchange on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_HTTP_GET;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

<span data-ttu-id="473dd-140">指定 Ws-MetadataExchange 要求的 URL 尾碼</span><span class="sxs-lookup"><span data-stu-id="473dd-140">Specifying URL suffix for Ws-MetadataExchange requests</span></span>

<span data-ttu-id="473dd-141">應用程式可以選擇性地只允許在特定路徑上接受 WS-MetadataExchange 的要求。</span><span class="sxs-lookup"><span data-stu-id="473dd-141">An application can optionally enable only accepting requests for WS-MetadataExchange on a specific path.</span></span> <span data-ttu-id="473dd-142">這是藉由為指定的 WS 服務端點指定尾碼來完成 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="473dd-142">This is done by specifying a suffix for the given WS\_SERVICE\_ENDPOINT.</span></span> <span data-ttu-id="473dd-143">此後綴會依原樣串連至 WS 服務端點的實際 URL \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="473dd-143">This suffix is concatenated as-is to the actual URL for the WS\_SERVICE\_ENDPOINT.</span></span> <span data-ttu-id="473dd-144">串連的字串會用來作為所收到的 ' to ' 標頭的相符 URL。</span><span class="sxs-lookup"><span data-stu-id="473dd-144">The concatenated string is used as the matching URL to the 'to' header received.</span></span>

``` syntax
const WS_STRING suffix = WS_STRING_VALUE(L&quot;mex&quot;);
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX;
serviceProperties[0].value =  &suffix;
serviceProperties[0].valueSize = sizeof(suffix);
```

<span data-ttu-id="473dd-145">下列 API 元素與服務中繼資料相關。</span><span class="sxs-lookup"><span data-stu-id="473dd-145">The following API elements relate to service metada.</span></span>

| <span data-ttu-id="473dd-146">列舉型別</span><span class="sxs-lookup"><span data-stu-id="473dd-146">Enumeration</span></span>                                                       | <span data-ttu-id="473dd-147">描述</span><span class="sxs-lookup"><span data-stu-id="473dd-147">Description</span></span>                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="473dd-148">**WS \_ 中繼資料 \_ 交換 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="473dd-148">**WS\_METADATA\_EXCHANGE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_exchange_type) | <span data-ttu-id="473dd-149">啟用或停用端點上的 WS-MetadataExchange 和 HTTP GET 服務。</span><span class="sxs-lookup"><span data-stu-id="473dd-149">Enables or disables WS-MetadataExchange and HTTP GET servicing on the endpoint.</span></span> |



 



| <span data-ttu-id="473dd-150">結構</span><span class="sxs-lookup"><span data-stu-id="473dd-150">Structure</span></span>                                                               | <span data-ttu-id="473dd-151">Description</span><span class="sxs-lookup"><span data-stu-id="473dd-151">Description</span></span>                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="473dd-152">**WS \_ 服務 \_ 端點 \_ 中繼資料**</span><span class="sxs-lookup"><span data-stu-id="473dd-152">**WS\_SERVICE\_ENDPOINT\_METADATA**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_metadata) | <span data-ttu-id="473dd-153">表示端點的通訊埠元素。</span><span class="sxs-lookup"><span data-stu-id="473dd-153">Represents the port element for the endpoint.</span></span>                         |
| [<span data-ttu-id="473dd-154">**WS \_ 服務 \_ 中繼資料**</span><span class="sxs-lookup"><span data-stu-id="473dd-154">**WS\_SERVICE\_METADATA**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)                    | <span data-ttu-id="473dd-155">指定服務元資料檔案陣列。</span><span class="sxs-lookup"><span data-stu-id="473dd-155">Specifies the service metadata documents array.</span></span>                       |
| [<span data-ttu-id="473dd-156">**WS \_ 服務 \_ 中繼資料 \_ 檔**</span><span class="sxs-lookup"><span data-stu-id="473dd-156">**WS\_SERVICE\_METADATA\_DOCUMENT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata_document) | <span data-ttu-id="473dd-157">指定組成服務中繼資料的個別檔。</span><span class="sxs-lookup"><span data-stu-id="473dd-157">Specifies the individual documents that make up the service metadata.</span></span> |



 

 

 




