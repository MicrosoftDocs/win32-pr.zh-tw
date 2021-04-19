---
title: '影片 (Windows Media Player SDK) '
description: 影片
ms.assetid: 3c654494-19b5-401e-bed8-02f7cc7d7f4e
keywords:
- Windows Media Player 行動外觀、影片
- 外觀、影片
- 外觀、影片的參考
- 外觀影片，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d505acec3f6917c7ed3d182c656ff5e9f29f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106994968"
---
# <a name="video-windows-media-player-sdk"></a><span data-ttu-id="4a92f-107">影片 (Windows Media Player SDK) </span><span class="sxs-lookup"><span data-stu-id="4a92f-107">Video (Windows Media Player SDK)</span></span>

<span data-ttu-id="4a92f-108">影片顯示器可讓使用者查看數位視訊檔案。</span><span class="sxs-lookup"><span data-stu-id="4a92f-108">A video display allows the user to view digital video files.</span></span> <span data-ttu-id="4a92f-109">只有當影片現正播放或暫停時，才會顯示影片顯示區域。</span><span class="sxs-lookup"><span data-stu-id="4a92f-109">The video display area is only visible when video is playing or paused.</span></span> <span data-ttu-id="4a92f-110">當您設計面板時，您會想要在背景影像中保留空間，以包含影片顯示。</span><span class="sxs-lookup"><span data-stu-id="4a92f-110">When you design your skin, you will want to reserve space in the Background image to contain the video display.</span></span> <span data-ttu-id="4a92f-111">如果您沒有這麼做，則影片顯示器可能會顯示在任何可見的圖片上，例如背景檔案、按鈕和 trackbars，這會讓使用者無法操作您面板上的控制項。</span><span class="sxs-lookup"><span data-stu-id="4a92f-111">If you don't, the video display may superimpose itself over any visible art, such as the Background file, buttons, and trackbars, which will keep the user from operating the controls on your skin.</span></span>

<span data-ttu-id="4a92f-112">面板定義檔的 [影片] 區段必須以以下這一行開頭：</span><span class="sxs-lookup"><span data-stu-id="4a92f-112">The Video section of the skin definition file must begin with this line:</span></span>


```C++
[ Video ]

```



<span data-ttu-id="4a92f-113">然後，您必須加入一行，以指定面板中影片顯示區域的位置和大小。</span><span class="sxs-lookup"><span data-stu-id="4a92f-113">You then must add a line that specifies the location and size of the video display area in your skin.</span></span>


```C++
0,38,240,172

```



<span data-ttu-id="4a92f-114">您可以使用下列範本作為面板定義檔的影片區段：</span><span class="sxs-lookup"><span data-stu-id="4a92f-114">You can use the following template for the Video section of your skin definition file:</span></span>


```C++
//  <Location>
//  ----------

```



<span data-ttu-id="4a92f-115">下列各節提供進一步的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4a92f-115">The following sections provide further details.</span></span>

-   [<span data-ttu-id="4a92f-116">影片位置</span><span class="sxs-lookup"><span data-stu-id="4a92f-116">Video Location</span></span>](video-location.md)
-   [<span data-ttu-id="4a92f-117">影片影像來源</span><span class="sxs-lookup"><span data-stu-id="4a92f-117">Video Image Source</span></span>](video-image-source.md)
-   [<span data-ttu-id="4a92f-118">影片大小</span><span class="sxs-lookup"><span data-stu-id="4a92f-118">Video Size</span></span>](video-size.md)
-   [<span data-ttu-id="4a92f-119">範例影片區段</span><span class="sxs-lookup"><span data-stu-id="4a92f-119">Sample Video Section</span></span>](sample-video-section.md)

## <a name="related-topics"></a><span data-ttu-id="4a92f-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="4a92f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a92f-121">**外觀參考**</span><span class="sxs-lookup"><span data-stu-id="4a92f-121">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




