---
description: Microsoft Windows 提供一些可供您的檔案格式使用的系統屬性。
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: 自訂檔案格式的 System-Defined 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1a3645e383ea751298f766eacf60f5ac95ece3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112401"
---
# <a name="system-defined-properties-for-custom-file-formats"></a><span data-ttu-id="61cd5-103">自訂檔案格式的 System-Defined 屬性</span><span class="sxs-lookup"><span data-stu-id="61cd5-103">System-Defined Properties for Custom File Formats</span></span>

<span data-ttu-id="61cd5-104">Microsoft Windows 提供一些可供您的檔案格式使用的系統屬性。</span><span class="sxs-lookup"><span data-stu-id="61cd5-104">Microsoft Windows supplies a number of system properties that you can use for your file formats.</span></span> <span data-ttu-id="61cd5-105">如果您要建立自訂檔案格式，您應該盡可能支援最多的系統定義屬性。</span><span class="sxs-lookup"><span data-stu-id="61cd5-105">If you are creating a custom file format, you should support as many system-defined properties as you can.</span></span> <span data-ttu-id="61cd5-106">建立自訂屬性處理常式之前，您應該先檢查系統提供的處理常式，看看您是否可以使用它，而不是撰寫自己的處理常式。</span><span class="sxs-lookup"><span data-stu-id="61cd5-106">Before creating a custom property handler, you should review the system-supplied handlers to see if you can use one instead of writing your own.</span></span>

<span data-ttu-id="61cd5-107">下表將檔案格式分類，然後列出檔案格式應支援的最重要系統屬性。</span><span class="sxs-lookup"><span data-stu-id="61cd5-107">The following table categorizes file formats and then lists the most important system properties your file format should support.</span></span> <span data-ttu-id="61cd5-108">為了提供絕佳的使用者體驗，您應該針對檔案格式的類別目錄支援所有優先順序1和2屬性。</span><span class="sxs-lookup"><span data-stu-id="61cd5-108">To provide a good user experience, you should support all priority 1 and 2 properties for your category of file format.</span></span>

-   [<span data-ttu-id="61cd5-109">通訊</span><span class="sxs-lookup"><span data-stu-id="61cd5-109">Communications</span></span>](#communications)
-   [<span data-ttu-id="61cd5-110">連絡人</span><span class="sxs-lookup"><span data-stu-id="61cd5-110">Contacts</span></span>](#contacts)
-   [<span data-ttu-id="61cd5-111">文件</span><span class="sxs-lookup"><span data-stu-id="61cd5-111">Documents</span></span>](#documents)
-   [<span data-ttu-id="61cd5-112">泛型</span><span class="sxs-lookup"><span data-stu-id="61cd5-112">Generic</span></span>](#generic)
-   [<span data-ttu-id="61cd5-113">音樂</span><span class="sxs-lookup"><span data-stu-id="61cd5-113">Music</span></span>](#music)
-   [<span data-ttu-id="61cd5-114">圖片</span><span class="sxs-lookup"><span data-stu-id="61cd5-114">Pictures</span></span>](#pictures)
-   [<span data-ttu-id="61cd5-115">影片</span><span class="sxs-lookup"><span data-stu-id="61cd5-115">Videos</span></span>](#videos)
-   [<span data-ttu-id="61cd5-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="61cd5-116">Related topics</span></span>](#related-topics)

## <a name="communications"></a><span data-ttu-id="61cd5-117">通訊</span><span class="sxs-lookup"><span data-stu-id="61cd5-117">Communications</span></span>



| <span data-ttu-id="61cd5-118">Name</span><span class="sxs-lookup"><span data-stu-id="61cd5-118">Name</span></span>            | <span data-ttu-id="61cd5-119">屬性</span><span class="sxs-lookup"><span data-stu-id="61cd5-119">Property</span></span>                               | <span data-ttu-id="61cd5-120">優先順序</span><span class="sxs-lookup"><span data-stu-id="61cd5-120">Priority</span></span> |
|-----------------|----------------------------------------|----------|
| <span data-ttu-id="61cd5-121">收到日期</span><span class="sxs-lookup"><span data-stu-id="61cd5-121">Date received</span></span>   | <span data-ttu-id="61cd5-122">DateReceived</span><span class="sxs-lookup"><span data-stu-id="61cd5-122">System.Message.DateReceived</span></span>            | <span data-ttu-id="61cd5-123">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-123">1</span></span>        |
| <span data-ttu-id="61cd5-124">從名稱</span><span class="sxs-lookup"><span data-stu-id="61cd5-124">From names</span></span>      | <span data-ttu-id="61cd5-125">FromName</span><span class="sxs-lookup"><span data-stu-id="61cd5-125">System.Message.FromName</span></span>                | <span data-ttu-id="61cd5-126">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-126">1</span></span>        |
| <span data-ttu-id="61cd5-127">具有附件</span><span class="sxs-lookup"><span data-stu-id="61cd5-127">Has attachments</span></span> | <span data-ttu-id="61cd5-128">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="61cd5-128">System.Message.HasAttachments</span></span>          | <span data-ttu-id="61cd5-129">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-129">1</span></span>        |
| <span data-ttu-id="61cd5-130">Mailbox</span><span class="sxs-lookup"><span data-stu-id="61cd5-130">Mailbox</span></span>         | <span data-ttu-id="61cd5-131">Storeddisplayname</span><span class="sxs-lookup"><span data-stu-id="61cd5-131">System.Communication.storeddisplayname</span></span> | <span data-ttu-id="61cd5-132">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-132">1</span></span>        |
| <span data-ttu-id="61cd5-133">Name</span><span class="sxs-lookup"><span data-stu-id="61cd5-133">Name</span></span>            | <span data-ttu-id="61cd5-134">System.string</span><span class="sxs-lookup"><span data-stu-id="61cd5-134">System.FileName</span></span>                        | <span data-ttu-id="61cd5-135">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-135">1</span></span>        |
| <span data-ttu-id="61cd5-136">主體</span><span class="sxs-lookup"><span data-stu-id="61cd5-136">Subject</span></span>         | <span data-ttu-id="61cd5-137">System. Subject</span><span class="sxs-lookup"><span data-stu-id="61cd5-137">System.Subject</span></span>                         | <span data-ttu-id="61cd5-138">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-138">1</span></span>        |
| <span data-ttu-id="61cd5-139">名稱</span><span class="sxs-lookup"><span data-stu-id="61cd5-139">To names</span></span>        | <span data-ttu-id="61cd5-140">ToName</span><span class="sxs-lookup"><span data-stu-id="61cd5-140">System.Message.ToName</span></span>                  | <span data-ttu-id="61cd5-141">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-141">1</span></span>        |
| <span data-ttu-id="61cd5-142">類別</span><span class="sxs-lookup"><span data-stu-id="61cd5-142">Category</span></span>        | <span data-ttu-id="61cd5-143">System. Category</span><span class="sxs-lookup"><span data-stu-id="61cd5-143">System.Category</span></span>                        | <span data-ttu-id="61cd5-144">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-144">2</span></span>        |
| <span data-ttu-id="61cd5-145">類型</span><span class="sxs-lookup"><span data-stu-id="61cd5-145">Type</span></span>            | <span data-ttu-id="61cd5-146">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="61cd5-146">System.PerceivedType</span></span>                   | <span data-ttu-id="61cd5-147">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-147">2</span></span>        |



 

## <a name="contacts"></a><span data-ttu-id="61cd5-148">連絡人</span><span class="sxs-lookup"><span data-stu-id="61cd5-148">Contacts</span></span>



| <span data-ttu-id="61cd5-149">Name</span><span class="sxs-lookup"><span data-stu-id="61cd5-149">Name</span></span>             | <span data-ttu-id="61cd5-150">屬性</span><span class="sxs-lookup"><span data-stu-id="61cd5-150">Property</span></span>                           | <span data-ttu-id="61cd5-151">優先順序</span><span class="sxs-lookup"><span data-stu-id="61cd5-151">Priority</span></span> |
|------------------|------------------------------------|----------|
| <span data-ttu-id="61cd5-152">帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="61cd5-152">Account Name</span></span>     | <span data-ttu-id="61cd5-153">System.servicemodel</span><span class="sxs-lookup"><span data-stu-id="61cd5-153">System.Communication.AccountName</span></span>   | <span data-ttu-id="61cd5-154">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-154">1</span></span>        |
| <span data-ttu-id="61cd5-155">公司電話</span><span class="sxs-lookup"><span data-stu-id="61cd5-155">Business Phone</span></span>   | <span data-ttu-id="61cd5-156">BusinessTelephone</span><span class="sxs-lookup"><span data-stu-id="61cd5-156">System.Contact.BusinessTelephone</span></span>   | <span data-ttu-id="61cd5-157">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-157">1</span></span>        |
| <span data-ttu-id="61cd5-158">公司</span><span class="sxs-lookup"><span data-stu-id="61cd5-158">Company</span></span>          | <span data-ttu-id="61cd5-159">Company</span><span class="sxs-lookup"><span data-stu-id="61cd5-159">System.Company</span></span>                     | <span data-ttu-id="61cd5-160">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-160">1</span></span>        |
| <span data-ttu-id="61cd5-161">電子郵件地址</span><span class="sxs-lookup"><span data-stu-id="61cd5-161">Email Address</span></span>    | <span data-ttu-id="61cd5-162">PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="61cd5-162">System.Contact.PrimaryEmailAddress</span></span> | <span data-ttu-id="61cd5-163">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-163">1</span></span>        |
| <span data-ttu-id="61cd5-164">重要性</span><span class="sxs-lookup"><span data-stu-id="61cd5-164">Importance</span></span>       | <span data-ttu-id="61cd5-165">System. ImportanceText</span><span class="sxs-lookup"><span data-stu-id="61cd5-165">System.ImportanceText</span></span>              | <span data-ttu-id="61cd5-166">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-166">1</span></span>        |
| <span data-ttu-id="61cd5-167">行動電話</span><span class="sxs-lookup"><span data-stu-id="61cd5-167">Mobile Phone</span></span>     | <span data-ttu-id="61cd5-168">MobileTelephone</span><span class="sxs-lookup"><span data-stu-id="61cd5-168">System.Contact.MobileTelephone</span></span>     | <span data-ttu-id="61cd5-169">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-169">1</span></span>        |
| <span data-ttu-id="61cd5-170">商務位址</span><span class="sxs-lookup"><span data-stu-id="61cd5-170">Business address</span></span> | <span data-ttu-id="61cd5-171">BusinessAddress</span><span class="sxs-lookup"><span data-stu-id="61cd5-171">System.Contact.BusinessAddress</span></span>     | <span data-ttu-id="61cd5-172">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-172">2</span></span>        |
| <span data-ttu-id="61cd5-173">企業傳真</span><span class="sxs-lookup"><span data-stu-id="61cd5-173">Business fax</span></span>     | <span data-ttu-id="61cd5-174">BusinessFaxNumber</span><span class="sxs-lookup"><span data-stu-id="61cd5-174">System.Contact.BusinessFaxNumber</span></span>   | <span data-ttu-id="61cd5-175">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-175">2</span></span>        |
| <span data-ttu-id="61cd5-176">類別</span><span class="sxs-lookup"><span data-stu-id="61cd5-176">Category</span></span>         | <span data-ttu-id="61cd5-177">System. Category</span><span class="sxs-lookup"><span data-stu-id="61cd5-177">System.Category</span></span>                    | <span data-ttu-id="61cd5-178">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-178">2</span></span>        |
| <span data-ttu-id="61cd5-179">首頁位址</span><span class="sxs-lookup"><span data-stu-id="61cd5-179">Home address</span></span>     | <span data-ttu-id="61cd5-180">HomeAddress</span><span class="sxs-lookup"><span data-stu-id="61cd5-180">System.Contact.HomeAddress</span></span>         | <span data-ttu-id="61cd5-181">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-181">2</span></span>        |
| <span data-ttu-id="61cd5-182">住家電話</span><span class="sxs-lookup"><span data-stu-id="61cd5-182">Home phone</span></span>       | <span data-ttu-id="61cd5-183">HomeTelephone</span><span class="sxs-lookup"><span data-stu-id="61cd5-183">System.Contact.HomeTelephone</span></span>       | <span data-ttu-id="61cd5-184">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-184">2</span></span>        |
| <span data-ttu-id="61cd5-185">標題</span><span class="sxs-lookup"><span data-stu-id="61cd5-185">Title</span></span>            | <span data-ttu-id="61cd5-186">System.Title</span><span class="sxs-lookup"><span data-stu-id="61cd5-186">System.Title</span></span>                       | <span data-ttu-id="61cd5-187">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-187">2</span></span>        |



 

## <a name="documents"></a><span data-ttu-id="61cd5-188">文件</span><span class="sxs-lookup"><span data-stu-id="61cd5-188">Documents</span></span>



| <span data-ttu-id="61cd5-189">Name</span><span class="sxs-lookup"><span data-stu-id="61cd5-189">Name</span></span>      | <span data-ttu-id="61cd5-190">屬性</span><span class="sxs-lookup"><span data-stu-id="61cd5-190">Property</span></span>             | <span data-ttu-id="61cd5-191">優先順序</span><span class="sxs-lookup"><span data-stu-id="61cd5-191">Priority</span></span> |
|-----------|----------------------|----------|
| <span data-ttu-id="61cd5-192">Authors</span><span class="sxs-lookup"><span data-stu-id="61cd5-192">Authors</span></span>   | <span data-ttu-id="61cd5-193">System.Author</span><span class="sxs-lookup"><span data-stu-id="61cd5-193">System.Author</span></span>        | <span data-ttu-id="61cd5-194">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-194">1</span></span>        |
| <span data-ttu-id="61cd5-195">全文檢索</span><span class="sxs-lookup"><span data-stu-id="61cd5-195">Full Text</span></span> | <span data-ttu-id="61cd5-196">System. 全文檢索</span><span class="sxs-lookup"><span data-stu-id="61cd5-196">System.FullText</span></span>      | <span data-ttu-id="61cd5-197">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-197">1</span></span>        |
| <span data-ttu-id="61cd5-198">標籤</span><span class="sxs-lookup"><span data-stu-id="61cd5-198">Tags</span></span>      | <span data-ttu-id="61cd5-199">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="61cd5-199">System.Keywords</span></span>      | <span data-ttu-id="61cd5-200">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-200">1</span></span>        |
| <span data-ttu-id="61cd5-201">類型</span><span class="sxs-lookup"><span data-stu-id="61cd5-201">Type</span></span>      | <span data-ttu-id="61cd5-202">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="61cd5-202">System.PerceivedType</span></span> | <span data-ttu-id="61cd5-203">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-203">1</span></span>        |
| <span data-ttu-id="61cd5-204">類別</span><span class="sxs-lookup"><span data-stu-id="61cd5-204">Category</span></span>  | <span data-ttu-id="61cd5-205">System. Category</span><span class="sxs-lookup"><span data-stu-id="61cd5-205">System.Category</span></span>      | <span data-ttu-id="61cd5-206">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-206">2</span></span>        |
| <span data-ttu-id="61cd5-207">標題</span><span class="sxs-lookup"><span data-stu-id="61cd5-207">Title</span></span>     | <span data-ttu-id="61cd5-208">System.Title</span><span class="sxs-lookup"><span data-stu-id="61cd5-208">System.Title</span></span>         | <span data-ttu-id="61cd5-209">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-209">2</span></span>        |



 

## <a name="generic"></a><span data-ttu-id="61cd5-210">泛型</span><span class="sxs-lookup"><span data-stu-id="61cd5-210">Generic</span></span>



| <span data-ttu-id="61cd5-211">Name</span><span class="sxs-lookup"><span data-stu-id="61cd5-211">Name</span></span>     | <span data-ttu-id="61cd5-212">屬性</span><span class="sxs-lookup"><span data-stu-id="61cd5-212">Property</span></span>             | <span data-ttu-id="61cd5-213">優先順序</span><span class="sxs-lookup"><span data-stu-id="61cd5-213">Priority</span></span> |
|----------|----------------------|----------|
| <span data-ttu-id="61cd5-214">Authors</span><span class="sxs-lookup"><span data-stu-id="61cd5-214">Authors</span></span>  | <span data-ttu-id="61cd5-215">System.Author</span><span class="sxs-lookup"><span data-stu-id="61cd5-215">System.Author</span></span>        | <span data-ttu-id="61cd5-216">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-216">1</span></span>        |
| <span data-ttu-id="61cd5-217">標題</span><span class="sxs-lookup"><span data-stu-id="61cd5-217">Title</span></span>    | <span data-ttu-id="61cd5-218">System.Title</span><span class="sxs-lookup"><span data-stu-id="61cd5-218">System.Title</span></span>         | <span data-ttu-id="61cd5-219">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-219">1</span></span>        |
| <span data-ttu-id="61cd5-220">類型</span><span class="sxs-lookup"><span data-stu-id="61cd5-220">Type</span></span>     | <span data-ttu-id="61cd5-221">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="61cd5-221">System.PerceivedType</span></span> | <span data-ttu-id="61cd5-222">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-222">1</span></span>        |
| <span data-ttu-id="61cd5-223">類別</span><span class="sxs-lookup"><span data-stu-id="61cd5-223">Category</span></span> | <span data-ttu-id="61cd5-224">System. Category</span><span class="sxs-lookup"><span data-stu-id="61cd5-224">System.Category</span></span>      | <span data-ttu-id="61cd5-225">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-225">2</span></span>        |
| <span data-ttu-id="61cd5-226">標籤</span><span class="sxs-lookup"><span data-stu-id="61cd5-226">Tags</span></span>     | <span data-ttu-id="61cd5-227">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="61cd5-227">System.Keywords</span></span>      | <span data-ttu-id="61cd5-228">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-228">2</span></span>        |



 

## <a name="music"></a><span data-ttu-id="61cd5-229">音樂</span><span class="sxs-lookup"><span data-stu-id="61cd5-229">Music</span></span>



| <span data-ttu-id="61cd5-230">Name</span><span class="sxs-lookup"><span data-stu-id="61cd5-230">Name</span></span>         | <span data-ttu-id="61cd5-231">屬性</span><span class="sxs-lookup"><span data-stu-id="61cd5-231">Property</span></span>                     | <span data-ttu-id="61cd5-232">優先順序</span><span class="sxs-lookup"><span data-stu-id="61cd5-232">Priority</span></span> |
|--------------|------------------------------|----------|
| \#           | <span data-ttu-id="61cd5-233">TrackNumber</span><span class="sxs-lookup"><span data-stu-id="61cd5-233">System.Music.TrackNumber</span></span>     | <span data-ttu-id="61cd5-234">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-234">1</span></span>        |
| <span data-ttu-id="61cd5-235">專輯</span><span class="sxs-lookup"><span data-stu-id="61cd5-235">Album</span></span>        | <span data-ttu-id="61cd5-236">AlbumTitle</span><span class="sxs-lookup"><span data-stu-id="61cd5-236">System.Music.AlbumTitle</span></span>      | <span data-ttu-id="61cd5-237">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-237">1</span></span>        |
| <span data-ttu-id="61cd5-238">演出者</span><span class="sxs-lookup"><span data-stu-id="61cd5-238">Artists</span></span>      | <span data-ttu-id="61cd5-239">系統音樂</span><span class="sxs-lookup"><span data-stu-id="61cd5-239">System.Music.Artist</span></span>          | <span data-ttu-id="61cd5-240">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-240">1</span></span>        |
| <span data-ttu-id="61cd5-241">Genre</span><span class="sxs-lookup"><span data-stu-id="61cd5-241">Genre</span></span>        | <span data-ttu-id="61cd5-242">System.object</span><span class="sxs-lookup"><span data-stu-id="61cd5-242">System.Music.Genre</span></span>           | <span data-ttu-id="61cd5-243">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-243">1</span></span>        |
| <span data-ttu-id="61cd5-244">分級</span><span class="sxs-lookup"><span data-stu-id="61cd5-244">Rating</span></span>       | <span data-ttu-id="61cd5-245">系統評分</span><span class="sxs-lookup"><span data-stu-id="61cd5-245">System.Rating</span></span>                | <span data-ttu-id="61cd5-246">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-246">1</span></span>        |
| <span data-ttu-id="61cd5-247">標題</span><span class="sxs-lookup"><span data-stu-id="61cd5-247">Title</span></span>        | <span data-ttu-id="61cd5-248">System.Title</span><span class="sxs-lookup"><span data-stu-id="61cd5-248">System.Title</span></span>                 | <span data-ttu-id="61cd5-249">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-249">1</span></span>        |
| <span data-ttu-id="61cd5-250">專輯演出者</span><span class="sxs-lookup"><span data-stu-id="61cd5-250">Album Artist</span></span> | <span data-ttu-id="61cd5-251">AlbumArtist</span><span class="sxs-lookup"><span data-stu-id="61cd5-251">System.Music.AlbumArtist</span></span>     | <span data-ttu-id="61cd5-252">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-252">2</span></span>        |
| <span data-ttu-id="61cd5-253">位元速度</span><span class="sxs-lookup"><span data-stu-id="61cd5-253">Bit Rate</span></span>     | <span data-ttu-id="61cd5-254">EncodingBitrate</span><span class="sxs-lookup"><span data-stu-id="61cd5-254">System.Audio.EncodingBitrate</span></span> | <span data-ttu-id="61cd5-255">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-255">2</span></span>        |
| <span data-ttu-id="61cd5-256">導體</span><span class="sxs-lookup"><span data-stu-id="61cd5-256">Conductors</span></span>   | <span data-ttu-id="61cd5-257">System.servicemodel</span><span class="sxs-lookup"><span data-stu-id="61cd5-257">System.Music.Conductor</span></span>       | <span data-ttu-id="61cd5-258">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-258">2</span></span>        |
| <span data-ttu-id="61cd5-259">長度</span><span class="sxs-lookup"><span data-stu-id="61cd5-259">Length</span></span>       | <span data-ttu-id="61cd5-260">System.object。持續時間</span><span class="sxs-lookup"><span data-stu-id="61cd5-260">System.Media.Duration</span></span>        | <span data-ttu-id="61cd5-261">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-261">2</span></span>        |
| <span data-ttu-id="61cd5-262">Protected</span><span class="sxs-lookup"><span data-stu-id="61cd5-262">Protected</span></span>    | <span data-ttu-id="61cd5-263">IsProtected</span><span class="sxs-lookup"><span data-stu-id="61cd5-263">System.DRM.IsProtected</span></span>       | <span data-ttu-id="61cd5-264">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-264">2</span></span>        |
| <span data-ttu-id="61cd5-265">Year</span><span class="sxs-lookup"><span data-stu-id="61cd5-265">Year</span></span>         | <span data-ttu-id="61cd5-266">Year</span><span class="sxs-lookup"><span data-stu-id="61cd5-266">System.Media.Year</span></span>            | <span data-ttu-id="61cd5-267">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-267">2</span></span>        |



 

## <a name="pictures"></a><span data-ttu-id="61cd5-268">圖片</span><span class="sxs-lookup"><span data-stu-id="61cd5-268">Pictures</span></span>



| <span data-ttu-id="61cd5-269">Name</span><span class="sxs-lookup"><span data-stu-id="61cd5-269">Name</span></span>          | <span data-ttu-id="61cd5-270">屬性</span><span class="sxs-lookup"><span data-stu-id="61cd5-270">Property</span></span>                        | <span data-ttu-id="61cd5-271">優先順序</span><span class="sxs-lookup"><span data-stu-id="61cd5-271">Priority</span></span> |
|---------------|---------------------------------|----------|
| <span data-ttu-id="61cd5-272">匯入日期</span><span class="sxs-lookup"><span data-stu-id="61cd5-272">Date imported</span></span> | <span data-ttu-id="61cd5-273">System. DateImported</span><span class="sxs-lookup"><span data-stu-id="61cd5-273">System.DateImported</span></span>             | <span data-ttu-id="61cd5-274">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-274">1</span></span>        |
| <span data-ttu-id="61cd5-275">拍攝日期</span><span class="sxs-lookup"><span data-stu-id="61cd5-275">Date Taken</span></span>    | <span data-ttu-id="61cd5-276">DateTaken</span><span class="sxs-lookup"><span data-stu-id="61cd5-276">System.Photo.DateTaken</span></span>          | <span data-ttu-id="61cd5-277">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-277">1</span></span>        |
| <span data-ttu-id="61cd5-278">分級</span><span class="sxs-lookup"><span data-stu-id="61cd5-278">Rating</span></span>        | <span data-ttu-id="61cd5-279">系統評分</span><span class="sxs-lookup"><span data-stu-id="61cd5-279">System.Rating</span></span>                   | <span data-ttu-id="61cd5-280">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-280">1</span></span>        |
| <span data-ttu-id="61cd5-281">標籤</span><span class="sxs-lookup"><span data-stu-id="61cd5-281">Tags</span></span>          | <span data-ttu-id="61cd5-282">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="61cd5-282">System.Keywords</span></span>                 | <span data-ttu-id="61cd5-283">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-283">1</span></span>        |
| <span data-ttu-id="61cd5-284">類型</span><span class="sxs-lookup"><span data-stu-id="61cd5-284">Type</span></span>          | <span data-ttu-id="61cd5-285">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="61cd5-285">System.PerceivedType</span></span>            | <span data-ttu-id="61cd5-286">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-286">1</span></span>        |
| <span data-ttu-id="61cd5-287">Authors</span><span class="sxs-lookup"><span data-stu-id="61cd5-287">Authors</span></span>       | <span data-ttu-id="61cd5-288">System.Author</span><span class="sxs-lookup"><span data-stu-id="61cd5-288">System.Author</span></span>                   | <span data-ttu-id="61cd5-289">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-289">2</span></span>        |
| <span data-ttu-id="61cd5-290">攝影機 maker</span><span class="sxs-lookup"><span data-stu-id="61cd5-290">Camera maker</span></span>  | <span data-ttu-id="61cd5-291">CameraManufacturer</span><span class="sxs-lookup"><span data-stu-id="61cd5-291">System.Photo.CameraManufacturer</span></span> | <span data-ttu-id="61cd5-292">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-292">2</span></span>        |
| <span data-ttu-id="61cd5-293">攝影機模型</span><span class="sxs-lookup"><span data-stu-id="61cd5-293">Camera model</span></span>  | <span data-ttu-id="61cd5-294">CameraModel</span><span class="sxs-lookup"><span data-stu-id="61cd5-294">System.Photo.CameraModel</span></span>        | <span data-ttu-id="61cd5-295">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-295">2</span></span>        |
| <span data-ttu-id="61cd5-296">註解</span><span class="sxs-lookup"><span data-stu-id="61cd5-296">Comments</span></span>      | <span data-ttu-id="61cd5-297">System. Comment</span><span class="sxs-lookup"><span data-stu-id="61cd5-297">System.Comment</span></span>                  | <span data-ttu-id="61cd5-298">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-298">2</span></span>        |
| <span data-ttu-id="61cd5-299">維度</span><span class="sxs-lookup"><span data-stu-id="61cd5-299">Dimensions</span></span>    | <span data-ttu-id="61cd5-300">系統維度</span><span class="sxs-lookup"><span data-stu-id="61cd5-300">System.Image.Dimensions</span></span>         | <span data-ttu-id="61cd5-301">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-301">2</span></span>        |



 

## <a name="videos"></a><span data-ttu-id="61cd5-302">影片</span><span class="sxs-lookup"><span data-stu-id="61cd5-302">Videos</span></span>



| <span data-ttu-id="61cd5-303">Name</span><span class="sxs-lookup"><span data-stu-id="61cd5-303">Name</span></span>         | <span data-ttu-id="61cd5-304">屬性</span><span class="sxs-lookup"><span data-stu-id="61cd5-304">Property</span></span>                 | <span data-ttu-id="61cd5-305">優先順序</span><span class="sxs-lookup"><span data-stu-id="61cd5-305">Priority</span></span> |
|--------------|--------------------------|----------|
| <span data-ttu-id="61cd5-306">長度</span><span class="sxs-lookup"><span data-stu-id="61cd5-306">Length</span></span>       | <span data-ttu-id="61cd5-307">System.object。持續時間</span><span class="sxs-lookup"><span data-stu-id="61cd5-307">System.Media.Duration</span></span>    | <span data-ttu-id="61cd5-308">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-308">1</span></span>        |
| <span data-ttu-id="61cd5-309">分級</span><span class="sxs-lookup"><span data-stu-id="61cd5-309">Rating</span></span>       | <span data-ttu-id="61cd5-310">系統評分</span><span class="sxs-lookup"><span data-stu-id="61cd5-310">System.Rating</span></span>            | <span data-ttu-id="61cd5-311">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-311">1</span></span>        |
| <span data-ttu-id="61cd5-312">標籤</span><span class="sxs-lookup"><span data-stu-id="61cd5-312">Tags</span></span>         | <span data-ttu-id="61cd5-313">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="61cd5-313">System.Keywords</span></span>          | <span data-ttu-id="61cd5-314">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-314">1</span></span>        |
| <span data-ttu-id="61cd5-315">類型</span><span class="sxs-lookup"><span data-stu-id="61cd5-315">Type</span></span>         | <span data-ttu-id="61cd5-316">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="61cd5-316">System.PerceivedType</span></span>     | <span data-ttu-id="61cd5-317">1</span><span class="sxs-lookup"><span data-stu-id="61cd5-317">1</span></span>        |
| <span data-ttu-id="61cd5-318">框架高度</span><span class="sxs-lookup"><span data-stu-id="61cd5-318">Frame height</span></span> | <span data-ttu-id="61cd5-319">FrameHeight</span><span class="sxs-lookup"><span data-stu-id="61cd5-319">System.Video.FrameHeight</span></span> | <span data-ttu-id="61cd5-320">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-320">2</span></span>        |
| <span data-ttu-id="61cd5-321">框架寬度</span><span class="sxs-lookup"><span data-stu-id="61cd5-321">Frame width</span></span>  | <span data-ttu-id="61cd5-322">FrameWidth</span><span class="sxs-lookup"><span data-stu-id="61cd5-322">System.Video.FrameWidth</span></span>  | <span data-ttu-id="61cd5-323">2</span><span class="sxs-lookup"><span data-stu-id="61cd5-323">2</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="61cd5-324">相關主題</span><span class="sxs-lookup"><span data-stu-id="61cd5-324">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="61cd5-325">**概念**</span><span class="sxs-lookup"><span data-stu-id="61cd5-325">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="61cd5-326">開發 Windows Search 的屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="61cd5-326">Developing Property Handlers for Windows Search</span></span>](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

<span data-ttu-id="61cd5-327">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="61cd5-327">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="61cd5-328">屬性系統</span><span class="sxs-lookup"><span data-stu-id="61cd5-328">Property System</span></span>](../properties/building-property-handlers.md)
</dt> <dt>

<span data-ttu-id="61cd5-329">[系統屬性](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="61cd5-329">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> </dl>

 

 
