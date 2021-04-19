---
title: 媒體物件
description: 媒體物件提供使用下列屬性和方法來指定或取出媒體專案屬性的方法。
ms.assetid: 45c1c760-808b-4d11-8e6b-057a2ca685d0
keywords:
- 媒體物件 Windows Media Player
topic_type:
- apiref
api_name:
- Media Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88eff6ee0a97e63df6a0c073ef18425cbb576e85
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106969081"
---
# <a name="media-object"></a><span data-ttu-id="6d94f-104">媒體物件</span><span class="sxs-lookup"><span data-stu-id="6d94f-104">Media Object</span></span>

<span data-ttu-id="6d94f-105">**媒體** 物件提供使用下列屬性和方法來指定或取出媒體專案屬性的方法。</span><span class="sxs-lookup"><span data-stu-id="6d94f-105">The **Media** object provides a way to specify or retrieve properties of a media item, using the following properties and methods.</span></span>

<span data-ttu-id="6d94f-106">**媒體** 物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="6d94f-106">The **Media** object supports the following properties.</span></span>



| <span data-ttu-id="6d94f-107">屬性</span><span class="sxs-lookup"><span data-stu-id="6d94f-107">Property</span></span>                                         | <span data-ttu-id="6d94f-108">描述</span><span class="sxs-lookup"><span data-stu-id="6d94f-108">Description</span></span>                                                                                        |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d94f-109">attributeCount</span><span class="sxs-lookup"><span data-stu-id="6d94f-109">attributeCount</span></span>](media-attributecount.md)       | <span data-ttu-id="6d94f-110">抓取可針對媒體專案查詢及/或設定的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="6d94f-110">Retrieves the number of attributes that can be queried and/or set for the media item.</span></span>              |
| [<span data-ttu-id="6d94f-111">duration</span><span class="sxs-lookup"><span data-stu-id="6d94f-111">duration</span></span>](media-duration.md)                   | <span data-ttu-id="6d94f-112">抓取目前媒體專案的持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6d94f-112">Retrieves the duration in seconds of the current media item.</span></span>                                       |
| [<span data-ttu-id="6d94f-113">durationString</span><span class="sxs-lookup"><span data-stu-id="6d94f-113">durationString</span></span>](media-durationstring.md)       | <span data-ttu-id="6d94f-114">抓取 **字串** 值，指出目前媒體專案的持續時間（以 HH： MM： SS 格式表示）。</span><span class="sxs-lookup"><span data-stu-id="6d94f-114">Retrieves a **String** value indicating the duration of the current media item in HH:MM:SS format.</span></span> |
| [<span data-ttu-id="6d94f-115">error</span><span class="sxs-lookup"><span data-stu-id="6d94f-115">error</span></span>](media-error.md)                         | <span data-ttu-id="6d94f-116">如果媒體專案有錯誤條件，則抓取 [ErrorItem](erroritem-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="6d94f-116">Retrieves an [ErrorItem](erroritem-object.md) object if the media item has an error condition.</span></span>    |
| [<span data-ttu-id="6d94f-117">imageSourceHeight</span><span class="sxs-lookup"><span data-stu-id="6d94f-117">imageSourceHeight</span></span>](media-imagesourceheight.md) | <span data-ttu-id="6d94f-118">抓取目前媒體專案的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="6d94f-118">Retrieves the height of the current media item in pixels.</span></span>                                          |
| [<span data-ttu-id="6d94f-119">imageSourceWidth</span><span class="sxs-lookup"><span data-stu-id="6d94f-119">imageSourceWidth</span></span>](media-imagesourcewidth.md)   | <span data-ttu-id="6d94f-120">抓取目前媒體專案的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="6d94f-120">Retrieves the width of the current media item in pixels.</span></span>                                           |
| [<span data-ttu-id="6d94f-121">markerCount</span><span class="sxs-lookup"><span data-stu-id="6d94f-121">markerCount</span></span>](media-markercount.md)             | <span data-ttu-id="6d94f-122">捕獲媒體專案中的標記數目。</span><span class="sxs-lookup"><span data-stu-id="6d94f-122">Retrieves the number of markers in the media item.</span></span>                                                 |
| [<span data-ttu-id="6d94f-123">name</span><span class="sxs-lookup"><span data-stu-id="6d94f-123">name</span></span>](media-name.md)                           | <span data-ttu-id="6d94f-124">指定或抓取媒體專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d94f-124">Specifies or retrieves the name of the media item.</span></span>                                                 |
| [<span data-ttu-id="6d94f-125">sourceURL</span><span class="sxs-lookup"><span data-stu-id="6d94f-125">sourceURL</span></span>](media-sourceurl.md)                 | <span data-ttu-id="6d94f-126">抓取媒體專案的 URL。</span><span class="sxs-lookup"><span data-stu-id="6d94f-126">Retrieves the URL of the media item.</span></span>                                                               |



 

<span data-ttu-id="6d94f-127">**媒體** 物件支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="6d94f-127">The **Media** object supports the following methods.</span></span>



| <span data-ttu-id="6d94f-128">方法</span><span class="sxs-lookup"><span data-stu-id="6d94f-128">Method</span></span>                                                       | <span data-ttu-id="6d94f-129">描述</span><span class="sxs-lookup"><span data-stu-id="6d94f-129">Description</span></span>                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d94f-130">getAttributeCountByType</span><span class="sxs-lookup"><span data-stu-id="6d94f-130">getAttributeCountByType</span></span>](media-getattributecountbytype.md) | <span data-ttu-id="6d94f-131">抓取與指定的屬性名稱和語言相關聯的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="6d94f-131">Retrieves the number of attributes associated with the specified attribute name and language.</span></span>            |
| [<span data-ttu-id="6d94f-132">getAttributeName</span><span class="sxs-lookup"><span data-stu-id="6d94f-132">getAttributeName</span></span>](media-getattributename.md)               | <span data-ttu-id="6d94f-133">抓取對應于指定索引之屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d94f-133">Retrieves the name of the attribute corresponding to the specified index.</span></span>                                |
| [<span data-ttu-id="6d94f-134">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="6d94f-134">getItemInfo</span></span>](media-getiteminfo.md)                         | <span data-ttu-id="6d94f-135">抓取媒體專案的指定屬性值。</span><span class="sxs-lookup"><span data-stu-id="6d94f-135">Retrieves the value of the specified attribute for the media item.</span></span>                                       |
| [<span data-ttu-id="6d94f-136">getItemInfoByAtom</span><span class="sxs-lookup"><span data-stu-id="6d94f-136">getItemInfoByAtom</span></span>](media-getiteminfobyatom.md)             | <span data-ttu-id="6d94f-137">抓取具有指定之索引編號的屬性值。</span><span class="sxs-lookup"><span data-stu-id="6d94f-137">Retrieves the value of the attribute with the specified index number.</span></span>                                    |
| [<span data-ttu-id="6d94f-138">getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="6d94f-138">getItemInfoByType</span></span>](media-getiteminfobytype.md)             | <span data-ttu-id="6d94f-139">抓取對應于指定屬性名稱、語言和索引的屬性值。</span><span class="sxs-lookup"><span data-stu-id="6d94f-139">Retrieves the value of the attribute corresponding to the specified attribute name, language, and index.</span></span> |
| [<span data-ttu-id="6d94f-140">getMarkerName</span><span class="sxs-lookup"><span data-stu-id="6d94f-140">getMarkerName</span></span>](media-getmarkername.md)                     | <span data-ttu-id="6d94f-141">抓取位於指定之索引處的標記名稱。</span><span class="sxs-lookup"><span data-stu-id="6d94f-141">Retrieves the name of the marker at the specified index.</span></span>                                                 |
| [<span data-ttu-id="6d94f-142">getMarkerTime</span><span class="sxs-lookup"><span data-stu-id="6d94f-142">getMarkerTime</span></span>](media-getmarkertime.md)                     | <span data-ttu-id="6d94f-143">抓取位於指定索引處之標記的時間。</span><span class="sxs-lookup"><span data-stu-id="6d94f-143">Retrieves the time of the marker at the specified index.</span></span>                                                 |
| [<span data-ttu-id="6d94f-144">isIdentical</span><span class="sxs-lookup"><span data-stu-id="6d94f-144">isIdentical</span></span>](media-isidentical.md)                         | <span data-ttu-id="6d94f-145">抓取值，指出提供的物件是否與目前的物件相同。</span><span class="sxs-lookup"><span data-stu-id="6d94f-145">Retrieves a value indicating whether the supplied object is the same as the current one.</span></span>                 |
| [<span data-ttu-id="6d94f-146">isMemberOf</span><span class="sxs-lookup"><span data-stu-id="6d94f-146">isMemberOf</span></span>](media-ismemberof.md)                           | <span data-ttu-id="6d94f-147">抓取值，指出指定的媒體專案是否為指定播放清單的成員。</span><span class="sxs-lookup"><span data-stu-id="6d94f-147">Retrieves a value indicating whether the specified media item is a member of the specified playlist.</span></span>     |
| [<span data-ttu-id="6d94f-148">isReadOnlyItem</span><span class="sxs-lookup"><span data-stu-id="6d94f-148">isReadOnlyItem</span></span>](media-isreadonlyitem.md)                   | <span data-ttu-id="6d94f-149">抓取值，指出是否可以編輯指定之媒體專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="6d94f-149">Retrieves a value indicating whether the attributes of the specified media item can be edited.</span></span>           |
| [<span data-ttu-id="6d94f-150">setItemInfo</span><span class="sxs-lookup"><span data-stu-id="6d94f-150">setItemInfo</span></span>](media-setiteminfo.md)                         | <span data-ttu-id="6d94f-151">設定媒體專案的指定屬性值。</span><span class="sxs-lookup"><span data-stu-id="6d94f-151">Sets the value of the specified attribute for the media item.</span></span>                                            |



 

<span data-ttu-id="6d94f-152">**媒體** 物件可透過下列屬性和方法來存取。</span><span class="sxs-lookup"><span data-stu-id="6d94f-152">The **Media** object is accessed through the following properties and methods.</span></span>



| <span data-ttu-id="6d94f-153">Object</span><span class="sxs-lookup"><span data-stu-id="6d94f-153">Object</span></span>                          | <span data-ttu-id="6d94f-154">屬性或方法</span><span class="sxs-lookup"><span data-stu-id="6d94f-154">Property or method</span></span>                                                       |
|---------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="6d94f-155">控制項</span><span class="sxs-lookup"><span data-stu-id="6d94f-155">Controls</span></span>](controls-object.md) | [<span data-ttu-id="6d94f-156">currentItem</span><span class="sxs-lookup"><span data-stu-id="6d94f-156">currentItem</span></span>](controls-currentitem.md)                                  |
| [<span data-ttu-id="6d94f-157">球員</span><span class="sxs-lookup"><span data-stu-id="6d94f-157">Player</span></span>](player-object.md)     | <span data-ttu-id="6d94f-158">[currentMedia](player-currentmedia.md)、 [newMedia](player-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="6d94f-158">[currentMedia](player-currentmedia.md), [newMedia](player-newmedia.md)</span></span> |
| [<span data-ttu-id="6d94f-159">播放 清單</span><span class="sxs-lookup"><span data-stu-id="6d94f-159">Playlist</span></span>](playlist-object.md) | [<span data-ttu-id="6d94f-160">item</span><span class="sxs-lookup"><span data-stu-id="6d94f-160">item</span></span>](playlist-item.md)                                                |



 

<span data-ttu-id="6d94f-161">因為這是最常見的存取方式，也就是 *播放機*。**currentMedia** 是用於參考語法區段中的說明用途。</span><span class="sxs-lookup"><span data-stu-id="6d94f-161">Because it is the most common means of access, *player*.**currentMedia** is used for purposes of illustration in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d94f-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d94f-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d94f-163">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="6d94f-163">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




