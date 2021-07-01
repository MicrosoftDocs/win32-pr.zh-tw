---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cc462895ff9f19f7e722660608a268af13446f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120203"
---
# <a name="iagentballoonsetfontcharset"></a><span data-ttu-id="0e5c7-103">IAgentBalloon::SetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="0e5c7-103">IAgentBalloon::SetFontCharSet</span></span>

<span data-ttu-id="0e5c7-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="0e5c7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="0e5c7-105">設定文字氣球中所顯示字型的字元集。</span><span class="sxs-lookup"><span data-stu-id="0e5c7-105">Sets the character set of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="0e5c7-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="0e5c7-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0e5c7-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="0e5c7-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="0e5c7-108">字型的字元集。</span><span class="sxs-lookup"><span data-stu-id="0e5c7-108">The character set of the font.</span></span> <span data-ttu-id="0e5c7-109">以下是一些常見的值設定：</span><span class="sxs-lookup"><span data-stu-id="0e5c7-109">The following are some common settings for value:</span></span>



| <span data-ttu-id="0e5c7-110">值</span><span class="sxs-lookup"><span data-stu-id="0e5c7-110">Value</span></span>    | <span data-ttu-id="0e5c7-111">字元集</span><span class="sxs-lookup"><span data-stu-id="0e5c7-111">Character set</span></span>                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e5c7-112">0</span><span class="sxs-lookup"><span data-stu-id="0e5c7-112">0</span></span>   | <span data-ttu-id="0e5c7-113">標準 Windows 字元 (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="0e5c7-113">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="0e5c7-114">1</span><span class="sxs-lookup"><span data-stu-id="0e5c7-114">1</span></span>   | <span data-ttu-id="0e5c7-115">預設字元集。</span><span class="sxs-lookup"><span data-stu-id="0e5c7-115">Default character set.</span></span>                                                                 |
| <span data-ttu-id="0e5c7-116">2</span><span class="sxs-lookup"><span data-stu-id="0e5c7-116">2</span></span>   | <span data-ttu-id="0e5c7-117">符號字元集。</span><span class="sxs-lookup"><span data-stu-id="0e5c7-117">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="0e5c7-118">128</span><span class="sxs-lookup"><span data-stu-id="0e5c7-118">128</span></span> | <span data-ttu-id="0e5c7-119">在日文版的 Windows 中，雙位元組字元集 (DBCS) 是唯一的。</span><span class="sxs-lookup"><span data-stu-id="0e5c7-119">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="0e5c7-120">129</span><span class="sxs-lookup"><span data-stu-id="0e5c7-120">129</span></span> | <span data-ttu-id="0e5c7-121">雙位元組字集 (DBCS) Windows 的韓文版本是唯一的。</span><span class="sxs-lookup"><span data-stu-id="0e5c7-121">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="0e5c7-122">134</span><span class="sxs-lookup"><span data-stu-id="0e5c7-122">134</span></span> | <span data-ttu-id="0e5c7-123">雙位元組字集 (DBCS) Windows 的簡體中文版本獨有。</span><span class="sxs-lookup"><span data-stu-id="0e5c7-123">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="0e5c7-124">136</span><span class="sxs-lookup"><span data-stu-id="0e5c7-124">136</span></span> | <span data-ttu-id="0e5c7-125">雙位元組字集 (DBCS) Windows 的唯一版本。</span><span class="sxs-lookup"><span data-stu-id="0e5c7-125">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="0e5c7-126">255</span><span class="sxs-lookup"><span data-stu-id="0e5c7-126">255</span></span> | <span data-ttu-id="0e5c7-127">MS-DOS 應用程式通常會顯示的擴充字元。</span><span class="sxs-lookup"><span data-stu-id="0e5c7-127">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="0e5c7-128">如需其他字元集值，請參閱 Platform SDK 檔集。</span><span class="sxs-lookup"><span data-stu-id="0e5c7-128">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="0e5c7-129">字元字提示字元中使用的預設字元集是在 Microsoft Agent 字元編輯器中定義。</span><span class="sxs-lookup"><span data-stu-id="0e5c7-129">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="0e5c7-130">您可以使用 [**IAgentBalloon：： SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**)來變更它。</span><span class="sxs-lookup"><span data-stu-id="0e5c7-130">You can change it with [**IAgentBalloon::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span></span> <span data-ttu-id="0e5c7-131">不過，使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字元集設定。</span><span class="sxs-lookup"><span data-stu-id="0e5c7-131">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="0e5c7-132">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="0e5c7-132">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e5c7-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e5c7-133">See Also</span></span>

[<span data-ttu-id="0e5c7-134">**IAgentBalloon::GetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="0e5c7-134">**IAgentBalloon::GetFontCharSet**</span></span>](iagentballoon--getfontcharset.md)


 

 




