---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f809fbd83e44259c96184c9f364a85151ec9ddde
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120403"
---
# <a name="iagentballoongetfontcharset"></a><span data-ttu-id="08b6c-103">IAgentBalloon::GetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="08b6c-103">IAgentBalloon::GetFontCharSet</span></span>

<span data-ttu-id="08b6c-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="08b6c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="08b6c-105">指出字型文字提示中所顯示字型的字元集。</span><span class="sxs-lookup"><span data-stu-id="08b6c-105">Indicates the character set of the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="08b6c-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="08b6c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="08b6c-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="08b6c-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="08b6c-108">接收字型字元集之值的位址。</span><span class="sxs-lookup"><span data-stu-id="08b6c-108">The address of a value that receives the font's character set.</span></span> <span data-ttu-id="08b6c-109">以下是一些常見的值設定：</span><span class="sxs-lookup"><span data-stu-id="08b6c-109">The following are some common settings for value:</span></span>



| <span data-ttu-id="08b6c-110">值</span><span class="sxs-lookup"><span data-stu-id="08b6c-110">Value</span></span>    | <span data-ttu-id="08b6c-111">字元集</span><span class="sxs-lookup"><span data-stu-id="08b6c-111">Character set</span></span>                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08b6c-112">0</span><span class="sxs-lookup"><span data-stu-id="08b6c-112">0</span></span>   | <span data-ttu-id="08b6c-113">標準 Windows 字元 (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="08b6c-113">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="08b6c-114">1</span><span class="sxs-lookup"><span data-stu-id="08b6c-114">1</span></span>   | <span data-ttu-id="08b6c-115">預設字元集。</span><span class="sxs-lookup"><span data-stu-id="08b6c-115">Default character set.</span></span>                                                                 |
| <span data-ttu-id="08b6c-116">2</span><span class="sxs-lookup"><span data-stu-id="08b6c-116">2</span></span>   | <span data-ttu-id="08b6c-117">符號字元集。</span><span class="sxs-lookup"><span data-stu-id="08b6c-117">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="08b6c-118">128</span><span class="sxs-lookup"><span data-stu-id="08b6c-118">128</span></span> | <span data-ttu-id="08b6c-119">在日文版的 Windows 中，雙位元組字元集 (DBCS) 是唯一的。</span><span class="sxs-lookup"><span data-stu-id="08b6c-119">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="08b6c-120">129</span><span class="sxs-lookup"><span data-stu-id="08b6c-120">129</span></span> | <span data-ttu-id="08b6c-121">雙位元組字集 (DBCS) Windows 的韓文版本是唯一的。</span><span class="sxs-lookup"><span data-stu-id="08b6c-121">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="08b6c-122">134</span><span class="sxs-lookup"><span data-stu-id="08b6c-122">134</span></span> | <span data-ttu-id="08b6c-123">雙位元組字集 (DBCS) Windows 的簡體中文版本獨有。</span><span class="sxs-lookup"><span data-stu-id="08b6c-123">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="08b6c-124">136</span><span class="sxs-lookup"><span data-stu-id="08b6c-124">136</span></span> | <span data-ttu-id="08b6c-125">雙位元組字集 (DBCS) Windows 的唯一版本。</span><span class="sxs-lookup"><span data-stu-id="08b6c-125">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="08b6c-126">255</span><span class="sxs-lookup"><span data-stu-id="08b6c-126">255</span></span> | <span data-ttu-id="08b6c-127">MS-DOS 應用程式通常會顯示的擴充字元。</span><span class="sxs-lookup"><span data-stu-id="08b6c-127">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="08b6c-128">如需其他字元集值，請參閱 Platform SDK 檔集。</span><span class="sxs-lookup"><span data-stu-id="08b6c-128">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="08b6c-129">字元字提示字元中使用的預設字元集是在 Microsoft Agent 字元編輯器中定義。</span><span class="sxs-lookup"><span data-stu-id="08b6c-129">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="08b6c-130">您可以使用 [**IAgentBalloon：： SetFontCharSet**](iagentballoon--setfontcharset.md)來變更它。</span><span class="sxs-lookup"><span data-stu-id="08b6c-130">You can change it using [**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md).</span></span> <span data-ttu-id="08b6c-131">不過，使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字元集設定。</span><span class="sxs-lookup"><span data-stu-id="08b6c-131">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="08b6c-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08b6c-132">See Also</span></span>

[<span data-ttu-id="08b6c-133">**IAgentBalloon::SetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="08b6c-133">**IAgentBalloon::SetFontCharSet**</span></span>](iagentballoon--setfontcharset.md)


 

 




