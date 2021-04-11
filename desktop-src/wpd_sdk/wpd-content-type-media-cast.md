---
description: WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換
ms.assetid: 368e7381-8978-421a-b450-59915f8e70e2
title: WPD_CONTENT_TYPE_MEDIA_CAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2daafb381aac802b9add130aa97e9750f30e7847
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116085"
---
# <a name="wpd_content_type_media_cast"></a><span data-ttu-id="c4b8e-103">WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換</span><span class="sxs-lookup"><span data-stu-id="c4b8e-103">WPD\_CONTENT\_TYPE\_MEDIA\_CAST</span></span>

<span data-ttu-id="c4b8e-104">描述其類型作為 WPD \_ 內容 \_ 類型媒體轉換的物件， \_ \_ 代表相關內容的集合。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-104">An object that describes its type as WPD\_CONTENT\_TYPE\_MEDIA\_CAST represents a collection of related content.</span></span>

<span data-ttu-id="c4b8e-105">Mediacast 物件可以視為將相關內容分組的容器物件，就像播放清單群組音樂一樣。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-105">A Mediacast object can be thought of as a container object that groups related content, just as a playlist groups music.</span></span> <span data-ttu-id="c4b8e-106">通常，Mediacast 物件是用來將線上發佈的媒體內容分組。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-106">Often, a Mediacast object is used to group media content that was published online.</span></span> <span data-ttu-id="c4b8e-107">例如，RSS 通道可以表示為 Mediacast 物件，其物件參考指向代表通道中每個專案的內容物件。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-107">For example, an RSS channel can be represented as a Mediacast object whose object references point to content objects that represent each item in the channel.</span></span>

<span data-ttu-id="c4b8e-108">這種類型的物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-108">This type of object supports the following properties.</span></span>



|                                                                                                                       |                                                                       |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c4b8e-109">**屬性名稱**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-109">**Property Name**</span></span>                                                                                                     | <span data-ttu-id="c4b8e-110">**必要或選擇性**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-110">**Required or Optional**</span></span>                                              |
| [<span data-ttu-id="c4b8e-111">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="c4b8e-111">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="c4b8e-112">必要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-112">Required.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-113">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="c4b8e-113">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="c4b8e-114">必要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-114">Required.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-115">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="c4b8e-115">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="c4b8e-116">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-116">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="c4b8e-117">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="c4b8e-117">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="c4b8e-118">必要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-118">Required.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-119">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="c4b8e-119">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="c4b8e-120">必要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-120">Required.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-121">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="c4b8e-121">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="c4b8e-122">必要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-122">Required.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-123">WPD \_ 物件 \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="c4b8e-123">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="c4b8e-124">如果物件是隱藏的，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-124">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="c4b8e-125">WPD \_ 物件 \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="c4b8e-125">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="c4b8e-126">如果物件為系統物件，則為必要項， (代表) 的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-126">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="c4b8e-127">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="c4b8e-127">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="c4b8e-128">如果物件至少有一個資源，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-128">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="c4b8e-129">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="c4b8e-129">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="c4b8e-130">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-130">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="c4b8e-131">不可取用的 WPD \_ 物件 \_ \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-131">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="c4b8e-132">如果物件不打算供裝置取用，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-132">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="c4b8e-133">WPD \_ 物件 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="c4b8e-133">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="c4b8e-134">如果物件具有其他物件的參考，則為必要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-134">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="c4b8e-135">WPD \_ 物件 \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="c4b8e-135">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="c4b8e-136">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-136">Optional.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-137">WPD \_ 物件 \_ 同步 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="c4b8e-137">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="c4b8e-138">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-138">Optional.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-139">WPD \_ 物件 \_ 受到 \_ DRM \_ 保護</span><span class="sxs-lookup"><span data-stu-id="c4b8e-139">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="c4b8e-140">如果物件受到 DRM 技術的保護，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-140">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="c4b8e-141">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-141">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="c4b8e-142">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-142">Optional.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-143">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-143">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="c4b8e-144">建議使用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-144">Recommended.</span></span>                                                          |
| [<span data-ttu-id="c4b8e-145">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-145">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="c4b8e-146">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-146">Optional.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-147">WPD \_ 物件 \_ 反向 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="c4b8e-147">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="c4b8e-148">如果物件是由另一個物件參考，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-148">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="c4b8e-149">WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="c4b8e-149">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="c4b8e-150">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-150">Optional.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-151">WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-151">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="c4b8e-152">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-152">Optional.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-153">WPD \_ 物件 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="c4b8e-153">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="c4b8e-154">如果可以刪除物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-154">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="c4b8e-155">WPD \_ 物件 \_ 語言 \_ 地區設定</span><span class="sxs-lookup"><span data-stu-id="c4b8e-155">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="c4b8e-156">如果無法刪除物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-156">Required if the object cannot be deleted.</span></span>                             |
| [<span data-ttu-id="c4b8e-157">WPD \_ 媒體 \_ 著作權</span><span class="sxs-lookup"><span data-stu-id="c4b8e-157">WPD\_MEDIA\_COPYRIGHT</span></span>](media-properties.md)                                                     | <span data-ttu-id="c4b8e-158">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-158">Optional.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-159">WPD \_ 媒體 \_ 家長 \_ 評等</span><span class="sxs-lookup"><span data-stu-id="c4b8e-159">WPD\_MEDIA\_PARENTAL\_RATING</span></span>](media-properties.md)                                        | <span data-ttu-id="c4b8e-160">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-160">Optional.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-161">WPD \_ 媒體 \_ 中繼 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="c4b8e-161">WPD\_MEDIA\_META\_GENRE</span></span>](media-properties.md)                                                  | <span data-ttu-id="c4b8e-162">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-162">Optional.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-163">WPD \_ 媒體 \_ 子 \_ 標題</span><span class="sxs-lookup"><span data-stu-id="c4b8e-163">WPD\_MEDIA\_SUB\_TITLE</span></span>](media-properties.md)                                                    | <span data-ttu-id="c4b8e-164">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-164">Optional.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-165">WPD \_ 媒體 \_ 發行 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="c4b8e-165">WPD\_MEDIA\_RELEASE\_DATE</span></span>](media-properties.md)                                              | <span data-ttu-id="c4b8e-166">建議使用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-166">Recommended.</span></span>                                                          |
| [<span data-ttu-id="c4b8e-167">WPD \_ 媒體 \_ 標題</span><span class="sxs-lookup"><span data-stu-id="c4b8e-167">WPD\_MEDIA\_TITLE</span></span>](media-properties.md)                                                             | <span data-ttu-id="c4b8e-168">建議使用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-168">Recommended.</span></span>                                                          |
| [<span data-ttu-id="c4b8e-169">WPD \_ 媒體 \_ 擁有者</span><span class="sxs-lookup"><span data-stu-id="c4b8e-169">WPD\_MEDIA\_OWNER</span></span>](media-properties.md)                                                             | <span data-ttu-id="c4b8e-170">建議使用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-170">Recommended.</span></span>                                                          |
| [<span data-ttu-id="c4b8e-171">WPD \_ 媒體 \_ 管理 \_ 編輯器</span><span class="sxs-lookup"><span data-stu-id="c4b8e-171">WPD\_MEDIA\_MANAGING\_EDITOR</span></span>](media-properties.md)                                        | <span data-ttu-id="c4b8e-172">建議使用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-172">Recommended.</span></span>                                                          |
| [<span data-ttu-id="c4b8e-173">WPD \_ 媒體 \_ 管理員</span><span class="sxs-lookup"><span data-stu-id="c4b8e-173">WPD\_MEDIA\_WEBMASTER</span></span>](media-properties.md)                                                     | <span data-ttu-id="c4b8e-174">建議使用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-174">Recommended.</span></span>                                                          |
| [<span data-ttu-id="c4b8e-175">WPD \_ 媒體 \_ 來源 \_ URL</span><span class="sxs-lookup"><span data-stu-id="c4b8e-175">WPD\_MEDIA\_SOURCE\_URL</span></span>](media-properties.md)                                                  | <span data-ttu-id="c4b8e-176">建議使用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-176">Recommended.</span></span>                                                          |
| [<span data-ttu-id="c4b8e-177">WPD \_ 媒體 \_ 目的地 \_ URL</span><span class="sxs-lookup"><span data-stu-id="c4b8e-177">WPD\_MEDIA\_DESTINATION\_URL</span></span>](media-properties.md)                                        | <span data-ttu-id="c4b8e-178">建議使用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-178">Recommended.</span></span>                                                          |
| [<span data-ttu-id="c4b8e-179">WPD \_ 媒體 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="c4b8e-179">WPD\_MEDIA\_DESCRIPTION</span></span>](media-properties.md)                                                 | <span data-ttu-id="c4b8e-180">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-180">Optional.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-181">WPD \_ 媒體內容類型 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-181">WPD\_MEDIA\_GENRE</span></span>](media-properties.md)                                                             | <span data-ttu-id="c4b8e-182">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-182">Optional.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-183">WPD \_ 媒體 \_ 物件 \_ 書簽</span><span class="sxs-lookup"><span data-stu-id="c4b8e-183">WPD\_MEDIA\_OBJECT\_BOOKMARK</span></span>](media-properties.md)                                        | <span data-ttu-id="c4b8e-184">建議</span><span class="sxs-lookup"><span data-stu-id="c4b8e-184">Recommended</span></span>                                                           |
| [<span data-ttu-id="c4b8e-185">WPD \_ 媒體 \_ 上次 \_ 組建 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="c4b8e-185">WPD\_MEDIA\_LAST\_BUILD\_DATE</span></span>](media-properties.md)                                       | <span data-ttu-id="c4b8e-186">建議使用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-186">Recommended.</span></span>                                                          |
| [<span data-ttu-id="c4b8e-187">WPD \_ 媒體 \_ 生存 \_ 時間 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-187">WPD\_MEDIA\_TIME\_TO\_LIVE</span></span>](media-properties.md)                                             | <span data-ttu-id="c4b8e-188">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-188">Optional.</span></span>                                                             |
| [<span data-ttu-id="c4b8e-189">WPD \_ 媒體 \_ 子 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="c4b8e-189">WPD\_MEDIA\_SUB\_DESCRIPTION</span></span>](object-properties.md)                                                                 | <span data-ttu-id="c4b8e-190">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-190">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="c4b8e-191">一般資源</span><span class="sxs-lookup"><span data-stu-id="c4b8e-191">Typical Resources</span></span>

<span data-ttu-id="c4b8e-192">這些物件通常包含下列資源。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-192">These objects typically include the following resources.</span></span>



| <span data-ttu-id="c4b8e-193">資源名稱</span><span class="sxs-lookup"><span data-stu-id="c4b8e-193">Resource Name</span></span>                                               | <span data-ttu-id="c4b8e-194">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="c4b8e-194">Required or Optional</span></span> | <span data-ttu-id="c4b8e-195">Description</span><span class="sxs-lookup"><span data-stu-id="c4b8e-195">Description</span></span>                                                                                                                 |
|-------------------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4b8e-196">**WPD \_ 資源 \_ 預設**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-196">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md)      | <span data-ttu-id="c4b8e-197">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-197">Optional.</span></span>            | <span data-ttu-id="c4b8e-198">包含 mediacast 檔案資料。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-198">Contains the mediacast file data.</span></span> <span data-ttu-id="c4b8e-199">例如，如果此 mediacast 代表 RSS 通道，這可能是 RSS 檔。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-199">For example, if this mediacast represents an RSS channel, this might be the RSS document.</span></span> |
| [<span data-ttu-id="c4b8e-200">**WPD \_ 資源 \_ 縮圖**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-200">**WPD\_RESOURCE\_THUMBNAIL**</span></span>](wpd-resource-thumbnail.md)  | <span data-ttu-id="c4b8e-201">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-201">Optional.</span></span>            | <span data-ttu-id="c4b8e-202">包含表示此 mediacast 的縮圖。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-202">Contains the thumbnail representing this mediacast.</span></span>                                                                         |
| [<span data-ttu-id="c4b8e-203">**WPD \_ 資源 \_ 專輯 \_ 封面**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-203">**WPD\_RESOURCE\_ALBUM\_ART**</span></span>](wpd-resource-album-art.md) | <span data-ttu-id="c4b8e-204">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-204">Optional.</span></span>            | <span data-ttu-id="c4b8e-205">包含此 mediacast 的作品。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-205">Contains the artwork for this mediacast.</span></span>                                                                                    |



 

## <a name="mapping-of-rss-elements-and-mediacast-properties"></a><span data-ttu-id="c4b8e-206">RSS 元素與 Mediacast 屬性的對應</span><span class="sxs-lookup"><span data-stu-id="c4b8e-206">Mapping of RSS Elements and Mediacast properties</span></span>

<span data-ttu-id="c4b8e-207">RSS 通道可以表示為 Mediacast 物件，其參考指向代表特定通道中每個專案的內容物件。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-207">An RSS channel can be represented as a Mediacast object whose references point to content objects representing each item in a given channel.</span></span>

<span data-ttu-id="c4b8e-208">RSS 饋送中的元素具有下列階層和屬性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-208">The elements in an RSS feed have the following hierarchy and attributes.</span></span>


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



<span data-ttu-id="c4b8e-209">下表列出 RSS 摘要中的通道元素，以及對應的 WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換屬性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-209">The following table lists the channel elements in an RSS feed and the corresponding WPD\_CONTENT\_TYPE\_MEDIA\_CAST properties.</span></span>



|                     |                          |                                                                                 |
|---------------------|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="c4b8e-210">**Channel 元素**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-210">**Channel Element**</span></span> | <span data-ttu-id="c4b8e-211">**RSS 饋送需求**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-211">**RSS Feed Requirement**</span></span> | <span data-ttu-id="c4b8e-212">**對應的 Mediacast 屬性**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-212">**Corresponding Mediacast Property**</span></span>                                            |
| <span data-ttu-id="c4b8e-213">category</span><span class="sxs-lookup"><span data-stu-id="c4b8e-213">category</span></span>            | <span data-ttu-id="c4b8e-214">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-214">Optional.</span></span>                | [<span data-ttu-id="c4b8e-215">WPD \_ 媒體內容類型 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-215">WPD\_MEDIA\_GENRE</span></span>](media-properties.md)                       |
| <span data-ttu-id="c4b8e-216">cloud</span><span class="sxs-lookup"><span data-stu-id="c4b8e-216">cloud</span></span>               | <span data-ttu-id="c4b8e-217">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-217">Not applicable.</span></span>          | <span data-ttu-id="c4b8e-218">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-218">Not applicable.</span></span>                                                                 |
| <span data-ttu-id="c4b8e-219">著作權</span><span class="sxs-lookup"><span data-stu-id="c4b8e-219">copyright</span></span>           | <span data-ttu-id="c4b8e-220">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-220">Optional.</span></span>                | [<span data-ttu-id="c4b8e-221">WPD \_ 媒體 \_ 著作權</span><span class="sxs-lookup"><span data-stu-id="c4b8e-221">WPD\_MEDIA\_COPYRIGHT</span></span>](media-properties.md)               |
| <span data-ttu-id="c4b8e-222">description</span><span class="sxs-lookup"><span data-stu-id="c4b8e-222">description</span></span>         | <span data-ttu-id="c4b8e-223">必要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-223">Required.</span></span>                | [<span data-ttu-id="c4b8e-224">WPD \_ 媒體 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="c4b8e-224">WPD\_MEDIA\_DESCRIPTION</span></span>](media-properties.md)           |
| <span data-ttu-id="c4b8e-225">docs</span><span class="sxs-lookup"><span data-stu-id="c4b8e-225">docs</span></span>                | <span data-ttu-id="c4b8e-226">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-226">Not applicable.</span></span>          | <span data-ttu-id="c4b8e-227">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-227">Not applicable.</span></span>                                                                 |
| <span data-ttu-id="c4b8e-228">產生器</span><span class="sxs-lookup"><span data-stu-id="c4b8e-228">generator</span></span>           | <span data-ttu-id="c4b8e-229">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-229">Not applicable.</span></span>          | <span data-ttu-id="c4b8e-230">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-230">Not applicable.</span></span>                                                                 |
| <span data-ttu-id="c4b8e-231">語言</span><span class="sxs-lookup"><span data-stu-id="c4b8e-231">language</span></span>            | <span data-ttu-id="c4b8e-232">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-232">Not applicable.</span></span>          | <span data-ttu-id="c4b8e-233">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-233">Not applicable.</span></span>                                                                 |
| <span data-ttu-id="c4b8e-234">lastBuildDate</span><span class="sxs-lookup"><span data-stu-id="c4b8e-234">lastBuildDate</span></span>       | <span data-ttu-id="c4b8e-235">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-235">Optional.</span></span>                | [<span data-ttu-id="c4b8e-236">WPD \_ 媒體 \_ 上次 \_ 組建 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="c4b8e-236">WPD\_MEDIA\_LAST\_BUILD\_DATE</span></span>](media-properties.md) |
| <span data-ttu-id="c4b8e-237">link</span><span class="sxs-lookup"><span data-stu-id="c4b8e-237">link</span></span>                | <span data-ttu-id="c4b8e-238">必要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-238">Required.</span></span>                | [<span data-ttu-id="c4b8e-239">WPD \_ 媒體 \_ 目的地 \_ URL</span><span class="sxs-lookup"><span data-stu-id="c4b8e-239">WPD\_MEDIA\_DESTINATION\_URL</span></span>](media-properties.md)  |
| <span data-ttu-id="c4b8e-240">managingEditor</span><span class="sxs-lookup"><span data-stu-id="c4b8e-240">managingEditor</span></span>      | <span data-ttu-id="c4b8e-241">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-241">Optional.</span></span>                | [<span data-ttu-id="c4b8e-242">WPD \_ 媒體 \_ 管理 \_ 編輯器</span><span class="sxs-lookup"><span data-stu-id="c4b8e-242">WPD\_MEDIA\_MANAGING\_EDITOR</span></span>](media-properties.md)  |
| <span data-ttu-id="c4b8e-243">pubDate</span><span class="sxs-lookup"><span data-stu-id="c4b8e-243">pubDate</span></span>             | <span data-ttu-id="c4b8e-244">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-244">Optional.</span></span>                | [<span data-ttu-id="c4b8e-245">WPD \_ 媒體 \_ 發行 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="c4b8e-245">WPD\_MEDIA\_RELEASE\_DATE</span></span>](media-properties.md)        |
| <span data-ttu-id="c4b8e-246">rating</span><span class="sxs-lookup"><span data-stu-id="c4b8e-246">rating</span></span>              | <span data-ttu-id="c4b8e-247">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-247">Not applicable.</span></span>          | <span data-ttu-id="c4b8e-248">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-248">Not applicable.</span></span>                                                                 |
| <span data-ttu-id="c4b8e-249">skipDays</span><span class="sxs-lookup"><span data-stu-id="c4b8e-249">skipDays</span></span>            | <span data-ttu-id="c4b8e-250">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-250">Not applicable.</span></span>          | <span data-ttu-id="c4b8e-251">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-251">Not applicable.</span></span>                                                                 |
| <span data-ttu-id="c4b8e-252">skipHours</span><span class="sxs-lookup"><span data-stu-id="c4b8e-252">skipHours</span></span>           | <span data-ttu-id="c4b8e-253">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-253">Not applicable.</span></span>          | <span data-ttu-id="c4b8e-254">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-254">Not applicable.</span></span>                                                                 |
| <span data-ttu-id="c4b8e-255">>textinput</span><span class="sxs-lookup"><span data-stu-id="c4b8e-255">textInput</span></span>           | <span data-ttu-id="c4b8e-256">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-256">Not applicable.</span></span>          | <span data-ttu-id="c4b8e-257">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-257">Not applicable.</span></span>                                                                 |
| <span data-ttu-id="c4b8e-258">title</span><span class="sxs-lookup"><span data-stu-id="c4b8e-258">title</span></span>               | <span data-ttu-id="c4b8e-259">必要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-259">Required.</span></span>                | [<span data-ttu-id="c4b8e-260">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="c4b8e-260">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                      |
| <span data-ttu-id="c4b8e-261">ttl</span><span class="sxs-lookup"><span data-stu-id="c4b8e-261">ttl</span></span>                 | <span data-ttu-id="c4b8e-262">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-262">Optional.</span></span>                | [<span data-ttu-id="c4b8e-263">WPD \_ 媒體 \_ 生存 \_ 時間 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-263">WPD\_MEDIA\_TIME\_TO\_LIVE</span></span>](media-properties.md)       |
| <span data-ttu-id="c4b8e-264">站長</span><span class="sxs-lookup"><span data-stu-id="c4b8e-264">webMaster</span></span>           | <span data-ttu-id="c4b8e-265">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-265">Optional.</span></span>                | [<span data-ttu-id="c4b8e-266">WPD \_ 媒體 \_ 管理員</span><span class="sxs-lookup"><span data-stu-id="c4b8e-266">WPD\_MEDIA\_WEBMASTER</span></span>](media-properties.md)               |



 

<span data-ttu-id="c4b8e-267">下表列出 RSS 摘要中的影像元素，以及對應的 WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換屬性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-267">The following table lists the image elements in an RSS feed and the corresponding WPD\_CONTENT\_TYPE\_MEDIA\_CAST properties.</span></span>



|                   |                          |                                                                                |
|-------------------|--------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="c4b8e-268">**Image 元素**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-268">**Image Element**</span></span> | <span data-ttu-id="c4b8e-269">**RSS 饋送需求**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-269">**RSS Feed Requirement**</span></span> | <span data-ttu-id="c4b8e-270">**Mediacast 屬性**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-270">**Mediacast Property**</span></span>                                                         |
| <span data-ttu-id="c4b8e-271">description</span><span class="sxs-lookup"><span data-stu-id="c4b8e-271">description</span></span>       | <span data-ttu-id="c4b8e-272">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-272">Optional.</span></span>                | [<span data-ttu-id="c4b8e-273">WPD \_ 媒體 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="c4b8e-273">WPD\_MEDIA\_DESCRIPTION</span></span>](media-properties.md)          |
| <span data-ttu-id="c4b8e-274">身高</span><span class="sxs-lookup"><span data-stu-id="c4b8e-274">height</span></span>            | <span data-ttu-id="c4b8e-275">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-275">Optional.</span></span>                | [<span data-ttu-id="c4b8e-276">WPD \_ 媒體 \_ 高度</span><span class="sxs-lookup"><span data-stu-id="c4b8e-276">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                    |
| <span data-ttu-id="c4b8e-277">link</span><span class="sxs-lookup"><span data-stu-id="c4b8e-277">link</span></span>              | <span data-ttu-id="c4b8e-278">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-278">Optional.</span></span>                | [<span data-ttu-id="c4b8e-279">WPD \_ 媒體 \_ 目的地 \_ URL</span><span class="sxs-lookup"><span data-stu-id="c4b8e-279">WPD\_MEDIA\_DESTINATION\_URL</span></span>](media-properties.md) |
| <span data-ttu-id="c4b8e-280">title</span><span class="sxs-lookup"><span data-stu-id="c4b8e-280">title</span></span>             | <span data-ttu-id="c4b8e-281">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-281">Optional.</span></span>                | [<span data-ttu-id="c4b8e-282">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="c4b8e-282">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                     |
| <span data-ttu-id="c4b8e-283">url</span><span class="sxs-lookup"><span data-stu-id="c4b8e-283">url</span></span>               | <span data-ttu-id="c4b8e-284">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-284">Optional.</span></span>                | [<span data-ttu-id="c4b8e-285">WPD \_ 媒體 \_ 來源 \_ URL</span><span class="sxs-lookup"><span data-stu-id="c4b8e-285">WPD\_MEDIA\_SOURCE\_URL</span></span>](media-properties.md)           |
| <span data-ttu-id="c4b8e-286">width</span><span class="sxs-lookup"><span data-stu-id="c4b8e-286">width</span></span>             | <span data-ttu-id="c4b8e-287">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-287">Optional.</span></span>                | [<span data-ttu-id="c4b8e-288">WPD \_ 媒體 \_ 寬度</span><span class="sxs-lookup"><span data-stu-id="c4b8e-288">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                      |



 

<span data-ttu-id="c4b8e-289">下表列出 RSS 摘要中的專案元素，以及對應的 WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換屬性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-289">The following table lists the item elements in an RSS feed and the corresponding WPD\_CONTENT\_TYPE\_MEDIA\_CAST properties.</span></span>



|                  |               |                          |                                                                                |
|------------------|---------------|--------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="c4b8e-290">**Item 元素**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-290">**Item Element**</span></span> | <span data-ttu-id="c4b8e-291">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-291">**Attribute**</span></span> | <span data-ttu-id="c4b8e-292">**RSS 饋送需求**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-292">**RSS Feed Requirement**</span></span> | <span data-ttu-id="c4b8e-293">**Mediacast 屬性**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-293">**Mediacast Property**</span></span>                                                         |
| <span data-ttu-id="c4b8e-294">編寫</span><span class="sxs-lookup"><span data-stu-id="c4b8e-294">author</span></span>           |               | <span data-ttu-id="c4b8e-295">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-295">Optional.</span></span>                | [<span data-ttu-id="c4b8e-296">WPD \_ MEDIA \_ 演出者</span><span class="sxs-lookup"><span data-stu-id="c4b8e-296">WPD\_MEDIA\_ARTIST</span></span>](media-properties.md)                    |
| <span data-ttu-id="c4b8e-297">category</span><span class="sxs-lookup"><span data-stu-id="c4b8e-297">category</span></span>         |               | <span data-ttu-id="c4b8e-298">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-298">Optional.</span></span>                | [<span data-ttu-id="c4b8e-299">WPD \_ 媒體內容類型 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-299">WPD\_MEDIA\_GENRE</span></span>](media-properties.md)                      |
|                  | <span data-ttu-id="c4b8e-300">網域</span><span class="sxs-lookup"><span data-stu-id="c4b8e-300">domain</span></span>        | <span data-ttu-id="c4b8e-301">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-301">Not applicable.</span></span>          | <span data-ttu-id="c4b8e-302">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-302">Not applicable.</span></span>                                                                |
| <span data-ttu-id="c4b8e-303">description</span><span class="sxs-lookup"><span data-stu-id="c4b8e-303">description</span></span>      |               | <span data-ttu-id="c4b8e-304">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-304">Optional.</span></span>                | [<span data-ttu-id="c4b8e-305">WPD \_ 媒體 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="c4b8e-305">WPD\_MEDIA\_DESCRIPTION</span></span>](media-properties.md)          |
| <span data-ttu-id="c4b8e-306">外殼</span><span class="sxs-lookup"><span data-stu-id="c4b8e-306">enclosure</span></span>        |               | <span data-ttu-id="c4b8e-307">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-307">Optional.</span></span>                |                                                                                |
|                  | <span data-ttu-id="c4b8e-308">url</span><span class="sxs-lookup"><span data-stu-id="c4b8e-308">url</span></span>           | <span data-ttu-id="c4b8e-309">必要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-309">Required.</span></span>                | [<span data-ttu-id="c4b8e-310">WPD \_ 媒體 \_ 來源 \_ URL</span><span class="sxs-lookup"><span data-stu-id="c4b8e-310">WPD\_MEDIA\_SOURCE\_URL</span></span>](media-properties.md)           |
|                  | <span data-ttu-id="c4b8e-311">長度</span><span class="sxs-lookup"><span data-stu-id="c4b8e-311">length</span></span>        | <span data-ttu-id="c4b8e-312">必要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-312">Required.</span></span>                | [<span data-ttu-id="c4b8e-313">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="c4b8e-313">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                     |
|                  | <span data-ttu-id="c4b8e-314">類型</span><span class="sxs-lookup"><span data-stu-id="c4b8e-314">type</span></span>          | <span data-ttu-id="c4b8e-315">必要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-315">Required.</span></span>                | <span data-ttu-id="c4b8e-316"> (MIME 類型應對應至屬性內容類型。 ) </span><span class="sxs-lookup"><span data-stu-id="c4b8e-316">(The MIME type should be mapped to the property content type.)</span></span>                 |
| <span data-ttu-id="c4b8e-317">guid</span><span class="sxs-lookup"><span data-stu-id="c4b8e-317">guid</span></span>             |               | <span data-ttu-id="c4b8e-318">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-318">Optional.</span></span>                | [<span data-ttu-id="c4b8e-319">WPD \_ 媒體 \_ GUID</span><span class="sxs-lookup"><span data-stu-id="c4b8e-319">WPD\_MEDIA\_GUID</span></span>](media-properties.md)                        |
|                  | <span data-ttu-id="c4b8e-320">isPermaLink</span><span class="sxs-lookup"><span data-stu-id="c4b8e-320">isPermaLink</span></span>   | <span data-ttu-id="c4b8e-321">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-321">Not applicable.</span></span>          | <span data-ttu-id="c4b8e-322">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-322">Not applicable.</span></span>                                                                |
| <span data-ttu-id="c4b8e-323">link</span><span class="sxs-lookup"><span data-stu-id="c4b8e-323">link</span></span>             |               | <span data-ttu-id="c4b8e-324">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-324">Optional.</span></span>                | [<span data-ttu-id="c4b8e-325">WPD \_ 媒體 \_ 目的地 \_ URL</span><span class="sxs-lookup"><span data-stu-id="c4b8e-325">WPD\_MEDIA\_DESTINATION\_URL</span></span>](media-properties.md) |
| <span data-ttu-id="c4b8e-326">pubDate</span><span class="sxs-lookup"><span data-stu-id="c4b8e-326">pubDate</span></span>          |               | <span data-ttu-id="c4b8e-327">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-327">Optional.</span></span>                | [<span data-ttu-id="c4b8e-328">WPD \_ 媒體 \_ 發行 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="c4b8e-328">WPD\_MEDIA\_RELEASE\_DATE</span></span>](media-properties.md)       |
| <span data-ttu-id="c4b8e-329">source</span><span class="sxs-lookup"><span data-stu-id="c4b8e-329">source</span></span>           |               | <span data-ttu-id="c4b8e-330">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-330">Not applicable.</span></span>          | <span data-ttu-id="c4b8e-331">不適用。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-331">Not applicable.</span></span>                                                                |
| <span data-ttu-id="c4b8e-332">title</span><span class="sxs-lookup"><span data-stu-id="c4b8e-332">title</span></span>            |               | <span data-ttu-id="c4b8e-333">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-333">Optional.</span></span>                | [<span data-ttu-id="c4b8e-334">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="c4b8e-334">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                     |



 

<span data-ttu-id="c4b8e-335">下列範例顯示發行公司的 CEO 所提供之虛構播客的完整 RSS 摘要。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-335">The following example shows a complete RSS feed for a fictitious podcast supplied by the CEO of a publishing company.</span></span>


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



## <a name="mapping-rss-channel-elements-to-wpd-property-values"></a><span data-ttu-id="c4b8e-336">將 RSS 通道元素對應至 WPD 屬性值</span><span class="sxs-lookup"><span data-stu-id="c4b8e-336">Mapping RSS Channel Elements to WPD Property Values</span></span>

<span data-ttu-id="c4b8e-337">下表說明上一個範例中 RSS 通道元素的值如何對應至特定的 WPD 屬性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-337">The following table describes how the values in the RSS channel elements in the previous example map to particular WPD properties.</span></span>



|                                                                                              |                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4b8e-338">**WPD 屬性**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-338">**WPD Property**</span></span>                                                                             | <span data-ttu-id="c4b8e-339">**值**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-339">**Value**</span></span>                                                                                     |
| [<span data-ttu-id="c4b8e-340">WPD \_ 媒體 \_ 著作權</span><span class="sxs-lookup"><span data-stu-id="c4b8e-340">WPD\_MEDIA\_COPYRIGHT</span></span>](media-properties.md)                            | <span data-ttu-id="c4b8e-341">2006 Lucerne 發行 LP，LLLP。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-341">2006 Lucerne Publishing LP, LLLP.</span></span> <span data-ttu-id="c4b8e-342">著作權所有，並保留一切權利。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-342">All Rights Reserved.</span></span>                                        |
| [<span data-ttu-id="c4b8e-343">WPD \_ 媒體 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="c4b8e-343">WPD\_MEDIA\_DESCRIPTION</span></span>](media-properties.md)                        | <span data-ttu-id="c4b8e-344">Lucerne 發佈 CEO Peter Bankov 會查看線上發行物的最新趨勢。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-344">Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</span></span> |
| [<span data-ttu-id="c4b8e-345">WPD \_ 媒體 \_ 目的地 \_ URL</span><span class="sxs-lookup"><span data-stu-id="c4b8e-345">WPD\_MEDIA\_DESTINATION\_URL</span></span>](media-properties.md)               | https://www.lucernepublishing.com/services/podcasting                                          |
| [<span data-ttu-id="c4b8e-346">WPD \_ 媒體內容類型 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-346">WPD\_MEDIA\_GENRE</span></span>](media-properties.md)                                    | <span data-ttu-id="c4b8e-347">新聞</span><span class="sxs-lookup"><span data-stu-id="c4b8e-347">News</span></span>                                                                                          |
| [<span data-ttu-id="c4b8e-348">WPD \_ 媒體 \_ 上次 \_ 組建 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="c4b8e-348">WPD\_MEDIA\_LAST\_BUILD\_DATE</span></span>](media-properties.md)              | <span data-ttu-id="c4b8e-349">2006年6月9日，14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="c4b8e-349">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="c4b8e-350">WPD \_ 媒體 \_ 管理 \_ 編輯器</span><span class="sxs-lookup"><span data-stu-id="c4b8e-350">WPD\_MEDIA\_MANAGING\_EDITOR</span></span>](media-properties.md)               | someone@example.com                                                                           |
| [<span data-ttu-id="c4b8e-351">WPD \_ 媒體 \_ 發行 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="c4b8e-351">WPD\_MEDIA\_RELEASE\_DATE</span></span>](media-properties.md)                     | <span data-ttu-id="c4b8e-352">2006年6月9日，14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="c4b8e-352">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="c4b8e-353">WPD \_ 媒體 \_ 生存 \_ 時間 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-353">WPD\_MEDIA\_TIME\_TO\_LIVE</span></span>](media-properties.md)                    | <span data-ttu-id="c4b8e-354">240</span><span class="sxs-lookup"><span data-stu-id="c4b8e-354">240</span></span>                                                                                           |
| [<span data-ttu-id="c4b8e-355">WPD \_ 媒體 \_ 標題</span><span class="sxs-lookup"><span data-stu-id="c4b8e-355">WPD\_MEDIA\_TITLE</span></span>](media-properties.md)                                    | <span data-ttu-id="c4b8e-356">數位發行</span><span class="sxs-lookup"><span data-stu-id="c4b8e-356">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="c4b8e-357">WPD \_ 媒體 \_ 來源 \_ URL</span><span class="sxs-lookup"><span data-stu-id="c4b8e-357">WPD\_MEDIA\_SOURCE\_URL</span></span>](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publication/rss.xml                  |
| [<span data-ttu-id="c4b8e-358">WPD \_ 媒體 \_ 管理員</span><span class="sxs-lookup"><span data-stu-id="c4b8e-358">WPD\_MEDIA\_WEBMASTER</span></span>](media-properties.md)                            | someone@example.com                                                                           |
| [<span data-ttu-id="c4b8e-359">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="c4b8e-359">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                  | <span data-ttu-id="c4b8e-360">WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換</span><span class="sxs-lookup"><span data-stu-id="c4b8e-360">WPD\_CONTENT\_TYPE\_MEDIA\_CAST</span></span>                                                               |
| [<span data-ttu-id="c4b8e-361">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-361">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                | <span data-ttu-id="c4b8e-362">2006年6月9日，14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="c4b8e-362">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="c4b8e-363">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-363">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                  | <span data-ttu-id="c4b8e-364">2006年6月9日，14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="c4b8e-364">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="c4b8e-365">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-365">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                | <span data-ttu-id="c4b8e-366">2006年6月9日，14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="c4b8e-366">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="c4b8e-367">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="c4b8e-367">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                               | <span data-ttu-id="c4b8e-368">WPD \_ 物件 \_ 格式 \_ 抽象 \_ 媒體 \_ 轉換</span><span class="sxs-lookup"><span data-stu-id="c4b8e-368">WPD\_OBJECT\_FORMAT\_ABSTRACT\_MEDIA\_CAST</span></span>                                                    |
| [<span data-ttu-id="c4b8e-369">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="c4b8e-369">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                       | <span data-ttu-id="c4b8e-370">會話相依值。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-370">Session dependent value.</span></span>                                                                      |
| [<span data-ttu-id="c4b8e-371">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="c4b8e-371">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                   | <span data-ttu-id="c4b8e-372">數位發行</span><span class="sxs-lookup"><span data-stu-id="c4b8e-372">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="c4b8e-373">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="c4b8e-373">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)     | <span data-ttu-id="c4b8e-374">數位發行</span><span class="sxs-lookup"><span data-stu-id="c4b8e-374">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="c4b8e-375">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="c4b8e-375">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                        | <span data-ttu-id="c4b8e-376">MyPodcasts (裝置上的虛構播客資料夾) 。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-376">MyPodcasts (a fictitious podcast folder on the device).</span></span> <span data-ttu-id="c4b8e-377">針對此範例，請採用 "0A0"。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-377">Assume "0A0" for this example.</span></span>        |
| [<span data-ttu-id="c4b8e-378">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="c4b8e-378">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md) | <span data-ttu-id="c4b8e-379">會話獨立值。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-379">Session independent value.</span></span> <span data-ttu-id="c4b8e-380"> (在此範例中採用 "0A1"。 ) </span><span class="sxs-lookup"><span data-stu-id="c4b8e-380">(Assume "0A1" for this example.)</span></span>                                   |
| [<span data-ttu-id="c4b8e-381">WPD \_ 物件 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="c4b8e-381">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                       | <span data-ttu-id="c4b8e-382">N 個專案的0A2</span><span class="sxs-lookup"><span data-stu-id="c4b8e-382">0A2  for N items</span></span><br/>                                                                   |
| [<span data-ttu-id="c4b8e-383">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="c4b8e-383">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                   | <span data-ttu-id="c4b8e-384">13790</span><span class="sxs-lookup"><span data-stu-id="c4b8e-384">13,790</span></span>                                                                                        |



 

## <a name="mapping-rss-image-elements-to-wpd-property-values"></a><span data-ttu-id="c4b8e-385">將 RSS 影像元素對應至 WPD 屬性值</span><span class="sxs-lookup"><span data-stu-id="c4b8e-385">Mapping RSS Image Elements to WPD Property Values</span></span>

<span data-ttu-id="c4b8e-386">下表說明上一個範例中 RSS 影像元素的值如何對應至特定的 WPD 屬性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-386">The following table describes how the values in the RSS Image elements in the previous example map to particular WPD properties.</span></span>



|                                                                                                                         |                                                     |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="c4b8e-387">**WPD 屬性**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-387">**WPD Property**</span></span>                                                                                                        | <span data-ttu-id="c4b8e-388">**值**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-388">**Value**</span></span>                                           |
| [<span data-ttu-id="c4b8e-389">WPD \_ 媒體 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="c4b8e-389">WPD\_MEDIA\_DESCRIPTION</span></span>](media-properties.md)                                                   | <span data-ttu-id="c4b8e-390">Lucerne 標誌</span><span class="sxs-lookup"><span data-stu-id="c4b8e-390">Lucerne Logo</span></span>                                        |
| [<span data-ttu-id="c4b8e-391">WPD \_ 媒體 \_ 目的地 \_ URL</span><span class="sxs-lookup"><span data-stu-id="c4b8e-391">WPD\_MEDIA\_DESTINATION\_URL</span></span>](media-properties.md)                                          | https://www.lucernepublishing.com/community/podcasts |
| [<span data-ttu-id="c4b8e-392">WPD \_ 媒體 \_ 高度</span><span class="sxs-lookup"><span data-stu-id="c4b8e-392">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                             | <span data-ttu-id="c4b8e-393">300</span><span class="sxs-lookup"><span data-stu-id="c4b8e-393">300</span></span>                                                 |
| [<span data-ttu-id="c4b8e-394">WPD \_ 媒體 \_ 來源 \_ URL</span><span class="sxs-lookup"><span data-stu-id="c4b8e-394">WPD\_MEDIA\_SOURCE\_URL</span></span>](media-properties.md)                                                    | https://www.lucernepublishing.com/images/logo.gif    |
| [<span data-ttu-id="c4b8e-395">WPD \_ 媒體 \_ 寬度</span><span class="sxs-lookup"><span data-stu-id="c4b8e-395">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                               | <span data-ttu-id="c4b8e-396">300</span><span class="sxs-lookup"><span data-stu-id="c4b8e-396">300</span></span>                                                 |
| [<span data-ttu-id="c4b8e-397">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="c4b8e-397">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                              | <span data-ttu-id="c4b8e-398">Lucerne 發行</span><span class="sxs-lookup"><span data-stu-id="c4b8e-398">Lucerne Publishing</span></span>                                  |
| [<span data-ttu-id="c4b8e-399">WPD \_ 資源 \_ 屬性 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="c4b8e-399">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                               | <span data-ttu-id="c4b8e-400">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="c4b8e-400">VARIANT\_TRUE</span></span>                                       |
| [<span data-ttu-id="c4b8e-401">WPD \_ 資源 \_ 屬性 \_ 可以 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="c4b8e-401">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                   | <span data-ttu-id="c4b8e-402">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="c4b8e-402">VARIANT\_TRUE</span></span>                                       |
| [<span data-ttu-id="c4b8e-403">WPD \_ 資源 \_ 屬性 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="c4b8e-403">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                     | <span data-ttu-id="c4b8e-404">WPD \_ 物件 \_ 格式 \_ GIF</span><span class="sxs-lookup"><span data-stu-id="c4b8e-404">WPD\_OBJECT\_FORMAT\_GIF</span></span>                            |
| [<span data-ttu-id="c4b8e-405">WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 讀取 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="c4b8e-405">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="c4b8e-406">1024</span><span class="sxs-lookup"><span data-stu-id="c4b8e-406">1024</span></span>                                                |
| [<span data-ttu-id="c4b8e-407">WPD \_ 資源 \_ 屬性 \_ 總 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="c4b8e-407">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)            | <span data-ttu-id="c4b8e-408">512</span><span class="sxs-lookup"><span data-stu-id="c4b8e-408">512</span></span>                                                 |



 

## <a name="mapping-rss-item-elements-to-wpd-property-values"></a><span data-ttu-id="c4b8e-409">將 RSS 專案元素對應至 WPD 屬性值</span><span class="sxs-lookup"><span data-stu-id="c4b8e-409">Mapping RSS Item Elements to WPD Property Values</span></span>

<span data-ttu-id="c4b8e-410">下表說明上一個範例中 RSS 專案專案的值如何對應至特定的 WPD 屬性。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-410">The following table describes how the values in the RSS Item elements in the previous example map to particular WPD properties.</span></span>



|                                                                                              |                                                                                                                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4b8e-411">**WPD 屬性**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-411">**WPD Property**</span></span><br/>                                                                  | <span data-ttu-id="c4b8e-412">**值**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-412">**Value**</span></span>                                                                                                                        |
| [<span data-ttu-id="c4b8e-413">WPD \_ 媒體 \_ 標題</span><span class="sxs-lookup"><span data-stu-id="c4b8e-413">WPD\_MEDIA\_TITLE</span></span>](media-properties.md)                                    | <span data-ttu-id="c4b8e-414">數位發行</span><span class="sxs-lookup"><span data-stu-id="c4b8e-414">The Digital Publication</span></span>                                                                                                          |
| [<span data-ttu-id="c4b8e-415">WPD \_ 媒體 \_ 持續時間</span><span class="sxs-lookup"><span data-stu-id="c4b8e-415">WPD\_MEDIA\_DURATION</span></span>](media-properties.md)                              | <span data-ttu-id="c4b8e-416">10329011</span><span class="sxs-lookup"><span data-stu-id="c4b8e-416">10329011</span></span>                                                                                                                         |
| [<span data-ttu-id="c4b8e-417">WPD \_ MEDIA \_ 演出者</span><span class="sxs-lookup"><span data-stu-id="c4b8e-417">WPD\_MEDIA\_ARTIST</span></span>](media-properties.md)                                  | <span data-ttu-id="c4b8e-418">苜蓿</span><span class="sxs-lookup"><span data-stu-id="c4b8e-418">Lucerne</span></span>                                                                                                                          |
| [<span data-ttu-id="c4b8e-419">WPD \_ 媒體 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="c4b8e-419">WPD\_MEDIA\_DESCRIPTION</span></span>](media-properties.md)                        | <span data-ttu-id="c4b8e-420">線上發行集很快就會改變。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-420">Online publications are rapidly changing.</span></span> <span data-ttu-id="c4b8e-421">發行公司的 CEO 會檢查過去5年的趨勢及其含意。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-421">A publishing house CEO examines the trends of the past 5 years and their implications.</span></span> |
| [<span data-ttu-id="c4b8e-422">WPD \_ 媒體 \_ 目的地 \_ URL</span><span class="sxs-lookup"><span data-stu-id="c4b8e-422">WPD\_MEDIA\_DESTINATION\_URL</span></span>](media-properties.md)               | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [<span data-ttu-id="c4b8e-423">WPD \_ 媒體內容類型 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-423">WPD\_MEDIA\_GENRE</span></span>](media-properties.md)                                    | <span data-ttu-id="c4b8e-424">新聞</span><span class="sxs-lookup"><span data-stu-id="c4b8e-424">News</span></span>                                                                                                                             |
| [<span data-ttu-id="c4b8e-425">WPD \_ 媒體 \_ GUID</span><span class="sxs-lookup"><span data-stu-id="c4b8e-425">WPD\_MEDIA\_GUID</span></span>](media-properties.md)                                      | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [<span data-ttu-id="c4b8e-426">WPD \_ 媒體 \_ 發行 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="c4b8e-426">WPD\_MEDIA\_RELEASE\_DATE</span></span>](media-properties.md)                     | <span data-ttu-id="c4b8e-427">週四，2006年6月1日 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="c4b8e-427">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                   |
| [<span data-ttu-id="c4b8e-428">WPD \_ 媒體 \_ 來源 \_ URL</span><span class="sxs-lookup"><span data-stu-id="c4b8e-428">WPD\_MEDIA\_SOURCE\_URL</span></span>](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [<span data-ttu-id="c4b8e-429">WPD \_ 物件 \_ 反向 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="c4b8e-429">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)            | <span data-ttu-id="c4b8e-430">0A1</span><span class="sxs-lookup"><span data-stu-id="c4b8e-430">0A1</span></span>                                                                                                                              |
| [<span data-ttu-id="c4b8e-431">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="c4b8e-431">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                  | <span data-ttu-id="c4b8e-432">WPD \_ 內容 \_ 類型 \_ 媒體 \_ 影像</span><span class="sxs-lookup"><span data-stu-id="c4b8e-432">WPD\_CONTENT\_TYPE\_MEDIA\_IMAGE</span></span>                                                                                                 |
| [<span data-ttu-id="c4b8e-433">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-433">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                | <span data-ttu-id="c4b8e-434">週四，2006年6月1日 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="c4b8e-434">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                   |
| [<span data-ttu-id="c4b8e-435">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-435">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                  | <span data-ttu-id="c4b8e-436">週四，2006年6月1日 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="c4b8e-436">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                   |
| [<span data-ttu-id="c4b8e-437">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="c4b8e-437">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                | <span data-ttu-id="c4b8e-438">週四，2006年6月1日 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="c4b8e-438">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                   |
| [<span data-ttu-id="c4b8e-439">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="c4b8e-439">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                               | <span data-ttu-id="c4b8e-440">WPD \_ 物件 \_ 格式 \_ MP3</span><span class="sxs-lookup"><span data-stu-id="c4b8e-440">WPD\_OBJECT\_FORMAT\_MP3</span></span>                                                                                                         |
| [<span data-ttu-id="c4b8e-441">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="c4b8e-441">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                       | <span data-ttu-id="c4b8e-442">會話相依。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-442">Session dependent.</span></span> <span data-ttu-id="c4b8e-443"> (在此範例中採用 "0A2"。 ) </span><span class="sxs-lookup"><span data-stu-id="c4b8e-443">(Assume "0A2" for this example.)</span></span>                                                                              |
| [<span data-ttu-id="c4b8e-444">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="c4b8e-444">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                   | <span data-ttu-id="c4b8e-445">數位發行</span><span class="sxs-lookup"><span data-stu-id="c4b8e-445">The Digital Publication</span></span>                                                                                                          |
| [<span data-ttu-id="c4b8e-446">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="c4b8e-446">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)     | <span data-ttu-id="c4b8e-447">digital0601.mp3</span><span class="sxs-lookup"><span data-stu-id="c4b8e-447">digital0601.mp3</span></span>                                                                                                                  |
| [<span data-ttu-id="c4b8e-448">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="c4b8e-448">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                        | <span data-ttu-id="c4b8e-449">0A0</span><span class="sxs-lookup"><span data-stu-id="c4b8e-449">0A0</span></span>                                                                                                                              |
| [<span data-ttu-id="c4b8e-450">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="c4b8e-450">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md) | <span data-ttu-id="c4b8e-451">與會話無關。</span><span class="sxs-lookup"><span data-stu-id="c4b8e-451">Session independent.</span></span>                                                                                                             |
| [<span data-ttu-id="c4b8e-452">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="c4b8e-452">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                   | <span data-ttu-id="c4b8e-453">10329011</span><span class="sxs-lookup"><span data-stu-id="c4b8e-453">10329011</span></span>                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="c4b8e-454">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4b8e-454">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4b8e-455">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="c4b8e-455">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 




