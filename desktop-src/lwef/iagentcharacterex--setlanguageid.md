---
title: IAgentCharacterEx SetLanguageID
description: IAgentCharacterEx SetLanguageID
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036e1d41878adaae878a5961b45d190971d790af
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119003"
---
# <a name="iagentcharacterexsetlanguageid"></a><span data-ttu-id="4f191-103">IAgentCharacterEx::SetLanguageID</span><span class="sxs-lookup"><span data-stu-id="4f191-103">IAgentCharacterEx::SetLanguageID</span></span>

<span data-ttu-id="4f191-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="4f191-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

<span data-ttu-id="4f191-105">設定為字元設定的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="4f191-105">Sets the language ID set for the character.</span></span>

-   <span data-ttu-id="4f191-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="4f191-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4f191-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="4f191-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="4f191-108">字元的語言識別項設定。</span><span class="sxs-lookup"><span data-stu-id="4f191-108">The language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="4f191-109">指定字元語言識別項的長整數。</span><span class="sxs-lookup"><span data-stu-id="4f191-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="4f191-110">字元的語言識別項 (LANGID) 是由 Windows 定義的16位值，其中包含主要語言識別項和次要語言識別項。</span><span class="sxs-lookup"><span data-stu-id="4f191-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="4f191-111">您可以針對指定的語言使用下列值。</span><span class="sxs-lookup"><span data-stu-id="4f191-111">You can use the following values for the specified languages.</span></span> <span data-ttu-id="4f191-112">如需詳細資訊，請參閱 Platform SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="4f191-112">For more information, see the Platform SDK documentation.</span></span>



| <span data-ttu-id="4f191-113">語言</span><span class="sxs-lookup"><span data-stu-id="4f191-113">Language</span></span>              | <span data-ttu-id="4f191-114">識別碼</span><span class="sxs-lookup"><span data-stu-id="4f191-114">ID</span></span>     |  <span data-ttu-id="4f191-115">語言</span><span class="sxs-lookup"><span data-stu-id="4f191-115">Language</span></span>             | <span data-ttu-id="4f191-116">識別碼</span><span class="sxs-lookup"><span data-stu-id="4f191-116">ID</span></span>     |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="4f191-117">阿拉伯文 (沙烏地阿拉伯) </span><span class="sxs-lookup"><span data-stu-id="4f191-117">Arabic (Saudi)</span></span>        | <span data-ttu-id="4f191-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="4f191-118">0x0401</span></span> | <span data-ttu-id="4f191-119">義大利文</span><span class="sxs-lookup"><span data-stu-id="4f191-119">Italian</span></span>               | <span data-ttu-id="4f191-120">0x0410</span><span class="sxs-lookup"><span data-stu-id="4f191-120">0x0410</span></span> |
| <span data-ttu-id="4f191-121">巴斯克文</span><span class="sxs-lookup"><span data-stu-id="4f191-121">Basque</span></span>                | <span data-ttu-id="4f191-122">0x042d</span><span class="sxs-lookup"><span data-stu-id="4f191-122">0x042d</span></span> | <span data-ttu-id="4f191-123">日文</span><span class="sxs-lookup"><span data-stu-id="4f191-123">Japanese</span></span>              | <span data-ttu-id="4f191-124">0x0411</span><span class="sxs-lookup"><span data-stu-id="4f191-124">0x0411</span></span> |
| <span data-ttu-id="4f191-125">簡體中文</span><span class="sxs-lookup"><span data-stu-id="4f191-125">Chinese (Simplified)</span></span>  | <span data-ttu-id="4f191-126">0x0804</span><span class="sxs-lookup"><span data-stu-id="4f191-126">0x0804</span></span> | <span data-ttu-id="4f191-127">韓文</span><span class="sxs-lookup"><span data-stu-id="4f191-127">Korean</span></span>                | <span data-ttu-id="4f191-128">0x0412</span><span class="sxs-lookup"><span data-stu-id="4f191-128">0x0412</span></span> |
| <span data-ttu-id="4f191-129">繁體中文</span><span class="sxs-lookup"><span data-stu-id="4f191-129">Chinese (Traditional)</span></span> | <span data-ttu-id="4f191-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="4f191-130">0x0404</span></span> | <span data-ttu-id="4f191-131">挪威文</span><span class="sxs-lookup"><span data-stu-id="4f191-131">Norwegian</span></span>             | <span data-ttu-id="4f191-132">0x0414</span><span class="sxs-lookup"><span data-stu-id="4f191-132">0x0414</span></span> |
| <span data-ttu-id="4f191-133">克羅埃西亞文</span><span class="sxs-lookup"><span data-stu-id="4f191-133">Croatian</span></span>              | <span data-ttu-id="4f191-134">0x041A</span><span class="sxs-lookup"><span data-stu-id="4f191-134">0x041A</span></span> | <span data-ttu-id="4f191-135">波蘭文</span><span class="sxs-lookup"><span data-stu-id="4f191-135">Polish</span></span>                | <span data-ttu-id="4f191-136">0x0415</span><span class="sxs-lookup"><span data-stu-id="4f191-136">0x0415</span></span> |
| <span data-ttu-id="4f191-137">捷克文</span><span class="sxs-lookup"><span data-stu-id="4f191-137">Czech</span></span>                 | <span data-ttu-id="4f191-138">0x0405</span><span class="sxs-lookup"><span data-stu-id="4f191-138">0x0405</span></span> | <span data-ttu-id="4f191-139">葡萄牙文 (葡萄牙)</span><span class="sxs-lookup"><span data-stu-id="4f191-139">Portuguese (Portugal)</span></span> | <span data-ttu-id="4f191-140">0x0816</span><span class="sxs-lookup"><span data-stu-id="4f191-140">0x0816</span></span> |
| <span data-ttu-id="4f191-141">丹麥文</span><span class="sxs-lookup"><span data-stu-id="4f191-141">Danish</span></span>                | <span data-ttu-id="4f191-142">0x0406</span><span class="sxs-lookup"><span data-stu-id="4f191-142">0x0406</span></span> | <span data-ttu-id="4f191-143">葡萄牙文 (巴西)</span><span class="sxs-lookup"><span data-stu-id="4f191-143">Portuguese (Brazil)</span></span>   | <span data-ttu-id="4f191-144">0x0416</span><span class="sxs-lookup"><span data-stu-id="4f191-144">0x0416</span></span> |
| <span data-ttu-id="4f191-145">荷蘭文</span><span class="sxs-lookup"><span data-stu-id="4f191-145">Dutch</span></span>                 | <span data-ttu-id="4f191-146">0x0413</span><span class="sxs-lookup"><span data-stu-id="4f191-146">0x0413</span></span> | <span data-ttu-id="4f191-147">羅馬尼亞文</span><span class="sxs-lookup"><span data-stu-id="4f191-147">Romanian</span></span>              | <span data-ttu-id="4f191-148">0x0418</span><span class="sxs-lookup"><span data-stu-id="4f191-148">0x0418</span></span> |
| <span data-ttu-id="4f191-149">英文 (英國)</span><span class="sxs-lookup"><span data-stu-id="4f191-149">English (British)</span></span>     | <span data-ttu-id="4f191-150">0x0809</span><span class="sxs-lookup"><span data-stu-id="4f191-150">0x0809</span></span> | <span data-ttu-id="4f191-151">俄文</span><span class="sxs-lookup"><span data-stu-id="4f191-151">Russian</span></span>               | <span data-ttu-id="4f191-152">0x0419</span><span class="sxs-lookup"><span data-stu-id="4f191-152">0x0419</span></span> |
| <span data-ttu-id="4f191-153">英文 (美國)</span><span class="sxs-lookup"><span data-stu-id="4f191-153">English (US)</span></span>          | <span data-ttu-id="4f191-154">0x0409</span><span class="sxs-lookup"><span data-stu-id="4f191-154">0x0409</span></span> | <span data-ttu-id="4f191-155">斯洛伐克文</span><span class="sxs-lookup"><span data-stu-id="4f191-155">Slovakian</span></span>             | <span data-ttu-id="4f191-156">0x041B</span><span class="sxs-lookup"><span data-stu-id="4f191-156">0x041B</span></span> |
| <span data-ttu-id="4f191-157">芬蘭文</span><span class="sxs-lookup"><span data-stu-id="4f191-157">Finnish</span></span>               | <span data-ttu-id="4f191-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="4f191-158">0x040B</span></span> | <span data-ttu-id="4f191-159">斯洛維尼亞文</span><span class="sxs-lookup"><span data-stu-id="4f191-159">Slovenian</span></span>             | <span data-ttu-id="4f191-160">0x0424</span><span class="sxs-lookup"><span data-stu-id="4f191-160">0x0424</span></span> |
| <span data-ttu-id="4f191-161">法文</span><span class="sxs-lookup"><span data-stu-id="4f191-161">French</span></span>                | <span data-ttu-id="4f191-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="4f191-162">0x040C</span></span> | <span data-ttu-id="4f191-163">西班牙文</span><span class="sxs-lookup"><span data-stu-id="4f191-163">Spanish</span></span>               | <span data-ttu-id="4f191-164">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="4f191-164">0x0C0A</span></span> |
| <span data-ttu-id="4f191-165">德文</span><span class="sxs-lookup"><span data-stu-id="4f191-165">German</span></span>                | <span data-ttu-id="4f191-166">0x0407</span><span class="sxs-lookup"><span data-stu-id="4f191-166">0x0407</span></span> | <span data-ttu-id="4f191-167">瑞典文</span><span class="sxs-lookup"><span data-stu-id="4f191-167">Swedish</span></span>               | <span data-ttu-id="4f191-168">0x041D</span><span class="sxs-lookup"><span data-stu-id="4f191-168">0x041D</span></span> |
| <span data-ttu-id="4f191-169">希臘文</span><span class="sxs-lookup"><span data-stu-id="4f191-169">Greek</span></span>                 | <span data-ttu-id="4f191-170">0x0408</span><span class="sxs-lookup"><span data-stu-id="4f191-170">0x0408</span></span> | <span data-ttu-id="4f191-171">泰文</span><span class="sxs-lookup"><span data-stu-id="4f191-171">Thai</span></span>                  | <span data-ttu-id="4f191-172">0x041E</span><span class="sxs-lookup"><span data-stu-id="4f191-172">0x041E</span></span> |
| <span data-ttu-id="4f191-173">Hebrew</span><span class="sxs-lookup"><span data-stu-id="4f191-173">Hebrew</span></span>                | <span data-ttu-id="4f191-174">0x040D</span><span class="sxs-lookup"><span data-stu-id="4f191-174">0x040D</span></span> | <span data-ttu-id="4f191-175">土耳其文</span><span class="sxs-lookup"><span data-stu-id="4f191-175">Turkish</span></span>               | <span data-ttu-id="4f191-176">0x041F</span><span class="sxs-lookup"><span data-stu-id="4f191-176">0x041F</span></span> |
| <span data-ttu-id="4f191-177">匈牙利文</span><span class="sxs-lookup"><span data-stu-id="4f191-177">Hungarian</span></span>             | <span data-ttu-id="4f191-178">0x040E</span><span class="sxs-lookup"><span data-stu-id="4f191-178">0x040E</span></span> |                       |        |



 

<span data-ttu-id="4f191-179">如果您未設定字元的語言識別項，則如果已安裝對應的代理程式語言 DLL，則其語言識別項會是目前的系統語言識別項;否則，字元的語言將會是英文 (US) 。</span><span class="sxs-lookup"><span data-stu-id="4f191-179">If you do not set the language ID for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed; otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="4f191-180">這個屬性也會決定文字註解文字的語言、字元快顯功能表中的命令，以及語音辨識引擎。</span><span class="sxs-lookup"><span data-stu-id="4f191-180">This property also determines the language for the word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="4f191-181">它也會決定 TTS 輸出的預設語言。</span><span class="sxs-lookup"><span data-stu-id="4f191-181">It also determines the default language for TTS output.</span></span> <span data-ttu-id="4f191-182">若要判斷是否有相容的語音引擎可用於該字元的語言，請使用 [**IAgentCharacterEx：： GetSRModeID**](iagentcharacterex--getsrmodeid.md) 或 [**IAgentCharacterEx：： GetTTSModeID**](iagentcharacterex--getttsmodeid.md)。</span><span class="sxs-lookup"><span data-stu-id="4f191-182">To determine if there is a compatible speech engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="4f191-183">如果您嘗試設定字元和代理程式語言資源的語言識別項、字碼頁或語言識別項的顯示字型無法使用，則代理程式會傳回錯誤，而字元的語言識別項仍會維持在其最後一個設定。</span><span class="sxs-lookup"><span data-stu-id="4f191-183">If you try to set the language ID for a character and the Agent language resources, the code page, or a display font for the language ID is not available, Agent returns an error and the character's language ID remains at its last setting.</span></span> <span data-ttu-id="4f191-184">如果語言沒有相符的語音引擎，則設定這個屬性不會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f191-184">Setting this property does not return an error if there are no matching speech engines for the language.</span></span>

<span data-ttu-id="4f191-185">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="4f191-185">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="4f191-186">如果您將字元的語言識別項設定為支援雙向文字 (例如阿拉伯文或希伯來文) ，但執行您的應用程式的系統沒有安裝雙向支援，則文字會以邏輯方式出現在文字提示字元中，而不是顯示順序。</span><span class="sxs-lookup"><span data-stu-id="4f191-186">If you set the character's language ID to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="4f191-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f191-187">See Also</span></span>

<span data-ttu-id="4f191-188">[**IAgentCharacterEx： GetLanguageID**](iagentcharacterex--getlanguageid.md)、 [**IAgentCharacterEx：： GetSRModeID**](iagentcharacterex--getsrmodeid.md)、 [**IAgentCharacterEx：： GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="4f191-188">[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




