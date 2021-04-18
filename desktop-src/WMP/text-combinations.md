---
title: 文字組合
description: 文字組合
ms.assetid: 0220b77e-5f1e-4569-a8fe-5085e0c16338
keywords:
- Windows Media Player 行動外觀、字幕
- 外觀、字幕
- 外觀、字幕的參考
- 外觀、文字組合中的字幕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5668a9e18555b871c82bae7ed1826766ec9429e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507284"
---
# <a name="text-combinations"></a><span data-ttu-id="27a30-107">文字組合</span><span class="sxs-lookup"><span data-stu-id="27a30-107">Text Combinations</span></span>

<span data-ttu-id="27a30-108">此值是文字顯示方塊組合的清單，以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="27a30-108">This value is a list of text display box combinations, separated by commas.</span></span> <span data-ttu-id="27a30-109">文字顯示方塊可透過加號聯結在一起，以建立新的天棚顯示值，而且在 [文字類型] 區段中定義的任何文字類型都可以在您的字幕中使用。</span><span class="sxs-lookup"><span data-stu-id="27a30-109">Text display boxes can be joined together by a plus character to create a new marquee display value and any text type defined in the Text Type section can be used in your marquee.</span></span>

<span data-ttu-id="27a30-110">當您決定要顯示的內容時，Windows Media Player 行動裝置會評估清單中的每個專案，以查看是否有可用的元件。</span><span class="sxs-lookup"><span data-stu-id="27a30-110">When determining what to display, Windows Media Player Mobile evaluates each item in the list to see if all parts are available.</span></span> <span data-ttu-id="27a30-111">如果沒有，則會評估下一個專案，依此類推，直到找到所有可用的部分為止。</span><span class="sxs-lookup"><span data-stu-id="27a30-111">If not, the next item is evaluated, and so on, until all the available parts have been found.</span></span> <span data-ttu-id="27a30-112">例如，如果您想要顯示 [作者] 和 [標題]，但不確定兩者是否可用，請使用下列值：</span><span class="sxs-lookup"><span data-stu-id="27a30-112">For example, if you want to display Author and Title, but you're not sure whether both are available, use the following value:</span></span>


```C++
Title+Author, Title, Author

```



<span data-ttu-id="27a30-113">在上述範例中，如果已針對媒體專案定義標題和作者，則會顯示 [標題 + 作者]。</span><span class="sxs-lookup"><span data-stu-id="27a30-113">In the preceding example, the Title+Author will be displayed if the title and author have been defined for the media item.</span></span> <span data-ttu-id="27a30-114">如果兩者都未定義，則會評估標題，並在已定義時顯示。</span><span class="sxs-lookup"><span data-stu-id="27a30-114">If both are not defined, the Title is evaluated and displayed if defined.</span></span> <span data-ttu-id="27a30-115">如果未定義標題，則會顯示作者（若已定義）。</span><span class="sxs-lookup"><span data-stu-id="27a30-115">If the Title is not defined, the Author is displayed if defined.</span></span> <span data-ttu-id="27a30-116">如果未定義任何專案，則不會顯示任何內容。</span><span class="sxs-lookup"><span data-stu-id="27a30-116">If neither is defined, then nothing is displayed.</span></span>

<span data-ttu-id="27a30-117">使用加號進行串連時，請確定加號的任一邊都沒有空格。</span><span class="sxs-lookup"><span data-stu-id="27a30-117">When using the plus sign for concatenation, be sure you have no spaces on either side of the plus sign.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27a30-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="27a30-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27a30-119">**Marquee**</span><span class="sxs-lookup"><span data-stu-id="27a30-119">**Marquee**</span></span>](marquee.md)
</dt> <dt>

[<span data-ttu-id="27a30-120">**文字類型**</span><span class="sxs-lookup"><span data-stu-id="27a30-120">**Text Type**</span></span>](text-type.md)
</dt> </dl>

 

 




