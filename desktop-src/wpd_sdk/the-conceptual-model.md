---
description: 概念模型
ms.assetid: f906466e-acdc-4d0f-bf27-c5a25dc56c01
title: 概念模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a17538e7fdb454fa8eb61ab951a3316b0f0c327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194249"
---
# <a name="the-conceptual-model"></a><span data-ttu-id="7017d-103">概念模型</span><span class="sxs-lookup"><span data-stu-id="7017d-103">The Conceptual Model</span></span>

<span data-ttu-id="7017d-104">本節說明構成 WPD 概念模型的物件、屬性和資源。</span><span class="sxs-lookup"><span data-stu-id="7017d-104">This section describes the objects, properties, and resources that constitute the WPD conceptual model.</span></span>

### <a name="objects"></a><span data-ttu-id="7017d-105">物件</span><span class="sxs-lookup"><span data-stu-id="7017d-105">Objects</span></span>

<span data-ttu-id="7017d-106">在 WPD 中，裝置上的邏輯實體稱為物件。</span><span class="sxs-lookup"><span data-stu-id="7017d-106">In WPD, logical entities on devices are referred to as objects.</span></span> <span data-ttu-id="7017d-107">通常（但不一定）表示裝置上的資料。</span><span class="sxs-lookup"><span data-stu-id="7017d-107">Typically, but not always, these represent data on the device.</span></span> <span data-ttu-id="7017d-108">物件具有屬性，並由物件識別碼參考。</span><span class="sxs-lookup"><span data-stu-id="7017d-108">Objects have properties, and are referenced by object identifiers.</span></span> <span data-ttu-id="7017d-109">物件的範例包括相機上的圖片和資料夾、媒體播放機上的歌曲和播放清單、行動電話上的連絡人等等。</span><span class="sxs-lookup"><span data-stu-id="7017d-109">Examples of objects include pictures and folders on a camera, songs and playlists on a media player, contacts on a mobile phone, and so on.</span></span>

<span data-ttu-id="7017d-110">物件也可以代表裝置的功能或資訊部分。</span><span class="sxs-lookup"><span data-stu-id="7017d-110">Objects can also represent functional or informational parts of the device.</span></span> <span data-ttu-id="7017d-111">這些範例包括 player 控制項 (播放/錄製/暫停) 、攝影機設定、行動電話的 SMS 功能等等。</span><span class="sxs-lookup"><span data-stu-id="7017d-111">Examples of these include player controls (play/record/pause), camera settings, a mobile phone's SMS capabilities, and so on.</span></span>

<span data-ttu-id="7017d-112">下列兩個主題提供兩種物件類型的範例和圖例： Image 物件和 Mediacast 物件。</span><span class="sxs-lookup"><span data-stu-id="7017d-112">The two following topics give examples and illustrations of two types of objects: the Image object and the Mediacast object.</span></span>

### <a name="image-object"></a><span data-ttu-id="7017d-113">Image 物件</span><span class="sxs-lookup"><span data-stu-id="7017d-113">Image Object</span></span>

<span data-ttu-id="7017d-114">影像物件代表靜止影像。</span><span class="sxs-lookup"><span data-stu-id="7017d-114">An image object represents a still image.</span></span> <span data-ttu-id="7017d-115">下圖顯示影像物件、其屬性和其資源之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="7017d-115">The following diagram shows the relationships between an Image object, its properties, and its resources.</span></span>

![顯示 wpd 物件及其屬性和資源關聯性的圖表](images/wpd-overview-figure2.gif)

<span data-ttu-id="7017d-117">如需影像物件和其屬性的詳細資訊，請參閱 [**WPD \_ 內容 \_ 類型 \_ 影像**](wpd-content-type-image.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="7017d-117">For more information about the Image object and its properties, see the [**WPD\_CONTENT\_TYPE\_IMAGE**](wpd-content-type-image.md) topic.</span></span>

### <a name="mediacast-object"></a><span data-ttu-id="7017d-118">Mediacast 物件</span><span class="sxs-lookup"><span data-stu-id="7017d-118">Mediacast Object</span></span>

<span data-ttu-id="7017d-119">Mediacast 物件可以視為將相關內容分組的容器物件，就像播放清單群組音樂一樣。</span><span class="sxs-lookup"><span data-stu-id="7017d-119">A Mediacast object can be thought of as a container object that groups related content, just as a playlist groups music.</span></span> <span data-ttu-id="7017d-120">通常，Mediacast 物件是用來將線上發佈的媒體內容分組。</span><span class="sxs-lookup"><span data-stu-id="7017d-120">Often, a Mediacast object is used to group media content that was published online.</span></span> <span data-ttu-id="7017d-121">例如，RSS 通道可以表示為 Mediacast 物件，其物件參考指向代表通道中每個專案的內容物件。</span><span class="sxs-lookup"><span data-stu-id="7017d-121">For example, an RSS channel can be represented as a Mediacast object whose object references point to content objects that represent each item in the channel.</span></span> <span data-ttu-id="7017d-122">下圖顯示 Mediacast 物件與其包含的三個音訊物件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="7017d-122">The following diagram shows the relationship between a Mediacast object and the three audio objects it contains.</span></span>

![顯示 medicast 物件的階層式結構以及其中包含的三個物件的圖表](images/mediacast1.gif)

<span data-ttu-id="7017d-124">音訊物件的參考是在 Mediacast 物件的 [WPD \_ 物件 \_ 參考](object-properties.md) 屬性中指定。</span><span class="sxs-lookup"><span data-stu-id="7017d-124">The references to the audio object are specified in the [WPD\_OBJECT\_REFERENCES](object-properties.md) property for the Mediacast object.</span></span> <span data-ttu-id="7017d-125">如需有關 Mediacast 物件所支援之屬性的詳細資訊，請參閱 [**WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換**](wpd-content-type-media-cast.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="7017d-125">For more information about the properties supported by a Mediacast object, see the [**WPD\_CONTENT\_TYPE\_MEDIA\_CAST**](wpd-content-type-media-cast.md) topic.</span></span>

### <a name="properties"></a><span data-ttu-id="7017d-126">屬性</span><span class="sxs-lookup"><span data-stu-id="7017d-126">Properties</span></span>

<span data-ttu-id="7017d-127">物件屬性提供交換物件描述中繼資料的機制。</span><span class="sxs-lookup"><span data-stu-id="7017d-127">Object properties provide a mechanism for exchanging object-describing metadata.</span></span> <span data-ttu-id="7017d-128">例如，影像物件可能會包含描述其檔案名、大小、格式、寬度（以圖元為單位）的屬性。</span><span class="sxs-lookup"><span data-stu-id="7017d-128">For example, an image object may include properties that describe its filename, size, format, width in pixels, and so on.</span></span>

<span data-ttu-id="7017d-129">屬性具有目前的值和屬性。</span><span class="sxs-lookup"><span data-stu-id="7017d-129">Properties have a current value, as well as attributes.</span></span> <span data-ttu-id="7017d-130">WPD 會定義一組組成 API 和 DDI 定義的標準屬性。</span><span class="sxs-lookup"><span data-stu-id="7017d-130">WPD defines a set of standard properties that make up the API and DDI definitions.</span></span> <span data-ttu-id="7017d-131">廠商不限於預先定義的 WPD 屬性，而且可以自由新增自己的屬性。</span><span class="sxs-lookup"><span data-stu-id="7017d-131">Vendors are not limited to the predefined WPD properties and are free to add their own.</span></span>

### <a name="property-attributes"></a><span data-ttu-id="7017d-132">Property 屬性</span><span class="sxs-lookup"><span data-stu-id="7017d-132">Property Attributes</span></span>

<span data-ttu-id="7017d-133">屬性屬性描述存取權限、有效值，以及與屬性相關的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="7017d-133">Property attributes describe the access rights, valid values, and other information related to a property.</span></span> <span data-ttu-id="7017d-134">例如，代表位元速率的屬性可以是每秒 8 kb 的範圍 (Kbps) 20 Kbps，且步驟值為 1 Kbps。</span><span class="sxs-lookup"><span data-stu-id="7017d-134">For example, the property representing bit rate could be a range from 8 kilobits per second (Kbps) to 20 Kbps with a step value of 1 Kbps.</span></span>

<span data-ttu-id="7017d-135">存取權限會指出呼叫端是否可以讀取、寫入及/或刪除屬性。</span><span class="sxs-lookup"><span data-stu-id="7017d-135">Access rights indicate whether callers can read, write and/or delete the property.</span></span> <span data-ttu-id="7017d-136">有效的值表示屬性值的限制。</span><span class="sxs-lookup"><span data-stu-id="7017d-136">Valid values indicate restrictions for property values.</span></span> <span data-ttu-id="7017d-137">有效的值會被視為特定的表單。</span><span class="sxs-lookup"><span data-stu-id="7017d-137">Valid values are said to be of a specific form.</span></span> <span data-ttu-id="7017d-138">有效的值表單包括範圍 (也就是，屬性可以從最小到最大值使用指定的步驟) 、列舉 (也就是，屬性值是指定清單) 中的其中一個值，而無 (表示沒有任何特定的有效值) 。</span><span class="sxs-lookup"><span data-stu-id="7017d-138">Valid value forms include Range (that is, property can take a value from Min to Max with specified Step), Enumeration (that is, property value is one of those in the specified List), and None (that is, there are no specific valid values).</span></span>

### <a name="resources"></a><span data-ttu-id="7017d-139">資源</span><span class="sxs-lookup"><span data-stu-id="7017d-139">Resources</span></span>

<span data-ttu-id="7017d-140">資源是二進位資料的預留位置。</span><span class="sxs-lookup"><span data-stu-id="7017d-140">Resources are placeholders for binary data.</span></span> <span data-ttu-id="7017d-141">物件可以有一個以上的資源。</span><span class="sxs-lookup"><span data-stu-id="7017d-141">An object can have more than one resource.</span></span> <span data-ttu-id="7017d-142">例如，如果物件代表具有音訊注釋的影像檔案，則此物件的資源可能如下所示：</span><span class="sxs-lookup"><span data-stu-id="7017d-142">For example, if the object represented an image file with an audio annotation, then the resources for this object might be as follows:</span></span>

-   <span data-ttu-id="7017d-143">預設資源。</span><span class="sxs-lookup"><span data-stu-id="7017d-143">A default resource.</span></span> <span data-ttu-id="7017d-144">此資源代表整個影像檔案。</span><span class="sxs-lookup"><span data-stu-id="7017d-144">This resource represents the entire image file.</span></span> <span data-ttu-id="7017d-145"> (這包括任何內嵌資料，例如音訊注釋、縮圖等) </span><span class="sxs-lookup"><span data-stu-id="7017d-145">(This includes any embedded data such as audio annotations, thumbnails, and so on)</span></span>
-   <span data-ttu-id="7017d-146">縮圖資源。</span><span class="sxs-lookup"><span data-stu-id="7017d-146">A thumbnail resource.</span></span> <span data-ttu-id="7017d-147">此資源代表影像的縮圖資料。</span><span class="sxs-lookup"><span data-stu-id="7017d-147">This resource represents the thumbnail data for the image.</span></span>
-   <span data-ttu-id="7017d-148">音訊注釋資源。</span><span class="sxs-lookup"><span data-stu-id="7017d-148">An audio annotation resource.</span></span> <span data-ttu-id="7017d-149">此資源代表與影像相關聯的音訊資料。</span><span class="sxs-lookup"><span data-stu-id="7017d-149">This resource represents the audio data associated with the image.</span></span>

### <a name="resource-attributes"></a><span data-ttu-id="7017d-150">資源屬性</span><span class="sxs-lookup"><span data-stu-id="7017d-150">Resource Attributes</span></span>

<span data-ttu-id="7017d-151">與屬性屬性類似，資源屬性會描述與資源相關的存取權限、大小、格式和其他資訊。</span><span class="sxs-lookup"><span data-stu-id="7017d-151">Similar to property attributes, resource attributes describe the access rights, size, format, and other information related to a resource.</span></span> <span data-ttu-id="7017d-152">例如，影像物件上之音訊注釋資源的屬性，可能會指定音訊的位元速率、通道計數和資料格式。</span><span class="sxs-lookup"><span data-stu-id="7017d-152">For example, the attributes for an audio annotation resource on an image object may specify the bit rate, channel count, and data format of the audio.</span></span>

### <a name="rendering-profiles-and-resource-attributes"></a><span data-ttu-id="7017d-153">轉譯設定檔和資源屬性</span><span class="sxs-lookup"><span data-stu-id="7017d-153">Rendering Profiles and Resource Attributes</span></span>

<span data-ttu-id="7017d-154">轉譯設定檔是應用程式用來探索指定資源之有效屬性的一種方法。</span><span class="sxs-lookup"><span data-stu-id="7017d-154">The rendering profile is one method that applications use to discover the valid attributes for a given resource.</span></span> <span data-ttu-id="7017d-155">例如，行動電話可能會支援點陣圖具有最小和最大寬度和高度值的特定限制。</span><span class="sxs-lookup"><span data-stu-id="7017d-155">For example, a mobile phone may support bitmaps with specific restrictions on the minimum and maximum width and height values.</span></span> <span data-ttu-id="7017d-156">藉由查詢 bitmap 物件的轉譯設定檔，應用程式可以取出這些確切的值。</span><span class="sxs-lookup"><span data-stu-id="7017d-156">By querying the rendering profiles for the bitmap object, an application can retrieve those exact values.</span></span>

<span data-ttu-id="7017d-157">下列範例輸出會識別裝置在支援點陣圖（最小高度為10圖元、最大寬度為20圖元、最大高度為1000圖元、最大寬度為2000圖元）時所傳回的轉譯設定檔資訊。</span><span class="sxs-lookup"><span data-stu-id="7017d-157">The following sample output identifies the rendering profile information that the device would return if it supported bitmaps with a minimum height of 10 pixels, a minimum width of 20 pixels, a maximum height of 1000 pixels and a maximum width of 2000 pixels.</span></span>


```C++
WPD_OBJECT_FORMAT = WPD_OBJECT_FORMAT_BMP
WPD_MEDIA_HEIGHT:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  10
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  10 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_MEDIA_WIDTH:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX =  2000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE = 0
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  2000 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
```



<span data-ttu-id="7017d-158">如需應用程式如何取得轉譯配置 (檔的說明，以及相關聯的資源屬性) 的說明，請參閱程式設計指南中的如何抓取 [裝置所支援的轉譯功能](retrieving-the-rendering-capabilities-supported-by-a-device.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="7017d-158">See the [Retrieving the Rendering Capabilities Supported by a Device](retrieving-the-rendering-capabilities-supported-by-a-device.md) topic in the programming guide for a description of how your application can retrieve a rendering profile (and the associated resource attributes).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7017d-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="7017d-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7017d-160">**應用程式總覽**</span><span class="sxs-lookup"><span data-stu-id="7017d-160">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



