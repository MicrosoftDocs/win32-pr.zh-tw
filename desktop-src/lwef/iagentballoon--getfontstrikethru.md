---
title: IAgentBalloon GetFontStrikethru
description: IAgentBalloon GetFontStrikethru
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2001ec0125949144843d500f125b3502e94723db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372598"
---
# <a name="iagentballoongetfontstrikethru"></a><span data-ttu-id="0b200-103">IAgentBalloon::GetFontStrikethru</span><span class="sxs-lookup"><span data-stu-id="0b200-103">IAgentBalloon::GetFontStrikethru</span></span>

<span data-ttu-id="0b200-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="0b200-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontStrikethru(
   long * pbFontStrikethru  // address of variable for strikethrough setting 
);                          // for font displayed in word balloon 
```

<span data-ttu-id="0b200-105">指出文字氣球中使用的字型是否已設定刪除線樣式。</span><span class="sxs-lookup"><span data-stu-id="0b200-105">Indicates whether the font used in a word balloon has the strikethrough style set.</span></span>

-   <span data-ttu-id="0b200-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="0b200-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0b200-107"><span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*</span><span class="sxs-lookup"><span data-stu-id="0b200-107"><span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*</span></span>
</dt> <dd>

<span data-ttu-id="0b200-108">如果已設定字型刪除線樣式，值的位址會收到 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="0b200-108">The address of a value that receives **True** if the font strikethrough style is set and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="0b200-109">字元字提示字元中使用的字型樣式是在 Microsoft Agent 字元編輯器中定義。</span><span class="sxs-lookup"><span data-stu-id="0b200-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="0b200-110">應用程式無法變更它。</span><span class="sxs-lookup"><span data-stu-id="0b200-110">It cannot be changed by an application.</span></span> <span data-ttu-id="0b200-111">不過，使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字型設定。</span><span class="sxs-lookup"><span data-stu-id="0b200-111">However, the user can override the font settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




