---
title: 評等
description: 評等
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Windows Media Player 行動外觀、評等
- 外觀、評等
- 外觀、評等的參考
- 外觀中的評等
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb90908c725fcb525e0be1547c27c588a4220c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969474"
---
# <a name="ratings"></a><span data-ttu-id="f0756-107">評等</span><span class="sxs-lookup"><span data-stu-id="f0756-107">Ratings</span></span>

<span data-ttu-id="f0756-108">當您建立適用于 Windows Media Player 10.1 行動裝置的面板時，您可以顯示與目前現正播放之以 Windows Media 音訊為基礎的內容相關聯的評等。</span><span class="sxs-lookup"><span data-stu-id="f0756-108">When you create a skin for Windows Media Player 10.1 Mobile, you can display the rating associated with Windows Media Audio-based content that is currently playing.</span></span> <span data-ttu-id="f0756-109">評等會顯示為星號，其中有一個數位。</span><span class="sxs-lookup"><span data-stu-id="f0756-109">The rating is displayed as a star with a number on it.</span></span> <span data-ttu-id="f0756-110">星號將會從1到5編號，表示該內容目前的評等。</span><span class="sxs-lookup"><span data-stu-id="f0756-110">The star will be numbered one through five, denoting the current rating for that content.</span></span> <span data-ttu-id="f0756-111">如果內容未分級，星號將會以零為數字。</span><span class="sxs-lookup"><span data-stu-id="f0756-111">If the content is not rated, the star will be numbered zero.</span></span>

<span data-ttu-id="f0756-112">面板定義檔的 [評等] 區段開頭為以下這一行：</span><span class="sxs-lookup"><span data-stu-id="f0756-112">The Ratings section of the skin definition file begins with this line:</span></span>


```C++
[ Ratings ]

```



<span data-ttu-id="f0756-113">然後，您必須在面板中新增包含評等圖示大小和位置相關資訊的行。</span><span class="sxs-lookup"><span data-stu-id="f0756-113">You then must add a line that contains information about the size and location of your ratings icon in your skin.</span></span>


```C++
147, 3, 22, 21       ratings96S.gif

```



<span data-ttu-id="f0756-114">您可以使用下列範本作為面板定義檔的評等區段：</span><span class="sxs-lookup"><span data-stu-id="f0756-114">You can use the following template for the Ratings section of your skin definition file:</span></span>


```C++
// <Location>           <Image>
// ---------------      --------------------
```



<span data-ttu-id="f0756-115">您也可以透過 Windows Media Player 10.1 行動裝置中的使用者介面，將分級值指派給媒體專案，並在裝置下次與電腦進行同步處理時，將新的分級值傳播至該媒體專案，如果該媒體專案位於 Windows Media Player 10 程式庫中。</span><span class="sxs-lookup"><span data-stu-id="f0756-115">You can also assign a ratings value to a media item through the user interface in Windows Media Player 10.1 Mobile, and the next time the device synchronizes with the a computer, the new ratings value will be propagated to that media item if it resides in the Windows Media Player 10 library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0756-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0756-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0756-117">**外觀參考**</span><span class="sxs-lookup"><span data-stu-id="f0756-117">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




