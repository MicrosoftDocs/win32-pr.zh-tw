---
title: LanguageID 屬性
description: LanguageID 屬性
ms.assetid: f57b0fa1-b3b8-49c8-b441-2a40e564d6ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7a10e6b16f9e35b223bada728871d253685538
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301876"
---
# <a name="languageid-property"></a><span data-ttu-id="411e1-103">LanguageID 屬性</span><span class="sxs-lookup"><span data-stu-id="411e1-103">LanguageID Property</span></span>

<span data-ttu-id="411e1-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="411e1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="411e1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="411e1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="411e1-106">傳回或設定字元的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="411e1-106">Returns or sets the language ID for the character.</span></span>

</dd> <dt>

<span data-ttu-id="411e1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="411e1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="411e1-108">*agent. \* \* \* 字元* \* **( "***CharacterID***" ) 。LanguageID** \[  =  *LanguageID*\]</span><span class="sxs-lookup"><span data-stu-id="411e1-108">*agent.\*\*\*Characters*\* **("***CharacterID***").LanguageID** \[ = *LanguageID*\]</span></span>



<span data-ttu-id="411e1-109">部分</span><span class="sxs-lookup"><span data-stu-id="411e1-109">Part</span></span>

<span data-ttu-id="411e1-110">描述</span><span class="sxs-lookup"><span data-stu-id="411e1-110">Description</span></span>

<span data-ttu-id="411e1-111">LanguageID</span><span class="sxs-lookup"><span data-stu-id="411e1-111">LanguageID</span></span>

<span data-ttu-id="411e1-112">指定字元語言識別項的長整數。</span><span class="sxs-lookup"><span data-stu-id="411e1-112">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="411e1-113">字元的語言識別項 (LANGID) 是由 Windows 定義的16位值，其中包含主要語言識別項和次要語言識別項。</span><span class="sxs-lookup"><span data-stu-id="411e1-113">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="411e1-114">下列範例是 Microsoft Agent 支援之語言的值。</span><span class="sxs-lookup"><span data-stu-id="411e1-114">The following examples are values for languages supported by Microsoft Agent.</span></span> <span data-ttu-id="411e1-115">若要判斷其他語言的值，請參閱 *PLATFORM SDK 檔*。</span><span class="sxs-lookup"><span data-stu-id="411e1-115">To determine the value for other languages, see the *Platform SDK documentation*.</span></span>

 

<span data-ttu-id="411e1-116">阿拉伯文</span><span class="sxs-lookup"><span data-stu-id="411e1-116">Arabic</span></span>

<span data-ttu-id="411e1-117">&H0401</span><span class="sxs-lookup"><span data-stu-id="411e1-117">&H0401</span></span>

<span data-ttu-id="411e1-118">義大利文</span><span class="sxs-lookup"><span data-stu-id="411e1-118">Italian</span></span>

<span data-ttu-id="411e1-119">&H0410</span><span class="sxs-lookup"><span data-stu-id="411e1-119">&H0410</span></span>

 

<span data-ttu-id="411e1-120">巴斯克文</span><span class="sxs-lookup"><span data-stu-id="411e1-120">Basque</span></span>

<span data-ttu-id="411e1-121">&H042D</span><span class="sxs-lookup"><span data-stu-id="411e1-121">&H042D</span></span>

<span data-ttu-id="411e1-122">日文</span><span class="sxs-lookup"><span data-stu-id="411e1-122">Japanese</span></span>

<span data-ttu-id="411e1-123">&H0411</span><span class="sxs-lookup"><span data-stu-id="411e1-123">&H0411</span></span>

 

<span data-ttu-id="411e1-124">簡體中文</span><span class="sxs-lookup"><span data-stu-id="411e1-124">Chinese (Simplified)</span></span>

<span data-ttu-id="411e1-125">&H0804</span><span class="sxs-lookup"><span data-stu-id="411e1-125">&H0804</span></span>

<span data-ttu-id="411e1-126">韓文</span><span class="sxs-lookup"><span data-stu-id="411e1-126">Korean</span></span>

<span data-ttu-id="411e1-127">&H0412</span><span class="sxs-lookup"><span data-stu-id="411e1-127">&H0412</span></span>

 

<span data-ttu-id="411e1-128">繁體中文</span><span class="sxs-lookup"><span data-stu-id="411e1-128">Chinese (Traditional)</span></span>

<span data-ttu-id="411e1-129">&H0404</span><span class="sxs-lookup"><span data-stu-id="411e1-129">&H0404</span></span>

<span data-ttu-id="411e1-130">挪威文</span><span class="sxs-lookup"><span data-stu-id="411e1-130">Norwegian</span></span>

<span data-ttu-id="411e1-131">&H0414</span><span class="sxs-lookup"><span data-stu-id="411e1-131">&H0414</span></span>

 

<span data-ttu-id="411e1-132">克羅埃西亞文</span><span class="sxs-lookup"><span data-stu-id="411e1-132">Croatian</span></span>

<span data-ttu-id="411e1-133">&H041A</span><span class="sxs-lookup"><span data-stu-id="411e1-133">&H041A</span></span>

<span data-ttu-id="411e1-134">波蘭文</span><span class="sxs-lookup"><span data-stu-id="411e1-134">Polish</span></span>

<span data-ttu-id="411e1-135">&H0415</span><span class="sxs-lookup"><span data-stu-id="411e1-135">&H0415</span></span>

 

<span data-ttu-id="411e1-136">捷克文</span><span class="sxs-lookup"><span data-stu-id="411e1-136">Czech</span></span>

<span data-ttu-id="411e1-137">&H0405</span><span class="sxs-lookup"><span data-stu-id="411e1-137">&H0405</span></span>

<span data-ttu-id="411e1-138">葡萄牙文 (葡萄牙)</span><span class="sxs-lookup"><span data-stu-id="411e1-138">Portuguese (Portugal)</span></span>

<span data-ttu-id="411e1-139">&H0816</span><span class="sxs-lookup"><span data-stu-id="411e1-139">&H0816</span></span>

 

<span data-ttu-id="411e1-140">丹麥文</span><span class="sxs-lookup"><span data-stu-id="411e1-140">Danish</span></span>

<span data-ttu-id="411e1-141">&H0406</span><span class="sxs-lookup"><span data-stu-id="411e1-141">&H0406</span></span>

<span data-ttu-id="411e1-142">葡萄牙文 (巴西)</span><span class="sxs-lookup"><span data-stu-id="411e1-142">Portuguese (Brazil)</span></span>

<span data-ttu-id="411e1-143">&H0416</span><span class="sxs-lookup"><span data-stu-id="411e1-143">&H0416</span></span>

 

<span data-ttu-id="411e1-144">荷蘭文</span><span class="sxs-lookup"><span data-stu-id="411e1-144">Dutch</span></span>

<span data-ttu-id="411e1-145">&H0413</span><span class="sxs-lookup"><span data-stu-id="411e1-145">&H0413</span></span>

<span data-ttu-id="411e1-146">羅馬尼亞文</span><span class="sxs-lookup"><span data-stu-id="411e1-146">Romanian</span></span>

<span data-ttu-id="411e1-147">&H0418</span><span class="sxs-lookup"><span data-stu-id="411e1-147">&H0418</span></span>

 

<span data-ttu-id="411e1-148">英文 (英國)</span><span class="sxs-lookup"><span data-stu-id="411e1-148">English (British)</span></span>

<span data-ttu-id="411e1-149">&H0809</span><span class="sxs-lookup"><span data-stu-id="411e1-149">&H0809</span></span>

<span data-ttu-id="411e1-150">俄文</span><span class="sxs-lookup"><span data-stu-id="411e1-150">Russian</span></span>

<span data-ttu-id="411e1-151">&H0419</span><span class="sxs-lookup"><span data-stu-id="411e1-151">&H0419</span></span>

 

<span data-ttu-id="411e1-152">英文 (美國)</span><span class="sxs-lookup"><span data-stu-id="411e1-152">English (US)</span></span>

<span data-ttu-id="411e1-153">&H0409</span><span class="sxs-lookup"><span data-stu-id="411e1-153">&H0409</span></span>

<span data-ttu-id="411e1-154">斯洛伐克文</span><span class="sxs-lookup"><span data-stu-id="411e1-154">Slovakian</span></span>

<span data-ttu-id="411e1-155">&H041B</span><span class="sxs-lookup"><span data-stu-id="411e1-155">&H041B</span></span>

 

<span data-ttu-id="411e1-156">芬蘭文</span><span class="sxs-lookup"><span data-stu-id="411e1-156">Finnish</span></span>

<span data-ttu-id="411e1-157">&H040B</span><span class="sxs-lookup"><span data-stu-id="411e1-157">&H040B</span></span>

<span data-ttu-id="411e1-158">斯洛維尼亞文</span><span class="sxs-lookup"><span data-stu-id="411e1-158">Slovenian</span></span>

<span data-ttu-id="411e1-159">&H0424</span><span class="sxs-lookup"><span data-stu-id="411e1-159">&H0424</span></span>

 

<span data-ttu-id="411e1-160">法文</span><span class="sxs-lookup"><span data-stu-id="411e1-160">French</span></span>

<span data-ttu-id="411e1-161">&H040C</span><span class="sxs-lookup"><span data-stu-id="411e1-161">&H040C</span></span>

<span data-ttu-id="411e1-162">西班牙文</span><span class="sxs-lookup"><span data-stu-id="411e1-162">Spanish</span></span>

<span data-ttu-id="411e1-163">&H0C0A</span><span class="sxs-lookup"><span data-stu-id="411e1-163">&H0C0A</span></span>

 

<span data-ttu-id="411e1-164">德文</span><span class="sxs-lookup"><span data-stu-id="411e1-164">German</span></span>

<span data-ttu-id="411e1-165">&H0407</span><span class="sxs-lookup"><span data-stu-id="411e1-165">&H0407</span></span>

<span data-ttu-id="411e1-166">瑞典文</span><span class="sxs-lookup"><span data-stu-id="411e1-166">Swedish</span></span>

<span data-ttu-id="411e1-167">&H041D</span><span class="sxs-lookup"><span data-stu-id="411e1-167">&H041D</span></span>

 

<span data-ttu-id="411e1-168">希臘文</span><span class="sxs-lookup"><span data-stu-id="411e1-168">Greek</span></span>

<span data-ttu-id="411e1-169">&H0408</span><span class="sxs-lookup"><span data-stu-id="411e1-169">&H0408</span></span>

<span data-ttu-id="411e1-170">泰文</span><span class="sxs-lookup"><span data-stu-id="411e1-170">Thai</span></span>

<span data-ttu-id="411e1-171">&H041E</span><span class="sxs-lookup"><span data-stu-id="411e1-171">&H041E</span></span>

 

<span data-ttu-id="411e1-172">Hebrew</span><span class="sxs-lookup"><span data-stu-id="411e1-172">Hebrew</span></span>

<span data-ttu-id="411e1-173">&H040D</span><span class="sxs-lookup"><span data-stu-id="411e1-173">&H040D</span></span>

<span data-ttu-id="411e1-174">土耳其文</span><span class="sxs-lookup"><span data-stu-id="411e1-174">Turkish</span></span>

<span data-ttu-id="411e1-175">&H041F</span><span class="sxs-lookup"><span data-stu-id="411e1-175">&H041F</span></span>

 

<span data-ttu-id="411e1-176">匈牙利文</span><span class="sxs-lookup"><span data-stu-id="411e1-176">Hungarian</span></span>

<span data-ttu-id="411e1-177">&H040E</span><span class="sxs-lookup"><span data-stu-id="411e1-177">&H040E</span></span>

 

 



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="411e1-178">備註</span><span class="sxs-lookup"><span data-stu-id="411e1-178">Remarks</span></span>

<span data-ttu-id="411e1-179">如果您未設定字元的 **LanguageID** ，則如果已安裝對應的代理程式語言 DLL，則其語言識別項將會是目前的系統語言識別項，否則，字元的語言會是英文 (US) 。</span><span class="sxs-lookup"><span data-stu-id="411e1-179">If you do not set the **LanguageID** for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed, otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="411e1-180">這個屬性也會決定文字註解文字的語言、字元快顯功能表中的命令，以及語音辨識引擎。</span><span class="sxs-lookup"><span data-stu-id="411e1-180">This property also determines the language for word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="411e1-181">它也會決定 TTS 輸出的預設語言。</span><span class="sxs-lookup"><span data-stu-id="411e1-181">It also determines the default language for TTS output.</span></span>

<span data-ttu-id="411e1-182">如果您嘗試設定字元的 **LanguageID** ，且未安裝該語言的代理程式語言 DLL，或無法使用語言識別項的顯示字型，則代理程式會引發錯誤，而 **LanguageID** 會維持在其最後一個設定。</span><span class="sxs-lookup"><span data-stu-id="411e1-182">If you try to set the **LanguageID** for a character and the Agent language DLL for that language is not installed or a display font for the language ID is not available, Agent raises an error and **LanguageID** remains at its last setting.</span></span>

<span data-ttu-id="411e1-183">如果語言沒有相符的語音引擎，則設定這個屬性不會引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="411e1-183">Setting this property does not raise an error if there are no matching speech engines for the language.</span></span> <span data-ttu-id="411e1-184">若要判斷 **LanguageID** 是否有相容的語音引擎可供使用，請檢查 [**SRModeID**](srmodeid-property.md) 或 [**TTSModeID**](ttsmodeid-property.md)。</span><span class="sxs-lookup"><span data-stu-id="411e1-184">To determine if there is a compatible speech engine available for the **LanguageID**, check [**SRModeID**](srmodeid-property.md) or [**TTSModeID**](ttsmodeid-property.md).</span></span> <span data-ttu-id="411e1-185">如果您未設定 **LanguageID**，則會設定為 [使用者預設語言識別項] 設定。</span><span class="sxs-lookup"><span data-stu-id="411e1-185">If you do not set **LanguageID**, it will be set to the user default language ID setting.</span></span>

<span data-ttu-id="411e1-186">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="411e1-186">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="411e1-187">如果您將 **LanguageID** 設定為支援雙向文字 (例如阿拉伯文或希伯來文) 的語言，但是執行應用程式的系統沒有安裝雙向支援，則會以邏輯而非顯示順序來顯示文字。</span><span class="sxs-lookup"><span data-stu-id="411e1-187">If you set **LanguageID** to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text in the word balloon will appear in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="411e1-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="411e1-188">See Also</span></span>

<span data-ttu-id="411e1-189">[**SRModeID 屬性**](srmodeid-property.md)， [ **TTSModeID 屬性**](ttsmodeid-property.md)</span><span class="sxs-lookup"><span data-stu-id="411e1-189">[**SRModeID property**](srmodeid-property.md), [**TTSModeID property**](ttsmodeid-property.md)</span></span>


 

 




