---
title: 播放清單。 hueShift
description: HueShift 屬性會指定或抓取下拉式影像之色調的位移量。
ms.assetid: 9d4d8b73-527e-43f3-a921-0576b8897918
keywords:
- 播放清單. hueShift Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.hueShift
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e9dbe89989ddd8f02d67ac8f14532b9b1fbf15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982078"
---
# <a name="playlisthueshift"></a><span data-ttu-id="3a8a5-104">播放清單。 hueShift</span><span class="sxs-lookup"><span data-stu-id="3a8a5-104">PLAYLIST.hueShift</span></span>

<span data-ttu-id="3a8a5-105">**HueShift** 屬性會指定或抓取下拉式影像之色調的位移量。</span><span class="sxs-lookup"><span data-stu-id="3a8a5-105">The **hueShift** attribute specifies or retrieves the amount by which the hue of the drop-down images is shifted.</span></span>

``` syntax
        elementID.hueShift
```

## <a name="possible-values"></a><span data-ttu-id="3a8a5-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="3a8a5-106">Possible Values</span></span>

<span data-ttu-id="3a8a5-107">這個屬性是一個讀/寫 **編號** (**float**) ，其值範圍從0.0 到360.0，預設值為0.0。</span><span class="sxs-lookup"><span data-stu-id="3a8a5-107">This attribute is a read/write **Number** (**float**) with a value ranging from 0.0 to 360.0 with a default value of 0.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a8a5-108">備註</span><span class="sxs-lookup"><span data-stu-id="3a8a5-108">Remarks</span></span>

<span data-ttu-id="3a8a5-109">這個屬性會變更 **dropDownBackgroundImage** 和 **dropDownImage** 屬性所指定之影像的色調值（如果已指定），而且它們參考的是8位的 BMP 影像。</span><span class="sxs-lookup"><span data-stu-id="3a8a5-109">This attribute changes the hue value of the images specified by the **dropDownBackgroundImage** and **dropDownImage** attributes if they have been specified and they refer to 8-bit BMP images.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a8a5-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a8a5-110">Requirements</span></span>



| <span data-ttu-id="3a8a5-111">需求</span><span class="sxs-lookup"><span data-stu-id="3a8a5-111">Requirement</span></span> | <span data-ttu-id="3a8a5-112">值</span><span class="sxs-lookup"><span data-stu-id="3a8a5-112">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="3a8a5-113">版本</span><span class="sxs-lookup"><span data-stu-id="3a8a5-113">Version</span></span><br/> | <span data-ttu-id="3a8a5-114">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="3a8a5-114">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a8a5-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a8a5-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a8a5-116">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="3a8a5-116">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="3a8a5-117">**播放清單。 dropDownBackgroundImage**</span><span class="sxs-lookup"><span data-stu-id="3a8a5-117">**PLAYLIST.dropDownBackgroundImage**</span></span>](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[<span data-ttu-id="3a8a5-118">**播放清單。 dropDownImage**</span><span class="sxs-lookup"><span data-stu-id="3a8a5-118">**PLAYLIST.dropDownImage**</span></span>](playlist-dropdownimage.md)
</dt> <dt>

[<span data-ttu-id="3a8a5-119">**播放清單。飽和度**</span><span class="sxs-lookup"><span data-stu-id="3a8a5-119">**PLAYLIST.saturation**</span></span>](playlist-saturation.md)
</dt> </dl>

 

 





