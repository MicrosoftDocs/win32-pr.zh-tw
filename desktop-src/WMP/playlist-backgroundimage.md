---
title: 播放清單。 backgroundImage
description: BackgroundImage 屬性會指定或抓取背景影像。
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- 播放清單. backgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eca04f47f6e157d5ede529c47fb6ae65b4333cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995944"
---
# <a name="playlistbackgroundimage"></a><span data-ttu-id="926ba-104">播放清單。 backgroundImage</span><span class="sxs-lookup"><span data-stu-id="926ba-104">PLAYLIST.backgroundImage</span></span>

<span data-ttu-id="926ba-105">**BackgroundImage** 屬性會指定或抓取背景影像。</span><span class="sxs-lookup"><span data-stu-id="926ba-105">The **backgroundImage** attribute specifies or retrieves the background image.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="926ba-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="926ba-106">Possible Values</span></span>

<span data-ttu-id="926ba-107">這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="926ba-107">This attribute is a read/write **String** containing the name of an image file.</span></span> <span data-ttu-id="926ba-108">它沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="926ba-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="926ba-109">備註</span><span class="sxs-lookup"><span data-stu-id="926ba-109">Remarks</span></span>

<span data-ttu-id="926ba-110">如果影像的高度和寬度小於 **播放清單** 元素的高度和寬度，則會將影像並排顯示。</span><span class="sxs-lookup"><span data-stu-id="926ba-110">If the image height and width are smaller than the height and width of the **PLAYLIST** element, the image is tiled.</span></span> <span data-ttu-id="926ba-111">支援的格式為 BMP、JPG、GIF 和 PNG。</span><span class="sxs-lookup"><span data-stu-id="926ba-111">The supported formats are BMP, JPG, GIF and PNG.</span></span>

<span data-ttu-id="926ba-112">針對背景影像指定 "漸層" 的值，會導致播放清單的背景顯示為色彩漸層。</span><span class="sxs-lookup"><span data-stu-id="926ba-112">Specifying a value of "gradient" for the background image causes the background of the playlist to display as a color gradient.</span></span> <span data-ttu-id="926ba-113">這表示背景色彩會在 [backgroundColor](playlist-backgroundcolor.md) (于背景) 和 [播放清單. statusColor](playlist-statuscolor.md) 值的上方逐漸轉換。</span><span class="sxs-lookup"><span data-stu-id="926ba-113">This means the background color gradually transitions between the [PLAYLIST.backgroundColor](playlist-backgroundcolor.md) (at the top of the background) and [PLAYLIST.statusColor](playlist-statuscolor.md) values.</span></span>

## <a name="requirements"></a><span data-ttu-id="926ba-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="926ba-114">Requirements</span></span>



| <span data-ttu-id="926ba-115">需求</span><span class="sxs-lookup"><span data-stu-id="926ba-115">Requirement</span></span> | <span data-ttu-id="926ba-116">值</span><span class="sxs-lookup"><span data-stu-id="926ba-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="926ba-117">版本</span><span class="sxs-lookup"><span data-stu-id="926ba-117">Version</span></span><br/> | <span data-ttu-id="926ba-118">Windows Media Player 7.0 版或更新版本，漸層功能的 Windows Media Player 10</span><span class="sxs-lookup"><span data-stu-id="926ba-118">Windows Media Player version 7.0 or later, Windows Media Player 10 for the gradient feature</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="926ba-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="926ba-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="926ba-120">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="926ba-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





