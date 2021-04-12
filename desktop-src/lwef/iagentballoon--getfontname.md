---
title: IAgentBalloon GetFontName
description: IAgentBalloon GetFontName
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f29ad981fb4b10249b17e55c92fb286552eedc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372600"
---
# <a name="iagentballoongetfontname"></a><span data-ttu-id="592a7-103">IAgentBalloon::GetFontName</span><span class="sxs-lookup"><span data-stu-id="592a7-103">IAgentBalloon::GetFontName</span></span>

<span data-ttu-id="592a7-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="592a7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in word balloon
```

<span data-ttu-id="592a7-105">抓取文字氣球中所顯示字型的值。</span><span class="sxs-lookup"><span data-stu-id="592a7-105">Retrieves the value for the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="592a7-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="592a7-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="592a7-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span><span class="sxs-lookup"><span data-stu-id="592a7-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="592a7-108">接收文字氣球中所顯示字型名稱的 BSTR 位址。</span><span class="sxs-lookup"><span data-stu-id="592a7-108">The address of a BSTR that receives the font name displayed in a word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="592a7-109">在「Microsoft 代理程式字元編輯器」中定義字元字提示字元中使用的預設字型。</span><span class="sxs-lookup"><span data-stu-id="592a7-109">The default font used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="592a7-110">您可以使用 [**IAgentBalloon：： SetFontName**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**)來變更它。</span><span class="sxs-lookup"><span data-stu-id="592a7-110">You can change it with [**IAgentBalloon::SetFontName**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**).</span></span> <span data-ttu-id="592a7-111">使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字型設定。</span><span class="sxs-lookup"><span data-stu-id="592a7-111">The user can override the font setting for all characters using the Microsoft Agent property sheet.</span></span>

 

 




