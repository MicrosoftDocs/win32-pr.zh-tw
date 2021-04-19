---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6202aa144d13c3c7435be03721a3f8fd4878b93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106978568"
---
# <a name="iagentballoonsetfontcharset"></a><span data-ttu-id="50eb9-103">IAgentBalloon::SetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="50eb9-103">IAgentBalloon::SetFontCharSet</span></span>

<span data-ttu-id="50eb9-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="50eb9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="50eb9-105">設定文字氣球中所顯示字型的字元集。</span><span class="sxs-lookup"><span data-stu-id="50eb9-105">Sets the character set of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="50eb9-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="50eb9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="50eb9-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="50eb9-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="50eb9-108">字型的字元集。</span><span class="sxs-lookup"><span data-stu-id="50eb9-108">The character set of the font.</span></span> <span data-ttu-id="50eb9-109">以下是一些常見的值設定：</span><span class="sxs-lookup"><span data-stu-id="50eb9-109">The following are some common settings for value:</span></span>



|     |                                                                                        |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50eb9-110">0</span><span class="sxs-lookup"><span data-stu-id="50eb9-110">0</span></span>   | <span data-ttu-id="50eb9-111">標準 Windows 字元 (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="50eb9-111">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="50eb9-112">1</span><span class="sxs-lookup"><span data-stu-id="50eb9-112">1</span></span>   | <span data-ttu-id="50eb9-113">預設字元集。</span><span class="sxs-lookup"><span data-stu-id="50eb9-113">Default character set.</span></span>                                                                 |
| <span data-ttu-id="50eb9-114">2</span><span class="sxs-lookup"><span data-stu-id="50eb9-114">2</span></span>   | <span data-ttu-id="50eb9-115">符號字元集。</span><span class="sxs-lookup"><span data-stu-id="50eb9-115">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="50eb9-116">128</span><span class="sxs-lookup"><span data-stu-id="50eb9-116">128</span></span> | <span data-ttu-id="50eb9-117">在日文版的 Windows 中，雙位元組字元集 (DBCS) 是唯一的。</span><span class="sxs-lookup"><span data-stu-id="50eb9-117">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="50eb9-118">129</span><span class="sxs-lookup"><span data-stu-id="50eb9-118">129</span></span> | <span data-ttu-id="50eb9-119">雙位元組字集 (DBCS) Windows 的韓文版本是唯一的。</span><span class="sxs-lookup"><span data-stu-id="50eb9-119">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="50eb9-120">134</span><span class="sxs-lookup"><span data-stu-id="50eb9-120">134</span></span> | <span data-ttu-id="50eb9-121">雙位元組字集 (DBCS) Windows 的簡體中文版本獨有。</span><span class="sxs-lookup"><span data-stu-id="50eb9-121">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="50eb9-122">136</span><span class="sxs-lookup"><span data-stu-id="50eb9-122">136</span></span> | <span data-ttu-id="50eb9-123">雙位元組字集 (DBCS) Windows 的唯一版本。</span><span class="sxs-lookup"><span data-stu-id="50eb9-123">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="50eb9-124">255</span><span class="sxs-lookup"><span data-stu-id="50eb9-124">255</span></span> | <span data-ttu-id="50eb9-125">MS-DOS 應用程式通常會顯示的擴充字元。</span><span class="sxs-lookup"><span data-stu-id="50eb9-125">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="50eb9-126">如需其他字元集值，請參閱 Platform SDK 檔集。</span><span class="sxs-lookup"><span data-stu-id="50eb9-126">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="50eb9-127">字元字提示字元中使用的預設字元集是在 Microsoft Agent 字元編輯器中定義。</span><span class="sxs-lookup"><span data-stu-id="50eb9-127">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="50eb9-128">您可以使用 [**IAgentBalloon：： SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**)來變更它。</span><span class="sxs-lookup"><span data-stu-id="50eb9-128">You can change it with [**IAgentBalloon::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span></span> <span data-ttu-id="50eb9-129">不過，使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字元集設定。</span><span class="sxs-lookup"><span data-stu-id="50eb9-129">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="50eb9-130">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="50eb9-130">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="50eb9-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50eb9-131">See Also</span></span>

[<span data-ttu-id="50eb9-132">**IAgentBalloon::GetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="50eb9-132">**IAgentBalloon::GetFontCharSet**</span></span>](iagentballoon--getfontcharset.md)


 

 




