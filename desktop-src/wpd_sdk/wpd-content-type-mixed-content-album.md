---
description: WPD \_ 內容 \_ 類型 \_ 混合式 \_ 內容 \_ 專輯
ms.assetid: 7b9d324c-8a9c-4764-9705-ea891e631ead
title: WPD_CONTENT_TYPE_MIXED_CONTENT_ALBUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14794282a58d4b5c1b74bccce34568deec780d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513868"
---
# <a name="wpd_content_type_mixed_content_album"></a><span data-ttu-id="825f3-103">WPD \_ 內容 \_ 類型 \_ 混合式 \_ 內容 \_ 專輯</span><span class="sxs-lookup"><span data-stu-id="825f3-103">WPD\_CONTENT\_TYPE\_MIXED\_CONTENT\_ALBUM</span></span>

<span data-ttu-id="825f3-104">將其類型描述為 WPD \_ 內容 \_ 類型 \_ 混合 \_ 內容專輯的物件 \_ 代表混合媒體物件的集合，例如音訊、影像和影片檔案。</span><span class="sxs-lookup"><span data-stu-id="825f3-104">An object that describes its type as WPD\_CONTENT\_TYPE\_MIXED\_CONTENT\_ALBUM represents a collection of mixed media objects, for example, audio, image, and video files.</span></span> <span data-ttu-id="825f3-105">混合的內容專輯在功能上相當於媒體檔案的播放清單，但可用來代表實體專輯給終端使用者。</span><span class="sxs-lookup"><span data-stu-id="825f3-105">A mixed content album is functionally equivalent to a playlist of media files, but is used to represent a physical album to the end user.</span></span>

<span data-ttu-id="825f3-106">這種類型的物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="825f3-106">This type of object supports the following properties.</span></span>



|                                                                                                                       |                                                                                |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="825f3-107">**屬性名稱**</span><span class="sxs-lookup"><span data-stu-id="825f3-107">**Property Name**</span></span>                                                                                                     | <span data-ttu-id="825f3-108">**必要或選擇性**</span><span class="sxs-lookup"><span data-stu-id="825f3-108">**Required or Optional**</span></span>                                                       |
| [<span data-ttu-id="825f3-109">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="825f3-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="825f3-110">必要、唯讀。</span><span class="sxs-lookup"><span data-stu-id="825f3-110">Required, read-only.</span></span> <span data-ttu-id="825f3-111">即使在建立時，用戶端也無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="825f3-111">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="825f3-112">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="825f3-112">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="825f3-113">必要。</span><span class="sxs-lookup"><span data-stu-id="825f3-113">Required.</span></span>                                                                      |
| [<span data-ttu-id="825f3-114">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="825f3-114">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="825f3-115">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="825f3-115">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="825f3-116">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="825f3-116">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="825f3-117">必要、唯讀。</span><span class="sxs-lookup"><span data-stu-id="825f3-117">Required, read-only.</span></span> <span data-ttu-id="825f3-118">即使在建立時，用戶端也無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="825f3-118">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="825f3-119">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="825f3-119">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="825f3-120">必要。</span><span class="sxs-lookup"><span data-stu-id="825f3-120">Required.</span></span>                                                                      |
| [<span data-ttu-id="825f3-121">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="825f3-121">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="825f3-122">必要。</span><span class="sxs-lookup"><span data-stu-id="825f3-122">Required.</span></span>                                                                      |
| [<span data-ttu-id="825f3-123">WPD \_ 物件 \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="825f3-123">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="825f3-124">如果物件是隱藏的，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="825f3-124">Required if the object is hidden.</span></span>                                              |
| [<span data-ttu-id="825f3-125">WPD \_ 物件 \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="825f3-125">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="825f3-126">如果物件為系統物件，則為必要項， (代表) 的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="825f3-126">Required if the object is a system object (represents a system file).</span></span>          |
| [<span data-ttu-id="825f3-127">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="825f3-127">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="825f3-128">如果物件至少有一個資源，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="825f3-128">Required if the object has at least one resource.</span></span>                              |
| [<span data-ttu-id="825f3-129">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="825f3-129">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="825f3-130">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="825f3-130">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="825f3-131">不可取用的 WPD \_ 物件 \_ \_</span><span class="sxs-lookup"><span data-stu-id="825f3-131">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="825f3-132">如果物件不打算供裝置取用，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="825f3-132">Recommended if the object is not meant for consumption by the device.</span></span>          |
| [<span data-ttu-id="825f3-133">WPD \_ 物件 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="825f3-133">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="825f3-134">如果物件具有其他物件的參考，則為必要。</span><span class="sxs-lookup"><span data-stu-id="825f3-134">Required if the object has references to other objects.</span></span>                        |
| [<span data-ttu-id="825f3-135">WPD \_ 物件 \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="825f3-135">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="825f3-136">選擇性。</span><span class="sxs-lookup"><span data-stu-id="825f3-136">Optional.</span></span>                                                                      |
| [<span data-ttu-id="825f3-137">WPD \_ 物件 \_ 同步 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="825f3-137">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="825f3-138">選擇性。</span><span class="sxs-lookup"><span data-stu-id="825f3-138">Optional.</span></span>                                                                      |
| [<span data-ttu-id="825f3-139">WPD \_ 物件 \_ 受到 \_ DRM \_ 保護</span><span class="sxs-lookup"><span data-stu-id="825f3-139">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="825f3-140">如果物件受到 DRM 技術的保護，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="825f3-140">Required if the object is protected by DRM technology.</span></span>                         |
| [<span data-ttu-id="825f3-141">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="825f3-141">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="825f3-142">選擇性。</span><span class="sxs-lookup"><span data-stu-id="825f3-142">Optional.</span></span>                                                                      |
| [<span data-ttu-id="825f3-143">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="825f3-143">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="825f3-144">建議使用。</span><span class="sxs-lookup"><span data-stu-id="825f3-144">Recommended.</span></span>                                                                   |
| [<span data-ttu-id="825f3-145">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="825f3-145">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="825f3-146">選擇性。</span><span class="sxs-lookup"><span data-stu-id="825f3-146">Optional.</span></span>                                                                      |
| [<span data-ttu-id="825f3-147">WPD \_ 物件 \_ 反向 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="825f3-147">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="825f3-148">如果物件是由另一個物件參考，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="825f3-148">Recommended if the object is referenced by another object.</span></span>                     |
| [<span data-ttu-id="825f3-149">WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="825f3-149">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="825f3-150">選擇性。</span><span class="sxs-lookup"><span data-stu-id="825f3-150">Optional.</span></span>                                                                      |
| [<span data-ttu-id="825f3-151">WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_</span><span class="sxs-lookup"><span data-stu-id="825f3-151">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="825f3-152">選擇性</span><span class="sxs-lookup"><span data-stu-id="825f3-152">Optional</span></span>                                                                       |
| [<span data-ttu-id="825f3-153">WPD \_ 物件 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="825f3-153">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="825f3-154">如果無法刪除物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="825f3-154">Required if the object cannot be deleted.</span></span>                                      |
| [<span data-ttu-id="825f3-155">WPD \_ 物件 \_ 語言 \_ 地區設定</span><span class="sxs-lookup"><span data-stu-id="825f3-155">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="825f3-156">選擇性。</span><span class="sxs-lookup"><span data-stu-id="825f3-156">Optional.</span></span>                                                                      |



 

## <a name="typical-resources"></a><span data-ttu-id="825f3-157">一般資源</span><span class="sxs-lookup"><span data-stu-id="825f3-157">Typical Resources</span></span>

<span data-ttu-id="825f3-158">這些物件通常不會裝載資源。</span><span class="sxs-lookup"><span data-stu-id="825f3-158">These objects typically do not host resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="825f3-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="825f3-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="825f3-160">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="825f3-160">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



