---
description: WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換
ms.assetid: 368e7381-8978-421a-b450-59915f8e70e2
title: WPD_CONTENT_TYPE_MEDIA_CAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d45c9bc1e8e41bae526f02102d341ef00fad435
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423458"
---
# <a name="wpd_content_type_media_cast"></a><span data-ttu-id="18ed2-103">WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換</span><span class="sxs-lookup"><span data-stu-id="18ed2-103">WPD\_CONTENT\_TYPE\_MEDIA\_CAST</span></span>

<span data-ttu-id="18ed2-104">描述其類型作為 WPD \_ 內容 \_ 類型媒體轉換的物件， \_ \_ 代表相關內容的集合。</span><span class="sxs-lookup"><span data-stu-id="18ed2-104">An object that describes its type as WPD\_CONTENT\_TYPE\_MEDIA\_CAST represents a collection of related content.</span></span>

<span data-ttu-id="18ed2-105">Mediacast 物件可以視為將相關內容分組的容器物件，就像播放清單群組音樂一樣。</span><span class="sxs-lookup"><span data-stu-id="18ed2-105">A Mediacast object can be thought of as a container object that groups related content, just as a playlist groups music.</span></span> <span data-ttu-id="18ed2-106">通常，Mediacast 物件是用來將線上發佈的媒體內容分組。</span><span class="sxs-lookup"><span data-stu-id="18ed2-106">Often, a Mediacast object is used to group media content that was published online.</span></span> <span data-ttu-id="18ed2-107">例如，RSS 通道可以表示為 Mediacast 物件，其物件參考指向代表通道中每個專案的內容物件。</span><span class="sxs-lookup"><span data-stu-id="18ed2-107">For example, an RSS channel can be represented as a Mediacast object whose object references point to content objects that represent each item in the channel.</span></span>

<span data-ttu-id="18ed2-108">這種類型的物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-108">This type of object supports the following properties.</span></span>



| <span data-ttu-id="18ed2-109">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="18ed2-109">Property Name</span></span>             |  <span data-ttu-id="18ed2-110">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="18ed2-110">Required or Optional</span></span>         |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="18ed2-111">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="18ed2-111">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="18ed2-112">必要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-112">Required.</span></span>                                                             |
| [<span data-ttu-id="18ed2-113">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="18ed2-113">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="18ed2-114">必要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-114">Required.</span></span>                                                             |
| [<span data-ttu-id="18ed2-115">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="18ed2-115">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="18ed2-116">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-116">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="18ed2-117">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="18ed2-117">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="18ed2-118">必要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-118">Required.</span></span>                                                             |
| [<span data-ttu-id="18ed2-119">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="18ed2-119">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="18ed2-120">必要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-120">Required.</span></span>                                                             |
| [<span data-ttu-id="18ed2-121">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="18ed2-121">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="18ed2-122">必要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-122">Required.</span></span>                                                             |
| [<span data-ttu-id="18ed2-123">WPD \_ 物件 \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="18ed2-123">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="18ed2-124">如果物件是隱藏的，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="18ed2-124">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="18ed2-125">WPD \_ 物件 \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="18ed2-125">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="18ed2-126">如果物件為系統物件，則為必要項， (代表) 的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="18ed2-126">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="18ed2-127">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="18ed2-127">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="18ed2-128">如果物件至少有一個資源，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="18ed2-128">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="18ed2-129">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="18ed2-129">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="18ed2-130">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-130">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="18ed2-131">不可取用的 WPD \_ 物件 \_ \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-131">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="18ed2-132">如果物件不打算供裝置取用，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-132">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="18ed2-133">WPD \_ 物件 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="18ed2-133">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="18ed2-134">如果物件具有其他物件的參考，則為必要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-134">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="18ed2-135">WPD \_ 物件 \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="18ed2-135">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="18ed2-136">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-136">Optional.</span></span>                                                             |
| [<span data-ttu-id="18ed2-137">WPD \_ 物件 \_ 同步 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="18ed2-137">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="18ed2-138">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-138">Optional.</span></span>                                                             |
| [<span data-ttu-id="18ed2-139">WPD \_ 物件 \_ 受到 \_ DRM \_ 保護</span><span class="sxs-lookup"><span data-stu-id="18ed2-139">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="18ed2-140">如果物件受到 DRM 技術的保護，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="18ed2-140">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="18ed2-141">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-141">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="18ed2-142">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-142">Optional.</span></span>                                                             |
| [<span data-ttu-id="18ed2-143">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-143">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="18ed2-144">建議使用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-144">Recommended.</span></span>                                                          |
| [<span data-ttu-id="18ed2-145">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-145">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="18ed2-146">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-146">Optional.</span></span>                                                             |
| [<span data-ttu-id="18ed2-147">WPD \_ 物件 \_ 反向 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="18ed2-147">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="18ed2-148">如果物件是由另一個物件參考，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-148">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="18ed2-149">WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="18ed2-149">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="18ed2-150">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-150">Optional.</span></span>                                                             |
| [<span data-ttu-id="18ed2-151">WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-151">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="18ed2-152">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-152">Optional.</span></span>                                                             |
| [<span data-ttu-id="18ed2-153">WPD \_ 物件 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="18ed2-153">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="18ed2-154">如果可以刪除物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-154">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="18ed2-155">WPD \_ 物件 \_ 語言 \_ 地區設定</span><span class="sxs-lookup"><span data-stu-id="18ed2-155">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="18ed2-156">如果無法刪除物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-156">Required if the object cannot be deleted.</span></span>                             |
| [<span data-ttu-id="18ed2-157">WPD \_ 媒體 \_ 著作權</span><span class="sxs-lookup"><span data-stu-id="18ed2-157">WPD\_MEDIA\_COPYRIGHT</span></span>](media-properties.md)                                                     | <span data-ttu-id="18ed2-158">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-158">Optional.</span></span>                                                             |
| [<span data-ttu-id="18ed2-159">WPD \_ 媒體 \_ 家長 \_ 評等</span><span class="sxs-lookup"><span data-stu-id="18ed2-159">WPD\_MEDIA\_PARENTAL\_RATING</span></span>](media-properties.md)                                        | <span data-ttu-id="18ed2-160">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-160">Optional.</span></span>                                                             |
| [<span data-ttu-id="18ed2-161">WPD \_ 媒體 \_ 中繼 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="18ed2-161">WPD\_MEDIA\_META\_GENRE</span></span>](media-properties.md)                                                  | <span data-ttu-id="18ed2-162">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-162">Optional.</span></span>                                                             |
| [<span data-ttu-id="18ed2-163">WPD \_ 媒體 \_ 子 \_ 標題</span><span class="sxs-lookup"><span data-stu-id="18ed2-163">WPD\_MEDIA\_SUB\_TITLE</span></span>](media-properties.md)                                                    | <span data-ttu-id="18ed2-164">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-164">Optional.</span></span>                                                             |
| [<span data-ttu-id="18ed2-165">WPD \_ 媒體 \_ 發行 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="18ed2-165">WPD\_MEDIA\_RELEASE\_DATE</span></span>](media-properties.md)                                              | <span data-ttu-id="18ed2-166">建議使用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-166">Recommended.</span></span>                                                          |
| [<span data-ttu-id="18ed2-167">WPD \_ 媒體 \_ 標題</span><span class="sxs-lookup"><span data-stu-id="18ed2-167">WPD\_MEDIA\_TITLE</span></span>](media-properties.md)                                                             | <span data-ttu-id="18ed2-168">建議使用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-168">Recommended.</span></span>                                                          |
| [<span data-ttu-id="18ed2-169">WPD \_ 媒體 \_ 擁有者</span><span class="sxs-lookup"><span data-stu-id="18ed2-169">WPD\_MEDIA\_OWNER</span></span>](media-properties.md)                                                             | <span data-ttu-id="18ed2-170">建議使用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-170">Recommended.</span></span>                                                          |
| [<span data-ttu-id="18ed2-171">WPD \_ 媒體 \_ 管理 \_ 編輯器</span><span class="sxs-lookup"><span data-stu-id="18ed2-171">WPD\_MEDIA\_MANAGING\_EDITOR</span></span>](media-properties.md)                                        | <span data-ttu-id="18ed2-172">建議使用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-172">Recommended.</span></span>                                                          |
| [<span data-ttu-id="18ed2-173">WPD \_ 媒體 \_ 管理員</span><span class="sxs-lookup"><span data-stu-id="18ed2-173">WPD\_MEDIA\_WEBMASTER</span></span>](media-properties.md)                                                     | <span data-ttu-id="18ed2-174">建議使用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-174">Recommended.</span></span>                                                          |
| [<span data-ttu-id="18ed2-175">WPD \_ 媒體 \_ 來源 \_ URL</span><span class="sxs-lookup"><span data-stu-id="18ed2-175">WPD\_MEDIA\_SOURCE\_URL</span></span>](media-properties.md)                                                  | <span data-ttu-id="18ed2-176">建議使用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-176">Recommended.</span></span>                                                          |
| [<span data-ttu-id="18ed2-177">WPD \_ 媒體 \_ 目的地 \_ URL</span><span class="sxs-lookup"><span data-stu-id="18ed2-177">WPD\_MEDIA\_DESTINATION\_URL</span></span>](media-properties.md)                                        | <span data-ttu-id="18ed2-178">建議使用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-178">Recommended.</span></span>                                                          |
| [<span data-ttu-id="18ed2-179">WPD \_ 媒體 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="18ed2-179">WPD\_MEDIA\_DESCRIPTION</span></span>](media-properties.md)                                                 | <span data-ttu-id="18ed2-180">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-180">Optional.</span></span>                                                             |
| [<span data-ttu-id="18ed2-181">WPD \_ 媒體內容類型 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-181">WPD\_MEDIA\_GENRE</span></span>](media-properties.md)                                                             | <span data-ttu-id="18ed2-182">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-182">Optional.</span></span>                                                             |
| [<span data-ttu-id="18ed2-183">WPD \_ 媒體 \_ 物件 \_ 書簽</span><span class="sxs-lookup"><span data-stu-id="18ed2-183">WPD\_MEDIA\_OBJECT\_BOOKMARK</span></span>](media-properties.md)                                        | <span data-ttu-id="18ed2-184">建議</span><span class="sxs-lookup"><span data-stu-id="18ed2-184">Recommended</span></span>                                                           |
| [<span data-ttu-id="18ed2-185">WPD \_ 媒體 \_ 上次 \_ 組建 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="18ed2-185">WPD\_MEDIA\_LAST\_BUILD\_DATE</span></span>](media-properties.md)                                       | <span data-ttu-id="18ed2-186">建議使用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-186">Recommended.</span></span>                                                          |
| [<span data-ttu-id="18ed2-187">WPD \_ 媒體 \_ 生存 \_ 時間 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-187">WPD\_MEDIA\_TIME\_TO\_LIVE</span></span>](media-properties.md)                                             | <span data-ttu-id="18ed2-188">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-188">Optional.</span></span>                                                             |
| [<span data-ttu-id="18ed2-189">WPD \_ 媒體 \_ 子 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="18ed2-189">WPD\_MEDIA\_SUB\_DESCRIPTION</span></span>](object-properties.md)                                                                 | <span data-ttu-id="18ed2-190">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-190">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="18ed2-191">一般資源</span><span class="sxs-lookup"><span data-stu-id="18ed2-191">Typical Resources</span></span>

<span data-ttu-id="18ed2-192">這些物件通常包含下列資源。</span><span class="sxs-lookup"><span data-stu-id="18ed2-192">These objects typically include the following resources.</span></span>



| <span data-ttu-id="18ed2-193">資源名稱</span><span class="sxs-lookup"><span data-stu-id="18ed2-193">Resource Name</span></span>                                               | <span data-ttu-id="18ed2-194">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="18ed2-194">Required or Optional</span></span> | <span data-ttu-id="18ed2-195">描述</span><span class="sxs-lookup"><span data-stu-id="18ed2-195">Description</span></span>                                                                                                                 |
|-------------------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18ed2-196">**WPD \_ 資源 \_ 預設**</span><span class="sxs-lookup"><span data-stu-id="18ed2-196">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md)      | <span data-ttu-id="18ed2-197">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-197">Optional.</span></span>            | <span data-ttu-id="18ed2-198">包含 mediacast 檔案資料。</span><span class="sxs-lookup"><span data-stu-id="18ed2-198">Contains the mediacast file data.</span></span> <span data-ttu-id="18ed2-199">例如，如果此 mediacast 代表 RSS 通道，這可能是 RSS 檔。</span><span class="sxs-lookup"><span data-stu-id="18ed2-199">For example, if this mediacast represents an RSS channel, this might be the RSS document.</span></span> |
| [<span data-ttu-id="18ed2-200">**WPD \_ 資源 \_ 縮圖**</span><span class="sxs-lookup"><span data-stu-id="18ed2-200">**WPD\_RESOURCE\_THUMBNAIL**</span></span>](wpd-resource-thumbnail.md)  | <span data-ttu-id="18ed2-201">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-201">Optional.</span></span>            | <span data-ttu-id="18ed2-202">包含表示此 mediacast 的縮圖。</span><span class="sxs-lookup"><span data-stu-id="18ed2-202">Contains the thumbnail representing this mediacast.</span></span>                                                                         |
| [<span data-ttu-id="18ed2-203">**WPD \_ 資源 \_ 專輯 \_ 封面**</span><span class="sxs-lookup"><span data-stu-id="18ed2-203">**WPD\_RESOURCE\_ALBUM\_ART**</span></span>](wpd-resource-album-art.md) | <span data-ttu-id="18ed2-204">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-204">Optional.</span></span>            | <span data-ttu-id="18ed2-205">包含此 mediacast 的作品。</span><span class="sxs-lookup"><span data-stu-id="18ed2-205">Contains the artwork for this mediacast.</span></span>                                                                                    |



 

## <a name="mapping-of-rss-elements-and-mediacast-properties"></a><span data-ttu-id="18ed2-206">RSS 元素與 Mediacast 屬性的對應</span><span class="sxs-lookup"><span data-stu-id="18ed2-206">Mapping of RSS Elements and Mediacast properties</span></span>

<span data-ttu-id="18ed2-207">RSS 通道可以表示為 Mediacast 物件，其參考指向代表特定通道中每個專案的內容物件。</span><span class="sxs-lookup"><span data-stu-id="18ed2-207">An RSS channel can be represented as a Mediacast object whose references point to content objects representing each item in a given channel.</span></span>

<span data-ttu-id="18ed2-208">RSS 饋送中的元素具有下列階層和屬性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-208">The elements in an RSS feed have the following hierarchy and attributes.</span></span>


```C++
<channel>
    <title />
    <link />
    <description />
    <language />
    <copyright />
    <managingEditor />
    <webMaster />
    <pubDate />
    <lastBuildDate />
    <category />
    <generator />
    <docs />
    <cloud />
    <ttl />

    <image>
        <url />
        <title />
        <link />
        <width />
        <height />
        <description />
    </image>

    <rating />

    <textInput>
        <title />
        <description />
        <name />
        <link />
    </textInput>

    <skipHours />
    <skipDays />

    <item>
        <title />
        <link />
        <description />
        <author />
        <category domain = " "/>
        <comments />
        <enclousure url = " " length = " " type = " "/>
        <guid isPermaLink = " "/>
        <pubDate />
        <source url = " " />
    </item>
</channel>
```



<span data-ttu-id="18ed2-209">下表列出 RSS 摘要中的通道元素，以及對應的 WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換屬性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-209">The following table lists the channel elements in an RSS feed and the corresponding WPD\_CONTENT\_TYPE\_MEDIA\_CAST properties.</span></span>



| <span data-ttu-id="18ed2-210">Channel 元素</span><span class="sxs-lookup"><span data-stu-id="18ed2-210">Channel Element</span></span> | <span data-ttu-id="18ed2-211">RSS 饋送需求</span><span class="sxs-lookup"><span data-stu-id="18ed2-211">RSS Feed Requirement</span></span> | <span data-ttu-id="18ed2-212">對應的 Mediacast 屬性</span><span class="sxs-lookup"><span data-stu-id="18ed2-212">Corresponding Mediacast Property</span></span>      |
|---------------------|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="18ed2-213">category</span><span class="sxs-lookup"><span data-stu-id="18ed2-213">category</span></span>            | <span data-ttu-id="18ed2-214">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-214">Optional.</span></span>                | [<span data-ttu-id="18ed2-215">WPD \_ 媒體內容類型 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-215">WPD\_MEDIA\_GENRE</span></span>](media-properties.md)                       |
| <span data-ttu-id="18ed2-216">cloud</span><span class="sxs-lookup"><span data-stu-id="18ed2-216">cloud</span></span>               | <span data-ttu-id="18ed2-217">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-217">Not applicable.</span></span>          | <span data-ttu-id="18ed2-218">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-218">Not applicable.</span></span>                                                                 |
| <span data-ttu-id="18ed2-219">著作權</span><span class="sxs-lookup"><span data-stu-id="18ed2-219">copyright</span></span>           | <span data-ttu-id="18ed2-220">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-220">Optional.</span></span>                | [<span data-ttu-id="18ed2-221">WPD \_ 媒體 \_ 著作權</span><span class="sxs-lookup"><span data-stu-id="18ed2-221">WPD\_MEDIA\_COPYRIGHT</span></span>](media-properties.md)               |
| <span data-ttu-id="18ed2-222">描述</span><span class="sxs-lookup"><span data-stu-id="18ed2-222">description</span></span>         | <span data-ttu-id="18ed2-223">必要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-223">Required.</span></span>                | [<span data-ttu-id="18ed2-224">WPD \_ 媒體 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="18ed2-224">WPD\_MEDIA\_DESCRIPTION</span></span>](media-properties.md)           |
| <span data-ttu-id="18ed2-225">docs</span><span class="sxs-lookup"><span data-stu-id="18ed2-225">docs</span></span>                | <span data-ttu-id="18ed2-226">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-226">Not applicable.</span></span>          | <span data-ttu-id="18ed2-227">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-227">Not applicable.</span></span>                                                                 |
| <span data-ttu-id="18ed2-228">產生器</span><span class="sxs-lookup"><span data-stu-id="18ed2-228">generator</span></span>           | <span data-ttu-id="18ed2-229">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-229">Not applicable.</span></span>          | <span data-ttu-id="18ed2-230">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-230">Not applicable.</span></span>                                                                 |
| <span data-ttu-id="18ed2-231">語言</span><span class="sxs-lookup"><span data-stu-id="18ed2-231">language</span></span>            | <span data-ttu-id="18ed2-232">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-232">Not applicable.</span></span>          | <span data-ttu-id="18ed2-233">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-233">Not applicable.</span></span>                                                                 |
| <span data-ttu-id="18ed2-234">lastBuildDate</span><span class="sxs-lookup"><span data-stu-id="18ed2-234">lastBuildDate</span></span>       | <span data-ttu-id="18ed2-235">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-235">Optional.</span></span>                | [<span data-ttu-id="18ed2-236">WPD \_ 媒體 \_ 上次 \_ 組建 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="18ed2-236">WPD\_MEDIA\_LAST\_BUILD\_DATE</span></span>](media-properties.md) |
| <span data-ttu-id="18ed2-237">link</span><span class="sxs-lookup"><span data-stu-id="18ed2-237">link</span></span>                | <span data-ttu-id="18ed2-238">必要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-238">Required.</span></span>                | [<span data-ttu-id="18ed2-239">WPD \_ 媒體 \_ 目的地 \_ URL</span><span class="sxs-lookup"><span data-stu-id="18ed2-239">WPD\_MEDIA\_DESTINATION\_URL</span></span>](media-properties.md)  |
| <span data-ttu-id="18ed2-240">managingEditor</span><span class="sxs-lookup"><span data-stu-id="18ed2-240">managingEditor</span></span>      | <span data-ttu-id="18ed2-241">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-241">Optional.</span></span>                | [<span data-ttu-id="18ed2-242">WPD \_ 媒體 \_ 管理 \_ 編輯器</span><span class="sxs-lookup"><span data-stu-id="18ed2-242">WPD\_MEDIA\_MANAGING\_EDITOR</span></span>](media-properties.md)  |
| <span data-ttu-id="18ed2-243">pubDate</span><span class="sxs-lookup"><span data-stu-id="18ed2-243">pubDate</span></span>             | <span data-ttu-id="18ed2-244">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-244">Optional.</span></span>                | [<span data-ttu-id="18ed2-245">WPD \_ 媒體 \_ 發行 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="18ed2-245">WPD\_MEDIA\_RELEASE\_DATE</span></span>](media-properties.md)        |
| <span data-ttu-id="18ed2-246">rating</span><span class="sxs-lookup"><span data-stu-id="18ed2-246">rating</span></span>              | <span data-ttu-id="18ed2-247">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-247">Not applicable.</span></span>          | <span data-ttu-id="18ed2-248">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-248">Not applicable.</span></span>                                                                 |
| <span data-ttu-id="18ed2-249">skipDays</span><span class="sxs-lookup"><span data-stu-id="18ed2-249">skipDays</span></span>            | <span data-ttu-id="18ed2-250">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-250">Not applicable.</span></span>          | <span data-ttu-id="18ed2-251">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-251">Not applicable.</span></span>                                                                 |
| <span data-ttu-id="18ed2-252">skipHours</span><span class="sxs-lookup"><span data-stu-id="18ed2-252">skipHours</span></span>           | <span data-ttu-id="18ed2-253">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-253">Not applicable.</span></span>          | <span data-ttu-id="18ed2-254">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-254">Not applicable.</span></span>                                                                 |
| <span data-ttu-id="18ed2-255">>textinput</span><span class="sxs-lookup"><span data-stu-id="18ed2-255">textInput</span></span>           | <span data-ttu-id="18ed2-256">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-256">Not applicable.</span></span>          | <span data-ttu-id="18ed2-257">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-257">Not applicable.</span></span>                                                                 |
| <span data-ttu-id="18ed2-258">title</span><span class="sxs-lookup"><span data-stu-id="18ed2-258">title</span></span>               | <span data-ttu-id="18ed2-259">必要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-259">Required.</span></span>                | [<span data-ttu-id="18ed2-260">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="18ed2-260">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                      |
| <span data-ttu-id="18ed2-261">ttl</span><span class="sxs-lookup"><span data-stu-id="18ed2-261">ttl</span></span>                 | <span data-ttu-id="18ed2-262">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-262">Optional.</span></span>                | [<span data-ttu-id="18ed2-263">WPD \_ 媒體 \_ 生存 \_ 時間 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-263">WPD\_MEDIA\_TIME\_TO\_LIVE</span></span>](media-properties.md)       |
| <span data-ttu-id="18ed2-264">站長</span><span class="sxs-lookup"><span data-stu-id="18ed2-264">webMaster</span></span>           | <span data-ttu-id="18ed2-265">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-265">Optional.</span></span>                | [<span data-ttu-id="18ed2-266">WPD \_ 媒體 \_ 管理員</span><span class="sxs-lookup"><span data-stu-id="18ed2-266">WPD\_MEDIA\_WEBMASTER</span></span>](media-properties.md)               |



 

<span data-ttu-id="18ed2-267">下表列出 RSS 摘要中的影像元素，以及對應的 WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換屬性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-267">The following table lists the image elements in an RSS feed and the corresponding WPD\_CONTENT\_TYPE\_MEDIA\_CAST properties.</span></span>



| <span data-ttu-id="18ed2-268">Image 元素</span><span class="sxs-lookup"><span data-stu-id="18ed2-268">Image Element</span></span> | <span data-ttu-id="18ed2-269">RSS 饋送需求</span><span class="sxs-lookup"><span data-stu-id="18ed2-269">RSS Feed Requirement</span></span> | <span data-ttu-id="18ed2-270">Mediacast 屬性</span><span class="sxs-lookup"><span data-stu-id="18ed2-270">Mediacast Property</span></span>                     |
|-------------------|--------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="18ed2-271">描述</span><span class="sxs-lookup"><span data-stu-id="18ed2-271">description</span></span>       | <span data-ttu-id="18ed2-272">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-272">Optional.</span></span>                | [<span data-ttu-id="18ed2-273">WPD \_ 媒體 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="18ed2-273">WPD\_MEDIA\_DESCRIPTION</span></span>](media-properties.md)          |
| <span data-ttu-id="18ed2-274">身高</span><span class="sxs-lookup"><span data-stu-id="18ed2-274">height</span></span>            | <span data-ttu-id="18ed2-275">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-275">Optional.</span></span>                | [<span data-ttu-id="18ed2-276">WPD \_ 媒體 \_ 高度</span><span class="sxs-lookup"><span data-stu-id="18ed2-276">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                    |
| <span data-ttu-id="18ed2-277">link</span><span class="sxs-lookup"><span data-stu-id="18ed2-277">link</span></span>              | <span data-ttu-id="18ed2-278">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-278">Optional.</span></span>                | [<span data-ttu-id="18ed2-279">WPD \_ 媒體 \_ 目的地 \_ URL</span><span class="sxs-lookup"><span data-stu-id="18ed2-279">WPD\_MEDIA\_DESTINATION\_URL</span></span>](media-properties.md) |
| <span data-ttu-id="18ed2-280">title</span><span class="sxs-lookup"><span data-stu-id="18ed2-280">title</span></span>             | <span data-ttu-id="18ed2-281">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-281">Optional.</span></span>                | [<span data-ttu-id="18ed2-282">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="18ed2-282">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                     |
| <span data-ttu-id="18ed2-283">url</span><span class="sxs-lookup"><span data-stu-id="18ed2-283">url</span></span>               | <span data-ttu-id="18ed2-284">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-284">Optional.</span></span>                | [<span data-ttu-id="18ed2-285">WPD \_ 媒體 \_ 來源 \_ URL</span><span class="sxs-lookup"><span data-stu-id="18ed2-285">WPD\_MEDIA\_SOURCE\_URL</span></span>](media-properties.md)           |
| <span data-ttu-id="18ed2-286">width</span><span class="sxs-lookup"><span data-stu-id="18ed2-286">width</span></span>             | <span data-ttu-id="18ed2-287">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-287">Optional.</span></span>                | [<span data-ttu-id="18ed2-288">WPD \_ 媒體 \_ 寬度</span><span class="sxs-lookup"><span data-stu-id="18ed2-288">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                      |



 

<span data-ttu-id="18ed2-289">下表列出 RSS 摘要中的專案元素，以及對應的 WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換屬性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-289">The following table lists the item elements in an RSS feed and the corresponding WPD\_CONTENT\_TYPE\_MEDIA\_CAST properties.</span></span>



| <span data-ttu-id="18ed2-290">Item 項目</span><span class="sxs-lookup"><span data-stu-id="18ed2-290">Item Element</span></span> | <span data-ttu-id="18ed2-291">屬性</span><span class="sxs-lookup"><span data-stu-id="18ed2-291">Attribute</span></span> | <span data-ttu-id="18ed2-292">RSS 饋送需求</span><span class="sxs-lookup"><span data-stu-id="18ed2-292">RSS Feed Requirement</span></span> | <span data-ttu-id="18ed2-293">Mediacast 屬性</span><span class="sxs-lookup"><span data-stu-id="18ed2-293">Mediacast Property</span></span>  |
|------------------|---------------|--------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="18ed2-294">編寫</span><span class="sxs-lookup"><span data-stu-id="18ed2-294">author</span></span>           |               | <span data-ttu-id="18ed2-295">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-295">Optional.</span></span>                | [<span data-ttu-id="18ed2-296">WPD \_ MEDIA \_ 演出者</span><span class="sxs-lookup"><span data-stu-id="18ed2-296">WPD\_MEDIA\_ARTIST</span></span>](media-properties.md)                    |
| <span data-ttu-id="18ed2-297">category</span><span class="sxs-lookup"><span data-stu-id="18ed2-297">category</span></span>         |               | <span data-ttu-id="18ed2-298">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-298">Optional.</span></span>                | [<span data-ttu-id="18ed2-299">WPD \_ 媒體內容類型 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-299">WPD\_MEDIA\_GENRE</span></span>](media-properties.md)                      |
|                  | <span data-ttu-id="18ed2-300">網域</span><span class="sxs-lookup"><span data-stu-id="18ed2-300">domain</span></span>        | <span data-ttu-id="18ed2-301">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-301">Not applicable.</span></span>          | <span data-ttu-id="18ed2-302">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-302">Not applicable.</span></span>                                                                |
| <span data-ttu-id="18ed2-303">描述</span><span class="sxs-lookup"><span data-stu-id="18ed2-303">description</span></span>      |               | <span data-ttu-id="18ed2-304">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-304">Optional.</span></span>                | [<span data-ttu-id="18ed2-305">WPD \_ 媒體 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="18ed2-305">WPD\_MEDIA\_DESCRIPTION</span></span>](media-properties.md)          |
| <span data-ttu-id="18ed2-306">外殼</span><span class="sxs-lookup"><span data-stu-id="18ed2-306">enclosure</span></span>        |               | <span data-ttu-id="18ed2-307">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-307">Optional.</span></span>                |                                                                                |
|                  | <span data-ttu-id="18ed2-308">url</span><span class="sxs-lookup"><span data-stu-id="18ed2-308">url</span></span>           | <span data-ttu-id="18ed2-309">必要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-309">Required.</span></span>                | [<span data-ttu-id="18ed2-310">WPD \_ 媒體 \_ 來源 \_ URL</span><span class="sxs-lookup"><span data-stu-id="18ed2-310">WPD\_MEDIA\_SOURCE\_URL</span></span>](media-properties.md)           |
|                  | <span data-ttu-id="18ed2-311">長度</span><span class="sxs-lookup"><span data-stu-id="18ed2-311">length</span></span>        | <span data-ttu-id="18ed2-312">必要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-312">Required.</span></span>                | [<span data-ttu-id="18ed2-313">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="18ed2-313">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                     |
|                  | <span data-ttu-id="18ed2-314">類型</span><span class="sxs-lookup"><span data-stu-id="18ed2-314">type</span></span>          | <span data-ttu-id="18ed2-315">必要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-315">Required.</span></span>                | <span data-ttu-id="18ed2-316"> (MIME 類型應對應至屬性內容類型。 ) </span><span class="sxs-lookup"><span data-stu-id="18ed2-316">(The MIME type should be mapped to the property content type.)</span></span>                 |
| <span data-ttu-id="18ed2-317">guid</span><span class="sxs-lookup"><span data-stu-id="18ed2-317">guid</span></span>             |               | <span data-ttu-id="18ed2-318">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-318">Optional.</span></span>                | [<span data-ttu-id="18ed2-319">WPD \_ 媒體 \_ GUID</span><span class="sxs-lookup"><span data-stu-id="18ed2-319">WPD\_MEDIA\_GUID</span></span>](media-properties.md)                        |
|                  | <span data-ttu-id="18ed2-320">isPermaLink</span><span class="sxs-lookup"><span data-stu-id="18ed2-320">isPermaLink</span></span>   | <span data-ttu-id="18ed2-321">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-321">Not applicable.</span></span>          | <span data-ttu-id="18ed2-322">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-322">Not applicable.</span></span>                                                                |
| <span data-ttu-id="18ed2-323">link</span><span class="sxs-lookup"><span data-stu-id="18ed2-323">link</span></span>             |               | <span data-ttu-id="18ed2-324">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-324">Optional.</span></span>                | [<span data-ttu-id="18ed2-325">WPD \_ 媒體 \_ 目的地 \_ URL</span><span class="sxs-lookup"><span data-stu-id="18ed2-325">WPD\_MEDIA\_DESTINATION\_URL</span></span>](media-properties.md) |
| <span data-ttu-id="18ed2-326">pubDate</span><span class="sxs-lookup"><span data-stu-id="18ed2-326">pubDate</span></span>          |               | <span data-ttu-id="18ed2-327">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-327">Optional.</span></span>                | [<span data-ttu-id="18ed2-328">WPD \_ 媒體 \_ 發行 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="18ed2-328">WPD\_MEDIA\_RELEASE\_DATE</span></span>](media-properties.md)       |
| <span data-ttu-id="18ed2-329">source</span><span class="sxs-lookup"><span data-stu-id="18ed2-329">source</span></span>           |               | <span data-ttu-id="18ed2-330">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-330">Not applicable.</span></span>          | <span data-ttu-id="18ed2-331">不適用。</span><span class="sxs-lookup"><span data-stu-id="18ed2-331">Not applicable.</span></span>                                                                |
| <span data-ttu-id="18ed2-332">title</span><span class="sxs-lookup"><span data-stu-id="18ed2-332">title</span></span>            |               | <span data-ttu-id="18ed2-333">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-333">Optional.</span></span>                | [<span data-ttu-id="18ed2-334">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="18ed2-334">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                     |



 

<span data-ttu-id="18ed2-335">下列範例顯示發行公司的 CEO 所提供之虛構播客的完整 RSS 摘要。</span><span class="sxs-lookup"><span data-stu-id="18ed2-335">The following example shows a complete RSS feed for a fictitious podcast supplied by the CEO of a publishing company.</span></span>


```C++
<channel>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/podcasting</link>
    <description>Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</description>
    <language>en-us</language>
    <copyright>2006 Lucerne Publishing LP, LLLP. All Rights Reserved.</copyright>
    <managingEditor>someone@example.com</managingEditor>
    <webMaster>someone@example.com</webMaster>
    <pubDate>Fri, 9 June 2006 14:00:28 EDT</pubDate>
    <lastBuildDate Fri, 9 June 2006 14:00:28 EDT />
    <category>News</category>
    <generator>Podcaster version 1.0</generator>
    <docs>https://www.lucernepublishing.com/tech/rss</docs>
    <cloud />
    <ttl>240</ttl>
    <rating />
    <textInput />
    <skipHours />
    <skipDays />

<image>
     <url>https://www.lucernepublishing.com/images/logo.gif</url>
     <title>Lucerne Publishing</title>
     <link>https://www.lucernepublishing.com/community/podcasts</link>
     <width>300</width>
     <height>300</height>
     <description>Lucerne Logo</description>
</image>

<item>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past 5 years and their implications.</description>
    <author>Lucerne</author>
    <category>News</category>
    <comments />
    <enclosure url="https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3" length="10329011" type="audio/mpeg" />
    <guid>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</guid>
    <pubDate>Thur, 1 June 2006 14:00:28 EDT</pubDate>
    <source />
</item>

</channel>
```



## <a name="mapping-rss-channel-elements-to-wpd-property-values"></a><span data-ttu-id="18ed2-336">將 RSS 通道元素對應至 WPD 屬性值</span><span class="sxs-lookup"><span data-stu-id="18ed2-336">Mapping RSS Channel Elements to WPD Property Values</span></span>

<span data-ttu-id="18ed2-337">下表說明上一個範例中 RSS 通道元素的值如何對應至特定的 WPD 屬性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-337">The following table describes how the values in the RSS channel elements in the previous example map to particular WPD properties.</span></span>



| <span data-ttu-id="18ed2-338">WPD 屬性</span><span class="sxs-lookup"><span data-stu-id="18ed2-338">WPD Property</span></span> | <span data-ttu-id="18ed2-339">值</span><span class="sxs-lookup"><span data-stu-id="18ed2-339">Value</span></span> |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18ed2-340">WPD \_ 媒體 \_ 著作權</span><span class="sxs-lookup"><span data-stu-id="18ed2-340">WPD\_MEDIA\_COPYRIGHT</span></span>](media-properties.md)                            | <span data-ttu-id="18ed2-341">2006 Lucerne 發行 LP，LLLP。</span><span class="sxs-lookup"><span data-stu-id="18ed2-341">2006 Lucerne Publishing LP, LLLP.</span></span> <span data-ttu-id="18ed2-342">著作權所有，並保留一切權利。</span><span class="sxs-lookup"><span data-stu-id="18ed2-342">All Rights Reserved.</span></span>                                        |
| [<span data-ttu-id="18ed2-343">WPD \_ 媒體 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="18ed2-343">WPD\_MEDIA\_DESCRIPTION</span></span>](media-properties.md)                        | <span data-ttu-id="18ed2-344">Lucerne 發佈 CEO Peter Bankov 會查看線上發行物的最新趨勢。</span><span class="sxs-lookup"><span data-stu-id="18ed2-344">Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</span></span> |
| [<span data-ttu-id="18ed2-345">WPD \_ 媒體 \_ 目的地 \_ URL</span><span class="sxs-lookup"><span data-stu-id="18ed2-345">WPD\_MEDIA\_DESTINATION\_URL</span></span>](media-properties.md)               | https://www.lucernepublishing.com/services/podcasting                                          |
| [<span data-ttu-id="18ed2-346">WPD \_ 媒體內容類型 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-346">WPD\_MEDIA\_GENRE</span></span>](media-properties.md)                                    | <span data-ttu-id="18ed2-347">新聞</span><span class="sxs-lookup"><span data-stu-id="18ed2-347">News</span></span>                                                                                          |
| [<span data-ttu-id="18ed2-348">WPD \_ 媒體 \_ 上次 \_ 組建 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="18ed2-348">WPD\_MEDIA\_LAST\_BUILD\_DATE</span></span>](media-properties.md)              | <span data-ttu-id="18ed2-349">2006年6月9日，14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="18ed2-349">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="18ed2-350">WPD \_ 媒體 \_ 管理 \_ 編輯器</span><span class="sxs-lookup"><span data-stu-id="18ed2-350">WPD\_MEDIA\_MANAGING\_EDITOR</span></span>](media-properties.md)               | someone@example.com                                                                           |
| [<span data-ttu-id="18ed2-351">WPD \_ 媒體 \_ 發行 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="18ed2-351">WPD\_MEDIA\_RELEASE\_DATE</span></span>](media-properties.md)                     | <span data-ttu-id="18ed2-352">2006年6月9日，14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="18ed2-352">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="18ed2-353">WPD \_ 媒體 \_ 生存 \_ 時間 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-353">WPD\_MEDIA\_TIME\_TO\_LIVE</span></span>](media-properties.md)                    | <span data-ttu-id="18ed2-354">240</span><span class="sxs-lookup"><span data-stu-id="18ed2-354">240</span></span>                                                                                           |
| [<span data-ttu-id="18ed2-355">WPD \_ 媒體 \_ 標題</span><span class="sxs-lookup"><span data-stu-id="18ed2-355">WPD\_MEDIA\_TITLE</span></span>](media-properties.md)                                    | <span data-ttu-id="18ed2-356">數位發行</span><span class="sxs-lookup"><span data-stu-id="18ed2-356">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="18ed2-357">WPD \_ 媒體 \_ 來源 \_ URL</span><span class="sxs-lookup"><span data-stu-id="18ed2-357">WPD\_MEDIA\_SOURCE\_URL</span></span>](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publication/rss.xml                  |
| [<span data-ttu-id="18ed2-358">WPD \_ 媒體 \_ 管理員</span><span class="sxs-lookup"><span data-stu-id="18ed2-358">WPD\_MEDIA\_WEBMASTER</span></span>](media-properties.md)                            | someone@example.com                                                                           |
| [<span data-ttu-id="18ed2-359">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="18ed2-359">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                  | <span data-ttu-id="18ed2-360">WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換</span><span class="sxs-lookup"><span data-stu-id="18ed2-360">WPD\_CONTENT\_TYPE\_MEDIA\_CAST</span></span>                                                               |
| [<span data-ttu-id="18ed2-361">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-361">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                | <span data-ttu-id="18ed2-362">2006年6月9日，14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="18ed2-362">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="18ed2-363">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-363">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                  | <span data-ttu-id="18ed2-364">2006年6月9日，14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="18ed2-364">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="18ed2-365">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-365">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                | <span data-ttu-id="18ed2-366">2006年6月9日，14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="18ed2-366">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="18ed2-367">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="18ed2-367">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                               | <span data-ttu-id="18ed2-368">WPD \_ 物件 \_ 格式 \_ 抽象 \_ 媒體 \_ 轉換</span><span class="sxs-lookup"><span data-stu-id="18ed2-368">WPD\_OBJECT\_FORMAT\_ABSTRACT\_MEDIA\_CAST</span></span>                                                    |
| [<span data-ttu-id="18ed2-369">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="18ed2-369">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                       | <span data-ttu-id="18ed2-370">會話相依值。</span><span class="sxs-lookup"><span data-stu-id="18ed2-370">Session dependent value.</span></span>                                                                      |
| [<span data-ttu-id="18ed2-371">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="18ed2-371">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                   | <span data-ttu-id="18ed2-372">數位發行</span><span class="sxs-lookup"><span data-stu-id="18ed2-372">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="18ed2-373">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="18ed2-373">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)     | <span data-ttu-id="18ed2-374">數位發行</span><span class="sxs-lookup"><span data-stu-id="18ed2-374">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="18ed2-375">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="18ed2-375">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                        | <span data-ttu-id="18ed2-376">MyPodcasts (裝置上的虛構播客資料夾) 。</span><span class="sxs-lookup"><span data-stu-id="18ed2-376">MyPodcasts (a fictitious podcast folder on the device).</span></span> <span data-ttu-id="18ed2-377">針對此範例，請採用 "0A0"。</span><span class="sxs-lookup"><span data-stu-id="18ed2-377">Assume "0A0" for this example.</span></span>        |
| [<span data-ttu-id="18ed2-378">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="18ed2-378">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md) | <span data-ttu-id="18ed2-379">會話獨立值。</span><span class="sxs-lookup"><span data-stu-id="18ed2-379">Session independent value.</span></span> <span data-ttu-id="18ed2-380"> (在此範例中採用 "0A1"。 ) </span><span class="sxs-lookup"><span data-stu-id="18ed2-380">(Assume "0A1" for this example.)</span></span>                                   |
| [<span data-ttu-id="18ed2-381">WPD \_ 物件 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="18ed2-381">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                       | <span data-ttu-id="18ed2-382">N 個專案的0A2</span><span class="sxs-lookup"><span data-stu-id="18ed2-382">0A2  for N items</span></span><br/>                                                                   |
| [<span data-ttu-id="18ed2-383">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="18ed2-383">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                   | <span data-ttu-id="18ed2-384">13790</span><span class="sxs-lookup"><span data-stu-id="18ed2-384">13,790</span></span>                                                                                        |



 

## <a name="mapping-rss-image-elements-to-wpd-property-values"></a><span data-ttu-id="18ed2-385">將 RSS 影像元素對應至 WPD 屬性值</span><span class="sxs-lookup"><span data-stu-id="18ed2-385">Mapping RSS Image Elements to WPD Property Values</span></span>

<span data-ttu-id="18ed2-386">下表說明上一個範例中 RSS 影像元素的值如何對應至特定的 WPD 屬性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-386">The following table describes how the values in the RSS Image elements in the previous example map to particular WPD properties.</span></span>



| <span data-ttu-id="18ed2-387">WPD 屬性</span><span class="sxs-lookup"><span data-stu-id="18ed2-387">WPD Property</span></span>               |                         <span data-ttu-id="18ed2-388">值</span><span class="sxs-lookup"><span data-stu-id="18ed2-388">Value</span></span>                                           |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="18ed2-389">WPD \_ 媒體 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="18ed2-389">WPD\_MEDIA\_DESCRIPTION</span></span>](media-properties.md)                                                   | <span data-ttu-id="18ed2-390">Lucerne 標誌</span><span class="sxs-lookup"><span data-stu-id="18ed2-390">Lucerne Logo</span></span>                                        |
| [<span data-ttu-id="18ed2-391">WPD \_ 媒體 \_ 目的地 \_ URL</span><span class="sxs-lookup"><span data-stu-id="18ed2-391">WPD\_MEDIA\_DESTINATION\_URL</span></span>](media-properties.md)                                          | https://www.lucernepublishing.com/community/podcasts |
| [<span data-ttu-id="18ed2-392">WPD \_ 媒體 \_ 高度</span><span class="sxs-lookup"><span data-stu-id="18ed2-392">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                             | <span data-ttu-id="18ed2-393">300</span><span class="sxs-lookup"><span data-stu-id="18ed2-393">300</span></span>                                                 |
| [<span data-ttu-id="18ed2-394">WPD \_ 媒體 \_ 來源 \_ URL</span><span class="sxs-lookup"><span data-stu-id="18ed2-394">WPD\_MEDIA\_SOURCE\_URL</span></span>](media-properties.md)                                                    | https://www.lucernepublishing.com/images/logo.gif    |
| [<span data-ttu-id="18ed2-395">WPD \_ 媒體 \_ 寬度</span><span class="sxs-lookup"><span data-stu-id="18ed2-395">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                               | <span data-ttu-id="18ed2-396">300</span><span class="sxs-lookup"><span data-stu-id="18ed2-396">300</span></span>                                                 |
| [<span data-ttu-id="18ed2-397">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="18ed2-397">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                              | <span data-ttu-id="18ed2-398">Lucerne 發行</span><span class="sxs-lookup"><span data-stu-id="18ed2-398">Lucerne Publishing</span></span>                                  |
| [<span data-ttu-id="18ed2-399">WPD \_ 資源 \_ 屬性 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="18ed2-399">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                               | <span data-ttu-id="18ed2-400">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="18ed2-400">VARIANT\_TRUE</span></span>                                       |
| [<span data-ttu-id="18ed2-401">WPD \_ 資源 \_ 屬性 \_ 可以 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="18ed2-401">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                   | <span data-ttu-id="18ed2-402">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="18ed2-402">VARIANT\_TRUE</span></span>                                       |
| [<span data-ttu-id="18ed2-403">WPD \_ 資源 \_ 屬性 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="18ed2-403">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                     | <span data-ttu-id="18ed2-404">WPD \_ 物件 \_ 格式 \_ GIF</span><span class="sxs-lookup"><span data-stu-id="18ed2-404">WPD\_OBJECT\_FORMAT\_GIF</span></span>                            |
| [<span data-ttu-id="18ed2-405">WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 讀取 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="18ed2-405">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="18ed2-406">1024</span><span class="sxs-lookup"><span data-stu-id="18ed2-406">1024</span></span>                                                |
| [<span data-ttu-id="18ed2-407">WPD \_ 資源 \_ 屬性 \_ 總 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="18ed2-407">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)            | <span data-ttu-id="18ed2-408">512</span><span class="sxs-lookup"><span data-stu-id="18ed2-408">512</span></span>                                                 |



 

## <a name="mapping-rss-item-elements-to-wpd-property-values"></a><span data-ttu-id="18ed2-409">將 RSS 專案元素對應至 WPD 屬性值</span><span class="sxs-lookup"><span data-stu-id="18ed2-409">Mapping RSS Item Elements to WPD Property Values</span></span>

<span data-ttu-id="18ed2-410">下表說明上一個範例中 RSS 專案專案的值如何對應至特定的 WPD 屬性。</span><span class="sxs-lookup"><span data-stu-id="18ed2-410">The following table describes how the values in the RSS Item elements in the previous example map to particular WPD properties.</span></span>



| <span data-ttu-id="18ed2-411">WPD 屬性</span><span class="sxs-lookup"><span data-stu-id="18ed2-411">WPD Property</span></span>  | <span data-ttu-id="18ed2-412">值</span><span class="sxs-lookup"><span data-stu-id="18ed2-412">Value</span></span>                   |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18ed2-413">WPD \_ 媒體 \_ 標題</span><span class="sxs-lookup"><span data-stu-id="18ed2-413">WPD\_MEDIA\_TITLE</span></span>](media-properties.md)                                    | <span data-ttu-id="18ed2-414">數位發行</span><span class="sxs-lookup"><span data-stu-id="18ed2-414">The Digital Publication</span></span>                                                                                                          |
| [<span data-ttu-id="18ed2-415">WPD \_ 媒體 \_ 持續時間</span><span class="sxs-lookup"><span data-stu-id="18ed2-415">WPD\_MEDIA\_DURATION</span></span>](media-properties.md)                              | <span data-ttu-id="18ed2-416">10329011</span><span class="sxs-lookup"><span data-stu-id="18ed2-416">10329011</span></span>                                                                                                                         |
| [<span data-ttu-id="18ed2-417">WPD \_ MEDIA \_ 演出者</span><span class="sxs-lookup"><span data-stu-id="18ed2-417">WPD\_MEDIA\_ARTIST</span></span>](media-properties.md)                                  | <span data-ttu-id="18ed2-418">苜蓿</span><span class="sxs-lookup"><span data-stu-id="18ed2-418">Lucerne</span></span>                                                                                                                          |
| [<span data-ttu-id="18ed2-419">WPD \_ 媒體 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="18ed2-419">WPD\_MEDIA\_DESCRIPTION</span></span>](media-properties.md)                        | <span data-ttu-id="18ed2-420">線上發行集很快就會改變。</span><span class="sxs-lookup"><span data-stu-id="18ed2-420">Online publications are rapidly changing.</span></span> <span data-ttu-id="18ed2-421">發行公司的 CEO 會檢查過去5年的趨勢及其含意。</span><span class="sxs-lookup"><span data-stu-id="18ed2-421">A publishing house CEO examines the trends of the past 5 years and their implications.</span></span> |
| [<span data-ttu-id="18ed2-422">WPD \_ 媒體 \_ 目的地 \_ URL</span><span class="sxs-lookup"><span data-stu-id="18ed2-422">WPD\_MEDIA\_DESTINATION\_URL</span></span>](media-properties.md)               | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [<span data-ttu-id="18ed2-423">WPD \_ 媒體內容類型 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-423">WPD\_MEDIA\_GENRE</span></span>](media-properties.md)                                    | <span data-ttu-id="18ed2-424">新聞</span><span class="sxs-lookup"><span data-stu-id="18ed2-424">News</span></span>                                                                                                                             |
| [<span data-ttu-id="18ed2-425">WPD \_ 媒體 \_ GUID</span><span class="sxs-lookup"><span data-stu-id="18ed2-425">WPD\_MEDIA\_GUID</span></span>](media-properties.md)                                      | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [<span data-ttu-id="18ed2-426">WPD \_ 媒體 \_ 發行 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="18ed2-426">WPD\_MEDIA\_RELEASE\_DATE</span></span>](media-properties.md)                     | <span data-ttu-id="18ed2-427">週四，2006年6月1日 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="18ed2-427">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                   |
| [<span data-ttu-id="18ed2-428">WPD \_ 媒體 \_ 來源 \_ URL</span><span class="sxs-lookup"><span data-stu-id="18ed2-428">WPD\_MEDIA\_SOURCE\_URL</span></span>](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [<span data-ttu-id="18ed2-429">WPD \_ 物件 \_ 反向 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="18ed2-429">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)            | <span data-ttu-id="18ed2-430">0A1</span><span class="sxs-lookup"><span data-stu-id="18ed2-430">0A1</span></span>                                                                                                                              |
| [<span data-ttu-id="18ed2-431">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="18ed2-431">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                  | <span data-ttu-id="18ed2-432">WPD \_ 內容 \_ 類型 \_ 媒體 \_ 影像</span><span class="sxs-lookup"><span data-stu-id="18ed2-432">WPD\_CONTENT\_TYPE\_MEDIA\_IMAGE</span></span>                                                                                                 |
| [<span data-ttu-id="18ed2-433">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-433">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                | <span data-ttu-id="18ed2-434">週四，2006年6月1日 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="18ed2-434">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                   |
| [<span data-ttu-id="18ed2-435">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-435">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                  | <span data-ttu-id="18ed2-436">週四，2006年6月1日 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="18ed2-436">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                   |
| [<span data-ttu-id="18ed2-437">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="18ed2-437">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                | <span data-ttu-id="18ed2-438">週四，2006年6月1日 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="18ed2-438">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                   |
| [<span data-ttu-id="18ed2-439">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="18ed2-439">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                               | <span data-ttu-id="18ed2-440">WPD \_ 物件 \_ 格式 \_ MP3</span><span class="sxs-lookup"><span data-stu-id="18ed2-440">WPD\_OBJECT\_FORMAT\_MP3</span></span>                                                                                                         |
| [<span data-ttu-id="18ed2-441">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="18ed2-441">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                       | <span data-ttu-id="18ed2-442">會話相依。</span><span class="sxs-lookup"><span data-stu-id="18ed2-442">Session dependent.</span></span> <span data-ttu-id="18ed2-443"> (在此範例中採用 "0A2"。 ) </span><span class="sxs-lookup"><span data-stu-id="18ed2-443">(Assume "0A2" for this example.)</span></span>                                                                              |
| [<span data-ttu-id="18ed2-444">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="18ed2-444">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                   | <span data-ttu-id="18ed2-445">數位發行</span><span class="sxs-lookup"><span data-stu-id="18ed2-445">The Digital Publication</span></span>                                                                                                          |
| [<span data-ttu-id="18ed2-446">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="18ed2-446">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)     | <span data-ttu-id="18ed2-447">digital0601.mp3</span><span class="sxs-lookup"><span data-stu-id="18ed2-447">digital0601.mp3</span></span>                                                                                                                  |
| [<span data-ttu-id="18ed2-448">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="18ed2-448">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                        | <span data-ttu-id="18ed2-449">0A0</span><span class="sxs-lookup"><span data-stu-id="18ed2-449">0A0</span></span>                                                                                                                              |
| [<span data-ttu-id="18ed2-450">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="18ed2-450">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md) | <span data-ttu-id="18ed2-451">與會話無關。</span><span class="sxs-lookup"><span data-stu-id="18ed2-451">Session independent.</span></span>                                                                                                             |
| [<span data-ttu-id="18ed2-452">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="18ed2-452">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                   | <span data-ttu-id="18ed2-453">10329011</span><span class="sxs-lookup"><span data-stu-id="18ed2-453">10329011</span></span>                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="18ed2-454">相關主題</span><span class="sxs-lookup"><span data-stu-id="18ed2-454">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18ed2-455">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="18ed2-455">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 




