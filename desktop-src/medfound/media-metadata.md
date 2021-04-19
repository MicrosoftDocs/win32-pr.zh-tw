---
description: 媒體中繼資料
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: 媒體中繼資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb17f286673663976e17b4178239507765c2101
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106975600"
---
# <a name="media-metadata"></a><span data-ttu-id="5c82f-103">媒體中繼資料</span><span class="sxs-lookup"><span data-stu-id="5c82f-103">Media Metadata</span></span>

<span data-ttu-id="5c82f-104">媒體檔案包含描述檔案內容的屬性。</span><span class="sxs-lookup"><span data-stu-id="5c82f-104">Media files contain properties that describe the contents of the file.</span></span> <span data-ttu-id="5c82f-105">在 Microsoft 媒體基礎中，這些屬性可以分類如下：</span><span class="sxs-lookup"><span data-stu-id="5c82f-105">In Microsoft Media Foundation, these properties can be categorized as follows:</span></span>

-   <span data-ttu-id="5c82f-106">**媒體類型屬性** 會指定編碼參數，例如編碼演算法 (媒體子類型) 、影片框架大小、影片畫面播放速率、音訊位元速率和音訊取樣率。</span><span class="sxs-lookup"><span data-stu-id="5c82f-106">**Media-type attributes** specify the encoding parameters, such as the encoding algorithm (media subtype), video frame size, video frame rate, audio bit rate, and audio sample rate.</span></span> <span data-ttu-id="5c82f-107">如需媒體類型屬性的詳細資訊，請參閱 [媒體類型](media-types.md)。</span><span class="sxs-lookup"><span data-stu-id="5c82f-107">For more information about media-type attributes, see [Media Types](media-types.md).</span></span>
-   <span data-ttu-id="5c82f-108">**中繼資料** 包含媒體內容的描述性資訊，例如標題、演出者、編輯器和內容類型。</span><span class="sxs-lookup"><span data-stu-id="5c82f-108">**Metadata** contains descriptive information for the media content, such as title, artist, composer, and genre.</span></span> <span data-ttu-id="5c82f-109">中繼資料也可以描述編碼參數。</span><span class="sxs-lookup"><span data-stu-id="5c82f-109">Metadata can also describe encoding parameters.</span></span> <span data-ttu-id="5c82f-110">透過中繼資料存取此資訊的速度，會比透過媒體類型屬性更快。</span><span class="sxs-lookup"><span data-stu-id="5c82f-110">It can be faster to access this information through metadata than through media-type attributes.</span></span>
-   <span data-ttu-id="5c82f-111">**DRM 屬性** 包含使用限制的資訊。</span><span class="sxs-lookup"><span data-stu-id="5c82f-111">**DRM properties** contain information on usage restrictions.</span></span> <span data-ttu-id="5c82f-112">目前媒體基礎不支援透過中繼資料的 DRM 屬性，但 **PKEY \_ DRM \_ IsProtected** 屬性除外。</span><span class="sxs-lookup"><span data-stu-id="5c82f-112">Currently Media Foundation does not support DRM properties through metadata, with the exception of the **PKEY\_DRM\_IsProtected** property.</span></span>

<span data-ttu-id="5c82f-113">有兩種方式可以在媒體基礎中讀取中繼資料：</span><span class="sxs-lookup"><span data-stu-id="5c82f-113">There are two ways to read metadata in Media Foundation:</span></span>

-   <span data-ttu-id="5c82f-114">[**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)介面 (媒體基礎第1版中繼資料) 。</span><span class="sxs-lookup"><span data-stu-id="5c82f-114">The [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface (Media Foundation version 1 metadata).</span></span>
-   <span data-ttu-id="5c82f-115">Windows Shell [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面 (Shell 中繼資料) 。</span><span class="sxs-lookup"><span data-stu-id="5c82f-115">The Windows Shell [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface (Shell metadata).</span></span>

<span data-ttu-id="5c82f-116">Shell 中繼資料不只會與媒體檔案相關，而是在系統上的檔案範圍更廣。</span><span class="sxs-lookup"><span data-stu-id="5c82f-116">Shell metadata pertains not only to media files but to a much wider range of files on the system.</span></span>

<span data-ttu-id="5c82f-117">下表比較每個中繼資料 API 的功能和限制。</span><span class="sxs-lookup"><span data-stu-id="5c82f-117">The following table compares the features and limitations of each metadata API.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c82f-118">媒體基礎 v1 中繼資料</span><span class="sxs-lookup"><span data-stu-id="5c82f-118">Media Foundation v1 Metadata</span></span></th>
<th><span data-ttu-id="5c82f-119">Shell 中繼資料</span><span class="sxs-lookup"><span data-stu-id="5c82f-119">Shell Metadata</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c82f-120">需要 Windows Vista 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="5c82f-120">Requires Windows Vista or later.</span></span></td>
<td><span data-ttu-id="5c82f-121">需要 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="5c82f-121">Requires Windows 7.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5c82f-122">一般而言，Shell 中繼資料不需要 Windows 7，但是媒體基礎不支援 Windows 7 之前的 Shell 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5c82f-122">Shell metadata in general does not require Windows 7, but Media Foundation did not support Shell metadata prior to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c82f-123">屬性與 Shell 屬性系統不相容。</span><span class="sxs-lookup"><span data-stu-id="5c82f-123">Properties are not compatible with Shell property system.</span></span></td>
<td><span data-ttu-id="5c82f-124">屬性與 Shell 屬性系統相容。</span><span class="sxs-lookup"><span data-stu-id="5c82f-124">Properties are compatible with the Shell property system.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c82f-125">屬性可套用至整個檔案，或在資料流程層級套用。</span><span class="sxs-lookup"><span data-stu-id="5c82f-125">Properties can apply to the entire file, or at the stream level.</span></span></td>
<td><span data-ttu-id="5c82f-126">僅支援檔案層級的屬性。</span><span class="sxs-lookup"><span data-stu-id="5c82f-126">Only file-level properties are supported.</span></span> <span data-ttu-id="5c82f-127">不支援資料流程層級屬性。</span><span class="sxs-lookup"><span data-stu-id="5c82f-127">Stream-level properties are not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c82f-128">屬性可以有多種語言的值。</span><span class="sxs-lookup"><span data-stu-id="5c82f-128">Properties can have values in multiple languages.</span></span></td>
<td><span data-ttu-id="5c82f-129">不支援多種語言的值。</span><span class="sxs-lookup"><span data-stu-id="5c82f-129">Values in multiple languages are not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c82f-130">屬性索引鍵是寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="5c82f-130">Property keys are wide-character strings.</span></span></td>
<td><span data-ttu-id="5c82f-131">屬性索引鍵是 <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> 值。</span><span class="sxs-lookup"><span data-stu-id="5c82f-131">Property keys are <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c82f-132">屬性值為 <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> 值。</span><span class="sxs-lookup"><span data-stu-id="5c82f-132">Property values are <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> values.</span></span></td>
<td><span data-ttu-id="5c82f-133">屬性值為 <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> 值。</span><span class="sxs-lookup"><span data-stu-id="5c82f-133">Property values are <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> values.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="in-this-section"></a><span data-ttu-id="5c82f-134">本節內容</span><span class="sxs-lookup"><span data-stu-id="5c82f-134">In this section</span></span>



| <span data-ttu-id="5c82f-135">主題</span><span class="sxs-lookup"><span data-stu-id="5c82f-135">Topic</span></span>                                                                                     | <span data-ttu-id="5c82f-136">描述</span><span class="sxs-lookup"><span data-stu-id="5c82f-136">Description</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c82f-137">Shell 中繼資料提供者</span><span class="sxs-lookup"><span data-stu-id="5c82f-137">Shell Metadata Providers</span></span>](shell-metadata-providers.md)<br/>                       | <span data-ttu-id="5c82f-138">從 Windows 7 開始，媒體基礎會透過 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面公開中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5c82f-138">Starting in Windows 7, Media Foundation exposes metadata through the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span><br/> |
| [<span data-ttu-id="5c82f-139">媒體檔案的中繼資料屬性</span><span class="sxs-lookup"><span data-stu-id="5c82f-139">Metadata Properties for Media Files</span></span>](metadata-properties-for-media-files.md)<br/> | <span data-ttu-id="5c82f-140">本主題列出媒體檔案最常見的中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="5c82f-140">This topic lists the most common metadata properties for media files.</span></span><br/>                                                           |
| [<span data-ttu-id="5c82f-141">Windows Vista 中的中繼資料提供者</span><span class="sxs-lookup"><span data-stu-id="5c82f-141">Metadata Providers in Windows Vista</span></span>](metadata-providers-in-windows-vista.md)<br/> | <span data-ttu-id="5c82f-142">在 Windows Vista 中，媒體基礎會透過 [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) 介面公開中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5c82f-142">In Windows Vista, Media Foundation exposes metadata through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span><br/>                   |



 

<span data-ttu-id="5c82f-143">如果您正在執行自訂媒體來源，並且想要公開 Shell 中繼資料，請參閱 [自訂媒體檔案的中繼資料提供者](custom-metadata-providers-for-media-files.md)。</span><span class="sxs-lookup"><span data-stu-id="5c82f-143">If you are implementing a custom media source and want to expose Shell metadata, see [Custom Metadata Providers for Media Files](custom-metadata-providers-for-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c82f-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c82f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c82f-145">媒體基礎程式設計指南</span><span class="sxs-lookup"><span data-stu-id="5c82f-145">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 
