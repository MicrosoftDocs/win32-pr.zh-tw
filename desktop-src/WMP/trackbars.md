---
title: Trackbars
description: Trackbars
ms.assetid: b9676697-c3ab-465c-8b50-eb784f53bb11
keywords:
- Windows Media Player 行動外觀 trackbars
- 外觀，trackbars
- 外觀的參考，trackbars
- 外觀 trackbars，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb7b64f7bada6f927b25aeecb71d584aa1ec2a68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968245"
---
# <a name="trackbars"></a><span data-ttu-id="fcae7-107">Trackbars</span><span class="sxs-lookup"><span data-stu-id="fcae7-107">Trackbars</span></span>

<span data-ttu-id="fcae7-108">[修訂] 會以較小的增量顯示影像。</span><span class="sxs-lookup"><span data-stu-id="fcae7-108">A trackbar displays an image that changes in small increments.</span></span> <span data-ttu-id="fcae7-109">Trackbars 用於音量控制項和播放位置控制項。</span><span class="sxs-lookup"><span data-stu-id="fcae7-109">Trackbars are used for volume controls and playback position controls.</span></span> <span data-ttu-id="fcae7-110">您可以使用 trackbars 顯示目前媒體專案的資訊，或允許使用者變更設定或播放位置。</span><span class="sxs-lookup"><span data-stu-id="fcae7-110">You can use trackbars to display information about the current media item or to allow the user to change settings or playback position.</span></span> <span data-ttu-id="fcae7-111">例如，您可以使用 [顯示] 來讓使用者調整音量，並使用另一個可向使用者顯示目前播放位置的顯示。</span><span class="sxs-lookup"><span data-stu-id="fcae7-111">For example, you can use a trackbar to enable the user to adjust the volume, and another trackbar that can show the user the current playback position.</span></span> <span data-ttu-id="fcae7-112">Trackbars 有一個 thumb 影像，可定義目前的 [程式] 值的設定。</span><span class="sxs-lookup"><span data-stu-id="fcae7-112">Trackbars have a thumb image that defines the current setting of the trackbar value.</span></span>

<span data-ttu-id="fcae7-113">面板定義檔的 Trackbars 區段必須以這一行開頭：</span><span class="sxs-lookup"><span data-stu-id="fcae7-113">The Trackbars section of the skin definition file must begin with this line:</span></span>


```C++
[ Trackbars ]

```



<span data-ttu-id="fcae7-114">然後，您必須新增一或多行，其中包含面板中每個 trackbars 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fcae7-114">You then must add one or more lines that contain information about each of the trackbars in your skin.</span></span>


```C++
    Seek        5,25,226,17    Disabled @ 4,1      SeekThumb.bmp      18,17
    Volume      32,220,172,23  Disabled @ 32,27    VolumeThumb.bmp    23,22

```



<span data-ttu-id="fcae7-115">您可以使用下列範本作為面板定義檔的 Trackbars 區段：</span><span class="sxs-lookup"><span data-stu-id="fcae7-115">You can use the following template for the Trackbars section of your skin definition file:</span></span>


```C++
//  <Type> <Location>     <Dis Image Src> <Thumb Image Src> <Thumb Size>
//  ------ ----------     --------------- ----------------- ------------

```



<span data-ttu-id="fcae7-116">您必須在 Trackbars 區段中，針對每一行的資料列資訊使用下列順序， (行的每個部分都必須) ：</span><span class="sxs-lookup"><span data-stu-id="fcae7-116">You must use the following order for trackbar information for each line in the Trackbars section (each part of the line is required):</span></span>

1.  <span data-ttu-id="fcae7-117">[[類型]](trackbar-type.md)</span><span class="sxs-lookup"><span data-stu-id="fcae7-117">[Trackbar Type](trackbar-type.md)</span></span>
2.  [<span data-ttu-id="fcae7-118">進行中的位置</span><span class="sxs-lookup"><span data-stu-id="fcae7-118">Trackbar Location</span></span>](trackbar-location.md)
3.  [<span data-ttu-id="fcae7-119">已停用之跟蹤的影像來源</span><span class="sxs-lookup"><span data-stu-id="fcae7-119">Image Source for Disabled Trackbar</span></span>](image-source-for-disabled-trackbar.md)
4.  [<span data-ttu-id="fcae7-120">Thumb 影像來源</span><span class="sxs-lookup"><span data-stu-id="fcae7-120">Thumb Image Source</span></span>](thumb-image-source.md)
5.  [<span data-ttu-id="fcae7-121">捲動方塊大小</span><span class="sxs-lookup"><span data-stu-id="fcae7-121">Thumb Size</span></span>](thumb-size.md)

<span data-ttu-id="fcae7-122">如需 Trackbars 程式碼的範例，請參閱 [範例 Trackbars 一節](sample-trackbars-section.md)。</span><span class="sxs-lookup"><span data-stu-id="fcae7-122">For an example of Trackbars code, see [Sample Trackbars Section](sample-trackbars-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcae7-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="fcae7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcae7-124">**外觀參考**</span><span class="sxs-lookup"><span data-stu-id="fcae7-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




