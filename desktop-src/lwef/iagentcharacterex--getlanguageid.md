---
title: IAgentCharacterEx GetLanguageID
description: IAgentCharacterEx GetLanguageID
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d847bf392709b2433b045a357a703173e2de454
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120644"
---
# <a name="iagentcharacterexgetlanguageid"></a><span data-ttu-id="8f877-103">IAgentCharacterEx::GetLanguageID</span><span class="sxs-lookup"><span data-stu-id="8f877-103">IAgentCharacterEx::GetLanguageID</span></span>

<span data-ttu-id="8f877-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="8f877-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

<span data-ttu-id="8f877-105">抓取為字元設定的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="8f877-105">Retrieves the language ID set for the character.</span></span>

-   <span data-ttu-id="8f877-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="8f877-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8f877-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span><span class="sxs-lookup"><span data-stu-id="8f877-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span></span>
</dt> <dd>

<span data-ttu-id="8f877-108">接收字元語言識別項設定之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="8f877-108">Address of a variable that receives the language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="8f877-109">指定字元語言識別項的長整數。</span><span class="sxs-lookup"><span data-stu-id="8f877-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="8f877-110">字元的語言識別項 (LANGID) 是由 Windows 定義的16位值，其中包含主要語言識別項和次要語言識別項。</span><span class="sxs-lookup"><span data-stu-id="8f877-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="8f877-111">下列範例是某些語言的值。</span><span class="sxs-lookup"><span data-stu-id="8f877-111">The following examples are values for some languages.</span></span> <span data-ttu-id="8f877-112">若要判斷其他語言的值，請參閱 Platform SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="8f877-112">To determine the values other languages, see the Platform SDK documentation.</span></span>



| <span data-ttu-id="8f877-113">語言</span><span class="sxs-lookup"><span data-stu-id="8f877-113">Language</span></span>              | <span data-ttu-id="8f877-114">識別碼</span><span class="sxs-lookup"><span data-stu-id="8f877-114">ID</span></span>     | <span data-ttu-id="8f877-115">語言</span><span class="sxs-lookup"><span data-stu-id="8f877-115">Language</span></span>              | <span data-ttu-id="8f877-116">識別碼</span><span class="sxs-lookup"><span data-stu-id="8f877-116">ID</span></span>     |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="8f877-117">阿拉伯文 (沙烏地阿拉伯) </span><span class="sxs-lookup"><span data-stu-id="8f877-117">Arabic (Saudi)</span></span>        | <span data-ttu-id="8f877-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="8f877-118">0x0401</span></span> | <span data-ttu-id="8f877-119">義大利文</span><span class="sxs-lookup"><span data-stu-id="8f877-119">Italian</span></span>               | <span data-ttu-id="8f877-120">0x0410</span><span class="sxs-lookup"><span data-stu-id="8f877-120">0x0410</span></span> |
| <span data-ttu-id="8f877-121">巴斯克文</span><span class="sxs-lookup"><span data-stu-id="8f877-121">Basque</span></span>                | <span data-ttu-id="8f877-122">0x042d</span><span class="sxs-lookup"><span data-stu-id="8f877-122">0x042d</span></span> | <span data-ttu-id="8f877-123">日文</span><span class="sxs-lookup"><span data-stu-id="8f877-123">Japanese</span></span>              | <span data-ttu-id="8f877-124">0x0411</span><span class="sxs-lookup"><span data-stu-id="8f877-124">0x0411</span></span> |
| <span data-ttu-id="8f877-125">簡體中文</span><span class="sxs-lookup"><span data-stu-id="8f877-125">Chinese (Simplified)</span></span>  | <span data-ttu-id="8f877-126">0x0804</span><span class="sxs-lookup"><span data-stu-id="8f877-126">0x0804</span></span> | <span data-ttu-id="8f877-127">韓文</span><span class="sxs-lookup"><span data-stu-id="8f877-127">Korean</span></span>                | <span data-ttu-id="8f877-128">0x0412</span><span class="sxs-lookup"><span data-stu-id="8f877-128">0x0412</span></span> |
| <span data-ttu-id="8f877-129">繁體中文</span><span class="sxs-lookup"><span data-stu-id="8f877-129">Chinese (Traditional)</span></span> | <span data-ttu-id="8f877-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="8f877-130">0x0404</span></span> | <span data-ttu-id="8f877-131">挪威文</span><span class="sxs-lookup"><span data-stu-id="8f877-131">Norwegian</span></span>             | <span data-ttu-id="8f877-132">0x0414</span><span class="sxs-lookup"><span data-stu-id="8f877-132">0x0414</span></span> |
| <span data-ttu-id="8f877-133">克羅埃西亞文</span><span class="sxs-lookup"><span data-stu-id="8f877-133">Croatian</span></span>              | <span data-ttu-id="8f877-134">0x041A</span><span class="sxs-lookup"><span data-stu-id="8f877-134">0x041A</span></span> | <span data-ttu-id="8f877-135">波蘭文</span><span class="sxs-lookup"><span data-stu-id="8f877-135">Polish</span></span>                | <span data-ttu-id="8f877-136">0x0415</span><span class="sxs-lookup"><span data-stu-id="8f877-136">0x0415</span></span> |
| <span data-ttu-id="8f877-137">捷克文</span><span class="sxs-lookup"><span data-stu-id="8f877-137">Czech</span></span>                 | <span data-ttu-id="8f877-138">0x0405</span><span class="sxs-lookup"><span data-stu-id="8f877-138">0x0405</span></span> | <span data-ttu-id="8f877-139">葡萄牙文 (葡萄牙)</span><span class="sxs-lookup"><span data-stu-id="8f877-139">Portuguese (Portugal)</span></span> | <span data-ttu-id="8f877-140">0x0816</span><span class="sxs-lookup"><span data-stu-id="8f877-140">0x0816</span></span> |
| <span data-ttu-id="8f877-141">丹麥文</span><span class="sxs-lookup"><span data-stu-id="8f877-141">Danish</span></span>                | <span data-ttu-id="8f877-142">0x0406</span><span class="sxs-lookup"><span data-stu-id="8f877-142">0x0406</span></span> | <span data-ttu-id="8f877-143">葡萄牙文 (巴西)</span><span class="sxs-lookup"><span data-stu-id="8f877-143">Portuguese (Brazil)</span></span>   | <span data-ttu-id="8f877-144">0x0416</span><span class="sxs-lookup"><span data-stu-id="8f877-144">0x0416</span></span> |
| <span data-ttu-id="8f877-145">荷蘭文</span><span class="sxs-lookup"><span data-stu-id="8f877-145">Dutch</span></span>                 | <span data-ttu-id="8f877-146">0x0413</span><span class="sxs-lookup"><span data-stu-id="8f877-146">0x0413</span></span> | <span data-ttu-id="8f877-147">羅馬尼亞文</span><span class="sxs-lookup"><span data-stu-id="8f877-147">Romanian</span></span>              | <span data-ttu-id="8f877-148">0x0418</span><span class="sxs-lookup"><span data-stu-id="8f877-148">0x0418</span></span> |
| <span data-ttu-id="8f877-149">英文 (英國)</span><span class="sxs-lookup"><span data-stu-id="8f877-149">English (British)</span></span>     | <span data-ttu-id="8f877-150">0x0809</span><span class="sxs-lookup"><span data-stu-id="8f877-150">0x0809</span></span> | <span data-ttu-id="8f877-151">俄文</span><span class="sxs-lookup"><span data-stu-id="8f877-151">Russian</span></span>               | <span data-ttu-id="8f877-152">0x0419</span><span class="sxs-lookup"><span data-stu-id="8f877-152">0x0419</span></span> |
| <span data-ttu-id="8f877-153">英文 (美國)</span><span class="sxs-lookup"><span data-stu-id="8f877-153">English (US)</span></span>          | <span data-ttu-id="8f877-154">0x0409</span><span class="sxs-lookup"><span data-stu-id="8f877-154">0x0409</span></span> | <span data-ttu-id="8f877-155">斯洛伐克文</span><span class="sxs-lookup"><span data-stu-id="8f877-155">Slovakian</span></span>             | <span data-ttu-id="8f877-156">0x041B</span><span class="sxs-lookup"><span data-stu-id="8f877-156">0x041B</span></span> |
| <span data-ttu-id="8f877-157">芬蘭文</span><span class="sxs-lookup"><span data-stu-id="8f877-157">Finnish</span></span>               | <span data-ttu-id="8f877-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="8f877-158">0x040B</span></span> | <span data-ttu-id="8f877-159">斯洛維尼亞文</span><span class="sxs-lookup"><span data-stu-id="8f877-159">Slovenian</span></span>             | <span data-ttu-id="8f877-160">0x0424</span><span class="sxs-lookup"><span data-stu-id="8f877-160">0x0424</span></span> |
| <span data-ttu-id="8f877-161">法文</span><span class="sxs-lookup"><span data-stu-id="8f877-161">French</span></span>                | <span data-ttu-id="8f877-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="8f877-162">0x040C</span></span> | <span data-ttu-id="8f877-163">西班牙文</span><span class="sxs-lookup"><span data-stu-id="8f877-163">Spanish</span></span>               | <span data-ttu-id="8f877-164">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="8f877-164">0x0C0A</span></span> |
| <span data-ttu-id="8f877-165">德文</span><span class="sxs-lookup"><span data-stu-id="8f877-165">German</span></span>                | <span data-ttu-id="8f877-166">0x0407</span><span class="sxs-lookup"><span data-stu-id="8f877-166">0x0407</span></span> | <span data-ttu-id="8f877-167">瑞典文</span><span class="sxs-lookup"><span data-stu-id="8f877-167">Swedish</span></span>               | <span data-ttu-id="8f877-168">0x041D</span><span class="sxs-lookup"><span data-stu-id="8f877-168">0x041D</span></span> |
| <span data-ttu-id="8f877-169">希臘文</span><span class="sxs-lookup"><span data-stu-id="8f877-169">Greek</span></span>                 | <span data-ttu-id="8f877-170">0x0408</span><span class="sxs-lookup"><span data-stu-id="8f877-170">0x0408</span></span> | <span data-ttu-id="8f877-171">泰文</span><span class="sxs-lookup"><span data-stu-id="8f877-171">Thai</span></span>                  | <span data-ttu-id="8f877-172">0x041E</span><span class="sxs-lookup"><span data-stu-id="8f877-172">0x041E</span></span> |
| <span data-ttu-id="8f877-173">Hebrew</span><span class="sxs-lookup"><span data-stu-id="8f877-173">Hebrew</span></span>                | <span data-ttu-id="8f877-174">0x040D</span><span class="sxs-lookup"><span data-stu-id="8f877-174">0x040D</span></span> | <span data-ttu-id="8f877-175">土耳其文</span><span class="sxs-lookup"><span data-stu-id="8f877-175">Turkish</span></span>               | <span data-ttu-id="8f877-176">0x041F</span><span class="sxs-lookup"><span data-stu-id="8f877-176">0x041F</span></span> |
| <span data-ttu-id="8f877-177">匈牙利文</span><span class="sxs-lookup"><span data-stu-id="8f877-177">Hungarian</span></span>             | <span data-ttu-id="8f877-178">0x040E</span><span class="sxs-lookup"><span data-stu-id="8f877-178">0x040E</span></span> |                       |        |



 

<span data-ttu-id="8f877-179">如果您未設定此字元的語言識別項，則字元的語言識別項將會是目前的系統語言識別項。</span><span class="sxs-lookup"><span data-stu-id="8f877-179">If you do not set this language ID for the character, the character's language ID will be the current system language ID.</span></span>

<span data-ttu-id="8f877-180">這項設定也會決定 TTS 輸出的語言、文字氣球文字、字元的快顯功能表中的命令，以及語音辨識引擎。</span><span class="sxs-lookup"><span data-stu-id="8f877-180">This setting also determines the language for TTS output, word balloon text, the commands in the character's pop-up menu, and speech recognition engine.</span></span> <span data-ttu-id="8f877-181">若要判斷是否有相容的語音辨識引擎可用於該字元的語言，請使用 [**IAgentCharacterEx：： GetSRModeID**](iagentcharacterex--getsrmodeid.md) 或 [**IAgentCharacterEx：： GetTTSModeID**](iagentcharacterex--getttsmodeid.md)。</span><span class="sxs-lookup"><span data-stu-id="8f877-181">To determine if there is a compatible speech recognition engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="8f877-182">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="8f877-182">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="8f877-183">如果語言識別項設定為支援雙向文字 (例如阿拉伯文或希伯來文) 的語言，但執行您應用程式的系統沒有安裝雙向支援，則文字會以邏輯方式出現在文字提示字元中，而不是顯示順序。</span><span class="sxs-lookup"><span data-stu-id="8f877-183">If the language ID is set to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="8f877-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f877-184">See Also</span></span>

<span data-ttu-id="8f877-185">[**IAgentCharacterEx： SetLanguageID**](iagentcharacterex--setlanguageid.md)、 [**IAgentCharacterEx：： GetSRModeID**](iagentcharacterex--getsrmodeid.md)、 [**IAgentCharacterEx：： GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="8f877-185">[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




