---
description: WPD \_ 內容 \_ 類型 \_ 影像 \_ 專輯
ms.assetid: e2ae9f89-5a71-4443-b0c1-81e4c650e1bb
title: WPD_CONTENT_TYPE_IMAGE_ALBUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67a20f6a6628008e31b23a0ceb05fee4931793a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975230"
---
# <a name="wpd_content_type_image_album"></a><span data-ttu-id="0937c-103">WPD \_ 內容 \_ 類型 \_ 影像 \_ 專輯</span><span class="sxs-lookup"><span data-stu-id="0937c-103">WPD\_CONTENT\_TYPE\_IMAGE\_ALBUM</span></span>

<span data-ttu-id="0937c-104">將其型別描述為 WPD \_ 內容 \_ 類型影像專輯的物件 \_ \_ 代表一組靜止影像。</span><span class="sxs-lookup"><span data-stu-id="0937c-104">An object that describes its type as WPD\_CONTENT\_TYPE\_IMAGE\_ALBUM represents a collection of still images.</span></span> <span data-ttu-id="0937c-105">影像專輯在功能上相當於影像檔案的播放清單，但是用來代表使用者的實體相片專輯。</span><span class="sxs-lookup"><span data-stu-id="0937c-105">An image album is functionally equivalent to a playlist of image files, but is used to represent a physical photo album to the end user.</span></span>

<span data-ttu-id="0937c-106">這種類型的物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="0937c-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="0937c-107">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="0937c-107">Property Name</span></span>                                                                                                         | <span data-ttu-id="0937c-108">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="0937c-108">Required or Optional</span></span>                                                              |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="0937c-109">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="0937c-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="0937c-110">必要、唯讀。</span><span class="sxs-lookup"><span data-stu-id="0937c-110">Required, read-only.</span></span> <span data-ttu-id="0937c-111">即使在建立時，用戶端也無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0937c-111">A client cannot set this property, even at creation time.</span></span>    |
| [<span data-ttu-id="0937c-112">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="0937c-112">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="0937c-113">必要。</span><span class="sxs-lookup"><span data-stu-id="0937c-113">Required.</span></span>                                                                         |
| [<span data-ttu-id="0937c-114">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="0937c-114">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="0937c-115">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="0937c-115">Required if the object represents a file.</span></span>                                         |
| [<span data-ttu-id="0937c-116">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="0937c-116">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="0937c-117">必要、唯讀。</span><span class="sxs-lookup"><span data-stu-id="0937c-117">Required, read-only.</span></span> <span data-ttu-id="0937c-118">即使在建立時，用戶端也無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0937c-118">A client cannot set this property even at creation time.</span></span>     |
| [<span data-ttu-id="0937c-119">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="0937c-119">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="0937c-120">必要。</span><span class="sxs-lookup"><span data-stu-id="0937c-120">Required.</span></span>                                                                         |
| [<span data-ttu-id="0937c-121">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="0937c-121">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="0937c-122">必要。</span><span class="sxs-lookup"><span data-stu-id="0937c-122">Required.</span></span>                                                                         |
| [<span data-ttu-id="0937c-123">WPD \_ 物件 \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="0937c-123">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="0937c-124">如果物件是隱藏的，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="0937c-124">Required if the object is hidden.</span></span>                                                 |
| [<span data-ttu-id="0937c-125">WPD \_ 物件 \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="0937c-125">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="0937c-126">如果物件為系統物件，則為必要項， (亦即，它代表) 的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="0937c-126">Required if the object is a system object (that is, it represents a system file).</span></span> |
| [<span data-ttu-id="0937c-127">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="0937c-127">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="0937c-128">如果物件至少有一個資源，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="0937c-128">Required if the object has at least one resource.</span></span>                                 |
| [<span data-ttu-id="0937c-129">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="0937c-129">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="0937c-130">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="0937c-130">Required if the object represents a file.</span></span>                                         |
| [<span data-ttu-id="0937c-131">不可取用的 WPD \_ 物件 \_ \_</span><span class="sxs-lookup"><span data-stu-id="0937c-131">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="0937c-132">如果物件不打算供裝置取用，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="0937c-132">Recommended if the object is not meant for consumption by the device.</span></span>             |
| [<span data-ttu-id="0937c-133">WPD \_ 物件 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="0937c-133">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="0937c-134">如果物件具有其他物件的參考，則為必要。</span><span class="sxs-lookup"><span data-stu-id="0937c-134">Required if the object has references to other objects.</span></span>                           |
| [<span data-ttu-id="0937c-135">WPD \_ 物件 \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="0937c-135">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="0937c-136">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0937c-136">Optional.</span></span>                                                                         |
| [<span data-ttu-id="0937c-137">WPD \_ 物件 \_ 同步 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="0937c-137">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="0937c-138">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0937c-138">Optional.</span></span>                                                                         |
| [<span data-ttu-id="0937c-139">WPD \_ 物件 \_ 受到 \_ DRM \_ 保護</span><span class="sxs-lookup"><span data-stu-id="0937c-139">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="0937c-140">如果物件受到 DRM 技術的保護，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="0937c-140">Required if the object is protected by DRM technology.</span></span>                            |
| [<span data-ttu-id="0937c-141">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="0937c-141">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="0937c-142">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0937c-142">Optional.</span></span>                                                                         |
| [<span data-ttu-id="0937c-143">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="0937c-143">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="0937c-144">建議使用。</span><span class="sxs-lookup"><span data-stu-id="0937c-144">Recommended.</span></span>                                                                      |
| [<span data-ttu-id="0937c-145">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="0937c-145">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="0937c-146">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0937c-146">Optional.</span></span>                                                                         |
| [<span data-ttu-id="0937c-147">WPD \_ 物件 \_ 反向 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="0937c-147">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="0937c-148">如果物件是由另一個物件參考，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="0937c-148">Recommended if the object is referenced by another object.</span></span>                        |
| [<span data-ttu-id="0937c-149">WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="0937c-149">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="0937c-150">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0937c-150">Optional.</span></span>                                                                         |
| [<span data-ttu-id="0937c-151">WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_</span><span class="sxs-lookup"><span data-stu-id="0937c-151">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="0937c-152">選擇性</span><span class="sxs-lookup"><span data-stu-id="0937c-152">Optional</span></span>                                                                          |
| [<span data-ttu-id="0937c-153">WPD \_ 物件 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="0937c-153">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="0937c-154">如果無法刪除物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="0937c-154">Required if the object cannot be deleted.</span></span>                                         |
| [<span data-ttu-id="0937c-155">WPD \_ 物件 \_ 語言 \_ 地區設定</span><span class="sxs-lookup"><span data-stu-id="0937c-155">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="0937c-156">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0937c-156">Optional.</span></span>                                                                         |



 

## <a name="typical-resources"></a><span data-ttu-id="0937c-157">一般資源</span><span class="sxs-lookup"><span data-stu-id="0937c-157">Typical Resources</span></span>

<span data-ttu-id="0937c-158">這些物件通常不會裝載資源。</span><span class="sxs-lookup"><span data-stu-id="0937c-158">These objects typically do not host resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0937c-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="0937c-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0937c-160">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="0937c-160">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



