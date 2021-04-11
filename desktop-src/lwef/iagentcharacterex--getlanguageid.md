---
title: IAgentCharacterEx GetLanguageID
description: IAgentCharacterEx GetLanguageID
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9679538f93d779acc6272dccada824585c4449f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021805"
---
# <a name="iagentcharacterexgetlanguageid"></a><span data-ttu-id="40339-103">IAgentCharacterEx::GetLanguageID</span><span class="sxs-lookup"><span data-stu-id="40339-103">IAgentCharacterEx::GetLanguageID</span></span>

<span data-ttu-id="40339-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="40339-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

<span data-ttu-id="40339-105">抓取為字元設定的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="40339-105">Retrieves the language ID set for the character.</span></span>

-   <span data-ttu-id="40339-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="40339-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="40339-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span><span class="sxs-lookup"><span data-stu-id="40339-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span></span>
</dt> <dd>

<span data-ttu-id="40339-108">接收字元語言識別項設定之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="40339-108">Address of a variable that receives the language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="40339-109">指定字元語言識別項的長整數。</span><span class="sxs-lookup"><span data-stu-id="40339-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="40339-110">字元的語言識別項 (LANGID) 是由 Windows 定義的16位值，其中包含主要語言識別項和次要語言識別項。</span><span class="sxs-lookup"><span data-stu-id="40339-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="40339-111">下列範例是某些語言的值。</span><span class="sxs-lookup"><span data-stu-id="40339-111">The following examples are values for some languages.</span></span> <span data-ttu-id="40339-112">若要判斷其他語言的值，請參閱 Platform SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="40339-112">To determine the values other languages, see the Platform SDK documentation.</span></span>



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="40339-113">阿拉伯文 (沙烏地阿拉伯) </span><span class="sxs-lookup"><span data-stu-id="40339-113">Arabic (Saudi)</span></span>        | <span data-ttu-id="40339-114">0x0401</span><span class="sxs-lookup"><span data-stu-id="40339-114">0x0401</span></span> | <span data-ttu-id="40339-115">義大利文</span><span class="sxs-lookup"><span data-stu-id="40339-115">Italian</span></span>               | <span data-ttu-id="40339-116">0x0410</span><span class="sxs-lookup"><span data-stu-id="40339-116">0x0410</span></span> |
| <span data-ttu-id="40339-117">巴斯克文</span><span class="sxs-lookup"><span data-stu-id="40339-117">Basque</span></span>                | <span data-ttu-id="40339-118">0x042d</span><span class="sxs-lookup"><span data-stu-id="40339-118">0x042d</span></span> | <span data-ttu-id="40339-119">日文</span><span class="sxs-lookup"><span data-stu-id="40339-119">Japanese</span></span>              | <span data-ttu-id="40339-120">0x0411</span><span class="sxs-lookup"><span data-stu-id="40339-120">0x0411</span></span> |
| <span data-ttu-id="40339-121">簡體中文</span><span class="sxs-lookup"><span data-stu-id="40339-121">Chinese (Simplified)</span></span>  | <span data-ttu-id="40339-122">0x0804</span><span class="sxs-lookup"><span data-stu-id="40339-122">0x0804</span></span> | <span data-ttu-id="40339-123">韓文</span><span class="sxs-lookup"><span data-stu-id="40339-123">Korean</span></span>                | <span data-ttu-id="40339-124">0x0412</span><span class="sxs-lookup"><span data-stu-id="40339-124">0x0412</span></span> |
| <span data-ttu-id="40339-125">繁體中文</span><span class="sxs-lookup"><span data-stu-id="40339-125">Chinese (Traditional)</span></span> | <span data-ttu-id="40339-126">0x0404</span><span class="sxs-lookup"><span data-stu-id="40339-126">0x0404</span></span> | <span data-ttu-id="40339-127">挪威文</span><span class="sxs-lookup"><span data-stu-id="40339-127">Norwegian</span></span>             | <span data-ttu-id="40339-128">0x0414</span><span class="sxs-lookup"><span data-stu-id="40339-128">0x0414</span></span> |
| <span data-ttu-id="40339-129">克羅埃西亞文</span><span class="sxs-lookup"><span data-stu-id="40339-129">Croatian</span></span>              | <span data-ttu-id="40339-130">0x041A</span><span class="sxs-lookup"><span data-stu-id="40339-130">0x041A</span></span> | <span data-ttu-id="40339-131">波蘭文</span><span class="sxs-lookup"><span data-stu-id="40339-131">Polish</span></span>                | <span data-ttu-id="40339-132">0x0415</span><span class="sxs-lookup"><span data-stu-id="40339-132">0x0415</span></span> |
| <span data-ttu-id="40339-133">捷克文</span><span class="sxs-lookup"><span data-stu-id="40339-133">Czech</span></span>                 | <span data-ttu-id="40339-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="40339-134">0x0405</span></span> | <span data-ttu-id="40339-135">葡萄牙文 (葡萄牙)</span><span class="sxs-lookup"><span data-stu-id="40339-135">Portuguese (Portugal)</span></span> | <span data-ttu-id="40339-136">0x0816</span><span class="sxs-lookup"><span data-stu-id="40339-136">0x0816</span></span> |
| <span data-ttu-id="40339-137">丹麥文</span><span class="sxs-lookup"><span data-stu-id="40339-137">Danish</span></span>                | <span data-ttu-id="40339-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="40339-138">0x0406</span></span> | <span data-ttu-id="40339-139">葡萄牙文 (巴西)</span><span class="sxs-lookup"><span data-stu-id="40339-139">Portuguese (Brazil)</span></span>   | <span data-ttu-id="40339-140">0x0416</span><span class="sxs-lookup"><span data-stu-id="40339-140">0x0416</span></span> |
| <span data-ttu-id="40339-141">荷蘭文</span><span class="sxs-lookup"><span data-stu-id="40339-141">Dutch</span></span>                 | <span data-ttu-id="40339-142">0x0413</span><span class="sxs-lookup"><span data-stu-id="40339-142">0x0413</span></span> | <span data-ttu-id="40339-143">羅馬尼亞文</span><span class="sxs-lookup"><span data-stu-id="40339-143">Romanian</span></span>              | <span data-ttu-id="40339-144">0x0418</span><span class="sxs-lookup"><span data-stu-id="40339-144">0x0418</span></span> |
| <span data-ttu-id="40339-145">英文 (英國)</span><span class="sxs-lookup"><span data-stu-id="40339-145">English (British)</span></span>     | <span data-ttu-id="40339-146">0x0809</span><span class="sxs-lookup"><span data-stu-id="40339-146">0x0809</span></span> | <span data-ttu-id="40339-147">俄文</span><span class="sxs-lookup"><span data-stu-id="40339-147">Russian</span></span>               | <span data-ttu-id="40339-148">0x0419</span><span class="sxs-lookup"><span data-stu-id="40339-148">0x0419</span></span> |
| <span data-ttu-id="40339-149">英文 (美國)</span><span class="sxs-lookup"><span data-stu-id="40339-149">English (US)</span></span>          | <span data-ttu-id="40339-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="40339-150">0x0409</span></span> | <span data-ttu-id="40339-151">斯洛伐克文</span><span class="sxs-lookup"><span data-stu-id="40339-151">Slovakian</span></span>             | <span data-ttu-id="40339-152">0x041B</span><span class="sxs-lookup"><span data-stu-id="40339-152">0x041B</span></span> |
| <span data-ttu-id="40339-153">芬蘭文</span><span class="sxs-lookup"><span data-stu-id="40339-153">Finnish</span></span>               | <span data-ttu-id="40339-154">0x040B</span><span class="sxs-lookup"><span data-stu-id="40339-154">0x040B</span></span> | <span data-ttu-id="40339-155">斯洛維尼亞文</span><span class="sxs-lookup"><span data-stu-id="40339-155">Slovenian</span></span>             | <span data-ttu-id="40339-156">0x0424</span><span class="sxs-lookup"><span data-stu-id="40339-156">0x0424</span></span> |
| <span data-ttu-id="40339-157">法文</span><span class="sxs-lookup"><span data-stu-id="40339-157">French</span></span>                | <span data-ttu-id="40339-158">0x040C</span><span class="sxs-lookup"><span data-stu-id="40339-158">0x040C</span></span> | <span data-ttu-id="40339-159">西班牙文</span><span class="sxs-lookup"><span data-stu-id="40339-159">Spanish</span></span>               | <span data-ttu-id="40339-160">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="40339-160">0x0C0A</span></span> |
| <span data-ttu-id="40339-161">德文</span><span class="sxs-lookup"><span data-stu-id="40339-161">German</span></span>                | <span data-ttu-id="40339-162">0x0407</span><span class="sxs-lookup"><span data-stu-id="40339-162">0x0407</span></span> | <span data-ttu-id="40339-163">瑞典文</span><span class="sxs-lookup"><span data-stu-id="40339-163">Swedish</span></span>               | <span data-ttu-id="40339-164">0x041D</span><span class="sxs-lookup"><span data-stu-id="40339-164">0x041D</span></span> |
| <span data-ttu-id="40339-165">希臘文</span><span class="sxs-lookup"><span data-stu-id="40339-165">Greek</span></span>                 | <span data-ttu-id="40339-166">0x0408</span><span class="sxs-lookup"><span data-stu-id="40339-166">0x0408</span></span> | <span data-ttu-id="40339-167">泰文</span><span class="sxs-lookup"><span data-stu-id="40339-167">Thai</span></span>                  | <span data-ttu-id="40339-168">0x041E</span><span class="sxs-lookup"><span data-stu-id="40339-168">0x041E</span></span> |
| <span data-ttu-id="40339-169">Hebrew</span><span class="sxs-lookup"><span data-stu-id="40339-169">Hebrew</span></span>                | <span data-ttu-id="40339-170">0x040D</span><span class="sxs-lookup"><span data-stu-id="40339-170">0x040D</span></span> | <span data-ttu-id="40339-171">土耳其文</span><span class="sxs-lookup"><span data-stu-id="40339-171">Turkish</span></span>               | <span data-ttu-id="40339-172">0x041F</span><span class="sxs-lookup"><span data-stu-id="40339-172">0x041F</span></span> |
| <span data-ttu-id="40339-173">匈牙利文</span><span class="sxs-lookup"><span data-stu-id="40339-173">Hungarian</span></span>             | <span data-ttu-id="40339-174">0x040E</span><span class="sxs-lookup"><span data-stu-id="40339-174">0x040E</span></span> |                       |        |



 

<span data-ttu-id="40339-175">如果您未設定此字元的語言識別項，則字元的語言識別項將會是目前的系統語言識別項。</span><span class="sxs-lookup"><span data-stu-id="40339-175">If you do not set this language ID for the character, the character's language ID will be the current system language ID.</span></span>

<span data-ttu-id="40339-176">這項設定也會決定 TTS 輸出的語言、文字氣球文字、字元的快顯功能表中的命令，以及語音辨識引擎。</span><span class="sxs-lookup"><span data-stu-id="40339-176">This setting also determines the language for TTS output, word balloon text, the commands in the character's pop-up menu, and speech recognition engine.</span></span> <span data-ttu-id="40339-177">若要判斷是否有相容的語音辨識引擎可用於該字元的語言，請使用 [**IAgentCharacterEx：： GetSRModeID**](iagentcharacterex--getsrmodeid.md) 或 [**IAgentCharacterEx：： GetTTSModeID**](iagentcharacterex--getttsmodeid.md)。</span><span class="sxs-lookup"><span data-stu-id="40339-177">To determine if there is a compatible speech recognition engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="40339-178">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="40339-178">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="40339-179">如果語言識別項設定為支援雙向文字 (例如阿拉伯文或希伯來文) 的語言，但執行您應用程式的系統沒有安裝雙向支援，則文字會以邏輯方式出現在文字提示字元中，而不是顯示順序。</span><span class="sxs-lookup"><span data-stu-id="40339-179">If the language ID is set to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="40339-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40339-180">See Also</span></span>

<span data-ttu-id="40339-181">[**IAgentCharacterEx： SetLanguageID**](iagentcharacterex--setlanguageid.md)、 [**IAgentCharacterEx：： GetSRModeID**](iagentcharacterex--getsrmodeid.md)、 [**IAgentCharacterEx：： GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="40339-181">[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




