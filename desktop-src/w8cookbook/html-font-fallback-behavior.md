---
title: HTML 字型回溯行為
description: HTML 字型回溯行為
ms.assetid: 5BDFBD58-0B34-4A58-BFAF-B8BB1DD569DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc7da95c46190fd348dda72edc8283ee6438b00
ms.sourcegitcommit: 80bac5863880f1bd4c1c3e06db27c5d8fb5232b4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "106969945"
---
# <a name="html-font-fallback-behavior"></a><span data-ttu-id="aa1b2-103">HTML 字型回溯行為</span><span class="sxs-lookup"><span data-stu-id="aa1b2-103">HTML font fallback behavior</span></span>

## <a name="platform"></a><span data-ttu-id="aa1b2-104">平台</span><span class="sxs-lookup"><span data-stu-id="aa1b2-104">Platform</span></span>

<span data-ttu-id="aa1b2-105">用戶端-\* \* Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="aa1b2-105">Clients -\*\* Windows 8.1</span></span>  
<span data-ttu-id="aa1b2-106">**伺服器-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="aa1b2-106">**Servers -** Windows Server 2012 R2</span></span>  


## <a name="description"></a><span data-ttu-id="aa1b2-107">Description</span><span class="sxs-lookup"><span data-stu-id="aa1b2-107">Description</span></span>

<span data-ttu-id="aa1b2-108">Microsoft 正在使用 HTML 更新 Windows Store 應用程式中數個語言的 UI 字型邏輯。</span><span class="sxs-lookup"><span data-stu-id="aa1b2-108">Microsoft is updating the logic for UI fonts for several languages in Windows Store apps using HTML.</span></span> <span data-ttu-id="aa1b2-109">UI 字型現在會以每個語言為基礎來決定，而不是使用所有語言的單一字型。</span><span class="sxs-lookup"><span data-stu-id="aa1b2-109">Rather than using a single font for all languages, the UI font will now be determined on a per language basis.</span></span> <span data-ttu-id="aa1b2-110">例如，日文的 UI 字型現在會在使用 HTML 的應用程式中 Meiryo UI。</span><span class="sxs-lookup"><span data-stu-id="aa1b2-110">For example, UI fonts for Japanese will now be Meiryo UI in apps that use HTML.</span></span>

## <a name="manifestation"></a><span data-ttu-id="aa1b2-111">表現</span><span class="sxs-lookup"><span data-stu-id="aa1b2-111">Manifestation</span></span>

<span data-ttu-id="aa1b2-112">相依于舊字型的應用程式看起來可能不同;雖然您的應用程式外觀會因更多可讀取的字型而整體改善，但根據圖元內容大小的版面配置可能會有問題。</span><span class="sxs-lookup"><span data-stu-id="aa1b2-112">Apps that depended on an old font may look different; while your app appearance will be improved overall thanks to more readable fonts, there could be an issue with layouts that depend on pixel-perfect content sizes.</span></span> <span data-ttu-id="aa1b2-113">例如，某些內容行可能大於先前的內容，導致非預期的分行符號及/或調整大小的容器元素。</span><span class="sxs-lookup"><span data-stu-id="aa1b2-113">For example, some lines of content may be bigger than they were previously, causing unexpected line breaks and/or resizing of container elements.</span></span> <span data-ttu-id="aa1b2-114">不過，實際上我們還沒注意到任何現有的應用程式有任何問題。</span><span class="sxs-lookup"><span data-stu-id="aa1b2-114">However, in practice we haven’t noticed any issues with any existing apps.</span></span>

## <a name="solution"></a><span data-ttu-id="aa1b2-115">解決方法</span><span class="sxs-lookup"><span data-stu-id="aa1b2-115">Solution</span></span>

<span data-ttu-id="aa1b2-116">受影響的應用程式可透過 (CSS 指定指定字型來緩和這項行為，例如「font-family： Meiryo UI」 ) ，而不是依賴舊的預設字型。</span><span class="sxs-lookup"><span data-stu-id="aa1b2-116">Affected apps can mitigate this behavior by specifying a given font via CSS (for example, “font-family: Meiryo UI”) instead of relying on the old default fonts.</span></span> <span data-ttu-id="aa1b2-117">下表提供每個腳本名稱的 UI 字型。</span><span class="sxs-lookup"><span data-stu-id="aa1b2-117">The following table provides the UI font for each of the script names.</span></span>



| <span data-ttu-id="aa1b2-118">指令碼名稱</span><span class="sxs-lookup"><span data-stu-id="aa1b2-118">Script Name</span></span>        | <span data-ttu-id="aa1b2-119">UI 字型</span><span class="sxs-lookup"><span data-stu-id="aa1b2-119">UI Font</span></span>               |
|--------------------|-----------------------|
| <span data-ttu-id="aa1b2-120">阿拉伯文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-120">Arabic</span></span>             | <span data-ttu-id="aa1b2-121">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-121">Segoe UI</span></span>              |
| <span data-ttu-id="aa1b2-122">亞美尼亞文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-122">Armenian</span></span>           | <span data-ttu-id="aa1b2-123">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-123">Segoe UI</span></span>              |
| <span data-ttu-id="aa1b2-124">孟加拉文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-124">Bengali</span></span>            | <span data-ttu-id="aa1b2-125">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-125">Nirmala UI</span></span>            |
| <span data-ttu-id="aa1b2-126">符號</span><span class="sxs-lookup"><span data-stu-id="aa1b2-126">Bopomofo</span></span>           | <span data-ttu-id="aa1b2-127">Microsoft JhengHei UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-127">Microsoft JhengHei UI</span></span> |
| <span data-ttu-id="aa1b2-128">盲文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-128">Braille</span></span>            | <span data-ttu-id="aa1b2-129">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="aa1b2-129">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="aa1b2-130">布吉斯文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-130">Buginese</span></span>           | <span data-ttu-id="aa1b2-131">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-131">Leelawadee UI</span></span>         |
| <span data-ttu-id="aa1b2-132">加拿大印第安方言</span><span class="sxs-lookup"><span data-stu-id="aa1b2-132">Canadian Syllabics</span></span> | <span data-ttu-id="aa1b2-133">Gadugi</span><span class="sxs-lookup"><span data-stu-id="aa1b2-133">Gadugi</span></span>                |
| <span data-ttu-id="aa1b2-134">卻洛奇文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-134">Cherokee</span></span>           | <span data-ttu-id="aa1b2-135">Gadugi</span><span class="sxs-lookup"><span data-stu-id="aa1b2-135">Gadugi</span></span>                |
| <span data-ttu-id="aa1b2-136">科普特文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-136">Coptic</span></span>             | <span data-ttu-id="aa1b2-137">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="aa1b2-137">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="aa1b2-138">簡 (簡) </span><span class="sxs-lookup"><span data-stu-id="aa1b2-138">Han (Simplified)</span></span>   | <span data-ttu-id="aa1b2-139">Microsoft YaHei UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-139">Microsoft YaHei UI</span></span>    |
| <span data-ttu-id="aa1b2-140"> (傳統) 的漢字</span><span class="sxs-lookup"><span data-stu-id="aa1b2-140">Han (Traditional)</span></span>  | <span data-ttu-id="aa1b2-141">Microsoft JhengHei UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-141">Microsoft JhengHei UI</span></span> |
| <span data-ttu-id="aa1b2-142">古斯拉夫文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-142">Cyrillic</span></span>           | <span data-ttu-id="aa1b2-143">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-143">Segoe UI</span></span>              |
| <span data-ttu-id="aa1b2-144">梵文字母</span><span class="sxs-lookup"><span data-stu-id="aa1b2-144">Devanagari</span></span>         | <span data-ttu-id="aa1b2-145">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-145">Nirmala UI</span></span>            |
| <span data-ttu-id="aa1b2-146">萊特</span><span class="sxs-lookup"><span data-stu-id="aa1b2-146">Deseret</span></span>            | <span data-ttu-id="aa1b2-147">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="aa1b2-147">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="aa1b2-148">文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-148">Ethiopic</span></span>           | <span data-ttu-id="aa1b2-149">Ebrima</span><span class="sxs-lookup"><span data-stu-id="aa1b2-149">Ebrima</span></span>                |
| <span data-ttu-id="aa1b2-150">喬治亞文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-150">Georgian</span></span>           | <span data-ttu-id="aa1b2-151">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-151">Segoe UI</span></span>              |
| <span data-ttu-id="aa1b2-152">文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-152">Glagolitic</span></span>         | <span data-ttu-id="aa1b2-153">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="aa1b2-153">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="aa1b2-154">哥 特 式</span><span class="sxs-lookup"><span data-stu-id="aa1b2-154">Gothic</span></span>             | <span data-ttu-id="aa1b2-155">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="aa1b2-155">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="aa1b2-156">希臘文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-156">Greek</span></span>              | <span data-ttu-id="aa1b2-157">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-157">Segoe UI</span></span>              |
| <span data-ttu-id="aa1b2-158">古吉拉特文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-158">Gujarati</span></span>           | <span data-ttu-id="aa1b2-159">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-159">Nirmala UI</span></span>            |
| <span data-ttu-id="aa1b2-160">古木基文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-160">Gurmukhi</span></span>           | <span data-ttu-id="aa1b2-161">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-161">Nirmala UI</span></span>            |
| <span data-ttu-id="aa1b2-162">Hebrew</span><span class="sxs-lookup"><span data-stu-id="aa1b2-162">Hebrew</span></span>             | <span data-ttu-id="aa1b2-163">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-163">Segoe UI</span></span>              |
| <span data-ttu-id="aa1b2-164">舊的斜體</span><span class="sxs-lookup"><span data-stu-id="aa1b2-164">Old Italic</span></span>         | <span data-ttu-id="aa1b2-165">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="aa1b2-165">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="aa1b2-166">爪哇文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-166">Javanese</span></span>           | <span data-ttu-id="aa1b2-167">爪哇文文字</span><span class="sxs-lookup"><span data-stu-id="aa1b2-167">Javanese Text</span></span>         |
| <span data-ttu-id="aa1b2-168">日文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-168">Japanese</span></span>           | <span data-ttu-id="aa1b2-169">Meiryo UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-169">Meiryo UI</span></span>             |
| <span data-ttu-id="aa1b2-170">坎那達文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-170">Kannada</span></span>            | <span data-ttu-id="aa1b2-171">Mirmala UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-171">Mirmala UI</span></span>            |
| <span data-ttu-id="aa1b2-172">高棉文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-172">Khmer</span></span>              | <span data-ttu-id="aa1b2-173">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-173">Leelawadee UI</span></span>         |
| <span data-ttu-id="aa1b2-174">韓文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-174">Korean</span></span>             | <span data-ttu-id="aa1b2-175">Malgun Gothic</span><span class="sxs-lookup"><span data-stu-id="aa1b2-175">Malgun Gothic</span></span>         |
| <span data-ttu-id="aa1b2-176">寮文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-176">Lao</span></span>                | <span data-ttu-id="aa1b2-177">Leelawadee</span><span class="sxs-lookup"><span data-stu-id="aa1b2-177">Leelawadee</span></span>            |
| <span data-ttu-id="aa1b2-178">拉丁文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-178">Latin</span></span>              | <span data-ttu-id="aa1b2-179">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-179">Segoe UI</span></span>              |
| <span data-ttu-id="aa1b2-180">馬來亞拉姆文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-180">Malayalam</span></span>          | <span data-ttu-id="aa1b2-181">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-181">Nirmala UI</span></span>            |
| <span data-ttu-id="aa1b2-182">蒙古文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-182">Mongolian</span></span>          | <span data-ttu-id="aa1b2-183">Mongolian Baiti</span><span class="sxs-lookup"><span data-stu-id="aa1b2-183">Mongolian Baiti</span></span>       |
| <span data-ttu-id="aa1b2-184">緬甸</span><span class="sxs-lookup"><span data-stu-id="aa1b2-184">Myanmar</span></span>            | <span data-ttu-id="aa1b2-185">Myanmar Text</span><span class="sxs-lookup"><span data-stu-id="aa1b2-185">Myanmar Text</span></span>          |
| <span data-ttu-id="aa1b2-186">西非書面</span><span class="sxs-lookup"><span data-stu-id="aa1b2-186">N'Ko</span></span>               | <span data-ttu-id="aa1b2-187">Ebrima</span><span class="sxs-lookup"><span data-stu-id="aa1b2-187">Ebrima</span></span>                |
| <span data-ttu-id="aa1b2-188">豎</span><span class="sxs-lookup"><span data-stu-id="aa1b2-188">Ogham</span></span>              | <span data-ttu-id="aa1b2-189">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="aa1b2-189">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="aa1b2-190">桑塔爾文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-190">Ol Chiki</span></span>           | <span data-ttu-id="aa1b2-191">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-191">Nirmala UI</span></span>            |
| <span data-ttu-id="aa1b2-192">舊的土耳其文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-192">Old Turkic</span></span>         | <span data-ttu-id="aa1b2-193">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="aa1b2-193">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="aa1b2-194">歐利亞文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-194">Oriya</span></span>              | <span data-ttu-id="aa1b2-195">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-195">Nirmala UI</span></span>            |
| <span data-ttu-id="aa1b2-196">文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-196">Osmanya</span></span>            | <span data-ttu-id="aa1b2-197">Ebrima</span><span class="sxs-lookup"><span data-stu-id="aa1b2-197">Ebrima</span></span>                |
| <span data-ttu-id="aa1b2-198">八位 pa</span><span class="sxs-lookup"><span data-stu-id="aa1b2-198">Phags-pa</span></span>           | <span data-ttu-id="aa1b2-199">Microsoft PhagsPa</span><span class="sxs-lookup"><span data-stu-id="aa1b2-199">Microsoft PhagsPa</span></span>     |
| <span data-ttu-id="aa1b2-200">符文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-200">Runic</span></span>              | <span data-ttu-id="aa1b2-201">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="aa1b2-201">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="aa1b2-202">Sora Sompeng</span><span class="sxs-lookup"><span data-stu-id="aa1b2-202">Sora Sompeng</span></span>       | <span data-ttu-id="aa1b2-203">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-203">Nirmala UI</span></span>            |
| <span data-ttu-id="aa1b2-204">僧伽羅文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-204">Sinhala</span></span>            | <span data-ttu-id="aa1b2-205">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-205">Nirmala UI</span></span>            |
| <span data-ttu-id="aa1b2-206">敘利亞文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-206">Syriac</span></span>             | <span data-ttu-id="aa1b2-207">Estrangelo Edessa</span><span class="sxs-lookup"><span data-stu-id="aa1b2-207">Estrangelo Edessa</span></span>     |
| <span data-ttu-id="aa1b2-208">泰 Le</span><span class="sxs-lookup"><span data-stu-id="aa1b2-208">Tai Le</span></span>             | <span data-ttu-id="aa1b2-209">Microsoft Tai Le</span><span class="sxs-lookup"><span data-stu-id="aa1b2-209">Microsoft Tai Le</span></span>      |
| <span data-ttu-id="aa1b2-210">新傣文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-210">New Tai Lue</span></span>        | <span data-ttu-id="aa1b2-211">Microsoft New Tai Lue</span><span class="sxs-lookup"><span data-stu-id="aa1b2-211">Microsoft New Tai Lue</span></span> |
| <span data-ttu-id="aa1b2-212">坦米爾文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-212">Tamil</span></span>              | <span data-ttu-id="aa1b2-213">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-213">Nirmala UI</span></span>            |
| <span data-ttu-id="aa1b2-214">泰盧固文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-214">Telugu</span></span>             | <span data-ttu-id="aa1b2-215">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-215">Nirmala UI</span></span>            |
| <span data-ttu-id="aa1b2-216">納</span><span class="sxs-lookup"><span data-stu-id="aa1b2-216">Tifinagh</span></span>           | <span data-ttu-id="aa1b2-217">Ebrima</span><span class="sxs-lookup"><span data-stu-id="aa1b2-217">Ebrima</span></span>                |
| <span data-ttu-id="aa1b2-218">塔安那文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-218">Thaana</span></span>             | <span data-ttu-id="aa1b2-219">MV Boli</span><span class="sxs-lookup"><span data-stu-id="aa1b2-219">MV Boli</span></span>               |
| <span data-ttu-id="aa1b2-220">泰文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-220">Thai</span></span>               | <span data-ttu-id="aa1b2-221">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="aa1b2-221">Leelawadee UI</span></span>         |
| <span data-ttu-id="aa1b2-222">西藏文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-222">Tibetan</span></span>            | <span data-ttu-id="aa1b2-223">Microsoft Himalaya</span><span class="sxs-lookup"><span data-stu-id="aa1b2-223">Microsoft Himalaya</span></span>    |
| <span data-ttu-id="aa1b2-224">范文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-224">Vai</span></span>                | <span data-ttu-id="aa1b2-225">Ebrima</span><span class="sxs-lookup"><span data-stu-id="aa1b2-225">Ebrima</span></span>                |
| <span data-ttu-id="aa1b2-226">爨文</span><span class="sxs-lookup"><span data-stu-id="aa1b2-226">Yi</span></span>                 | <span data-ttu-id="aa1b2-227">Microsoft Yi Baiti</span><span class="sxs-lookup"><span data-stu-id="aa1b2-227">Microsoft Yi Baiti</span></span>    |



 

 

 




