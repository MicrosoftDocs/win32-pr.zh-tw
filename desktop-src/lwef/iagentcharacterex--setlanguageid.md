---
title: IAgentCharacterEx SetLanguageID
description: IAgentCharacterEx SetLanguageID
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec8a396c174fd251b1cc7ac8d7e9696c9b9f2d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672119"
---
# <a name="iagentcharacterexsetlanguageid"></a><span data-ttu-id="75f19-103">IAgentCharacterEx::SetLanguageID</span><span class="sxs-lookup"><span data-stu-id="75f19-103">IAgentCharacterEx::SetLanguageID</span></span>

<span data-ttu-id="75f19-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="75f19-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

<span data-ttu-id="75f19-105">設定為字元設定的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="75f19-105">Sets the language ID set for the character.</span></span>

-   <span data-ttu-id="75f19-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="75f19-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="75f19-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="75f19-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="75f19-108">字元的語言識別項設定。</span><span class="sxs-lookup"><span data-stu-id="75f19-108">The language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="75f19-109">指定字元語言識別項的長整數。</span><span class="sxs-lookup"><span data-stu-id="75f19-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="75f19-110">字元的語言識別項 (LANGID) 是由 Windows 定義的16位值，其中包含主要語言識別項和次要語言識別項。</span><span class="sxs-lookup"><span data-stu-id="75f19-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="75f19-111">您可以針對指定的語言使用下列值。</span><span class="sxs-lookup"><span data-stu-id="75f19-111">You can use the following values for the specified languages.</span></span> <span data-ttu-id="75f19-112">如需詳細資訊，請參閱 Platform SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="75f19-112">For more information, see the Platform SDK documentation.</span></span>



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="75f19-113">阿拉伯文 (沙烏地阿拉伯) </span><span class="sxs-lookup"><span data-stu-id="75f19-113">Arabic (Saudi)</span></span>        | <span data-ttu-id="75f19-114">0x0401</span><span class="sxs-lookup"><span data-stu-id="75f19-114">0x0401</span></span> | <span data-ttu-id="75f19-115">義大利文</span><span class="sxs-lookup"><span data-stu-id="75f19-115">Italian</span></span>               | <span data-ttu-id="75f19-116">0x0410</span><span class="sxs-lookup"><span data-stu-id="75f19-116">0x0410</span></span> |
| <span data-ttu-id="75f19-117">巴斯克文</span><span class="sxs-lookup"><span data-stu-id="75f19-117">Basque</span></span>                | <span data-ttu-id="75f19-118">0x042d</span><span class="sxs-lookup"><span data-stu-id="75f19-118">0x042d</span></span> | <span data-ttu-id="75f19-119">日文</span><span class="sxs-lookup"><span data-stu-id="75f19-119">Japanese</span></span>              | <span data-ttu-id="75f19-120">0x0411</span><span class="sxs-lookup"><span data-stu-id="75f19-120">0x0411</span></span> |
| <span data-ttu-id="75f19-121">簡體中文</span><span class="sxs-lookup"><span data-stu-id="75f19-121">Chinese (Simplified)</span></span>  | <span data-ttu-id="75f19-122">0x0804</span><span class="sxs-lookup"><span data-stu-id="75f19-122">0x0804</span></span> | <span data-ttu-id="75f19-123">韓文</span><span class="sxs-lookup"><span data-stu-id="75f19-123">Korean</span></span>                | <span data-ttu-id="75f19-124">0x0412</span><span class="sxs-lookup"><span data-stu-id="75f19-124">0x0412</span></span> |
| <span data-ttu-id="75f19-125">繁體中文</span><span class="sxs-lookup"><span data-stu-id="75f19-125">Chinese (Traditional)</span></span> | <span data-ttu-id="75f19-126">0x0404</span><span class="sxs-lookup"><span data-stu-id="75f19-126">0x0404</span></span> | <span data-ttu-id="75f19-127">挪威文</span><span class="sxs-lookup"><span data-stu-id="75f19-127">Norwegian</span></span>             | <span data-ttu-id="75f19-128">0x0414</span><span class="sxs-lookup"><span data-stu-id="75f19-128">0x0414</span></span> |
| <span data-ttu-id="75f19-129">克羅埃西亞文</span><span class="sxs-lookup"><span data-stu-id="75f19-129">Croatian</span></span>              | <span data-ttu-id="75f19-130">0x041A</span><span class="sxs-lookup"><span data-stu-id="75f19-130">0x041A</span></span> | <span data-ttu-id="75f19-131">波蘭文</span><span class="sxs-lookup"><span data-stu-id="75f19-131">Polish</span></span>                | <span data-ttu-id="75f19-132">0x0415</span><span class="sxs-lookup"><span data-stu-id="75f19-132">0x0415</span></span> |
| <span data-ttu-id="75f19-133">捷克文</span><span class="sxs-lookup"><span data-stu-id="75f19-133">Czech</span></span>                 | <span data-ttu-id="75f19-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="75f19-134">0x0405</span></span> | <span data-ttu-id="75f19-135">葡萄牙文 (葡萄牙)</span><span class="sxs-lookup"><span data-stu-id="75f19-135">Portuguese (Portugal)</span></span> | <span data-ttu-id="75f19-136">0x0816</span><span class="sxs-lookup"><span data-stu-id="75f19-136">0x0816</span></span> |
| <span data-ttu-id="75f19-137">丹麥文</span><span class="sxs-lookup"><span data-stu-id="75f19-137">Danish</span></span>                | <span data-ttu-id="75f19-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="75f19-138">0x0406</span></span> | <span data-ttu-id="75f19-139">葡萄牙文 (巴西)</span><span class="sxs-lookup"><span data-stu-id="75f19-139">Portuguese (Brazil)</span></span>   | <span data-ttu-id="75f19-140">0x0416</span><span class="sxs-lookup"><span data-stu-id="75f19-140">0x0416</span></span> |
| <span data-ttu-id="75f19-141">荷蘭文</span><span class="sxs-lookup"><span data-stu-id="75f19-141">Dutch</span></span>                 | <span data-ttu-id="75f19-142">0x0413</span><span class="sxs-lookup"><span data-stu-id="75f19-142">0x0413</span></span> | <span data-ttu-id="75f19-143">羅馬尼亞文</span><span class="sxs-lookup"><span data-stu-id="75f19-143">Romanian</span></span>              | <span data-ttu-id="75f19-144">0x0418</span><span class="sxs-lookup"><span data-stu-id="75f19-144">0x0418</span></span> |
| <span data-ttu-id="75f19-145">英文 (英國)</span><span class="sxs-lookup"><span data-stu-id="75f19-145">English (British)</span></span>     | <span data-ttu-id="75f19-146">0x0809</span><span class="sxs-lookup"><span data-stu-id="75f19-146">0x0809</span></span> | <span data-ttu-id="75f19-147">俄文</span><span class="sxs-lookup"><span data-stu-id="75f19-147">Russian</span></span>               | <span data-ttu-id="75f19-148">0x0419</span><span class="sxs-lookup"><span data-stu-id="75f19-148">0x0419</span></span> |
| <span data-ttu-id="75f19-149">英文 (美國)</span><span class="sxs-lookup"><span data-stu-id="75f19-149">English (US)</span></span>          | <span data-ttu-id="75f19-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="75f19-150">0x0409</span></span> | <span data-ttu-id="75f19-151">斯洛伐克文</span><span class="sxs-lookup"><span data-stu-id="75f19-151">Slovakian</span></span>             | <span data-ttu-id="75f19-152">0x041B</span><span class="sxs-lookup"><span data-stu-id="75f19-152">0x041B</span></span> |
| <span data-ttu-id="75f19-153">芬蘭文</span><span class="sxs-lookup"><span data-stu-id="75f19-153">Finnish</span></span>               | <span data-ttu-id="75f19-154">0x040B</span><span class="sxs-lookup"><span data-stu-id="75f19-154">0x040B</span></span> | <span data-ttu-id="75f19-155">斯洛維尼亞文</span><span class="sxs-lookup"><span data-stu-id="75f19-155">Slovenian</span></span>             | <span data-ttu-id="75f19-156">0x0424</span><span class="sxs-lookup"><span data-stu-id="75f19-156">0x0424</span></span> |
| <span data-ttu-id="75f19-157">法文</span><span class="sxs-lookup"><span data-stu-id="75f19-157">French</span></span>                | <span data-ttu-id="75f19-158">0x040C</span><span class="sxs-lookup"><span data-stu-id="75f19-158">0x040C</span></span> | <span data-ttu-id="75f19-159">西班牙文</span><span class="sxs-lookup"><span data-stu-id="75f19-159">Spanish</span></span>               | <span data-ttu-id="75f19-160">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="75f19-160">0x0C0A</span></span> |
| <span data-ttu-id="75f19-161">德文</span><span class="sxs-lookup"><span data-stu-id="75f19-161">German</span></span>                | <span data-ttu-id="75f19-162">0x0407</span><span class="sxs-lookup"><span data-stu-id="75f19-162">0x0407</span></span> | <span data-ttu-id="75f19-163">瑞典文</span><span class="sxs-lookup"><span data-stu-id="75f19-163">Swedish</span></span>               | <span data-ttu-id="75f19-164">0x041D</span><span class="sxs-lookup"><span data-stu-id="75f19-164">0x041D</span></span> |
| <span data-ttu-id="75f19-165">希臘文</span><span class="sxs-lookup"><span data-stu-id="75f19-165">Greek</span></span>                 | <span data-ttu-id="75f19-166">0x0408</span><span class="sxs-lookup"><span data-stu-id="75f19-166">0x0408</span></span> | <span data-ttu-id="75f19-167">泰文</span><span class="sxs-lookup"><span data-stu-id="75f19-167">Thai</span></span>                  | <span data-ttu-id="75f19-168">0x041E</span><span class="sxs-lookup"><span data-stu-id="75f19-168">0x041E</span></span> |
| <span data-ttu-id="75f19-169">Hebrew</span><span class="sxs-lookup"><span data-stu-id="75f19-169">Hebrew</span></span>                | <span data-ttu-id="75f19-170">0x040D</span><span class="sxs-lookup"><span data-stu-id="75f19-170">0x040D</span></span> | <span data-ttu-id="75f19-171">土耳其文</span><span class="sxs-lookup"><span data-stu-id="75f19-171">Turkish</span></span>               | <span data-ttu-id="75f19-172">0x041F</span><span class="sxs-lookup"><span data-stu-id="75f19-172">0x041F</span></span> |
| <span data-ttu-id="75f19-173">匈牙利文</span><span class="sxs-lookup"><span data-stu-id="75f19-173">Hungarian</span></span>             | <span data-ttu-id="75f19-174">0x040E</span><span class="sxs-lookup"><span data-stu-id="75f19-174">0x040E</span></span> |                       |        |



 

<span data-ttu-id="75f19-175">如果您未設定字元的語言識別項，則如果已安裝對應的代理程式語言 DLL，則其語言識別項會是目前的系統語言識別項;否則，字元的語言將會是英文 (US) 。</span><span class="sxs-lookup"><span data-stu-id="75f19-175">If you do not set the language ID for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed; otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="75f19-176">這個屬性也會決定文字註解文字的語言、字元快顯功能表中的命令，以及語音辨識引擎。</span><span class="sxs-lookup"><span data-stu-id="75f19-176">This property also determines the language for the word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="75f19-177">它也會決定 TTS 輸出的預設語言。</span><span class="sxs-lookup"><span data-stu-id="75f19-177">It also determines the default language for TTS output.</span></span> <span data-ttu-id="75f19-178">若要判斷是否有相容的語音引擎可用於該字元的語言，請使用 [**IAgentCharacterEx：： GetSRModeID**](iagentcharacterex--getsrmodeid.md) 或 [**IAgentCharacterEx：： GetTTSModeID**](iagentcharacterex--getttsmodeid.md)。</span><span class="sxs-lookup"><span data-stu-id="75f19-178">To determine if there is a compatible speech engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="75f19-179">如果您嘗試設定字元和代理程式語言資源的語言識別項、字碼頁或語言識別項的顯示字型無法使用，則代理程式會傳回錯誤，而字元的語言識別項仍會維持在其最後一個設定。</span><span class="sxs-lookup"><span data-stu-id="75f19-179">If you try to set the language ID for a character and the Agent language resources, the code page, or a display font for the language ID is not available, Agent returns an error and the character's language ID remains at its last setting.</span></span> <span data-ttu-id="75f19-180">如果語言沒有相符的語音引擎，則設定這個屬性不會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="75f19-180">Setting this property does not return an error if there are no matching speech engines for the language.</span></span>

<span data-ttu-id="75f19-181">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="75f19-181">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="75f19-182">如果您將字元的語言識別項設定為支援雙向文字 (例如阿拉伯文或希伯來文) ，但執行您的應用程式的系統沒有安裝雙向支援，則文字會以邏輯方式出現在文字提示字元中，而不是顯示順序。</span><span class="sxs-lookup"><span data-stu-id="75f19-182">If you set the character's language ID to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="75f19-183">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75f19-183">See Also</span></span>

<span data-ttu-id="75f19-184">[**IAgentCharacterEx： GetLanguageID**](iagentcharacterex--getlanguageid.md)、 [**IAgentCharacterEx：： GetSRModeID**](iagentcharacterex--getsrmodeid.md)、 [**IAgentCharacterEx：： GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="75f19-184">[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




