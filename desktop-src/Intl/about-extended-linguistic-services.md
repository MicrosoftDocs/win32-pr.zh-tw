---
description: 擴充的語言服務 (ELS) 會實作為動態連結程式庫 (DLL) ，可針對應用程式所指定的文字提供各種語言支援功能。
ms.assetid: 23d4e42a-a5bb-467c-a8b9-6a57ae39daa0
title: 關於擴充的語言服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6594fcfe67954a56cb09e239221b2b529d4d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983753"
---
# <a name="about-extended-linguistic-services"></a><span data-ttu-id="50f06-103">關於擴充的語言服務</span><span class="sxs-lookup"><span data-stu-id="50f06-103">About Extended Linguistic Services</span></span>

<span data-ttu-id="50f06-104">擴充的語言服務 (ELS) 會實作為動態連結程式庫 (DLL) ，可針對應用程式所指定的文字提供各種語言支援功能。</span><span class="sxs-lookup"><span data-stu-id="50f06-104">Extended Linguistic Services (ELS) is implemented as a dynamic-link library (DLL) that provides a variety of linguistic support functionality for text that the application specifies.</span></span> <span data-ttu-id="50f06-105">這項技術包含了 ELS 平臺和外掛程式，可讓應用程式透過平臺存取數個預先定義的語言服務類型。</span><span class="sxs-lookup"><span data-stu-id="50f06-105">The technology includes the ELS platform and plug-ins for several predefined linguistic service types accessible to the application through the platform.</span></span>

> [!Note]  
> <span data-ttu-id="50f06-106">在 Windows 7 和更新版本中，會自動安裝 ELS 模組。</span><span class="sxs-lookup"><span data-stu-id="50f06-106">The ELS module is installed automatically with Windows 7 and later.</span></span>

 

## <a name="els-platform"></a><span data-ttu-id="50f06-107">ELS 平臺</span><span class="sxs-lookup"><span data-stu-id="50f06-107">ELS Platform</span></span>

<span data-ttu-id="50f06-108">ELS 平臺是您的應用程式和 ELS 服務之間的介面。</span><span class="sxs-lookup"><span data-stu-id="50f06-108">The ELS platform is the interface between your application and the ELS services.</span></span> <span data-ttu-id="50f06-109">它提供簡單的方法，讓您透過相同的 API 來執行數種語言功能，讓應用程式能夠存取及使用特定的服務。</span><span class="sxs-lookup"><span data-stu-id="50f06-109">It provides a simple way to implement several kinds of linguistic functionality through the same API, which allows the application to access and use specific services.</span></span> <span data-ttu-id="50f06-110">如需 API 的詳細資訊，請參閱 [擴充語言服務參考。](extended-linguistic-services-reference.md)</span><span class="sxs-lookup"><span data-stu-id="50f06-110">For more information about the API, see [Extended Linguistic Services Reference.](extended-linguistic-services-reference.md)</span></span>

> [!Note]  
> <span data-ttu-id="50f06-111">當應用程式呼叫任何的 ELS API 函式時，此平臺會視需要配置記憶體和資源，以便與服務通訊。</span><span class="sxs-lookup"><span data-stu-id="50f06-111">When the application calls any of the ELS API functions, the platform allocates memory and resources as needed for communication with the services.</span></span> <span data-ttu-id="50f06-112">應用程式會負責再次呼叫平臺以釋放這些資源。</span><span class="sxs-lookup"><span data-stu-id="50f06-112">The application is responsible for calling the platform again to free these resources.</span></span>

 

<span data-ttu-id="50f06-113">該平臺會在應用程式虛擬記憶體空間內部執行，而且所有配置的記憶體都是此空間的一部分。</span><span class="sxs-lookup"><span data-stu-id="50f06-113">The platform runs inside the application virtual memory space, and all allocated memory is part of this space.</span></span> <span data-ttu-id="50f06-114">因此，您的應用程式只需要連結至 Elscore 或動態載入 Elscore.dll，就可以連結至 ELS 元件 DLL (Elscore.dll) 。</span><span class="sxs-lookup"><span data-stu-id="50f06-114">Thus your application only needs to link to the ELS component DLL (Elscore.dll) by linking to Elscore.lib or by dynamically loading Elscore.dll.</span></span>

## <a name="els-services"></a><span data-ttu-id="50f06-115">ELS 服務</span><span class="sxs-lookup"><span data-stu-id="50f06-115">ELS Services</span></span>

<span data-ttu-id="50f06-116">針對 Windows 7 和更新版本，ELS 平臺僅支援下列預先定義的服務。</span><span class="sxs-lookup"><span data-stu-id="50f06-116">For Windows 7 and later, the ELS platform supports only the following predefined services.</span></span>

-   [<span data-ttu-id="50f06-117">Microsoft 語言偵測</span><span class="sxs-lookup"><span data-stu-id="50f06-117">Microsoft Language Detection</span></span>](microsoft-language-detection.md)
-   [<span data-ttu-id="50f06-118">Microsoft 腳本偵測</span><span class="sxs-lookup"><span data-stu-id="50f06-118">Microsoft Script Detection</span></span>](microsoft-script-detection.md)
-   [<span data-ttu-id="50f06-119">音譯服務</span><span class="sxs-lookup"><span data-stu-id="50f06-119">Transliteration services</span></span>](transliteration-services.md)

> [!Note]  
> <span data-ttu-id="50f06-120">未來的 ELS 版本將會支援 Microsoft 或服務提供者所提供的其他服務。</span><span class="sxs-lookup"><span data-stu-id="50f06-120">Future versions of ELS will support additional services provided by Microsoft or service providers.</span></span>

 

<span data-ttu-id="50f06-121">每項服務都與描述服務用途的服務類別相關聯。</span><span class="sxs-lookup"><span data-stu-id="50f06-121">Each service is associated with a service category describing what the service does.</span></span> <span data-ttu-id="50f06-122">類別目錄是以 nonlocalizable 字串表示。</span><span class="sxs-lookup"><span data-stu-id="50f06-122">The category is represented by a nonlocalizable string.</span></span> <span data-ttu-id="50f06-123">應用程式會使用它來列舉可用的服務。</span><span class="sxs-lookup"><span data-stu-id="50f06-123">It is used by applications to enumerate available services.</span></span> <span data-ttu-id="50f06-124">目前的服務類別為：</span><span class="sxs-lookup"><span data-stu-id="50f06-124">The current service categories are:</span></span>

-   <span data-ttu-id="50f06-125">"語言偵測"</span><span class="sxs-lookup"><span data-stu-id="50f06-125">"Language Detection"</span></span>
-   <span data-ttu-id="50f06-126">「腳本偵測」</span><span class="sxs-lookup"><span data-stu-id="50f06-126">"Script Detection"</span></span>
-   <span data-ttu-id="50f06-127">音譯</span><span class="sxs-lookup"><span data-stu-id="50f06-127">"Transliteration"</span></span>

<span data-ttu-id="50f06-128">平臺會使用服務中繼資料來列舉應用程式所要求的服務。</span><span class="sxs-lookup"><span data-stu-id="50f06-128">The platform uses service metadata to enumerate the services requested by the application.</span></span> <span data-ttu-id="50f06-129">服務全域唯一識別碼 (GUID) 、支援的輸入和輸出語言和腳本等屬性，以及應用程式可使用服務類別來列舉所需的 ELS 服務。</span><span class="sxs-lookup"><span data-stu-id="50f06-129">Properties such as the service globally unique identifier (GUID), supported input and output languages and scripts, and the service category can be used by the application to enumerate the desired ELS services.</span></span>

<span data-ttu-id="50f06-130">每個 ELS 服務都會實作為可安裝在作業系統上的 DLL 所支援的外掛程式，讓 ELS 平臺可以偵測和使用它。</span><span class="sxs-lookup"><span data-stu-id="50f06-130">Each ELS service is implemented as a plug-in supported by a DLL that can be installed on the operating system so that the ELS platform can detect and use it.</span></span> <span data-ttu-id="50f06-131">如有必要，服務可以公開自己的子服務。</span><span class="sxs-lookup"><span data-stu-id="50f06-131">Services can expose their own subservices, if required.</span></span>

## <a name="main-els-operations"></a><span data-ttu-id="50f06-132">主要的 ELS 作業</span><span class="sxs-lookup"><span data-stu-id="50f06-132">Main ELS Operations</span></span>

<span data-ttu-id="50f06-133">本節說明 ELS 平臺所支援的主要作業。</span><span class="sxs-lookup"><span data-stu-id="50f06-133">This section describes the main operations supported by the ELS platform.</span></span> <span data-ttu-id="50f06-134">平臺同時支援同步和非同步呼叫模式。</span><span class="sxs-lookup"><span data-stu-id="50f06-134">The platform supports both synchronous and asynchronous calling modes.</span></span> <span data-ttu-id="50f06-135">非同步呼叫模式會使用應用程式執行緒集區來排程處理要求的執行緒。</span><span class="sxs-lookup"><span data-stu-id="50f06-135">The asynchronous calling mode uses an application thread pool to schedule threads for processing requests.</span></span>

> [!Note]  
> <span data-ttu-id="50f06-136">因為此平臺支援非同步模式，所以 ELS 服務不需要自行執行這類的功能。</span><span class="sxs-lookup"><span data-stu-id="50f06-136">Since the platform supports an asynchronous mode, ELS services do not have to implement this type of functionality on their own.</span></span>

 

### <a name="service-enumeration"></a><span data-ttu-id="50f06-137">服務列舉</span><span class="sxs-lookup"><span data-stu-id="50f06-137">Service Enumeration</span></span>

<span data-ttu-id="50f06-138">ELS 平臺會載入和管理所有的 ELS 服務，讓應用程式透明地運作。</span><span class="sxs-lookup"><span data-stu-id="50f06-138">The ELS platform loads and manages all ELS services, making operation transparent to the application.</span></span> <span data-ttu-id="50f06-139">應用程式會藉由呼叫 [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)來列舉可用的服務。</span><span class="sxs-lookup"><span data-stu-id="50f06-139">The application enumerates the available services by calling [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices).</span></span> <span data-ttu-id="50f06-140">如需程式設計指示，請參閱 [列舉和釋放服務](enumerating-and-freeing-services.md)。</span><span class="sxs-lookup"><span data-stu-id="50f06-140">For programming instructions, see [Enumerating and Freeing Services](enumerating-and-freeing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="50f06-141">基於效能考慮，建議您讓應用程式只列舉可用服務一次。</span><span class="sxs-lookup"><span data-stu-id="50f06-141">It is advisable for performance reasons to have your application enumerate the available services only once.</span></span> <span data-ttu-id="50f06-142">ELS 平臺會再次檢查下一個列舉上的服務，以確保它的列舉結果一律是最新的。</span><span class="sxs-lookup"><span data-stu-id="50f06-142">The ELS platform checks the services again on the next enumeration to ensure that its enumeration results are always current.</span></span>

 

### <a name="text-recognition"></a><span data-ttu-id="50f06-143">文字辨識</span><span class="sxs-lookup"><span data-stu-id="50f06-143">Text Recognition</span></span>

<span data-ttu-id="50f06-144">在服務列舉之後，應用程式會呼叫 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 函數，以使用特定的 ELS 服務，將輸入文字的任何文字範圍對應至輸出文字。</span><span class="sxs-lookup"><span data-stu-id="50f06-144">After service enumeration, the application calls the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) function to use a particular ELS service to map any text range of input text to output text.</span></span> <span data-ttu-id="50f06-145">文字辨識的範例是使用語言偵測服務來接收文字區段，並偵測其最可能的語言。</span><span class="sxs-lookup"><span data-stu-id="50f06-145">An example of text recognition is the use of a language detection service that receives a text segment and detects its most probable language.</span></span>

<span data-ttu-id="50f06-146">在服務辨識出文字之後， [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 會傳回 [**對應 \_ 屬性 \_ 包**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) 結構，其中填入了服務所產生的輸出資料和屬性。</span><span class="sxs-lookup"><span data-stu-id="50f06-146">After the service has recognized the text, [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) returns with a [**MAPPING\_PROPERTY\_BAG**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) structure populated with output data and properties produced by the service.</span></span> <span data-ttu-id="50f06-147">為了避免記憶體流失，應用程式必須在每次 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)傳回 S OK 時呼叫 [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) ，以釋放屬性包 \_ 。</span><span class="sxs-lookup"><span data-stu-id="50f06-147">To avoid memory leaks, the application must free the property bag by calling [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) for each time that the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) returns S\_OK.</span></span> <span data-ttu-id="50f06-148">應用程式通常會在使用輸出資料完成時，或輸出資料不再相關時執行這項工作，因為文字的輸入區域已經過修改，例如編輯或刪除。</span><span class="sxs-lookup"><span data-stu-id="50f06-148">Usually the application does this either when it finishes using the output data or when the output data is no longer relevant because the input region of text has been modified, for example, edited or deleted.</span></span> <span data-ttu-id="50f06-149">釋放屬性包時， **MappingFreePropertyBag** 會傳回。</span><span class="sxs-lookup"><span data-stu-id="50f06-149">When the property bag is released, **MappingFreePropertyBag** returns.</span></span>

<span data-ttu-id="50f06-150">文字辨識的程式設計指示是在 [要求文字](requesting-text-recognition.md)辨識中提供。</span><span class="sxs-lookup"><span data-stu-id="50f06-150">Programming instructions for text recognition are provided in [Requesting Text Recognition](requesting-text-recognition.md).</span></span>

### <a name="service-termination"></a><span data-ttu-id="50f06-151">服務終止</span><span class="sxs-lookup"><span data-stu-id="50f06-151">Service Termination</span></span>

<span data-ttu-id="50f06-152">當您的應用程式不再需要 ELS 服務時，它會在結束之前呼叫 [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) 。</span><span class="sxs-lookup"><span data-stu-id="50f06-152">When your application no longer requires ELS services, it calls [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) before it terminates.</span></span> <span data-ttu-id="50f06-153">如需詳細資訊，請參閱 [列舉和釋放服務](enumerating-and-freeing-services.md)。</span><span class="sxs-lookup"><span data-stu-id="50f06-153">For more information, see [Enumerating and Freeing Services](enumerating-and-freeing-services.md).</span></span>

### <a name="versioning"></a><span data-ttu-id="50f06-154">版本控制</span><span class="sxs-lookup"><span data-stu-id="50f06-154">Versioning</span></span>

<span data-ttu-id="50f06-155">未來的 ELS 版本將允許更新 ELS 服務。</span><span class="sxs-lookup"><span data-stu-id="50f06-155">Future versions of ELS will allow the ELS services to be updated.</span></span> <span data-ttu-id="50f06-156">應用程式將能夠檢查 [**對應 \_ 服務 \_ 資訊**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) 結構的版本號碼，以偵測服務中的任何變更。</span><span class="sxs-lookup"><span data-stu-id="50f06-156">The application will be able to check the version numbers of the [**MAPPING\_SERVICE\_INFO**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) structure to detect any changes in the services.</span></span>

> [!Note]  
> <span data-ttu-id="50f06-157">您的 ELS 應用程式不應假設相同服務的不同版本可以完全取得相同的結果。</span><span class="sxs-lookup"><span data-stu-id="50f06-157">Your ELS application should not make the assumption that different versions of the same service can retrieve exactly the same results.</span></span>

 

 

 



