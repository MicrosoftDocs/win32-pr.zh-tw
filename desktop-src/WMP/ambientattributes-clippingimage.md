---
title: AmbientAttributes.clippingImage
description: ClippingImage 屬性會指定或抓取要裁剪控制項的區域。
ms.assetid: e4b51d31-f9c7-4398-983d-95867a2cab45
keywords:
- AmbientAttributes. clippingImage Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e05e05ca9c7c3efdf842ffd4297da6f9fee035d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000918"
---
# <a name="ambientattributesclippingimage"></a><span data-ttu-id="ee014-104">AmbientAttributes.clippingImage</span><span class="sxs-lookup"><span data-stu-id="ee014-104">AmbientAttributes.clippingImage</span></span>

<span data-ttu-id="ee014-105">**ClippingImage** 屬性會指定或抓取要裁剪控制項的區域。</span><span class="sxs-lookup"><span data-stu-id="ee014-105">The **clippingImage** attribute specifies or retrieves the region to clip the control to.</span></span>

``` syntax
        elementID.clippingImage
```

## <a name="possible-values"></a><span data-ttu-id="ee014-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="ee014-106">Possible Values</span></span>

<span data-ttu-id="ee014-107">這個屬性是讀取/寫入 **字串** ，表示影像檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="ee014-107">This attribute is a read/write **String** indicating the image file name.</span></span> <span data-ttu-id="ee014-108">它沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="ee014-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee014-109">備註</span><span class="sxs-lookup"><span data-stu-id="ee014-109">Remarks</span></span>

<span data-ttu-id="ee014-110">**ClippingImage** 屬性支援 PNG、JPG、BMP 和 GIF 檔案 (不包括動畫 gif) 。</span><span class="sxs-lookup"><span data-stu-id="ee014-110">The **clippingImage** attribute supports PNG, JPG, BMP, and GIF files (not including animated GIFs).</span></span> <span data-ttu-id="ee014-111">由於 Jpg 是有損耗的，因此可能會發生非預期的色彩變更，因此不建議將影像裁剪。</span><span class="sxs-lookup"><span data-stu-id="ee014-111">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended for clipping images.</span></span>

<span data-ttu-id="ee014-112">當您只想要顯示控制項影像的一部分，而不是整個矩形區域時，這個屬性就很有用。</span><span class="sxs-lookup"><span data-stu-id="ee014-112">This attribute is useful when you want to display only a part of the control image and not the entire rectangular area.</span></span> <span data-ttu-id="ee014-113">**ClippingColor** 屬性指出裁剪影像的區域，其對應至控制項的透明、不可按的部分。</span><span class="sxs-lookup"><span data-stu-id="ee014-113">The **clippingColor** attribute indicates the regions of the clipping image that correspond to transparent, non-clickable portions of the control.</span></span> <span data-ttu-id="ee014-114">因此，控制項可以是任何圖形。</span><span class="sxs-lookup"><span data-stu-id="ee014-114">The control can therefore be of any shape.</span></span> <span data-ttu-id="ee014-115">為了獲得最佳結果，裁剪影像的大小應該與控制項影像相同。</span><span class="sxs-lookup"><span data-stu-id="ee014-115">For best results, the clipping image should be the same size as the control image.</span></span>

<span data-ttu-id="ee014-116">**播放清單**、 **VIEW** 和子 **視圖** 元素不支援 **clippingImage** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ee014-116">The **clippingImage** attribute is not supported by the **PLAYLIST**, **VIEW**, and **SUBVIEW** elements.</span></span> <span data-ttu-id="ee014-117">如果 *影片*，裁剪影像將無法搭配 **video** 元素使用。[**無視窗**] 會設定為 false，而效果元素 *則會* 設定為 [**效果**]。**視窗** 設定為 true。</span><span class="sxs-lookup"><span data-stu-id="ee014-117">A clipping image will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if *EFFECTS*.**windowed** is set to true.</span></span>

<span data-ttu-id="ee014-118">因為裁剪影像的使用會影響效能，所以不應在效率為問題時使用。</span><span class="sxs-lookup"><span data-stu-id="ee014-118">Because the use of clipping images imposes a performance penalty, they should not be used when efficiency is an issue.</span></span>

## <a name="examples"></a><span data-ttu-id="ee014-119">範例</span><span class="sxs-lookup"><span data-stu-id="ee014-119">Examples</span></span>

<span data-ttu-id="ee014-120">如需說明如何使用此屬性的範例，請參閱 [BUTTONELEMENT mappingColor](buttonelement-mappingcolor.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="ee014-120">See the [BUTTONELEMENT.mappingColor](buttonelement-mappingcolor.md) attribute for a sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee014-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee014-121">Requirements</span></span>



| <span data-ttu-id="ee014-122">需求</span><span class="sxs-lookup"><span data-stu-id="ee014-122">Requirement</span></span> | <span data-ttu-id="ee014-123">值</span><span class="sxs-lookup"><span data-stu-id="ee014-123">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ee014-124">版本</span><span class="sxs-lookup"><span data-stu-id="ee014-124">Version</span></span><br/> | <span data-ttu-id="ee014-125">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="ee014-125">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee014-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee014-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee014-127">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="ee014-127">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="ee014-128">**AmbientAttributes.clippingColor**</span><span class="sxs-lookup"><span data-stu-id="ee014-128">**AmbientAttributes.clippingColor**</span></span>](ambientattributes-clippingcolor.md)
</dt> </dl>

 

 





