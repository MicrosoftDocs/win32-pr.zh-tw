---
title: Marquee
description: Marquee
ms.assetid: 2715732a-25cc-4ba9-9aa6-181ebb9e1d1c
keywords:
- Windows Media Player 行動外觀、字幕
- 外觀、字幕
- 外觀、字幕的參考
- 外觀中的字幕，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efa2db2c6079d47d207240b18a57ebbf7e41ae1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372422"
---
# <a name="marquee"></a><span data-ttu-id="71fdd-107">Marquee</span><span class="sxs-lookup"><span data-stu-id="71fdd-107">Marquee</span></span>

<span data-ttu-id="71fdd-108">[字幕] 是一個滾動文字顯示方塊，可顯示一或多個文字顯示方塊的資訊。</span><span class="sxs-lookup"><span data-stu-id="71fdd-108">A marquee is a scrolling text display box that displays information from one or more text display boxes.</span></span> <span data-ttu-id="71fdd-109">您不需要加入字幕，但是當您有想要在有限空間中顯示給使用者的詳細資訊時，這可能非常有用。</span><span class="sxs-lookup"><span data-stu-id="71fdd-109">You do not need to add a marquee, but it can be very useful when you have detailed information you want to display to the user in a limited space.</span></span>

<span data-ttu-id="71fdd-110">只有在符合下列兩個條件時，才會滾動字幕中的文字：</span><span class="sxs-lookup"><span data-stu-id="71fdd-110">The text in the marquee will scroll only if both of the following conditions are met:</span></span>

-   <span data-ttu-id="71fdd-111">您有比 [字幕] 顯示方塊寬度還多的文字，可顯示在捲動方塊中。</span><span class="sxs-lookup"><span data-stu-id="71fdd-111">You have more text to display in the marquee than the width of the marquee display box.</span></span>
-   <span data-ttu-id="71fdd-112">媒體專案可能已停止或暫停。</span><span class="sxs-lookup"><span data-stu-id="71fdd-112">The media item is either stopped or paused.</span></span>

<span data-ttu-id="71fdd-113">面板定義檔的 [字幕] 區段必須以以下這一行開頭：</span><span class="sxs-lookup"><span data-stu-id="71fdd-113">The Marquee section of the skin definition file must begin with this line:</span></span>


```C++
[ Marquee ]

```



> [!Note]  
> <span data-ttu-id="71fdd-114">若要維持與 Windows Media Player 10 行動裝置版 Windows Media Player Mobile 的相容性，在面板定義檔中使用 "Marquis" 仍會被視為有效。</span><span class="sxs-lookup"><span data-stu-id="71fdd-114">To maintain compatibility with versions of Windows Media Player Mobile older than Windows Media Player 10 Mobile, using "Marquis" in a skin definition file is still considered valid.</span></span>

 

<span data-ttu-id="71fdd-115">然後，您必須新增一或多行，其中包含面板中每個字幕顯示方塊的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71fdd-115">You then must add one or more lines that contain information about each of the marquee display boxes in your skin.</span></span>


```C++
    3,2,234,20   Tahoma,12,N  255,0,0    Playlist, Time, Filename

```



<span data-ttu-id="71fdd-116">您可以使用下列範本作為面板定義檔的 [字幕] 區段：</span><span class="sxs-lookup"><span data-stu-id="71fdd-116">You can use the following template for the Marquee section of your skin definition file:</span></span>


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------

```



<span data-ttu-id="71fdd-117">您必須使用下列順序來取得 [字幕] 區段中每一行的資訊， (行的每個部分都必須) ：</span><span class="sxs-lookup"><span data-stu-id="71fdd-117">You must use the following order for information in each line of the Marquee section (each part of the line is required):</span></span>

1.  [<span data-ttu-id="71fdd-118">天棚位置</span><span class="sxs-lookup"><span data-stu-id="71fdd-118">Marquee Location</span></span>](marquee-location.md)
2.  [<span data-ttu-id="71fdd-119">天棚字型</span><span class="sxs-lookup"><span data-stu-id="71fdd-119">Marquee Font</span></span>](marquee-font.md)
3.  [<span data-ttu-id="71fdd-120">天棚色彩</span><span class="sxs-lookup"><span data-stu-id="71fdd-120">Marquee Color</span></span>](marquee-color.md)
4.  [<span data-ttu-id="71fdd-121">文字組合</span><span class="sxs-lookup"><span data-stu-id="71fdd-121">Text Combinations</span></span>](text-combinations.md)

<span data-ttu-id="71fdd-122">如需字幕程式碼的範例，請參閱 [範例天棚一節](sample-marquee-section.md)。</span><span class="sxs-lookup"><span data-stu-id="71fdd-122">For an example of Marquee code, see [Sample Marquee Section](sample-marquee-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="71fdd-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="71fdd-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71fdd-124">**外觀參考**</span><span class="sxs-lookup"><span data-stu-id="71fdd-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




