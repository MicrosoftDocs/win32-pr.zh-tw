---
title: 將 RSS 摘要對應至 Windows Media 裝置管理員屬性
description: 將 RSS 摘要對應至 Windows Media 裝置管理員屬性
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Windows Media 裝置管理員，RSS 摘要
- 裝置管理員，RSS 摘要
- 程式設計指南，RSS 摘要
- 桌面應用程式，RSS 摘要
- 建立 Windows Media 裝置管理員應用程式、RSS 摘要
- RSS 摘要
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a81d52b4099d77542963d2e87ae5b7dc26b034
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839456"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a><span data-ttu-id="d308e-109">將 RSS 摘要對應至 Windows Media 裝置管理員屬性</span><span class="sxs-lookup"><span data-stu-id="d308e-109">Mapping RSS Feeds to Windows Media Device Manager Properties</span></span>

<span data-ttu-id="d308e-110">Windows Media Player 11 提供 RSS 匯總程式功能，可讓使用者在他們的電腦上儲存從播客取得的內容。</span><span class="sxs-lookup"><span data-stu-id="d308e-110">Windows Media Player 11 provides an RSS aggregator feature that enables users to store content obtained from podcasts on their computers.</span></span> <span data-ttu-id="d308e-111">本主題說明在 RSS 摘要中找到的 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="d308e-111">This topic describes the XML elements found in an RSS feed.</span></span> <span data-ttu-id="d308e-112">此外，它還會將這些 RSS 元素對應至 Windows Media 裝置管理員屬性。</span><span class="sxs-lookup"><span data-stu-id="d308e-112">In addition, it maps these RSS elements to Windows Media Device Manager properties.</span></span>

<span data-ttu-id="d308e-113">RSS 饋送中的元素具有下列階層和屬性：</span><span class="sxs-lookup"><span data-stu-id="d308e-113">The elements in an RSS feed have the following hierarchy and attributes:</span></span>


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



<span data-ttu-id="d308e-114">下表列出 RSS 摘要中的通道元素，以及對應的 Windows Media 裝置管理員屬性。</span><span class="sxs-lookup"><span data-stu-id="d308e-114">The following table lists the channel elements in an RSS feed and the corresponding Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="d308e-115">Channel 元素</span><span class="sxs-lookup"><span data-stu-id="d308e-115">Channel element</span></span> | <span data-ttu-id="d308e-116">狀態</span><span class="sxs-lookup"><span data-stu-id="d308e-116">Status</span></span>         | <span data-ttu-id="d308e-117">對應的 Windows Media 裝置管理員屬性</span><span class="sxs-lookup"><span data-stu-id="d308e-117">Corresponding Windows Media Device Manager property</span></span>   |
|-----------------|----------------|-------------------------------------------------------|
| <span data-ttu-id="d308e-118">category</span><span class="sxs-lookup"><span data-stu-id="d308e-118">category</span></span>        | <span data-ttu-id="d308e-119">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-119">Optional</span></span>       | [<span data-ttu-id="d308e-120">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="d308e-120">g\_wszWMDMGenre</span></span>](metadata-constants.md)             |
| <span data-ttu-id="d308e-121">cloud</span><span class="sxs-lookup"><span data-stu-id="d308e-121">cloud</span></span>           | <span data-ttu-id="d308e-122">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-122">Not applicable</span></span> | <span data-ttu-id="d308e-123">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-123">Not applicable</span></span>                                        |
| <span data-ttu-id="d308e-124">著作權</span><span class="sxs-lookup"><span data-stu-id="d308e-124">copyright</span></span>       | <span data-ttu-id="d308e-125">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-125">Optional</span></span>       | [<span data-ttu-id="d308e-126">g \_ wszWMDMProviderCopyright</span><span class="sxs-lookup"><span data-stu-id="d308e-126">g\_wszWMDMProviderCopyright</span></span>](metadata-constants.md) |
| <span data-ttu-id="d308e-127">description</span><span class="sxs-lookup"><span data-stu-id="d308e-127">description</span></span>     | <span data-ttu-id="d308e-128">必要</span><span class="sxs-lookup"><span data-stu-id="d308e-128">Required</span></span>       | [<span data-ttu-id="d308e-129">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="d308e-129">g\_wszWMDMDescription</span></span>](metadata-constants.md)       |
| <span data-ttu-id="d308e-130">docs</span><span class="sxs-lookup"><span data-stu-id="d308e-130">docs</span></span>            | <span data-ttu-id="d308e-131">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-131">Not applicable</span></span> | <span data-ttu-id="d308e-132">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-132">Not applicable</span></span>                                        |
| <span data-ttu-id="d308e-133">產生器</span><span class="sxs-lookup"><span data-stu-id="d308e-133">generator</span></span>       | <span data-ttu-id="d308e-134">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-134">Not applicable</span></span> | <span data-ttu-id="d308e-135">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-135">Not applicable</span></span>                                        |
| <span data-ttu-id="d308e-136">語言</span><span class="sxs-lookup"><span data-stu-id="d308e-136">language</span></span>        | <span data-ttu-id="d308e-137">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-137">Not applicable</span></span> | <span data-ttu-id="d308e-138">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-138">Not applicable</span></span>                                        |
| <span data-ttu-id="d308e-139">lastBuildDate</span><span class="sxs-lookup"><span data-stu-id="d308e-139">lastBuildDate</span></span>   | <span data-ttu-id="d308e-140">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-140">Optional</span></span>       | [<span data-ttu-id="d308e-141">g \_ wszWMDMLastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="d308e-141">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md)  |
| <span data-ttu-id="d308e-142">link</span><span class="sxs-lookup"><span data-stu-id="d308e-142">link</span></span>            | <span data-ttu-id="d308e-143">必要</span><span class="sxs-lookup"><span data-stu-id="d308e-143">Required</span></span>       | [<span data-ttu-id="d308e-144">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="d308e-144">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)    |
| <span data-ttu-id="d308e-145">managingEditor</span><span class="sxs-lookup"><span data-stu-id="d308e-145">managingEditor</span></span>  | <span data-ttu-id="d308e-146">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-146">Optional</span></span>       | [<span data-ttu-id="d308e-147">g \_ wszWMDMEditor</span><span class="sxs-lookup"><span data-stu-id="d308e-147">g\_wszWMDMEditor</span></span>](metadata-constants.md)            |
| <span data-ttu-id="d308e-148">pubDate</span><span class="sxs-lookup"><span data-stu-id="d308e-148">pubDate</span></span>         | <span data-ttu-id="d308e-149">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-149">Optional</span></span>       | [<span data-ttu-id="d308e-150">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="d308e-150">g\_wszWMDMYear</span></span>](metadata-constants.md)              |
| <span data-ttu-id="d308e-151">rating</span><span class="sxs-lookup"><span data-stu-id="d308e-151">rating</span></span>          | <span data-ttu-id="d308e-152">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-152">Not applicable</span></span> | <span data-ttu-id="d308e-153">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-153">Not applicable</span></span>                                        |
| <span data-ttu-id="d308e-154">skipDays</span><span class="sxs-lookup"><span data-stu-id="d308e-154">skipDays</span></span>        | <span data-ttu-id="d308e-155">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-155">Not applicable</span></span> | <span data-ttu-id="d308e-156">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-156">Not applicable</span></span>                                        |
| <span data-ttu-id="d308e-157">skipHours</span><span class="sxs-lookup"><span data-stu-id="d308e-157">skipHours</span></span>       | <span data-ttu-id="d308e-158">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-158">Not applicable</span></span> | <span data-ttu-id="d308e-159">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-159">Not applicable</span></span>                                        |
| <span data-ttu-id="d308e-160">>textinput</span><span class="sxs-lookup"><span data-stu-id="d308e-160">textInput</span></span>       | <span data-ttu-id="d308e-161">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-161">Not applicable</span></span> | <span data-ttu-id="d308e-162">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-162">Not applicable</span></span>                                        |
| <span data-ttu-id="d308e-163">title</span><span class="sxs-lookup"><span data-stu-id="d308e-163">title</span></span>           | <span data-ttu-id="d308e-164">必要</span><span class="sxs-lookup"><span data-stu-id="d308e-164">Required</span></span>       | [<span data-ttu-id="d308e-165">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="d308e-165">g\_wszWMDMTitle</span></span>](metadata-constants.md)             |
| <span data-ttu-id="d308e-166">ttl</span><span class="sxs-lookup"><span data-stu-id="d308e-166">ttl</span></span>             | <span data-ttu-id="d308e-167">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-167">Optional</span></span>       | [<span data-ttu-id="d308e-168">g \_ wszWMDMTimeToLive</span><span class="sxs-lookup"><span data-stu-id="d308e-168">g\_wszWMDMTimeToLive</span></span>](metadata-constants.md)        |
| <span data-ttu-id="d308e-169">站長</span><span class="sxs-lookup"><span data-stu-id="d308e-169">webMaster</span></span>       | <span data-ttu-id="d308e-170">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-170">Optional</span></span>       | [<span data-ttu-id="d308e-171">g \_ wszWMDMWebMaster</span><span class="sxs-lookup"><span data-stu-id="d308e-171">g\_wszWMDMWebMaster</span></span>](metadata-constants.md)         |



 

<span data-ttu-id="d308e-172">下表列出 RSS 摘要中的影像元素和對應的 WMDM 屬性。</span><span class="sxs-lookup"><span data-stu-id="d308e-172">The following table lists the image elements in an RSS feed and the corresponding WMDM properties.</span></span>



| <span data-ttu-id="d308e-173">Image 項目</span><span class="sxs-lookup"><span data-stu-id="d308e-173">Image element</span></span> | <span data-ttu-id="d308e-174">狀態</span><span class="sxs-lookup"><span data-stu-id="d308e-174">Status</span></span>   | <span data-ttu-id="d308e-175">對應的 Windows Media 裝置管理員屬性</span><span class="sxs-lookup"><span data-stu-id="d308e-175">Corresponding Windows Media Device Manager property</span></span> |
|---------------|----------|-----------------------------------------------------|
| <span data-ttu-id="d308e-176">description</span><span class="sxs-lookup"><span data-stu-id="d308e-176">description</span></span>   | <span data-ttu-id="d308e-177">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-177">Optional</span></span> | [<span data-ttu-id="d308e-178">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="d308e-178">g\_wszWMDMDescription</span></span>](metadata-constants.md)     |
| <span data-ttu-id="d308e-179">身高</span><span class="sxs-lookup"><span data-stu-id="d308e-179">height</span></span>        | <span data-ttu-id="d308e-180">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-180">Optional</span></span> | [<span data-ttu-id="d308e-181">g \_ wszWMDMHeight</span><span class="sxs-lookup"><span data-stu-id="d308e-181">g\_wszWMDMHeight</span></span>](metadata-constants.md)          |
| <span data-ttu-id="d308e-182">link</span><span class="sxs-lookup"><span data-stu-id="d308e-182">link</span></span>          | <span data-ttu-id="d308e-183">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-183">Optional</span></span> | [<span data-ttu-id="d308e-184">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="d308e-184">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)  |
| <span data-ttu-id="d308e-185">title</span><span class="sxs-lookup"><span data-stu-id="d308e-185">title</span></span>         | <span data-ttu-id="d308e-186">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-186">Optional</span></span> | [<span data-ttu-id="d308e-187">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="d308e-187">g\_wszWMDMTitle</span></span>](metadata-constants.md)           |
| <span data-ttu-id="d308e-188">url</span><span class="sxs-lookup"><span data-stu-id="d308e-188">url</span></span>           | <span data-ttu-id="d308e-189">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-189">Optional</span></span> | [<span data-ttu-id="d308e-190">g \_ wszWMDMSourceURL</span><span class="sxs-lookup"><span data-stu-id="d308e-190">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)       |
| <span data-ttu-id="d308e-191">width</span><span class="sxs-lookup"><span data-stu-id="d308e-191">width</span></span>         | <span data-ttu-id="d308e-192">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-192">Optional</span></span> | [<span data-ttu-id="d308e-193">g \_ wszWMDMWidth</span><span class="sxs-lookup"><span data-stu-id="d308e-193">g\_wszWMDMWidth</span></span>](metadata-constants.md)           |



 

<span data-ttu-id="d308e-194">下表列出 RSS 摘要中的專案元素，以及對應的 Windows Media 裝置管理員屬性。</span><span class="sxs-lookup"><span data-stu-id="d308e-194">The following table lists the item elements in an RSS feed and the corresponding Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="d308e-195">Item 項目</span><span class="sxs-lookup"><span data-stu-id="d308e-195">Item element</span></span> | <span data-ttu-id="d308e-196">屬性</span><span class="sxs-lookup"><span data-stu-id="d308e-196">Attribute</span></span>   | <span data-ttu-id="d308e-197">狀態</span><span class="sxs-lookup"><span data-stu-id="d308e-197">Status</span></span>         | <span data-ttu-id="d308e-198">對應的 Windows Media 裝置管理員屬性</span><span class="sxs-lookup"><span data-stu-id="d308e-198">Corresponding Windows Media Device Manager property</span></span>            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| <span data-ttu-id="d308e-199">編寫</span><span class="sxs-lookup"><span data-stu-id="d308e-199">author</span></span>       |             | <span data-ttu-id="d308e-200">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-200">Optional</span></span>       | [<span data-ttu-id="d308e-201">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="d308e-201">g\_wszWMDMAuthor</span></span>](metadata-constants.md)                     |
| <span data-ttu-id="d308e-202">category</span><span class="sxs-lookup"><span data-stu-id="d308e-202">category</span></span>     |             | <span data-ttu-id="d308e-203">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-203">Optional</span></span>       | [<span data-ttu-id="d308e-204">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="d308e-204">g\_wszWMDMGenre</span></span>](metadata-constants.md)                      |
|              | <span data-ttu-id="d308e-205">網域</span><span class="sxs-lookup"><span data-stu-id="d308e-205">domain</span></span>      | <span data-ttu-id="d308e-206">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-206">Not applicable</span></span> | <span data-ttu-id="d308e-207">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-207">Not applicable</span></span>                                                 |
| <span data-ttu-id="d308e-208">description</span><span class="sxs-lookup"><span data-stu-id="d308e-208">description</span></span>  |             | <span data-ttu-id="d308e-209">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-209">Optional</span></span>       | [<span data-ttu-id="d308e-210">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="d308e-210">g\_wszWMDMDescription</span></span>](metadata-constants.md)                |
| <span data-ttu-id="d308e-211">外殼</span><span class="sxs-lookup"><span data-stu-id="d308e-211">enclosure</span></span>    |             | <span data-ttu-id="d308e-212">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-212">Optional</span></span>       | <span data-ttu-id="d308e-213">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-213">Not applicable</span></span>                                                 |
|              | <span data-ttu-id="d308e-214">長度</span><span class="sxs-lookup"><span data-stu-id="d308e-214">length</span></span>      | <span data-ttu-id="d308e-215">必要</span><span class="sxs-lookup"><span data-stu-id="d308e-215">Required</span></span>       | [<span data-ttu-id="d308e-216">g \_ wszWMDMFileSize</span><span class="sxs-lookup"><span data-stu-id="d308e-216">g\_wszWMDMFileSize</span></span>](metadata-constants.md)                   |
|              | <span data-ttu-id="d308e-217">type</span><span class="sxs-lookup"><span data-stu-id="d308e-217">type</span></span>        | <span data-ttu-id="d308e-218">必要</span><span class="sxs-lookup"><span data-stu-id="d308e-218">Required</span></span>       | <span data-ttu-id="d308e-219"> (MIME 類型應對應至屬性內容類型。 ) </span><span class="sxs-lookup"><span data-stu-id="d308e-219">(The MIME type should be mapped to the property content type.)</span></span> |
|              | <span data-ttu-id="d308e-220">url</span><span class="sxs-lookup"><span data-stu-id="d308e-220">url</span></span>         | <span data-ttu-id="d308e-221">必要</span><span class="sxs-lookup"><span data-stu-id="d308e-221">Required</span></span>       | [<span data-ttu-id="d308e-222">g \_ wszWMDMSourceURL</span><span class="sxs-lookup"><span data-stu-id="d308e-222">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)                  |
| <span data-ttu-id="d308e-223">guid</span><span class="sxs-lookup"><span data-stu-id="d308e-223">guid</span></span>         |             | <span data-ttu-id="d308e-224">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-224">Optional</span></span>       | [<span data-ttu-id="d308e-225">g \_ wszWMDMediaGuid</span><span class="sxs-lookup"><span data-stu-id="d308e-225">g\_wszWMDMediaGuid</span></span>](metadata-constants.md)                   |
|              | <span data-ttu-id="d308e-226">isPermaLink</span><span class="sxs-lookup"><span data-stu-id="d308e-226">isPermaLink</span></span> | <span data-ttu-id="d308e-227">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-227">Not applicable</span></span> | <span data-ttu-id="d308e-228">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-228">Not applicable</span></span>                                                 |
| <span data-ttu-id="d308e-229">link</span><span class="sxs-lookup"><span data-stu-id="d308e-229">link</span></span>         |             | <span data-ttu-id="d308e-230">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-230">Optional</span></span>       | [<span data-ttu-id="d308e-231">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="d308e-231">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)             |
| <span data-ttu-id="d308e-232">pubDate</span><span class="sxs-lookup"><span data-stu-id="d308e-232">pubDate</span></span>      |             | <span data-ttu-id="d308e-233">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-233">Optional</span></span>       | [<span data-ttu-id="d308e-234">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="d308e-234">g\_wszWMDMYear</span></span>](metadata-constants.md)                       |
| <span data-ttu-id="d308e-235">source</span><span class="sxs-lookup"><span data-stu-id="d308e-235">source</span></span>       |             | <span data-ttu-id="d308e-236">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-236">Not applicable</span></span> | <span data-ttu-id="d308e-237">不適用</span><span class="sxs-lookup"><span data-stu-id="d308e-237">Not applicable</span></span>                                                 |
| <span data-ttu-id="d308e-238">title</span><span class="sxs-lookup"><span data-stu-id="d308e-238">title</span></span>        |             | <span data-ttu-id="d308e-239">選擇性</span><span class="sxs-lookup"><span data-stu-id="d308e-239">Optional</span></span>       | [<span data-ttu-id="d308e-240">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="d308e-240">g\_wszWMDMTitle</span></span>](metadata-constants.md)                      |



 

<span data-ttu-id="d308e-241">範例</span><span class="sxs-lookup"><span data-stu-id="d308e-241">Example</span></span>

<span data-ttu-id="d308e-242">下列範例顯示發行公司的 CEO 所提供之虛構播客的完整 RSS 摘要。</span><span class="sxs-lookup"><span data-stu-id="d308e-242">The following example shows a complete RSS feed for a fictitious podcast supplied by the CEO of a publishing company.</span></span>


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
    <link>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past five years and their implications.</description>
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



<span data-ttu-id="d308e-243">RSS 通道元素與 Windows Media 裝置管理員屬性值的對應</span><span class="sxs-lookup"><span data-stu-id="d308e-243">Mapping of RSS Channel Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="d308e-244">下表說明上一個範例中 RSS 通道元素的值如何對應至特定的 Windows Media 裝置管理員屬性。</span><span class="sxs-lookup"><span data-stu-id="d308e-244">The following table describes how the values in the RSS Channel elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="d308e-245">Windows Media 裝置管理員屬性</span><span class="sxs-lookup"><span data-stu-id="d308e-245">Windows Media Device Manager property</span></span>                    | <span data-ttu-id="d308e-246">值</span><span class="sxs-lookup"><span data-stu-id="d308e-246">Value</span></span>                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d308e-247">g \_ wszWMDMAuthorDate</span><span class="sxs-lookup"><span data-stu-id="d308e-247">g\_wszWMDMAuthorDate</span></span>](metadata-constants.md)           | <span data-ttu-id="d308e-248">2006年6月9日，14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="d308e-248">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="d308e-249">g \_ wszWMDMDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d308e-249">g\_wszWMDMDESCRIPTION</span></span>](metadata-constants.md)          | <span data-ttu-id="d308e-250">Lucerne 發佈 CEO Peter Bankov 會查看線上發行物的最新趨勢。</span><span class="sxs-lookup"><span data-stu-id="d308e-250">Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</span></span> |
| [<span data-ttu-id="d308e-251">g \_ wszWMDMDESTINATION \_ URL</span><span class="sxs-lookup"><span data-stu-id="d308e-251">g\_wszWMDMDESTINATION\_URL</span></span>](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [<span data-ttu-id="d308e-252">g \_ wszWMDMEDITOR</span><span class="sxs-lookup"><span data-stu-id="d308e-252">g\_wszWMDMEDITOR</span></span>](metadata-constants.md)               | someone@example.com                                                                           |
| [<span data-ttu-id="d308e-253">g \_ wszWMDMFileCreationDate</span><span class="sxs-lookup"><span data-stu-id="d308e-253">g\_wszWMDMFileCreationDate</span></span>](metadata-constants.md)     | <span data-ttu-id="d308e-254">2006年6月9日，14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="d308e-254">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="d308e-255">g \_ wszWMDMFileName</span><span class="sxs-lookup"><span data-stu-id="d308e-255">g\_wszWMDMFileName</span></span>](metadata-constants.md)             | <span data-ttu-id="d308e-256">數位發行</span><span class="sxs-lookup"><span data-stu-id="d308e-256">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="d308e-257">g \_ wszWMDMFileSize</span><span class="sxs-lookup"><span data-stu-id="d308e-257">g\_wszWMDMFileSize</span></span>](metadata-constants.md)             | <span data-ttu-id="d308e-258">13790</span><span class="sxs-lookup"><span data-stu-id="d308e-258">13,790</span></span>                                                                                        |
| [<span data-ttu-id="d308e-259">g \_ wszWMDMFormatCode</span><span class="sxs-lookup"><span data-stu-id="d308e-259">g\_wszWMDMFormatCode</span></span>](metadata-constants.md)           | <span data-ttu-id="d308e-260">WMDM \_ FORMATCODE \_ 媒體 \_ 轉換</span><span class="sxs-lookup"><span data-stu-id="d308e-260">WMDM\_FORMATCODE\_MEDIA\_CAST</span></span>                                                                 |
| [<span data-ttu-id="d308e-261">g \_ wszWMDMGENRE</span><span class="sxs-lookup"><span data-stu-id="d308e-261">g\_wszWMDMGENRE</span></span>](metadata-constants.md)                | <span data-ttu-id="d308e-262">新聞</span><span class="sxs-lookup"><span data-stu-id="d308e-262">News</span></span>                                                                                          |
| [<span data-ttu-id="d308e-263">g \_ wszWMDMLAST \_ 修改 \_ 日期</span><span class="sxs-lookup"><span data-stu-id="d308e-263">g\_wszWMDMLAST\_MODIFIED\_DATE</span></span>](metadata-constants.md) | <span data-ttu-id="d308e-264">2006年6月9日，14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="d308e-264">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="d308e-265">g \_ wszWMDMLastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="d308e-265">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md)     | <span data-ttu-id="d308e-266">2006年6月9日，14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="d308e-266">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="d308e-267">g \_ wszWMDMProviderCopyright</span><span class="sxs-lookup"><span data-stu-id="d308e-267">g\_wszWMDMProviderCopyright</span></span>](metadata-constants.md)    | <span data-ttu-id="d308e-268">2006 Lucerne 發行 LP，LLLP。</span><span class="sxs-lookup"><span data-stu-id="d308e-268">2006 Lucerne Publishing LP, LLLP.</span></span> <span data-ttu-id="d308e-269">著作權所有，並保留一切權利。</span><span class="sxs-lookup"><span data-stu-id="d308e-269">All Rights Reserved.</span></span>                                        |
| [<span data-ttu-id="d308e-270">g \_ wszWMDMTimeToLive</span><span class="sxs-lookup"><span data-stu-id="d308e-270">g\_wszWMDMTimeToLive</span></span>](metadata-constants.md)           | <span data-ttu-id="d308e-271">240</span><span class="sxs-lookup"><span data-stu-id="d308e-271">240</span></span>                                                                                           |
| [<span data-ttu-id="d308e-272">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="d308e-272">g\_wszWMDMTitle</span></span>](metadata-constants.md)                | <span data-ttu-id="d308e-273">數位發行</span><span class="sxs-lookup"><span data-stu-id="d308e-273">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="d308e-274">g \_ wszWMDMWEBMASTER</span><span class="sxs-lookup"><span data-stu-id="d308e-274">g\_wszWMDMWEBMASTER</span></span>](metadata-constants.md)            | someone@example.com                                                                           |
| [<span data-ttu-id="d308e-275">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="d308e-275">g\_wszWMDMYear</span></span>](metadata-constants.md)                 | <span data-ttu-id="d308e-276">2006年6月9日，14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="d308e-276">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |



 

<span data-ttu-id="d308e-277">將 RSS 影像元素對應至 Windows Media 裝置管理員屬性值</span><span class="sxs-lookup"><span data-stu-id="d308e-277">Mapping of RSS Image Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="d308e-278">下表說明上一個範例中 RSS 影像元素的值如何對應至特定的 Windows Media 裝置管理員屬性。</span><span class="sxs-lookup"><span data-stu-id="d308e-278">The following table describes how the values in the RSS Image elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="d308e-279">Windows Media 裝置管理員屬性</span><span class="sxs-lookup"><span data-stu-id="d308e-279">Windows Media Device Manager property</span></span>                | <span data-ttu-id="d308e-280">值</span><span class="sxs-lookup"><span data-stu-id="d308e-280">Value</span></span>                                            |
|------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="d308e-281">g \_ wszWMDMAlbumCoverFormat</span><span class="sxs-lookup"><span data-stu-id="d308e-281">g\_wszWMDMAlbumCoverFormat</span></span>](metadata-constants.md) | <span data-ttu-id="d308e-282">WPD \_ 物件 \_ 格式 \_ GIF</span><span class="sxs-lookup"><span data-stu-id="d308e-282">WPD\_OBJECT\_FORMAT\_GIF</span></span>                         |
| [<span data-ttu-id="d308e-283">g \_ wszWMDMAlbumCoverSize</span><span class="sxs-lookup"><span data-stu-id="d308e-283">g\_wszWMDMAlbumCoverSize</span></span>](metadata-constants.md)   | <span data-ttu-id="d308e-284">512</span><span class="sxs-lookup"><span data-stu-id="d308e-284">512</span></span>                                              |
| [<span data-ttu-id="d308e-285">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="d308e-285">g\_wszWMDMDescription</span></span>](metadata-constants.md)      | <span data-ttu-id="d308e-286">Lucerne 標誌</span><span class="sxs-lookup"><span data-stu-id="d308e-286">Lucerne Logo</span></span>                                     |
| [<span data-ttu-id="d308e-287">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="d308e-287">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)   | <span data-ttu-id="d308e-288">www.lucernepublishing.com/community/podcasts</span><span class="sxs-lookup"><span data-stu-id="d308e-288">//www.lucernepublishing.com/community/podcasts</span></span>   |
| [<span data-ttu-id="d308e-289">g \_ wszWMDMHeight</span><span class="sxs-lookup"><span data-stu-id="d308e-289">g\_wszWMDMHeight</span></span>](metadata-constants.md)           | <span data-ttu-id="d308e-290">300</span><span class="sxs-lookup"><span data-stu-id="d308e-290">300</span></span>                                              |
| [<span data-ttu-id="d308e-291">g \_ wszWMDMSourceURL</span><span class="sxs-lookup"><span data-stu-id="d308e-291">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [<span data-ttu-id="d308e-292">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="d308e-292">g\_wszWMDMTitle</span></span>](metadata-constants.md)            | <span data-ttu-id="d308e-293">Lucerne 發行</span><span class="sxs-lookup"><span data-stu-id="d308e-293">Lucerne Publishing</span></span>                               |
| [<span data-ttu-id="d308e-294">g \_ wszWMDMWidth</span><span class="sxs-lookup"><span data-stu-id="d308e-294">g\_wszWMDMWidth</span></span>](metadata-constants.md)            | <span data-ttu-id="d308e-295">300</span><span class="sxs-lookup"><span data-stu-id="d308e-295">300</span></span>                                              |



 

<span data-ttu-id="d308e-296">將 RSS 專案元素對應至 Windows Media 裝置管理員屬性值</span><span class="sxs-lookup"><span data-stu-id="d308e-296">Mapping of RSS Item Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="d308e-297">下表說明上一個範例中 RSS 專案專案的值如何對應至特定的 Windows Media 裝置管理員屬性。</span><span class="sxs-lookup"><span data-stu-id="d308e-297">The following table describes how the values in the RSS Item elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="d308e-298">Windows Media 裝置管理員屬性</span><span class="sxs-lookup"><span data-stu-id="d308e-298">Windows Media Device Manager property</span></span>                | <span data-ttu-id="d308e-299">值</span><span class="sxs-lookup"><span data-stu-id="d308e-299">Value</span></span>                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d308e-300">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="d308e-300">g\_wszWMDMAuthor</span></span>](metadata-constants.md)           | <span data-ttu-id="d308e-301">苜蓿</span><span class="sxs-lookup"><span data-stu-id="d308e-301">Lucerne</span></span>                                                                                                                             |
| [<span data-ttu-id="d308e-302">g \_ wszWMDMAuthorDate</span><span class="sxs-lookup"><span data-stu-id="d308e-302">g\_wszWMDMAuthorDate</span></span>](metadata-constants.md)       | <span data-ttu-id="d308e-303">週四，2006年6月1日 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="d308e-303">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="d308e-304">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="d308e-304">g\_wszWMDMDescription</span></span>](metadata-constants.md)      | <span data-ttu-id="d308e-305">線上發行集很快就會改變。</span><span class="sxs-lookup"><span data-stu-id="d308e-305">Online publications are rapidly changing.</span></span> <span data-ttu-id="d308e-306">發行公司的 CEO 會檢查過去五年的趨勢及其含意。</span><span class="sxs-lookup"><span data-stu-id="d308e-306">A publishing house CEO examines the trends of the past five years and their implications.</span></span> |
| [<span data-ttu-id="d308e-307">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="d308e-307">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="d308e-308">g \_ wszWMDMDuration</span><span class="sxs-lookup"><span data-stu-id="d308e-308">g\_wszWMDMDuration</span></span>](metadata-constants.md)         | <span data-ttu-id="d308e-309">120325445</span><span class="sxs-lookup"><span data-stu-id="d308e-309">120325445</span></span>                                                                                                                           |
| [<span data-ttu-id="d308e-310">g \_ wszWMDMFileCreationDate</span><span class="sxs-lookup"><span data-stu-id="d308e-310">g\_wszWMDMFileCreationDate</span></span>](metadata-constants.md) | <span data-ttu-id="d308e-311">週四，2006年6月1日 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="d308e-311">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="d308e-312">g \_ wszWMDMFileSize</span><span class="sxs-lookup"><span data-stu-id="d308e-312">g\_wszWMDMFileSize</span></span>](metadata-constants.md)         | <span data-ttu-id="d308e-313">10329011</span><span class="sxs-lookup"><span data-stu-id="d308e-313">10329011</span></span>                                                                                                                            |
| [<span data-ttu-id="d308e-314">g \_ wszWMDMFormatCode</span><span class="sxs-lookup"><span data-stu-id="d308e-314">g\_wszWMDMFormatCode</span></span>](metadata-constants.md)       | <span data-ttu-id="d308e-315">WMDM \_ FORMATCODE \_ MP3</span><span class="sxs-lookup"><span data-stu-id="d308e-315">WMDM\_FORMATCODE\_MP3</span></span>                                                                                                               |
| [<span data-ttu-id="d308e-316">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="d308e-316">g\_wszWMDMGenre</span></span>](metadata-constants.md)            | <span data-ttu-id="d308e-317">新聞</span><span class="sxs-lookup"><span data-stu-id="d308e-317">News</span></span>                                                                                                                                |
| [<span data-ttu-id="d308e-318">g \_ wszWMDMLastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="d308e-318">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md) | <span data-ttu-id="d308e-319">週四，2006年6月1日 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="d308e-319">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="d308e-320">g \_ wszWMDMMediaGuid</span><span class="sxs-lookup"><span data-stu-id="d308e-320">g\_wszWMDMMediaGuid</span></span>](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="d308e-321">g \_ wszWMDMSourceURL</span><span class="sxs-lookup"><span data-stu-id="d308e-321">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="d308e-322">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="d308e-322">g\_wszWMDMTitle</span></span>](metadata-constants.md)            | <span data-ttu-id="d308e-323">數位發行</span><span class="sxs-lookup"><span data-stu-id="d308e-323">The Digital Publication</span></span>                                                                                                             |
| [<span data-ttu-id="d308e-324">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="d308e-324">g\_wszWMDMYear</span></span>](metadata-constants.md)             | <span data-ttu-id="d308e-325">週四，2006年6月1日 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="d308e-325">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="d308e-326">相關主題</span><span class="sxs-lookup"><span data-stu-id="d308e-326">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d308e-327">**中繼資料常數**</span><span class="sxs-lookup"><span data-stu-id="d308e-327">**Metadata Constants**</span></span>](metadata-constants.md)
</dt> </dl>

 

 




