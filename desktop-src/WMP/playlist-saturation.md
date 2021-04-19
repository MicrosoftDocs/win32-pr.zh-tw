---
title: 播放清單。飽和度
description: 飽和度屬性會指定或抓取下拉式影像的飽和度值。
ms.assetid: 4c5dd3d9-828a-45c9-896a-9a702d354544
keywords:
- 播放清單。飽和度 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eb53afeafb0754f0e754f68fd5ff785eaade8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982573"
---
# <a name="playlistsaturation"></a><span data-ttu-id="58d28-104">播放清單。飽和度</span><span class="sxs-lookup"><span data-stu-id="58d28-104">PLAYLIST.saturation</span></span>

<span data-ttu-id="58d28-105">**飽和度** 屬性會指定或抓取下拉式影像的飽和度值。</span><span class="sxs-lookup"><span data-stu-id="58d28-105">The **saturation** attribute specifies or retrieves the saturation value of the drop-down images.</span></span>

``` syntax
        elementID.saturation
```

## <a name="possible-values"></a><span data-ttu-id="58d28-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="58d28-106">Possible Values</span></span>

<span data-ttu-id="58d28-107">這個屬性是一個讀/寫 **編號** (**float**) ，其值範圍從0.0 到2.0，預設值為1.0。</span><span class="sxs-lookup"><span data-stu-id="58d28-107">This attribute is a read/write **Number** (**float**) with a value ranging from 0.0 to 2.0 with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="58d28-108">備註</span><span class="sxs-lookup"><span data-stu-id="58d28-108">Remarks</span></span>

<span data-ttu-id="58d28-109">這個屬性會變更 **dropDownBackgroundImage** 和 **dropDownImage** 屬性所指定之影像的飽和度值（如果已指定），而且它們參考的是8位的 BMP 影像。</span><span class="sxs-lookup"><span data-stu-id="58d28-109">This attribute changes the saturation value of the images specified by the **dropDownBackgroundImage** and **dropDownImage** attributes if they have been specified and they refer to 8-bit BMP images.</span></span>

## <a name="requirements"></a><span data-ttu-id="58d28-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="58d28-110">Requirements</span></span>



| <span data-ttu-id="58d28-111">需求</span><span class="sxs-lookup"><span data-stu-id="58d28-111">Requirement</span></span> | <span data-ttu-id="58d28-112">值</span><span class="sxs-lookup"><span data-stu-id="58d28-112">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="58d28-113">版本</span><span class="sxs-lookup"><span data-stu-id="58d28-113">Version</span></span><br/> | <span data-ttu-id="58d28-114">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="58d28-114">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58d28-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58d28-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58d28-116">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="58d28-116">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="58d28-117">**播放清單。 dropDownBackgroundImage**</span><span class="sxs-lookup"><span data-stu-id="58d28-117">**PLAYLIST.dropDownBackgroundImage**</span></span>](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[<span data-ttu-id="58d28-118">**播放清單。 dropDownImage**</span><span class="sxs-lookup"><span data-stu-id="58d28-118">**PLAYLIST.dropDownImage**</span></span>](playlist-dropdownimage.md)
</dt> <dt>

[<span data-ttu-id="58d28-119">**播放清單。 hueShift**</span><span class="sxs-lookup"><span data-stu-id="58d28-119">**PLAYLIST.hueShift**</span></span>](playlist-hueshift.md)
</dt> </dl>

 

 





