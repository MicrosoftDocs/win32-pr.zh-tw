---
title: 範例天棚區段
description: 範例天棚區段
ms.assetid: 44ed3257-2e1a-4b8d-9d55-a13b0400422d
keywords:
- Windows Media Player 行動外觀、字幕
- 外觀、字幕
- 外觀、字幕的參考
- 外觀、字幕區段中的字幕
- 外觀定義檔，天棚區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f66588d81b22051a9289a80c8733d5cfe154bed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462388"
---
# <a name="sample-marquee-section"></a><span data-ttu-id="d7ae0-108">範例天棚區段</span><span class="sxs-lookup"><span data-stu-id="d7ae0-108">Sample Marquee Section</span></span>

<span data-ttu-id="d7ae0-109">下列各行顯示面板定義檔案的一般字幕區段：</span><span class="sxs-lookup"><span data-stu-id="d7ae0-109">The following lines show a typical Marquee section of a skin definition file:</span></span>


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>

//  ----------   ------       -------      ------------------------

    3,2,234,20   Tahoma,12,N  255,0,0    Title+Author, Title, Author


```



<span data-ttu-id="d7ae0-110">這會定義顯示標題和作者的標題和作者（如果兩者都已定義）、只定義標題的標題，或是作者的名稱（如果只定義了作者）。</span><span class="sxs-lookup"><span data-stu-id="d7ae0-110">This defines a marquee display box that shows the title and author if both are defined, the title if only Title is defined, or the name of the author if only Author is defined.</span></span> <span data-ttu-id="d7ae0-111">如果未定義任何專案，則不會顯示任何專案。</span><span class="sxs-lookup"><span data-stu-id="d7ae0-111">If neither is defined, nothing will be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7ae0-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="d7ae0-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7ae0-113">**Marquee**</span><span class="sxs-lookup"><span data-stu-id="d7ae0-113">**Marquee**</span></span>](marquee.md)
</dt> </dl>

 

 




