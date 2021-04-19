---
description: FONTSIGNATURE 和 LOCALESIGNATURE 結構中會使用 Unicode 子集位欄位 (USBs) 。
ms.assetid: f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d
title: Unicode 子集位欄位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fced251b1bf8e04dd4c0d7d7cb0dca15c8bdfa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981013"
---
# <a name="unicode-subset-bitfields"></a><span data-ttu-id="b51dd-103">Unicode 子集位欄位</span><span class="sxs-lookup"><span data-stu-id="b51dd-103">Unicode Subset Bitfields</span></span>

<span data-ttu-id="b51dd-104">[**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature)和 [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature)結構中會使用 Unicode 子集位欄位 (USBs) 。</span><span class="sxs-lookup"><span data-stu-id="b51dd-104">The Unicode subset bitfields (USBs) are used in the [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) and [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) structures.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b51dd-105">bit</span><span class="sxs-lookup"><span data-stu-id="b51dd-105">Bit</span></span></th>
<th><span data-ttu-id="b51dd-106">Unicode 子範圍</span><span class="sxs-lookup"><span data-stu-id="b51dd-106">Unicode subrange</span></span></th>
<th><span data-ttu-id="b51dd-107">描述</span><span class="sxs-lookup"><span data-stu-id="b51dd-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b51dd-108">0</span><span class="sxs-lookup"><span data-stu-id="b51dd-108">0</span></span></td>
<td><span data-ttu-id="b51dd-109">0000 - 007F</span><span class="sxs-lookup"><span data-stu-id="b51dd-109">0000 - 007F</span></span></td>
<td><span data-ttu-id="b51dd-110">基本拉丁</span><span class="sxs-lookup"><span data-stu-id="b51dd-110">Basic Latin</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-111">1</span><span class="sxs-lookup"><span data-stu-id="b51dd-111">1</span></span></td>
<td><span data-ttu-id="b51dd-112">0080 - 00FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-112">0080 - 00FF</span></span></td>
<td><span data-ttu-id="b51dd-113">拉丁文1補充</span><span class="sxs-lookup"><span data-stu-id="b51dd-113">Latin-1 Supplement</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-114">2</span><span class="sxs-lookup"><span data-stu-id="b51dd-114">2</span></span></td>
<td><span data-ttu-id="b51dd-115">0100 - 017F</span><span class="sxs-lookup"><span data-stu-id="b51dd-115">0100 - 017F</span></span></td>
<td><span data-ttu-id="b51dd-116">拉丁文擴充-A</span><span class="sxs-lookup"><span data-stu-id="b51dd-116">Latin Extended-A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-117">3</span><span class="sxs-lookup"><span data-stu-id="b51dd-117">3</span></span></td>
<td><span data-ttu-id="b51dd-118">0180 - 024F</span><span class="sxs-lookup"><span data-stu-id="b51dd-118">0180 - 024F</span></span></td>
<td><span data-ttu-id="b51dd-119">拉丁文擴充-B</span><span class="sxs-lookup"><span data-stu-id="b51dd-119">Latin Extended-B</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="b51dd-120">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-120">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-121">0250 - 02AF</span><span class="sxs-lookup"><span data-stu-id="b51dd-121">0250 - 02AF</span></span></td>
<td><span data-ttu-id="b51dd-122">IPA 延伸模組</span><span class="sxs-lookup"><span data-stu-id="b51dd-122">IPA Extensions</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-123">1D00 - 1D7F</span><span class="sxs-lookup"><span data-stu-id="b51dd-123">1D00 - 1D7F</span></span></td>
<td><span data-ttu-id="b51dd-124">拼音延伸模組</span><span class="sxs-lookup"><span data-stu-id="b51dd-124">Phonetic Extensions</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-125">1D80 - 1DBF</span><span class="sxs-lookup"><span data-stu-id="b51dd-125">1D80 - 1DBF</span></span></td>
<td><span data-ttu-id="b51dd-126">注音擴充功能補充</span><span class="sxs-lookup"><span data-stu-id="b51dd-126">Phonetic Extensions Supplement</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="b51dd-127">5 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-127">5${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-128">02B0 - 02FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-128">02B0 - 02FF</span></span></td>
<td><span data-ttu-id="b51dd-129">間距修飾詞字母</span><span class="sxs-lookup"><span data-stu-id="b51dd-129">Spacing Modifier Letters</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-130">A700 - A71F</span><span class="sxs-lookup"><span data-stu-id="b51dd-130">A700 - A71F</span></span></td>
<td><span data-ttu-id="b51dd-131">修飾詞音調字母</span><span class="sxs-lookup"><span data-stu-id="b51dd-131">Modifier Tone Letters</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="b51dd-132">6 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-132">6${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-133">0300 - 036F</span><span class="sxs-lookup"><span data-stu-id="b51dd-133">0300 - 036F</span></span></td>
<td><span data-ttu-id="b51dd-134">結合變音符號標記</span><span class="sxs-lookup"><span data-stu-id="b51dd-134">Combining Diacritical Marks</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-135">1DC0 - 1DFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-135">1DC0 - 1DFF</span></span></td>
<td><span data-ttu-id="b51dd-136">結合變音符號補充符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-136">Combining Diacritical Marks Supplement</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-137">7</span><span class="sxs-lookup"><span data-stu-id="b51dd-137">7</span></span></td>
<td><span data-ttu-id="b51dd-138">0370 - 03FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-138">0370 - 03FF</span></span></td>
<td><span data-ttu-id="b51dd-139">希臘文和哥普特文</span><span class="sxs-lookup"><span data-stu-id="b51dd-139">Greek and Coptic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-140">8</span><span class="sxs-lookup"><span data-stu-id="b51dd-140">8</span></span></td>
<td><span data-ttu-id="b51dd-141">2C80 - 2CFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-141">2C80 - 2CFF</span></span></td>
<td><span data-ttu-id="b51dd-142">科普特文</span><span class="sxs-lookup"><span data-stu-id="b51dd-142">Coptic</span></span></td>
</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="b51dd-143">9 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-143">9${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-144">0400 - 04FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-144">0400 - 04FF</span></span></td>
<td><span data-ttu-id="b51dd-145">古斯拉夫文</span><span class="sxs-lookup"><span data-stu-id="b51dd-145">Cyrillic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-146">0500 - 052F</span><span class="sxs-lookup"><span data-stu-id="b51dd-146">0500 - 052F</span></span></td>
<td><span data-ttu-id="b51dd-147">斯拉夫文增補</span><span class="sxs-lookup"><span data-stu-id="b51dd-147">Cyrillic Supplement</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-148">2DE0 - 2DFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-148">2DE0 - 2DFF</span></span></td>
<td><span data-ttu-id="b51dd-149">斯拉夫文擴充-A</span><span class="sxs-lookup"><span data-stu-id="b51dd-149">Cyrillic Extended-A</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-150">A640 - A69F</span><span class="sxs-lookup"><span data-stu-id="b51dd-150">A640 - A69F</span></span></td>
<td><span data-ttu-id="b51dd-151">斯拉夫文擴充-B</span><span class="sxs-lookup"><span data-stu-id="b51dd-151">Cyrillic Extended-B</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-152">10</span><span class="sxs-lookup"><span data-stu-id="b51dd-152">10</span></span></td>
<td><span data-ttu-id="b51dd-153">0530 - 058F</span><span class="sxs-lookup"><span data-stu-id="b51dd-153">0530 - 058F</span></span></td>
<td><span data-ttu-id="b51dd-154">亞美尼亞文</span><span class="sxs-lookup"><span data-stu-id="b51dd-154">Armenian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-155">11</span><span class="sxs-lookup"><span data-stu-id="b51dd-155">11</span></span></td>
<td><span data-ttu-id="b51dd-156">0590 - 05FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-156">0590 - 05FF</span></span></td>
<td><span data-ttu-id="b51dd-157">Hebrew</span><span class="sxs-lookup"><span data-stu-id="b51dd-157">Hebrew</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-158">12</span><span class="sxs-lookup"><span data-stu-id="b51dd-158">12</span></span></td>
<td><span data-ttu-id="b51dd-159">A500-A63F</span><span class="sxs-lookup"><span data-stu-id="b51dd-159">A500 - A63F</span></span></td>
<td><span data-ttu-id="b51dd-160">范文</span><span class="sxs-lookup"><span data-stu-id="b51dd-160">Vai</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="b51dd-161">13 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-161">13${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-162">0600 - 06FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-162">0600 - 06FF</span></span></td>
<td><span data-ttu-id="b51dd-163">阿拉伯文</span><span class="sxs-lookup"><span data-stu-id="b51dd-163">Arabic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-164">0750-077F</span><span class="sxs-lookup"><span data-stu-id="b51dd-164">0750 - 077F</span></span></td>
<td><span data-ttu-id="b51dd-165">阿拉伯文增補</span><span class="sxs-lookup"><span data-stu-id="b51dd-165">Arabic Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-166">14</span><span class="sxs-lookup"><span data-stu-id="b51dd-166">14</span></span></td>
<td><span data-ttu-id="b51dd-167">07C0 - 07FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-167">07C0 - 07FF</span></span></td>
<td><span data-ttu-id="b51dd-168">NKo</span><span class="sxs-lookup"><span data-stu-id="b51dd-168">NKo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-169">15</span><span class="sxs-lookup"><span data-stu-id="b51dd-169">15</span></span></td>
<td><span data-ttu-id="b51dd-170">0900 - 097F</span><span class="sxs-lookup"><span data-stu-id="b51dd-170">0900 - 097F</span></span></td>
<td><span data-ttu-id="b51dd-171">梵文字母</span><span class="sxs-lookup"><span data-stu-id="b51dd-171">Devanagari</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-172">16</span><span class="sxs-lookup"><span data-stu-id="b51dd-172">16</span></span></td>
<td><span data-ttu-id="b51dd-173">0980 - 09FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-173">0980 - 09FF</span></span></td>
<td><span data-ttu-id="b51dd-174">孟加拉文</span><span class="sxs-lookup"><span data-stu-id="b51dd-174">Bangla</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-175">17</span><span class="sxs-lookup"><span data-stu-id="b51dd-175">17</span></span></td>
<td><span data-ttu-id="b51dd-176">0A00 - 0A7F</span><span class="sxs-lookup"><span data-stu-id="b51dd-176">0A00 - 0A7F</span></span></td>
<td><span data-ttu-id="b51dd-177">古木基文</span><span class="sxs-lookup"><span data-stu-id="b51dd-177">Gurmukhi</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-178">18</span><span class="sxs-lookup"><span data-stu-id="b51dd-178">18</span></span></td>
<td><span data-ttu-id="b51dd-179">0A80 - 0AFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-179">0A80 - 0AFF</span></span></td>
<td><span data-ttu-id="b51dd-180">古吉拉特文</span><span class="sxs-lookup"><span data-stu-id="b51dd-180">Gujarati</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-181">19</span><span class="sxs-lookup"><span data-stu-id="b51dd-181">19</span></span></td>
<td><span data-ttu-id="b51dd-182">0B00 - 0B7F</span><span class="sxs-lookup"><span data-stu-id="b51dd-182">0B00 - 0B7F</span></span></td>
<td><span data-ttu-id="b51dd-183">歐迪亞文</span><span class="sxs-lookup"><span data-stu-id="b51dd-183">Odia</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-184">20</span><span class="sxs-lookup"><span data-stu-id="b51dd-184">20</span></span></td>
<td><span data-ttu-id="b51dd-185">0B80 - 0BFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-185">0B80 - 0BFF</span></span></td>
<td><span data-ttu-id="b51dd-186">坦米爾文</span><span class="sxs-lookup"><span data-stu-id="b51dd-186">Tamil</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-187">21</span><span class="sxs-lookup"><span data-stu-id="b51dd-187">21</span></span></td>
<td><span data-ttu-id="b51dd-188">0C00 - 0C7F</span><span class="sxs-lookup"><span data-stu-id="b51dd-188">0C00 - 0C7F</span></span></td>
<td><span data-ttu-id="b51dd-189">泰盧固文</span><span class="sxs-lookup"><span data-stu-id="b51dd-189">Telugu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-190">22</span><span class="sxs-lookup"><span data-stu-id="b51dd-190">22</span></span></td>
<td><span data-ttu-id="b51dd-191">0C80 - 0CFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-191">0C80 - 0CFF</span></span></td>
<td><span data-ttu-id="b51dd-192">坎那達文</span><span class="sxs-lookup"><span data-stu-id="b51dd-192">Kannada</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-193">23</span><span class="sxs-lookup"><span data-stu-id="b51dd-193">23</span></span></td>
<td><span data-ttu-id="b51dd-194">0D00 - 0D7F</span><span class="sxs-lookup"><span data-stu-id="b51dd-194">0D00 - 0D7F</span></span></td>
<td><span data-ttu-id="b51dd-195">馬來亞拉姆文</span><span class="sxs-lookup"><span data-stu-id="b51dd-195">Malayalam</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-196">24</span><span class="sxs-lookup"><span data-stu-id="b51dd-196">24</span></span></td>
<td><span data-ttu-id="b51dd-197">0E00 - 0E7F</span><span class="sxs-lookup"><span data-stu-id="b51dd-197">0E00 - 0E7F</span></span></td>
<td><span data-ttu-id="b51dd-198">泰文</span><span class="sxs-lookup"><span data-stu-id="b51dd-198">Thai</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-199">25</span><span class="sxs-lookup"><span data-stu-id="b51dd-199">25</span></span></td>
<td><span data-ttu-id="b51dd-200">0E80 - 0EFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-200">0E80 - 0EFF</span></span></td>
<td><span data-ttu-id="b51dd-201">寮文</span><span class="sxs-lookup"><span data-stu-id="b51dd-201">Lao</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="b51dd-202">26 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-202">26${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-203">10A0 - 10FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-203">10A0 - 10FF</span></span></td>
<td><span data-ttu-id="b51dd-204">喬治亞文</span><span class="sxs-lookup"><span data-stu-id="b51dd-204">Georgian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-205">2D00 - 2D2F</span><span class="sxs-lookup"><span data-stu-id="b51dd-205">2D00 - 2D2F</span></span></td>
<td><span data-ttu-id="b51dd-206">格魯吉亞文補充</span><span class="sxs-lookup"><span data-stu-id="b51dd-206">Georgian Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-207">27</span><span class="sxs-lookup"><span data-stu-id="b51dd-207">27</span></span></td>
<td><span data-ttu-id="b51dd-208">1B00 - 1B7F</span><span class="sxs-lookup"><span data-stu-id="b51dd-208">1B00 - 1B7F</span></span></td>
<td><span data-ttu-id="b51dd-209">峇里文</span><span class="sxs-lookup"><span data-stu-id="b51dd-209">Balinese</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-210">28</span><span class="sxs-lookup"><span data-stu-id="b51dd-210">28</span></span></td>
<td><span data-ttu-id="b51dd-211">1100 - 11FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-211">1100 - 11FF</span></span></td>
<td><span data-ttu-id="b51dd-212">韓文拼音字母</span><span class="sxs-lookup"><span data-stu-id="b51dd-212">Hangul Jamo</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="b51dd-213">29 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-213">29${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-214">1E00 - 1EFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-214">1E00 - 1EFF</span></span></td>
<td><span data-ttu-id="b51dd-215">其他拉丁文擴充</span><span class="sxs-lookup"><span data-stu-id="b51dd-215">Latin Extended Additional</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-216">2C60 - 2C7F</span><span class="sxs-lookup"><span data-stu-id="b51dd-216">2C60 - 2C7F</span></span></td>
<td><span data-ttu-id="b51dd-217">拉丁擴充-C</span><span class="sxs-lookup"><span data-stu-id="b51dd-217">Latin Extended-C</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-218">A720 - A7FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-218">A720 - A7FF</span></span></td>
<td><span data-ttu-id="b51dd-219">拉丁文擴充-D</span><span class="sxs-lookup"><span data-stu-id="b51dd-219">Latin Extended-D</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-220">30</span><span class="sxs-lookup"><span data-stu-id="b51dd-220">30</span></span></td>
<td><span data-ttu-id="b51dd-221">1F00 - 1FFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-221">1F00 - 1FFF</span></span></td>
<td><span data-ttu-id="b51dd-222">希臘文擴充</span><span class="sxs-lookup"><span data-stu-id="b51dd-222">Greek Extended</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="b51dd-223">31 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-223">31${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-224">2000 - 206F</span><span class="sxs-lookup"><span data-stu-id="b51dd-224">2000 - 206F</span></span></td>
<td><span data-ttu-id="b51dd-225">一般標點符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-225">General Punctuation</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-226">2E00 - 2E7F</span><span class="sxs-lookup"><span data-stu-id="b51dd-226">2E00 - 2E7F</span></span></td>
<td><span data-ttu-id="b51dd-227">補充標點符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-227">Supplemental Punctuation</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-228">32</span><span class="sxs-lookup"><span data-stu-id="b51dd-228">32</span></span></td>
<td><span data-ttu-id="b51dd-229">2070 - 209F</span><span class="sxs-lookup"><span data-stu-id="b51dd-229">2070 - 209F</span></span></td>
<td><span data-ttu-id="b51dd-230">上標和下標</span><span class="sxs-lookup"><span data-stu-id="b51dd-230">Superscripts And Subscripts</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-231">33</span><span class="sxs-lookup"><span data-stu-id="b51dd-231">33</span></span></td>
<td><span data-ttu-id="b51dd-232">20A0 - 20CF</span><span class="sxs-lookup"><span data-stu-id="b51dd-232">20A0 - 20CF</span></span></td>
<td><span data-ttu-id="b51dd-233">貨幣符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-233">Currency Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-234">34</span><span class="sxs-lookup"><span data-stu-id="b51dd-234">34</span></span></td>
<td><span data-ttu-id="b51dd-235">20D0 - 20FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-235">20D0 - 20FF</span></span></td>
<td><span data-ttu-id="b51dd-236">合併符號的變音符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-236">Combining Diacritical Marks For Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-237">35</span><span class="sxs-lookup"><span data-stu-id="b51dd-237">35</span></span></td>
<td><span data-ttu-id="b51dd-238">2100 - 214F</span><span class="sxs-lookup"><span data-stu-id="b51dd-238">2100 - 214F</span></span></td>
<td><span data-ttu-id="b51dd-239">字母符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-239">Letterlike Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-240">36</span><span class="sxs-lookup"><span data-stu-id="b51dd-240">36</span></span></td>
<td><span data-ttu-id="b51dd-241">2150 - 218F</span><span class="sxs-lookup"><span data-stu-id="b51dd-241">2150 - 218F</span></span></td>
<td><span data-ttu-id="b51dd-242">數位形式</span><span class="sxs-lookup"><span data-stu-id="b51dd-242">Number Forms</span></span></td>
</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="b51dd-243">37 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-243">37${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-244">2190 - 21FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-244">2190 - 21FF</span></span></td>
<td><span data-ttu-id="b51dd-245">箭頭</span><span class="sxs-lookup"><span data-stu-id="b51dd-245">Arrows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-246">27F0 - 27FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-246">27F0 - 27FF</span></span></td>
<td><span data-ttu-id="b51dd-247">補充箭號-A</span><span class="sxs-lookup"><span data-stu-id="b51dd-247">Supplemental Arrows-A</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-248">2900 - 297F</span><span class="sxs-lookup"><span data-stu-id="b51dd-248">2900 - 297F</span></span></td>
<td><span data-ttu-id="b51dd-249">補充箭號-B</span><span class="sxs-lookup"><span data-stu-id="b51dd-249">Supplemental Arrows-B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-250">2B00 - 2BFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-250">2B00 - 2BFF</span></span></td>
<td><span data-ttu-id="b51dd-251">其他符號和箭號</span><span class="sxs-lookup"><span data-stu-id="b51dd-251">Miscellaneous Symbols and Arrows</span></span></td>

</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="b51dd-252">38 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-252">38${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-253">2200 - 22FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-253">2200 - 22FF</span></span></td>
<td><span data-ttu-id="b51dd-254">數學運算子</span><span class="sxs-lookup"><span data-stu-id="b51dd-254">Mathematical Operators</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-255">27C0 - 27EF</span><span class="sxs-lookup"><span data-stu-id="b51dd-255">27C0 - 27EF</span></span></td>
<td><span data-ttu-id="b51dd-256">其他數學符號-A</span><span class="sxs-lookup"><span data-stu-id="b51dd-256">Miscellaneous Mathematical Symbols-A</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-257">2980 - 29FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-257">2980 - 29FF</span></span></td>
<td><span data-ttu-id="b51dd-258">其他數學符號-B</span><span class="sxs-lookup"><span data-stu-id="b51dd-258">Miscellaneous Mathematical Symbols-B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-259">2A00 - 2AFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-259">2A00 - 2AFF</span></span></td>
<td><span data-ttu-id="b51dd-260">補充的數學運算子</span><span class="sxs-lookup"><span data-stu-id="b51dd-260">Supplemental Mathematical Operators</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-261">39</span><span class="sxs-lookup"><span data-stu-id="b51dd-261">39</span></span></td>
<td><span data-ttu-id="b51dd-262">2300 - 23FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-262">2300 - 23FF</span></span></td>
<td><span data-ttu-id="b51dd-263">其他技術</span><span class="sxs-lookup"><span data-stu-id="b51dd-263">Miscellaneous Technical</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-264">40</span><span class="sxs-lookup"><span data-stu-id="b51dd-264">40</span></span></td>
<td><span data-ttu-id="b51dd-265">2400 - 243F</span><span class="sxs-lookup"><span data-stu-id="b51dd-265">2400 - 243F</span></span></td>
<td><span data-ttu-id="b51dd-266">控制圖片</span><span class="sxs-lookup"><span data-stu-id="b51dd-266">Control Pictures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-267">41</span><span class="sxs-lookup"><span data-stu-id="b51dd-267">41</span></span></td>
<td><span data-ttu-id="b51dd-268">2440 - 245F</span><span class="sxs-lookup"><span data-stu-id="b51dd-268">2440 - 245F</span></span></td>
<td><span data-ttu-id="b51dd-269">光學字元辨識</span><span class="sxs-lookup"><span data-stu-id="b51dd-269">Optical Character Recognition</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-270">42</span><span class="sxs-lookup"><span data-stu-id="b51dd-270">42</span></span></td>
<td><span data-ttu-id="b51dd-271">2460 - 24FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-271">2460 - 24FF</span></span></td>
<td><span data-ttu-id="b51dd-272">包含英數位元</span><span class="sxs-lookup"><span data-stu-id="b51dd-272">Enclosed Alphanumerics</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-273">43</span><span class="sxs-lookup"><span data-stu-id="b51dd-273">43</span></span></td>
<td><span data-ttu-id="b51dd-274">2500 - 257F</span><span class="sxs-lookup"><span data-stu-id="b51dd-274">2500 - 257F</span></span></td>
<td><span data-ttu-id="b51dd-275">盒繪圖</span><span class="sxs-lookup"><span data-stu-id="b51dd-275">Box Drawing</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-276">44</span><span class="sxs-lookup"><span data-stu-id="b51dd-276">44</span></span></td>
<td><span data-ttu-id="b51dd-277">2580 - 259F</span><span class="sxs-lookup"><span data-stu-id="b51dd-277">2580 - 259F</span></span></td>
<td><span data-ttu-id="b51dd-278">Block 元素</span><span class="sxs-lookup"><span data-stu-id="b51dd-278">Block Elements</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-279">45</span><span class="sxs-lookup"><span data-stu-id="b51dd-279">45</span></span></td>
<td><span data-ttu-id="b51dd-280">25A0 - 25FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-280">25A0 - 25FF</span></span></td>
<td><span data-ttu-id="b51dd-281">幾何圖形</span><span class="sxs-lookup"><span data-stu-id="b51dd-281">Geometric Shapes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-282">46</span><span class="sxs-lookup"><span data-stu-id="b51dd-282">46</span></span></td>
<td><span data-ttu-id="b51dd-283">2600 - 26FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-283">2600 - 26FF</span></span></td>
<td><span data-ttu-id="b51dd-284">其他符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-284">Miscellaneous Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-285">47</span><span class="sxs-lookup"><span data-stu-id="b51dd-285">47</span></span></td>
<td><span data-ttu-id="b51dd-286">2700 - 27BF</span><span class="sxs-lookup"><span data-stu-id="b51dd-286">2700 - 27BF</span></span></td>
<td><span data-ttu-id="b51dd-287">Dingbats</span><span class="sxs-lookup"><span data-stu-id="b51dd-287">Dingbats</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-288">48</span><span class="sxs-lookup"><span data-stu-id="b51dd-288">48</span></span></td>
<td><span data-ttu-id="b51dd-289">3000 - 303F</span><span class="sxs-lookup"><span data-stu-id="b51dd-289">3000 - 303F</span></span></td>
<td><span data-ttu-id="b51dd-290">CJK 符號和標點符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-290">CJK Symbols And Punctuation</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-291">49</span><span class="sxs-lookup"><span data-stu-id="b51dd-291">49</span></span></td>
<td><span data-ttu-id="b51dd-292">3040 - 309F</span><span class="sxs-lookup"><span data-stu-id="b51dd-292">3040 - 309F</span></span></td>
<td><span data-ttu-id="b51dd-293">平假名</span><span class="sxs-lookup"><span data-stu-id="b51dd-293">Hiragana</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="b51dd-294">50 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-294">50${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-295">30A0 - 30FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-295">30A0 - 30FF</span></span></td>
<td><span data-ttu-id="b51dd-296">片假名</span><span class="sxs-lookup"><span data-stu-id="b51dd-296">Katakana</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-297">31F0 - 31FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-297">31F0 - 31FF</span></span></td>
<td><span data-ttu-id="b51dd-298">片假名注音延伸模組</span><span class="sxs-lookup"><span data-stu-id="b51dd-298">Katakana Phonetic Extensions</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="b51dd-299">51 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-299">51${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-300">3100 - 312F</span><span class="sxs-lookup"><span data-stu-id="b51dd-300">3100 - 312F</span></span></td>
<td><span data-ttu-id="b51dd-301">符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-301">Bopomofo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-302">31A0 - 31BF</span><span class="sxs-lookup"><span data-stu-id="b51dd-302">31A0 - 31BF</span></span></td>
<td><span data-ttu-id="b51dd-303">注音擴充</span><span class="sxs-lookup"><span data-stu-id="b51dd-303">Bopomofo Extended</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-304">52</span><span class="sxs-lookup"><span data-stu-id="b51dd-304">52</span></span></td>
<td><span data-ttu-id="b51dd-305">3130 - 318F</span><span class="sxs-lookup"><span data-stu-id="b51dd-305">3130 - 318F</span></span></td>
<td><span data-ttu-id="b51dd-306">韓文相容性拼音字母</span><span class="sxs-lookup"><span data-stu-id="b51dd-306">Hangul Compatibility Jamo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-307">53</span><span class="sxs-lookup"><span data-stu-id="b51dd-307">53</span></span></td>
<td><span data-ttu-id="b51dd-308">A840 - A87F</span><span class="sxs-lookup"><span data-stu-id="b51dd-308">A840 - A87F</span></span></td>
<td><span data-ttu-id="b51dd-309">八位 pa</span><span class="sxs-lookup"><span data-stu-id="b51dd-309">Phags-pa</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-310">54</span><span class="sxs-lookup"><span data-stu-id="b51dd-310">54</span></span></td>
<td><span data-ttu-id="b51dd-311">3200 - 32FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-311">3200 - 32FF</span></span></td>
<td><span data-ttu-id="b51dd-312">包含 CJK 字母和月</span><span class="sxs-lookup"><span data-stu-id="b51dd-312">Enclosed CJK Letters And Months</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-313">55</span><span class="sxs-lookup"><span data-stu-id="b51dd-313">55</span></span></td>
<td><span data-ttu-id="b51dd-314">3300 - 33FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-314">3300 - 33FF</span></span></td>
<td><span data-ttu-id="b51dd-315">CJK 相容性</span><span class="sxs-lookup"><span data-stu-id="b51dd-315">CJK Compatibility</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-316">56</span><span class="sxs-lookup"><span data-stu-id="b51dd-316">56</span></span></td>
<td><span data-ttu-id="b51dd-317">AC00 - D7AF</span><span class="sxs-lookup"><span data-stu-id="b51dd-317">AC00 - D7AF</span></span></td>
<td><span data-ttu-id="b51dd-318">韓文音節</span><span class="sxs-lookup"><span data-stu-id="b51dd-318">Hangul Syllables</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-319">57</span><span class="sxs-lookup"><span data-stu-id="b51dd-319">57</span></span></td>
<td><span data-ttu-id="b51dd-320">D800-DFFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-320">D800 - DFFF</span></span></td>
<td><span data-ttu-id="b51dd-321">非平面0。</span><span class="sxs-lookup"><span data-stu-id="b51dd-321">Non-Plane 0.</span></span> <span data-ttu-id="b51dd-322">請注意，設定這個位表示至少有一個增補程式碼點超出這個字型所支援的基本多語系平面 (BMP) 。</span><span class="sxs-lookup"><span data-stu-id="b51dd-322">Note that setting this bit implies that there is at least one supplementary code point beyond the Basic Multilingual Plane (BMP) that is supported by this font.</span></span> <span data-ttu-id="b51dd-323">請參閱 <a href="surrogates-and-supplementary-characters.md">代理和補充字元</a>。</span><span class="sxs-lookup"><span data-stu-id="b51dd-323">See <a href="surrogates-and-supplementary-characters.md">Surrogates and Supplementary Characters</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-324">58</span><span class="sxs-lookup"><span data-stu-id="b51dd-324">58</span></span></td>
<td><span data-ttu-id="b51dd-325">10900-1091F</span><span class="sxs-lookup"><span data-stu-id="b51dd-325">10900 - 1091F</span></span></td>
<td><span data-ttu-id="b51dd-326">腓 尼 基</span><span class="sxs-lookup"><span data-stu-id="b51dd-326">Phoenician</span></span></td>
</tr>
<tr class="even">
<td rowspan="7"><span data-ttu-id="b51dd-327">59 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-327">59${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-328">2E80 - 2EFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-328">2E80 - 2EFF</span></span></td>
<td><span data-ttu-id="b51dd-329">CJK 根式補充</span><span class="sxs-lookup"><span data-stu-id="b51dd-329">CJK Radicals Supplement</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-330">2F00 - 2FDF</span><span class="sxs-lookup"><span data-stu-id="b51dd-330">2F00 - 2FDF</span></span></td>
<td><span data-ttu-id="b51dd-331">康熙字根裡</span><span class="sxs-lookup"><span data-stu-id="b51dd-331">Kangxi Radicals</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-332">2FF0 - 2FFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-332">2FF0 - 2FFF</span></span></td>
<td><span data-ttu-id="b51dd-333">表意字元描述字元</span><span class="sxs-lookup"><span data-stu-id="b51dd-333">Ideographic Description Characters</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-334">3190 - 319F</span><span class="sxs-lookup"><span data-stu-id="b51dd-334">3190 - 319F</span></span></td>
<td><span data-ttu-id="b51dd-335">漢文</span><span class="sxs-lookup"><span data-stu-id="b51dd-335">Kanbun</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-336">3400 - 4DBF</span><span class="sxs-lookup"><span data-stu-id="b51dd-336">3400 - 4DBF</span></span></td>
<td><span data-ttu-id="b51dd-337">CJK 整合漢字擴充功能 A</span><span class="sxs-lookup"><span data-stu-id="b51dd-337">CJK Unified Ideographs Extension A</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-338">4E00 - 9FFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-338">4E00 - 9FFF</span></span></td>
<td><span data-ttu-id="b51dd-339">CJK 統一的表意文字</span><span class="sxs-lookup"><span data-stu-id="b51dd-339">CJK Unified Ideographs</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-340">20000-2A6DF</span><span class="sxs-lookup"><span data-stu-id="b51dd-340">20000 - 2A6DF</span></span></td>
<td><span data-ttu-id="b51dd-341">CJK 統一的表意文字擴充功能 B</span><span class="sxs-lookup"><span data-stu-id="b51dd-341">CJK Unified Ideographs Extension B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-342">60</span><span class="sxs-lookup"><span data-stu-id="b51dd-342">60</span></span></td>
<td><span data-ttu-id="b51dd-343">E000 - F8FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-343">E000 - F8FF</span></span></td>
<td><span data-ttu-id="b51dd-344">私用區域</span><span class="sxs-lookup"><span data-stu-id="b51dd-344">Private Use Area</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="b51dd-345">61 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-345">61${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-346">31C0 - 31EF</span><span class="sxs-lookup"><span data-stu-id="b51dd-346">31C0 - 31EF</span></span></td>
<td><span data-ttu-id="b51dd-347">CJK 筆觸</span><span class="sxs-lookup"><span data-stu-id="b51dd-347">CJK Strokes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-348">F900 - FAFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-348">F900 - FAFF</span></span></td>
<td><span data-ttu-id="b51dd-349">CJK 相容性表意文字</span><span class="sxs-lookup"><span data-stu-id="b51dd-349">CJK Compatibility Ideographs</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-350">2F800 - 2FA1F</span><span class="sxs-lookup"><span data-stu-id="b51dd-350">2F800 - 2FA1F</span></span></td>
<td><span data-ttu-id="b51dd-351">CJK 相容性表意文字補充</span><span class="sxs-lookup"><span data-stu-id="b51dd-351">CJK Compatibility Ideographs Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-352">62</span><span class="sxs-lookup"><span data-stu-id="b51dd-352">62</span></span></td>
<td><span data-ttu-id="b51dd-353">FB00 - FB4F</span><span class="sxs-lookup"><span data-stu-id="b51dd-353">FB00 - FB4F</span></span></td>
<td><span data-ttu-id="b51dd-354">字母簡報形式</span><span class="sxs-lookup"><span data-stu-id="b51dd-354">Alphabetic Presentation Forms</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-355">63</span><span class="sxs-lookup"><span data-stu-id="b51dd-355">63</span></span></td>
<td><span data-ttu-id="b51dd-356">FB50 - FDFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-356">FB50 - FDFF</span></span></td>
<td><span data-ttu-id="b51dd-357">阿拉伯文簡報表單-A</span><span class="sxs-lookup"><span data-stu-id="b51dd-357">Arabic Presentation Forms-A</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-358">64</span><span class="sxs-lookup"><span data-stu-id="b51dd-358">64</span></span></td>
<td><span data-ttu-id="b51dd-359">FE20 - FE2F</span><span class="sxs-lookup"><span data-stu-id="b51dd-359">FE20 - FE2F</span></span></td>
<td><span data-ttu-id="b51dd-360">組合半標記</span><span class="sxs-lookup"><span data-stu-id="b51dd-360">Combining Half Marks</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="b51dd-361">65 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-361">65${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-362">FE10 - FE1F</span><span class="sxs-lookup"><span data-stu-id="b51dd-362">FE10 - FE1F</span></span></td>
<td><span data-ttu-id="b51dd-363">垂直表單</span><span class="sxs-lookup"><span data-stu-id="b51dd-363">Vertical Forms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-364">FE30 - FE4F</span><span class="sxs-lookup"><span data-stu-id="b51dd-364">FE30 - FE4F</span></span></td>
<td><span data-ttu-id="b51dd-365">CJK 相容性表單</span><span class="sxs-lookup"><span data-stu-id="b51dd-365">CJK Compatibility Forms</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-366">66</span><span class="sxs-lookup"><span data-stu-id="b51dd-366">66</span></span></td>
<td><span data-ttu-id="b51dd-367">FE50 - FE6F</span><span class="sxs-lookup"><span data-stu-id="b51dd-367">FE50 - FE6F</span></span></td>
<td><span data-ttu-id="b51dd-368">小型表單變體</span><span class="sxs-lookup"><span data-stu-id="b51dd-368">Small Form Variants</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-369">67</span><span class="sxs-lookup"><span data-stu-id="b51dd-369">67</span></span></td>
<td><span data-ttu-id="b51dd-370">FE70 - FEFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-370">FE70 - FEFF</span></span></td>
<td><span data-ttu-id="b51dd-371">阿拉伯文簡報表單-B</span><span class="sxs-lookup"><span data-stu-id="b51dd-371">Arabic Presentation Forms-B</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-372">68</span><span class="sxs-lookup"><span data-stu-id="b51dd-372">68</span></span></td>
<td><span data-ttu-id="b51dd-373">FF00 - FFEF</span><span class="sxs-lookup"><span data-stu-id="b51dd-373">FF00 - FFEF</span></span></td>
<td><span data-ttu-id="b51dd-374">半形和全形形式</span><span class="sxs-lookup"><span data-stu-id="b51dd-374">Halfwidth And Fullwidth Forms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-375">69</span><span class="sxs-lookup"><span data-stu-id="b51dd-375">69</span></span></td>
<td><span data-ttu-id="b51dd-376">FFF0 - FFFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-376">FFF0 - FFFF</span></span></td>
<td><span data-ttu-id="b51dd-377">特價</span><span class="sxs-lookup"><span data-stu-id="b51dd-377">Specials</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-378">70</span><span class="sxs-lookup"><span data-stu-id="b51dd-378">70</span></span></td>
<td><span data-ttu-id="b51dd-379">0F00 - 0FFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-379">0F00 - 0FFF</span></span></td>
<td><span data-ttu-id="b51dd-380">西藏文</span><span class="sxs-lookup"><span data-stu-id="b51dd-380">Tibetan</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-381">71</span><span class="sxs-lookup"><span data-stu-id="b51dd-381">71</span></span></td>
<td><span data-ttu-id="b51dd-382">0700 - 074F</span><span class="sxs-lookup"><span data-stu-id="b51dd-382">0700 - 074F</span></span></td>
<td><span data-ttu-id="b51dd-383">敘利亞文</span><span class="sxs-lookup"><span data-stu-id="b51dd-383">Syriac</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-384">72</span><span class="sxs-lookup"><span data-stu-id="b51dd-384">72</span></span></td>
<td><span data-ttu-id="b51dd-385">0780 - 07BF</span><span class="sxs-lookup"><span data-stu-id="b51dd-385">0780 - 07BF</span></span></td>
<td><span data-ttu-id="b51dd-386">塔安那文</span><span class="sxs-lookup"><span data-stu-id="b51dd-386">Thaana</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-387">73</span><span class="sxs-lookup"><span data-stu-id="b51dd-387">73</span></span></td>
<td><span data-ttu-id="b51dd-388">0D80 - 0DFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-388">0D80 - 0DFF</span></span></td>
<td><span data-ttu-id="b51dd-389">僧伽羅文</span><span class="sxs-lookup"><span data-stu-id="b51dd-389">Sinhala</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-390">74</span><span class="sxs-lookup"><span data-stu-id="b51dd-390">74</span></span></td>
<td><span data-ttu-id="b51dd-391">1000 - 109F</span><span class="sxs-lookup"><span data-stu-id="b51dd-391">1000 - 109F</span></span></td>
<td><span data-ttu-id="b51dd-392">緬甸</span><span class="sxs-lookup"><span data-stu-id="b51dd-392">Myanmar</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="b51dd-393">75 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-393">75${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-394">1200 - 137F</span><span class="sxs-lookup"><span data-stu-id="b51dd-394">1200 - 137F</span></span></td>
<td><span data-ttu-id="b51dd-395">文</span><span class="sxs-lookup"><span data-stu-id="b51dd-395">Ethiopic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-396">1380-139F</span><span class="sxs-lookup"><span data-stu-id="b51dd-396">1380 - 139F</span></span></td>
<td><span data-ttu-id="b51dd-397">埃塞俄比亞文補充</span><span class="sxs-lookup"><span data-stu-id="b51dd-397">Ethiopic Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-398">2D80 - 2DDF</span><span class="sxs-lookup"><span data-stu-id="b51dd-398">2D80 - 2DDF</span></span></td>
<td><span data-ttu-id="b51dd-399">埃塞俄比亞文擴充</span><span class="sxs-lookup"><span data-stu-id="b51dd-399">Ethiopic Extended</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-400">76</span><span class="sxs-lookup"><span data-stu-id="b51dd-400">76</span></span></td>
<td><span data-ttu-id="b51dd-401">13A0 - 13FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-401">13A0 - 13FF</span></span></td>
<td><span data-ttu-id="b51dd-402">卻洛奇文</span><span class="sxs-lookup"><span data-stu-id="b51dd-402">Cherokee</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-403">77</span><span class="sxs-lookup"><span data-stu-id="b51dd-403">77</span></span></td>
<td><span data-ttu-id="b51dd-404">1400 - 167F</span><span class="sxs-lookup"><span data-stu-id="b51dd-404">1400 - 167F</span></span></td>
<td><span data-ttu-id="b51dd-405">整合加拿大土著音節</span><span class="sxs-lookup"><span data-stu-id="b51dd-405">Unified Canadian Aboriginal Syllabics</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-406">78</span><span class="sxs-lookup"><span data-stu-id="b51dd-406">78</span></span></td>
<td><span data-ttu-id="b51dd-407">1680 - 169F</span><span class="sxs-lookup"><span data-stu-id="b51dd-407">1680 - 169F</span></span></td>
<td><span data-ttu-id="b51dd-408">豎</span><span class="sxs-lookup"><span data-stu-id="b51dd-408">Ogham</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-409">79</span><span class="sxs-lookup"><span data-stu-id="b51dd-409">79</span></span></td>
<td><span data-ttu-id="b51dd-410">16A0 - 16FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-410">16A0 - 16FF</span></span></td>
<td><span data-ttu-id="b51dd-411">符文</span><span class="sxs-lookup"><span data-stu-id="b51dd-411">Runic</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="b51dd-412">80 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-412">80${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-413">1780 - 17FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-413">1780 - 17FF</span></span></td>
<td><span data-ttu-id="b51dd-414">高棉文</span><span class="sxs-lookup"><span data-stu-id="b51dd-414">Khmer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-415">19E0 - 19FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-415">19E0 - 19FF</span></span></td>
<td><span data-ttu-id="b51dd-416">高棉符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-416">Khmer Symbols</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-417">81</span><span class="sxs-lookup"><span data-stu-id="b51dd-417">81</span></span></td>
<td><span data-ttu-id="b51dd-418">1800 - 18AF</span><span class="sxs-lookup"><span data-stu-id="b51dd-418">1800 - 18AF</span></span></td>
<td><span data-ttu-id="b51dd-419">蒙古文</span><span class="sxs-lookup"><span data-stu-id="b51dd-419">Mongolian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-420">82</span><span class="sxs-lookup"><span data-stu-id="b51dd-420">82</span></span></td>
<td><span data-ttu-id="b51dd-421">2800 - 28FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-421">2800 - 28FF</span></span></td>
<td><span data-ttu-id="b51dd-422">盲文模式</span><span class="sxs-lookup"><span data-stu-id="b51dd-422">Braille Patterns</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="b51dd-423">83 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-423">83${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-424">A000 - A48F</span><span class="sxs-lookup"><span data-stu-id="b51dd-424">A000 - A48F</span></span></td>
<td><span data-ttu-id="b51dd-425">彝語音節</span><span class="sxs-lookup"><span data-stu-id="b51dd-425">Yi Syllables</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-426">A490 - A4CF</span><span class="sxs-lookup"><span data-stu-id="b51dd-426">A490 - A4CF</span></span></td>
<td><span data-ttu-id="b51dd-427">Yi 根式</span><span class="sxs-lookup"><span data-stu-id="b51dd-427">Yi Radicals</span></span></td>

</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="b51dd-428">84 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-428">84${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-429">1700 - 171F</span><span class="sxs-lookup"><span data-stu-id="b51dd-429">1700 - 171F</span></span></td>
<td><span data-ttu-id="b51dd-430">他加祿文</span><span class="sxs-lookup"><span data-stu-id="b51dd-430">Tagalog</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-431">1720 - 173F</span><span class="sxs-lookup"><span data-stu-id="b51dd-431">1720 - 173F</span></span></td>
<td><span data-ttu-id="b51dd-432">族</span><span class="sxs-lookup"><span data-stu-id="b51dd-432">Hanunoo</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-433">1740 - 175F</span><span class="sxs-lookup"><span data-stu-id="b51dd-433">1740 - 175F</span></span></td>
<td><span data-ttu-id="b51dd-434">布錫文</span><span class="sxs-lookup"><span data-stu-id="b51dd-434">Buhid</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-435">1760 - 177F</span><span class="sxs-lookup"><span data-stu-id="b51dd-435">1760 - 177F</span></span></td>
<td><span data-ttu-id="b51dd-436">塔班瓦文</span><span class="sxs-lookup"><span data-stu-id="b51dd-436">Tagbanwa</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-437">85</span><span class="sxs-lookup"><span data-stu-id="b51dd-437">85</span></span></td>
<td><span data-ttu-id="b51dd-438">10300-1032F</span><span class="sxs-lookup"><span data-stu-id="b51dd-438">10300 - 1032F</span></span></td>
<td><span data-ttu-id="b51dd-439">舊的斜體</span><span class="sxs-lookup"><span data-stu-id="b51dd-439">Old Italic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-440">86</span><span class="sxs-lookup"><span data-stu-id="b51dd-440">86</span></span></td>
<td><span data-ttu-id="b51dd-441">10330-1034F</span><span class="sxs-lookup"><span data-stu-id="b51dd-441">10330 - 1034F</span></span></td>
<td><span data-ttu-id="b51dd-442">哥 特 式</span><span class="sxs-lookup"><span data-stu-id="b51dd-442">Gothic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-443">87</span><span class="sxs-lookup"><span data-stu-id="b51dd-443">87</span></span></td>
<td><span data-ttu-id="b51dd-444">10400-1044F</span><span class="sxs-lookup"><span data-stu-id="b51dd-444">10400 - 1044F</span></span></td>
<td><span data-ttu-id="b51dd-445">萊特</span><span class="sxs-lookup"><span data-stu-id="b51dd-445">Deseret</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="b51dd-446">88 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-446">88${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-447">1D000 - 1D0FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-447">1D000 - 1D0FF</span></span></td>
<td><span data-ttu-id="b51dd-448">拜占庭音樂符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-448">Byzantine Musical Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-449">1D100 - 1D1FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-449">1D100 - 1D1FF</span></span></td>
<td><span data-ttu-id="b51dd-450">音樂符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-450">Musical Symbols</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-451">1D200 - 1D24F</span><span class="sxs-lookup"><span data-stu-id="b51dd-451">1D200 - 1D24F</span></span></td>
<td><span data-ttu-id="b51dd-452">古希臘文音樂標記法</span><span class="sxs-lookup"><span data-stu-id="b51dd-452">Ancient Greek Musical Notation</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-453">89</span><span class="sxs-lookup"><span data-stu-id="b51dd-453">89</span></span></td>
<td><span data-ttu-id="b51dd-454">1D400 - 1D7FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-454">1D400 - 1D7FF</span></span></td>
<td><span data-ttu-id="b51dd-455">數學英數位元符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-455">Mathematical Alphanumeric Symbols</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="b51dd-456">90 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-456">90${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-457">FF000 - FFFFD</span><span class="sxs-lookup"><span data-stu-id="b51dd-457">FF000 - FFFFD</span></span></td>
<td><span data-ttu-id="b51dd-458">私用 (平面 15) </span><span class="sxs-lookup"><span data-stu-id="b51dd-458">Private Use (plane 15)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-459">100000-10FFFD</span><span class="sxs-lookup"><span data-stu-id="b51dd-459">100000 - 10FFFD</span></span></td>
<td><span data-ttu-id="b51dd-460">私用 (平面 16) </span><span class="sxs-lookup"><span data-stu-id="b51dd-460">Private Use (plane 16)</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="b51dd-461">91 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-461">91${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-462">FE00 - FE0F</span><span class="sxs-lookup"><span data-stu-id="b51dd-462">FE00 - FE0F</span></span></td>
<td><span data-ttu-id="b51dd-463">變化選取器</span><span class="sxs-lookup"><span data-stu-id="b51dd-463">Variation Selectors</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-464">E0100 - E01EF</span><span class="sxs-lookup"><span data-stu-id="b51dd-464">E0100 - E01EF</span></span></td>
<td><span data-ttu-id="b51dd-465">變化選取器補充</span><span class="sxs-lookup"><span data-stu-id="b51dd-465">Variation Selectors Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-466">92</span><span class="sxs-lookup"><span data-stu-id="b51dd-466">92</span></span></td>
<td><span data-ttu-id="b51dd-467">E0000 - E007F</span><span class="sxs-lookup"><span data-stu-id="b51dd-467">E0000 - E007F</span></span></td>
<td><span data-ttu-id="b51dd-468">標籤</span><span class="sxs-lookup"><span data-stu-id="b51dd-468">Tags</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-469">93</span><span class="sxs-lookup"><span data-stu-id="b51dd-469">93</span></span></td>
<td><span data-ttu-id="b51dd-470">1900 - 194F</span><span class="sxs-lookup"><span data-stu-id="b51dd-470">1900 - 194F</span></span></td>
<td><span data-ttu-id="b51dd-471">林布文</span><span class="sxs-lookup"><span data-stu-id="b51dd-471">Limbu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-472">94</span><span class="sxs-lookup"><span data-stu-id="b51dd-472">94</span></span></td>
<td><span data-ttu-id="b51dd-473">1950 - 197F</span><span class="sxs-lookup"><span data-stu-id="b51dd-473">1950 - 197F</span></span></td>
<td><span data-ttu-id="b51dd-474">泰 Le</span><span class="sxs-lookup"><span data-stu-id="b51dd-474">Tai Le</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-475">95</span><span class="sxs-lookup"><span data-stu-id="b51dd-475">95</span></span></td>
<td><span data-ttu-id="b51dd-476">1980-19DF</span><span class="sxs-lookup"><span data-stu-id="b51dd-476">1980 - 19DF</span></span></td>
<td><span data-ttu-id="b51dd-477">新傣文</span><span class="sxs-lookup"><span data-stu-id="b51dd-477">New Tai Lue</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-478">96</span><span class="sxs-lookup"><span data-stu-id="b51dd-478">96</span></span></td>
<td><span data-ttu-id="b51dd-479">1A00 - 1A1F</span><span class="sxs-lookup"><span data-stu-id="b51dd-479">1A00 - 1A1F</span></span></td>
<td><span data-ttu-id="b51dd-480">布吉斯文</span><span class="sxs-lookup"><span data-stu-id="b51dd-480">Buginese</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-481">97</span><span class="sxs-lookup"><span data-stu-id="b51dd-481">97</span></span></td>
<td><span data-ttu-id="b51dd-482">2C00 - 2C5F</span><span class="sxs-lookup"><span data-stu-id="b51dd-482">2C00 - 2C5F</span></span></td>
<td><span data-ttu-id="b51dd-483">文</span><span class="sxs-lookup"><span data-stu-id="b51dd-483">Glagolitic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-484">98</span><span class="sxs-lookup"><span data-stu-id="b51dd-484">98</span></span></td>
<td><span data-ttu-id="b51dd-485">2D30 - 2D7F</span><span class="sxs-lookup"><span data-stu-id="b51dd-485">2D30 - 2D7F</span></span></td>
<td><span data-ttu-id="b51dd-486">納</span><span class="sxs-lookup"><span data-stu-id="b51dd-486">Tifinagh</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-487">99</span><span class="sxs-lookup"><span data-stu-id="b51dd-487">99</span></span></td>
<td><span data-ttu-id="b51dd-488">4DC0 - 4DFF</span><span class="sxs-lookup"><span data-stu-id="b51dd-488">4DC0 - 4DFF</span></span></td>
<td><span data-ttu-id="b51dd-489">易經帶字元符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-489">Yijing Hexagram Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-490">100</span><span class="sxs-lookup"><span data-stu-id="b51dd-490">100</span></span></td>
<td><span data-ttu-id="b51dd-491">A800 - A82F</span><span class="sxs-lookup"><span data-stu-id="b51dd-491">A800 - A82F</span></span></td>
<td><span data-ttu-id="b51dd-492">的</span><span class="sxs-lookup"><span data-stu-id="b51dd-492">Syloti Nagri</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="b51dd-493">101 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-493">101${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-494">10000-1007F</span><span class="sxs-lookup"><span data-stu-id="b51dd-494">10000 - 1007F</span></span></td>
<td><span data-ttu-id="b51dd-495">線性 B 音節</span><span class="sxs-lookup"><span data-stu-id="b51dd-495">Linear B Syllabary</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-496">10080-100FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-496">10080 - 100FF</span></span></td>
<td><span data-ttu-id="b51dd-497">線性 B 表意文字</span><span class="sxs-lookup"><span data-stu-id="b51dd-497">Linear B Ideograms</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-498">10100-1013F</span><span class="sxs-lookup"><span data-stu-id="b51dd-498">10100 - 1013F</span></span></td>
<td><span data-ttu-id="b51dd-499">希臘愛琴大學號碼</span><span class="sxs-lookup"><span data-stu-id="b51dd-499">Aegean Numbers</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-500">102</span><span class="sxs-lookup"><span data-stu-id="b51dd-500">102</span></span></td>
<td><span data-ttu-id="b51dd-501">10140-1018F</span><span class="sxs-lookup"><span data-stu-id="b51dd-501">10140 - 1018F</span></span></td>
<td><span data-ttu-id="b51dd-502">古希臘文數位</span><span class="sxs-lookup"><span data-stu-id="b51dd-502">Ancient Greek Numbers</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-503">103</span><span class="sxs-lookup"><span data-stu-id="b51dd-503">103</span></span></td>
<td><span data-ttu-id="b51dd-504">10380-1039F</span><span class="sxs-lookup"><span data-stu-id="b51dd-504">10380 - 1039F</span></span></td>
<td><span data-ttu-id="b51dd-505">烏加里特文</span><span class="sxs-lookup"><span data-stu-id="b51dd-505">Ugaritic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-506">104</span><span class="sxs-lookup"><span data-stu-id="b51dd-506">104</span></span></td>
<td><span data-ttu-id="b51dd-507">103A0 - 103DF</span><span class="sxs-lookup"><span data-stu-id="b51dd-507">103A0 - 103DF</span></span></td>
<td><span data-ttu-id="b51dd-508">舊的波斯</span><span class="sxs-lookup"><span data-stu-id="b51dd-508">Old Persian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-509">105</span><span class="sxs-lookup"><span data-stu-id="b51dd-509">105</span></span></td>
<td><span data-ttu-id="b51dd-510">10450-1047F</span><span class="sxs-lookup"><span data-stu-id="b51dd-510">10450 - 1047F</span></span></td>
<td><span data-ttu-id="b51dd-511">Shavian</span><span class="sxs-lookup"><span data-stu-id="b51dd-511">Shavian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-512">106</span><span class="sxs-lookup"><span data-stu-id="b51dd-512">106</span></span></td>
<td><span data-ttu-id="b51dd-513">10480-104AF</span><span class="sxs-lookup"><span data-stu-id="b51dd-513">10480 - 104AF</span></span></td>
<td><span data-ttu-id="b51dd-514">文</span><span class="sxs-lookup"><span data-stu-id="b51dd-514">Osmanya</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-515">107</span><span class="sxs-lookup"><span data-stu-id="b51dd-515">107</span></span></td>
<td><span data-ttu-id="b51dd-516">10800-1083F</span><span class="sxs-lookup"><span data-stu-id="b51dd-516">10800 - 1083F</span></span></td>
<td><span data-ttu-id="b51dd-517">Cypriot 音節</span><span class="sxs-lookup"><span data-stu-id="b51dd-517">Cypriot Syllabary</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-518">108</span><span class="sxs-lookup"><span data-stu-id="b51dd-518">108</span></span></td>
<td><span data-ttu-id="b51dd-519">10A00 - 10A5F</span><span class="sxs-lookup"><span data-stu-id="b51dd-519">10A00 - 10A5F</span></span></td>
<td><span data-ttu-id="b51dd-520">須</span><span class="sxs-lookup"><span data-stu-id="b51dd-520">Kharoshthi</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-521">109</span><span class="sxs-lookup"><span data-stu-id="b51dd-521">109</span></span></td>
<td><span data-ttu-id="b51dd-522">1D300 - 1D35F</span><span class="sxs-lookup"><span data-stu-id="b51dd-522">1D300 - 1D35F</span></span></td>
<td><span data-ttu-id="b51dd-523">泰 Xuan Jing 符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-523">Tai Xuan Jing Symbols</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="b51dd-524">110 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-524">110${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-525">12000-123FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-525">12000 - 123FF</span></span></td>
<td><span data-ttu-id="b51dd-526">楔 形</span><span class="sxs-lookup"><span data-stu-id="b51dd-526">Cuneiform</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-527">12400-1247F</span><span class="sxs-lookup"><span data-stu-id="b51dd-527">12400 - 1247F</span></span></td>
<td><span data-ttu-id="b51dd-528">Cuneiform 數位和標點符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-528">Cuneiform Numbers and Punctuation</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-529">111</span><span class="sxs-lookup"><span data-stu-id="b51dd-529">111</span></span></td>
<td><span data-ttu-id="b51dd-530">1D360 - 1D37F</span><span class="sxs-lookup"><span data-stu-id="b51dd-530">1D360 - 1D37F</span></span></td>
<td><span data-ttu-id="b51dd-531">計算杆數位</span><span class="sxs-lookup"><span data-stu-id="b51dd-531">Counting Rod Numerals</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-532">112</span><span class="sxs-lookup"><span data-stu-id="b51dd-532">112</span></span></td>
<td><span data-ttu-id="b51dd-533">1B80 - 1BBF</span><span class="sxs-lookup"><span data-stu-id="b51dd-533">1B80 - 1BBF</span></span></td>
<td><span data-ttu-id="b51dd-534">巽丹文</span><span class="sxs-lookup"><span data-stu-id="b51dd-534">Sundanese</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-535">113</span><span class="sxs-lookup"><span data-stu-id="b51dd-535">113</span></span></td>
<td><span data-ttu-id="b51dd-536">1C00 - 1C4F</span><span class="sxs-lookup"><span data-stu-id="b51dd-536">1C00 - 1C4F</span></span></td>
<td><span data-ttu-id="b51dd-537">雷布查文</span><span class="sxs-lookup"><span data-stu-id="b51dd-537">Lepcha</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-538">114</span><span class="sxs-lookup"><span data-stu-id="b51dd-538">114</span></span></td>
<td><span data-ttu-id="b51dd-539">1C50 - 1C7F</span><span class="sxs-lookup"><span data-stu-id="b51dd-539">1C50 - 1C7F</span></span></td>
<td><span data-ttu-id="b51dd-540">桑塔爾文</span><span class="sxs-lookup"><span data-stu-id="b51dd-540">Ol Chiki</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-541">115</span><span class="sxs-lookup"><span data-stu-id="b51dd-541">115</span></span></td>
<td><span data-ttu-id="b51dd-542">A880 - A8DF</span><span class="sxs-lookup"><span data-stu-id="b51dd-542">A880 - A8DF</span></span></td>
<td><span data-ttu-id="b51dd-543">紹拉斯徹文</span><span class="sxs-lookup"><span data-stu-id="b51dd-543">Saurashtra</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-544">116</span><span class="sxs-lookup"><span data-stu-id="b51dd-544">116</span></span></td>
<td><span data-ttu-id="b51dd-545">A900 - A92F</span><span class="sxs-lookup"><span data-stu-id="b51dd-545">A900 - A92F</span></span></td>
<td><span data-ttu-id="b51dd-546">開亞里文</span><span class="sxs-lookup"><span data-stu-id="b51dd-546">Kayah Li</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-547">117</span><span class="sxs-lookup"><span data-stu-id="b51dd-547">117</span></span></td>
<td><span data-ttu-id="b51dd-548">A930 - A95F</span><span class="sxs-lookup"><span data-stu-id="b51dd-548">A930 - A95F</span></span></td>
<td><span data-ttu-id="b51dd-549">拉讓文</span><span class="sxs-lookup"><span data-stu-id="b51dd-549">Rejang</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-550">118</span><span class="sxs-lookup"><span data-stu-id="b51dd-550">118</span></span></td>
<td><span data-ttu-id="b51dd-551">AA00 - AA5F</span><span class="sxs-lookup"><span data-stu-id="b51dd-551">AA00 - AA5F</span></span></td>
<td><span data-ttu-id="b51dd-552">Cham</span><span class="sxs-lookup"><span data-stu-id="b51dd-552">Cham</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-553">119</span><span class="sxs-lookup"><span data-stu-id="b51dd-553">119</span></span></td>
<td><span data-ttu-id="b51dd-554">10190-101CF</span><span class="sxs-lookup"><span data-stu-id="b51dd-554">10190 - 101CF</span></span></td>
<td><span data-ttu-id="b51dd-555">古符號</span><span class="sxs-lookup"><span data-stu-id="b51dd-555">Ancient Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-556">120</span><span class="sxs-lookup"><span data-stu-id="b51dd-556">120</span></span></td>
<td><span data-ttu-id="b51dd-557">101D0 - 101FF</span><span class="sxs-lookup"><span data-stu-id="b51dd-557">101D0 - 101FF</span></span></td>
<td><span data-ttu-id="b51dd-558">Phaistos 光碟</span><span class="sxs-lookup"><span data-stu-id="b51dd-558">Phaistos Disc</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="b51dd-559">121 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-559">121${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-560">10280-1029F</span><span class="sxs-lookup"><span data-stu-id="b51dd-560">10280 - 1029F</span></span></td>
<td><span data-ttu-id="b51dd-561">呂西亞文</span><span class="sxs-lookup"><span data-stu-id="b51dd-561">Lycian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-562">102A0 - 102DF</span><span class="sxs-lookup"><span data-stu-id="b51dd-562">102A0 - 102DF</span></span></td>
<td><span data-ttu-id="b51dd-563">卡里亞文</span><span class="sxs-lookup"><span data-stu-id="b51dd-563">Carian</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-564">10920-1093F</span><span class="sxs-lookup"><span data-stu-id="b51dd-564">10920 - 1093F</span></span></td>
<td><span data-ttu-id="b51dd-565">利底亞文</span><span class="sxs-lookup"><span data-stu-id="b51dd-565">Lydian</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="b51dd-566">122 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b51dd-566">122${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b51dd-567">1F000 - 1F02F</span><span class="sxs-lookup"><span data-stu-id="b51dd-567">1F000 - 1F02F</span></span></td>
<td><span data-ttu-id="b51dd-568">麻將底圖</span><span class="sxs-lookup"><span data-stu-id="b51dd-568">Mahjong Tiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-569">1F030 - 1F09F</span><span class="sxs-lookup"><span data-stu-id="b51dd-569">1F030 - 1F09F</span></span></td>
<td><span data-ttu-id="b51dd-570">Domino 磚</span><span class="sxs-lookup"><span data-stu-id="b51dd-570">Domino Tiles</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-571">123</span><span class="sxs-lookup"><span data-stu-id="b51dd-571">123</span></span></td>

<td><span data-ttu-id="b51dd-572"><strong>Windows 2000 和更新版本：</strong> 版面配置進度，從右至左水準</span><span class="sxs-lookup"><span data-stu-id="b51dd-572"><strong>Windows 2000 and later:</strong> Layout progress, horizontal from right to left</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-573">124</span><span class="sxs-lookup"><span data-stu-id="b51dd-573">124</span></span></td>

<td><span data-ttu-id="b51dd-574"><strong>Windows 2000 和更新版本：</strong> 版面配置進度、水準垂直</span><span class="sxs-lookup"><span data-stu-id="b51dd-574"><strong>Windows 2000 and later:</strong> Layout progress, vertical before horizontal</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b51dd-575">125</span><span class="sxs-lookup"><span data-stu-id="b51dd-575">125</span></span></td>

<td><span data-ttu-id="b51dd-576"><strong>Windows 2000 和更新版本：</strong> 版面配置進度，垂直靠上</span><span class="sxs-lookup"><span data-stu-id="b51dd-576"><strong>Windows 2000 and later:</strong> Layout progress, vertical bottom to top</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b51dd-577">126-127</span><span class="sxs-lookup"><span data-stu-id="b51dd-577">126-127</span></span></td>

<td><span data-ttu-id="b51dd-578">保留給進程-內部使用</span><span class="sxs-lookup"><span data-stu-id="b51dd-578">Reserved for process-internal usage</span></span></td>
</tr>
</tbody>
</table>



 

 

 



