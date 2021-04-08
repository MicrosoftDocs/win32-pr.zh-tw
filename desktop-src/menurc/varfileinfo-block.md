---
title: VarFileInfo BLOCK 語句
description: 描述變數資訊區塊的格式。
ms.assetid: 81c7f5df-78fa-4571-9dad-a6c3e932471e
keywords:
- VarFileInfo 區塊語句功能表和其他資源
topic_type:
- apiref
api_name:
- VarFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09645801618de130439bdf1998b92183e4791783
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022622"
---
# <a name="varfileinfo-block-statement"></a><span data-ttu-id="2bd09-104">VarFileInfo BLOCK 語句</span><span class="sxs-lookup"><span data-stu-id="2bd09-104">VarFileInfo BLOCK statement</span></span>

<span data-ttu-id="2bd09-105">定義變數資訊區塊。</span><span class="sxs-lookup"><span data-stu-id="2bd09-105">Defines a variable information block.</span></span>

``` syntax
BLOCK "VarFileInfo" { VALUE "Translation", langID, charsetID . . . }
```

## <a name="parameters"></a><span data-ttu-id="2bd09-106">參數</span><span class="sxs-lookup"><span data-stu-id="2bd09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bd09-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="2bd09-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="2bd09-108">[備註] 區段中指定的其中一個語言識別項。</span><span class="sxs-lookup"><span data-stu-id="2bd09-108">One of the language identifiers specified in the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="2bd09-109"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span><span class="sxs-lookup"><span data-stu-id="2bd09-109"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span></span>
</dt> <dd>

<span data-ttu-id="2bd09-110">在 [備註] 區段中指定的其中一個字元組識別碼。</span><span class="sxs-lookup"><span data-stu-id="2bd09-110">One of the character-set identifiers specified in the Remarks section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2bd09-111">備註</span><span class="sxs-lookup"><span data-stu-id="2bd09-111">Remarks</span></span>

<span data-ttu-id="2bd09-112">您可以指定一個以上的識別碼組，但每一組都必須以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="2bd09-112">More than one identifier pair can be given, but each pair must be separated from the preceding pair with a comma.</span></span>

<span data-ttu-id="2bd09-113">*LangID* 參數會指定下列其中一種語言代碼。</span><span class="sxs-lookup"><span data-stu-id="2bd09-113">The *langID* parameter specifies one of the following language codes.</span></span>



| <span data-ttu-id="2bd09-114">程式碼</span><span class="sxs-lookup"><span data-stu-id="2bd09-114">Code</span></span>   | <span data-ttu-id="2bd09-115">語言</span><span class="sxs-lookup"><span data-stu-id="2bd09-115">Language</span></span>            | <span data-ttu-id="2bd09-116">程式碼</span><span class="sxs-lookup"><span data-stu-id="2bd09-116">Code</span></span>   | <span data-ttu-id="2bd09-117">語言</span><span class="sxs-lookup"><span data-stu-id="2bd09-117">Language</span></span>                  |
|--------|---------------------|--------|---------------------------|
| <span data-ttu-id="2bd09-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="2bd09-118">0x0401</span></span> | <span data-ttu-id="2bd09-119">阿拉伯文</span><span class="sxs-lookup"><span data-stu-id="2bd09-119">Arabic</span></span>              | <span data-ttu-id="2bd09-120">0x0415</span><span class="sxs-lookup"><span data-stu-id="2bd09-120">0x0415</span></span> | <span data-ttu-id="2bd09-121">波蘭文</span><span class="sxs-lookup"><span data-stu-id="2bd09-121">Polish</span></span>                    |
| <span data-ttu-id="2bd09-122">0x0402</span><span class="sxs-lookup"><span data-stu-id="2bd09-122">0x0402</span></span> | <span data-ttu-id="2bd09-123">保加利亞文</span><span class="sxs-lookup"><span data-stu-id="2bd09-123">Bulgarian</span></span>           | <span data-ttu-id="2bd09-124">0x0416</span><span class="sxs-lookup"><span data-stu-id="2bd09-124">0x0416</span></span> | <span data-ttu-id="2bd09-125">葡萄牙文 (巴西)</span><span class="sxs-lookup"><span data-stu-id="2bd09-125">Portuguese (Brazil)</span></span>       |
| <span data-ttu-id="2bd09-126">0x0403</span><span class="sxs-lookup"><span data-stu-id="2bd09-126">0x0403</span></span> | <span data-ttu-id="2bd09-127">卡達隆尼亞文</span><span class="sxs-lookup"><span data-stu-id="2bd09-127">Catalan</span></span>             | <span data-ttu-id="2bd09-128">0x0417</span><span class="sxs-lookup"><span data-stu-id="2bd09-128">0x0417</span></span> | <span data-ttu-id="2bd09-129">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="2bd09-129">Rhaeto-Romanic</span></span>            |
| <span data-ttu-id="2bd09-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="2bd09-130">0x0404</span></span> | <span data-ttu-id="2bd09-131">繁體中文</span><span class="sxs-lookup"><span data-stu-id="2bd09-131">Traditional Chinese</span></span> | <span data-ttu-id="2bd09-132">0x0418</span><span class="sxs-lookup"><span data-stu-id="2bd09-132">0x0418</span></span> | <span data-ttu-id="2bd09-133">羅馬尼亞文</span><span class="sxs-lookup"><span data-stu-id="2bd09-133">Romanian</span></span>                  |
| <span data-ttu-id="2bd09-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="2bd09-134">0x0405</span></span> | <span data-ttu-id="2bd09-135">捷克文</span><span class="sxs-lookup"><span data-stu-id="2bd09-135">Czech</span></span>               | <span data-ttu-id="2bd09-136">0x0419</span><span class="sxs-lookup"><span data-stu-id="2bd09-136">0x0419</span></span> | <span data-ttu-id="2bd09-137">俄文</span><span class="sxs-lookup"><span data-stu-id="2bd09-137">Russian</span></span>                   |
| <span data-ttu-id="2bd09-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="2bd09-138">0x0406</span></span> | <span data-ttu-id="2bd09-139">丹麥文</span><span class="sxs-lookup"><span data-stu-id="2bd09-139">Danish</span></span>              | <span data-ttu-id="2bd09-140">0x041A</span><span class="sxs-lookup"><span data-stu-id="2bd09-140">0x041A</span></span> | <span data-ttu-id="2bd09-141">Croato-Serbian (拉丁) </span><span class="sxs-lookup"><span data-stu-id="2bd09-141">Croato-Serbian (Latin)</span></span>    |
| <span data-ttu-id="2bd09-142">0x0407</span><span class="sxs-lookup"><span data-stu-id="2bd09-142">0x0407</span></span> | <span data-ttu-id="2bd09-143">德文</span><span class="sxs-lookup"><span data-stu-id="2bd09-143">German</span></span>              | <span data-ttu-id="2bd09-144">0x041B</span><span class="sxs-lookup"><span data-stu-id="2bd09-144">0x041B</span></span> | <span data-ttu-id="2bd09-145">斯洛伐克文</span><span class="sxs-lookup"><span data-stu-id="2bd09-145">Slovak</span></span>                    |
| <span data-ttu-id="2bd09-146">0x0408</span><span class="sxs-lookup"><span data-stu-id="2bd09-146">0x0408</span></span> | <span data-ttu-id="2bd09-147">希臘文</span><span class="sxs-lookup"><span data-stu-id="2bd09-147">Greek</span></span>               | <span data-ttu-id="2bd09-148">0x041C</span><span class="sxs-lookup"><span data-stu-id="2bd09-148">0x041C</span></span> | <span data-ttu-id="2bd09-149">阿爾巴尼亞文</span><span class="sxs-lookup"><span data-stu-id="2bd09-149">Albanian</span></span>                  |
| <span data-ttu-id="2bd09-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="2bd09-150">0x0409</span></span> | <span data-ttu-id="2bd09-151">美式英文</span><span class="sxs-lookup"><span data-stu-id="2bd09-151">U.S. English</span></span>        | <span data-ttu-id="2bd09-152">0x041D</span><span class="sxs-lookup"><span data-stu-id="2bd09-152">0x041D</span></span> | <span data-ttu-id="2bd09-153">瑞典文</span><span class="sxs-lookup"><span data-stu-id="2bd09-153">Swedish</span></span>                   |
| <span data-ttu-id="2bd09-154">0x040A</span><span class="sxs-lookup"><span data-stu-id="2bd09-154">0x040A</span></span> | <span data-ttu-id="2bd09-155">標準西班牙文</span><span class="sxs-lookup"><span data-stu-id="2bd09-155">Castilian Spanish</span></span>   | <span data-ttu-id="2bd09-156">0x041E</span><span class="sxs-lookup"><span data-stu-id="2bd09-156">0x041E</span></span> | <span data-ttu-id="2bd09-157">泰文</span><span class="sxs-lookup"><span data-stu-id="2bd09-157">Thai</span></span>                      |
| <span data-ttu-id="2bd09-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="2bd09-158">0x040B</span></span> | <span data-ttu-id="2bd09-159">芬蘭文</span><span class="sxs-lookup"><span data-stu-id="2bd09-159">Finnish</span></span>             | <span data-ttu-id="2bd09-160">0x041F</span><span class="sxs-lookup"><span data-stu-id="2bd09-160">0x041F</span></span> | <span data-ttu-id="2bd09-161">土耳其文</span><span class="sxs-lookup"><span data-stu-id="2bd09-161">Turkish</span></span>                   |
| <span data-ttu-id="2bd09-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="2bd09-162">0x040C</span></span> | <span data-ttu-id="2bd09-163">法文</span><span class="sxs-lookup"><span data-stu-id="2bd09-163">French</span></span>              | <span data-ttu-id="2bd09-164">0x0420</span><span class="sxs-lookup"><span data-stu-id="2bd09-164">0x0420</span></span> | <span data-ttu-id="2bd09-165">烏都文</span><span class="sxs-lookup"><span data-stu-id="2bd09-165">Urdu</span></span>                      |
| <span data-ttu-id="2bd09-166">0x040D</span><span class="sxs-lookup"><span data-stu-id="2bd09-166">0x040D</span></span> | <span data-ttu-id="2bd09-167">Hebrew</span><span class="sxs-lookup"><span data-stu-id="2bd09-167">Hebrew</span></span>              | <span data-ttu-id="2bd09-168">0x0421</span><span class="sxs-lookup"><span data-stu-id="2bd09-168">0x0421</span></span> | <span data-ttu-id="2bd09-169">Bahasa</span><span class="sxs-lookup"><span data-stu-id="2bd09-169">Bahasa</span></span>                    |
| <span data-ttu-id="2bd09-170">0x040E</span><span class="sxs-lookup"><span data-stu-id="2bd09-170">0x040E</span></span> | <span data-ttu-id="2bd09-171">匈牙利文</span><span class="sxs-lookup"><span data-stu-id="2bd09-171">Hungarian</span></span>           | <span data-ttu-id="2bd09-172">0x0804</span><span class="sxs-lookup"><span data-stu-id="2bd09-172">0x0804</span></span> | <span data-ttu-id="2bd09-173">簡體中文</span><span class="sxs-lookup"><span data-stu-id="2bd09-173">Simplified Chinese</span></span>        |
| <span data-ttu-id="2bd09-174">0x040F</span><span class="sxs-lookup"><span data-stu-id="2bd09-174">0x040F</span></span> | <span data-ttu-id="2bd09-175">冰島文</span><span class="sxs-lookup"><span data-stu-id="2bd09-175">Icelandic</span></span>           | <span data-ttu-id="2bd09-176">0x0807</span><span class="sxs-lookup"><span data-stu-id="2bd09-176">0x0807</span></span> | <span data-ttu-id="2bd09-177">瑞士德文</span><span class="sxs-lookup"><span data-stu-id="2bd09-177">Swiss German</span></span>              |
| <span data-ttu-id="2bd09-178">0x0410</span><span class="sxs-lookup"><span data-stu-id="2bd09-178">0x0410</span></span> | <span data-ttu-id="2bd09-179">義大利文</span><span class="sxs-lookup"><span data-stu-id="2bd09-179">Italian</span></span>             | <span data-ttu-id="2bd09-180">0x0809</span><span class="sxs-lookup"><span data-stu-id="2bd09-180">0x0809</span></span> | <span data-ttu-id="2bd09-181">英國。</span><span class="sxs-lookup"><span data-stu-id="2bd09-181">U.K.</span></span> <span data-ttu-id="2bd09-182">英文</span><span class="sxs-lookup"><span data-stu-id="2bd09-182">English</span></span>              |
| <span data-ttu-id="2bd09-183">0x0411</span><span class="sxs-lookup"><span data-stu-id="2bd09-183">0x0411</span></span> | <span data-ttu-id="2bd09-184">日文</span><span class="sxs-lookup"><span data-stu-id="2bd09-184">Japanese</span></span>            | <span data-ttu-id="2bd09-185">0x080A</span><span class="sxs-lookup"><span data-stu-id="2bd09-185">0x080A</span></span> | <span data-ttu-id="2bd09-186">西班牙文 (墨西哥)</span><span class="sxs-lookup"><span data-stu-id="2bd09-186">Spanish (Mexico)</span></span>          |
| <span data-ttu-id="2bd09-187">0x0412</span><span class="sxs-lookup"><span data-stu-id="2bd09-187">0x0412</span></span> | <span data-ttu-id="2bd09-188">韓文</span><span class="sxs-lookup"><span data-stu-id="2bd09-188">Korean</span></span>              | <span data-ttu-id="2bd09-189">0x080C</span><span class="sxs-lookup"><span data-stu-id="2bd09-189">0x080C</span></span> | <span data-ttu-id="2bd09-190">比利時法文</span><span class="sxs-lookup"><span data-stu-id="2bd09-190">Belgian French</span></span>            |
| <span data-ttu-id="2bd09-191">0x0413</span><span class="sxs-lookup"><span data-stu-id="2bd09-191">0x0413</span></span> | <span data-ttu-id="2bd09-192">荷蘭文</span><span class="sxs-lookup"><span data-stu-id="2bd09-192">Dutch</span></span>               | <span data-ttu-id="2bd09-193">0x0C0C</span><span class="sxs-lookup"><span data-stu-id="2bd09-193">0x0C0C</span></span> | <span data-ttu-id="2bd09-194">法文 (加拿大)</span><span class="sxs-lookup"><span data-stu-id="2bd09-194">Canadian French</span></span>           |
| <span data-ttu-id="2bd09-195">0x0414</span><span class="sxs-lookup"><span data-stu-id="2bd09-195">0x0414</span></span> | <span data-ttu-id="2bd09-196">挪威文–博克瑪律</span><span class="sxs-lookup"><span data-stu-id="2bd09-196">Norwegian – Bokmal</span></span>  | <span data-ttu-id="2bd09-197">0x100C</span><span class="sxs-lookup"><span data-stu-id="2bd09-197">0x100C</span></span> | <span data-ttu-id="2bd09-198">瑞士法文</span><span class="sxs-lookup"><span data-stu-id="2bd09-198">Swiss French</span></span>              |
| <span data-ttu-id="2bd09-199">0x0810</span><span class="sxs-lookup"><span data-stu-id="2bd09-199">0x0810</span></span> | <span data-ttu-id="2bd09-200">瑞士義大利文</span><span class="sxs-lookup"><span data-stu-id="2bd09-200">Swiss Italian</span></span>       | <span data-ttu-id="2bd09-201">0x0816</span><span class="sxs-lookup"><span data-stu-id="2bd09-201">0x0816</span></span> | <span data-ttu-id="2bd09-202">葡萄牙文 (葡萄牙)</span><span class="sxs-lookup"><span data-stu-id="2bd09-202">Portuguese (Portugal)</span></span>     |
| <span data-ttu-id="2bd09-203">0x0813</span><span class="sxs-lookup"><span data-stu-id="2bd09-203">0x0813</span></span> | <span data-ttu-id="2bd09-204">比利時荷蘭文</span><span class="sxs-lookup"><span data-stu-id="2bd09-204">Belgian Dutch</span></span>       | <span data-ttu-id="2bd09-205">0x081A</span><span class="sxs-lookup"><span data-stu-id="2bd09-205">0x081A</span></span> | <span data-ttu-id="2bd09-206">Serbo-Croatian (斯拉夫) </span><span class="sxs-lookup"><span data-stu-id="2bd09-206">Serbo-Croatian (Cyrillic)</span></span> |
| <span data-ttu-id="2bd09-207">0x0814</span><span class="sxs-lookup"><span data-stu-id="2bd09-207">0x0814</span></span> | <span data-ttu-id="2bd09-208">挪威文–挪威文</span><span class="sxs-lookup"><span data-stu-id="2bd09-208">Norwegian – Nynorsk</span></span> | <span data-ttu-id="2bd09-209">?</span><span class="sxs-lookup"><span data-stu-id="2bd09-209">?</span></span>      | <span data-ttu-id="2bd09-210">?</span><span class="sxs-lookup"><span data-stu-id="2bd09-210">?</span></span>                         |



 

<span data-ttu-id="2bd09-211">*CharsetID* 參數會指定下列其中一個字元集識別碼：</span><span class="sxs-lookup"><span data-stu-id="2bd09-211">The *charsetID* parameter specifies one of the following character-set identifiers:</span></span>



| <span data-ttu-id="2bd09-212">識別碼</span><span class="sxs-lookup"><span data-stu-id="2bd09-212">Identifier</span></span> | <span data-ttu-id="2bd09-213">字元集</span><span class="sxs-lookup"><span data-stu-id="2bd09-213">Character Set</span></span>              |
|------------|----------------------------|
| <span data-ttu-id="2bd09-214">0</span><span class="sxs-lookup"><span data-stu-id="2bd09-214">0</span></span>          | <span data-ttu-id="2bd09-215">7位 ASCII</span><span class="sxs-lookup"><span data-stu-id="2bd09-215">7-bit ASCII</span></span>                |
| <span data-ttu-id="2bd09-216">932</span><span class="sxs-lookup"><span data-stu-id="2bd09-216">932</span></span>        | <span data-ttu-id="2bd09-217">日本 (Shift – JIS X-0208) </span><span class="sxs-lookup"><span data-stu-id="2bd09-217">Japan (Shift – JIS X-0208)</span></span> |
| <span data-ttu-id="2bd09-218">949</span><span class="sxs-lookup"><span data-stu-id="2bd09-218">949</span></span>        | <span data-ttu-id="2bd09-219">韓國 (Shift – KSC 5601) </span><span class="sxs-lookup"><span data-stu-id="2bd09-219">Korea (Shift – KSC 5601)</span></span>   |
| <span data-ttu-id="2bd09-220">950</span><span class="sxs-lookup"><span data-stu-id="2bd09-220">950</span></span>        | <span data-ttu-id="2bd09-221">臺灣 (Big5) </span><span class="sxs-lookup"><span data-stu-id="2bd09-221">Taiwan (Big5)</span></span>              |
| <span data-ttu-id="2bd09-222">1200</span><span class="sxs-lookup"><span data-stu-id="2bd09-222">1200</span></span>       | <span data-ttu-id="2bd09-223">Unicode</span><span class="sxs-lookup"><span data-stu-id="2bd09-223">Unicode</span></span>                    |
| <span data-ttu-id="2bd09-224">1250</span><span class="sxs-lookup"><span data-stu-id="2bd09-224">1250</span></span>       | <span data-ttu-id="2bd09-225">拉丁美洲 (東部歐洲) </span><span class="sxs-lookup"><span data-stu-id="2bd09-225">Latin-2 (Eastern European)</span></span> |
| <span data-ttu-id="2bd09-226">1251</span><span class="sxs-lookup"><span data-stu-id="2bd09-226">1251</span></span>       | <span data-ttu-id="2bd09-227">古斯拉夫文</span><span class="sxs-lookup"><span data-stu-id="2bd09-227">Cyrillic</span></span>                   |
| <span data-ttu-id="2bd09-228">1252</span><span class="sxs-lookup"><span data-stu-id="2bd09-228">1252</span></span>       | <span data-ttu-id="2bd09-229">多 語種</span><span class="sxs-lookup"><span data-stu-id="2bd09-229">Multilingual</span></span>               |
| <span data-ttu-id="2bd09-230">1253</span><span class="sxs-lookup"><span data-stu-id="2bd09-230">1253</span></span>       | <span data-ttu-id="2bd09-231">希臘文</span><span class="sxs-lookup"><span data-stu-id="2bd09-231">Greek</span></span>                      |
| <span data-ttu-id="2bd09-232">1254</span><span class="sxs-lookup"><span data-stu-id="2bd09-232">1254</span></span>       | <span data-ttu-id="2bd09-233">土耳其文</span><span class="sxs-lookup"><span data-stu-id="2bd09-233">Turkish</span></span>                    |
| <span data-ttu-id="2bd09-234">1255</span><span class="sxs-lookup"><span data-stu-id="2bd09-234">1255</span></span>       | <span data-ttu-id="2bd09-235">Hebrew</span><span class="sxs-lookup"><span data-stu-id="2bd09-235">Hebrew</span></span>                     |
| <span data-ttu-id="2bd09-236">1256</span><span class="sxs-lookup"><span data-stu-id="2bd09-236">1256</span></span>       | <span data-ttu-id="2bd09-237">阿拉伯文</span><span class="sxs-lookup"><span data-stu-id="2bd09-237">Arabic</span></span>                     |



 

 

 




