---
title: 專輯封面
description: 專輯封面
ms.assetid: a5996232-e1ee-41ae-a6ca-f841321644fe
keywords:
- Windows Media Player 行動裝置外觀、專輯封面
- 外觀，專輯封面
- 外觀、專輯封面的參考
- 面板的美工圖案，專輯封面
- 外觀中的專輯封面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0974f8683da98469e75a4472d086dcb1a244c75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967613"
---
# <a name="album-art"></a><span data-ttu-id="78a4d-108">專輯封面</span><span class="sxs-lookup"><span data-stu-id="78a4d-108">Album Art</span></span>

<span data-ttu-id="78a4d-109">當您建立 Windows Media Player 10 行動裝置版或更新版本的面板時，可能會想要顯示與目前播放之媒體專案相關的專輯封面。</span><span class="sxs-lookup"><span data-stu-id="78a4d-109">When you create a skin for Windows Media Player 10 Mobile or later, you may want to display album art that relates to the currently playing media item.</span></span> <span data-ttu-id="78a4d-110">當您設計面板時，您會想要在背景影像中保留空間，以包含專輯封面。</span><span class="sxs-lookup"><span data-stu-id="78a4d-110">When you design your skin, you will want to reserve space in the Background image to contain the album art.</span></span>

<span data-ttu-id="78a4d-111">面板定義檔的專輯封面區段必須以下行開頭：</span><span class="sxs-lookup"><span data-stu-id="78a4d-111">The Album Art section of the skin definition file must begin with the following line:</span></span>


```C++
[ Album Art ]

```



<span data-ttu-id="78a4d-112">然後，您必須新增資訊，以指定面板中專輯封面的位置和大小。</span><span class="sxs-lookup"><span data-stu-id="78a4d-112">You then must add information that specifies the location and size of the album art in your skin.</span></span> <span data-ttu-id="78a4d-113">您必須輸入四個正整數（以逗號分隔），以定義相對於背景影像的專輯封面左邊、頂端、寬度和高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="78a4d-113">You must enter four positive integers, separated by commas that define the left, top, width, and height of the album art, in pixels, relative to the background image.</span></span> <span data-ttu-id="78a4d-114">下列範例顯示如何指定維度：</span><span class="sxs-lookup"><span data-stu-id="78a4d-114">The following example shows how to specify dimensions:</span></span>


```C++
//  <Location>
//  ----------
   5,37,230,155

```



<span data-ttu-id="78a4d-115">如果您計畫在面板中包含影片區段，您可以針對專輯封面使用相同的大小和位置來節省空間。</span><span class="sxs-lookup"><span data-stu-id="78a4d-115">If you plan on including a video section in your skin, you can use the same size and location for your album art to conserve space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78a4d-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="78a4d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78a4d-117">**外觀參考**</span><span class="sxs-lookup"><span data-stu-id="78a4d-117">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




