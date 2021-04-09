---
title: 天棚區段
description: 天棚區段
ms.assetid: ff48c922-e6fc-4ba2-89ad-dcb34be0fea5
keywords:
- Windows Media Player 行動外觀、字幕
- 外觀、字幕
- 建立外觀、天棚區段
- 撰寫面板的程式碼，天棚區段
- 外觀、字幕區段中的字幕
- 外觀定義檔，天棚區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf92a9f8ba3c1ca34559d355801d74ba6ed6382
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675879"
---
# <a name="marquee-section"></a><span data-ttu-id="12935-109">天棚區段</span><span class="sxs-lookup"><span data-stu-id="12935-109">Marquee Section</span></span>

<span data-ttu-id="12935-110">[字幕] 區段包含 [字幕] 文字方塊的相關資訊，此文字方塊將會顯示滾動文字：</span><span class="sxs-lookup"><span data-stu-id="12935-110">The Marquee section contains information about the marquee text box, which will display scrolling text:</span></span>


```C++
[ Marquee ]

//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------
    100,150,100,20   Tahoma,12,N  255,0,0    Title+Author, Author, Title

```



<span data-ttu-id="12935-111">這會顯示目前媒體專案的標題和作者，雖然您可以在字幕中顯示任何文字類型。</span><span class="sxs-lookup"><span data-stu-id="12935-111">This will display the title and author of the current media item although you can display any text type in the marquee.</span></span> <span data-ttu-id="12935-112">例如，您也可以在字幕中包含檔案名、狀態和播放清單。</span><span class="sxs-lookup"><span data-stu-id="12935-112">For example, you could also include Filename, Status, and Playlist in your marquee.</span></span>

> [!Note]  
> <span data-ttu-id="12935-113">若要維持與 Windows Media Player 10 行動裝置版 Windows Media Player Mobile 的相容性，在面板定義檔中使用 "Marquis" 仍會被視為有效。</span><span class="sxs-lookup"><span data-stu-id="12935-113">To maintain compatibility with versions of Windows Media Player Mobile older than Windows Media Player 10 Mobile, using "Marquis" in a skin definition file is still considered valid.</span></span>

 

<span data-ttu-id="12935-114">如需 [字幕] 區段的詳細資訊，請參閱面板參考中的 [[字幕]](marquee.md) 。</span><span class="sxs-lookup"><span data-stu-id="12935-114">For more about the Marquee section, see [Marquee](marquee.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12935-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="12935-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12935-116">**撰寫程式碼**</span><span class="sxs-lookup"><span data-stu-id="12935-116">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




