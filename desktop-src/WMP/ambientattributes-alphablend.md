---
title: AmbientAttributes. AlphaBlend
description: AlphaBlend 屬性會指定或抓取 Alpha 混合任何視圖、子視圖或 UI widget 的值。
ms.assetid: a6c47d32-a497-4bfa-8fa3-ef94e267d94b
keywords:
- AmbientAttributes. AlphaBlend Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlend
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8c0f0cb9d885f643b39acfbc5148403a5c8b788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993603"
---
# <a name="ambientattributesalphablend"></a><span data-ttu-id="34a60-104">AmbientAttributes. AlphaBlend</span><span class="sxs-lookup"><span data-stu-id="34a60-104">AmbientAttributes.alphaBlend</span></span>

<span data-ttu-id="34a60-105">**AlphaBlend** 屬性會指定或抓取 Alpha 混合任何 **視圖**、子 **視圖** 或 UI widget 的值。</span><span class="sxs-lookup"><span data-stu-id="34a60-105">The **alphaBlend** attribute specifies or retrieves a value for alpha blending any **VIEW**, **SUBVIEW**, or UI widget.</span></span>

``` syntax
        elementID.alphaBlend
```

## <a name="possible-values"></a><span data-ttu-id="34a60-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="34a60-106">Possible Values</span></span>

<span data-ttu-id="34a60-107">此屬性是讀取/寫入 **號碼** (**long**) ，其值範圍從 0 (不透明度) 255 (完全不透明度) 和預設值255。</span><span class="sxs-lookup"><span data-stu-id="34a60-107">This attribute is a read/write **Number** (**long**) with a value ranging from 0 (no opacity) to 255 (full opacity) and a default value of 255.</span></span>

## <a name="remarks"></a><span data-ttu-id="34a60-108">備註</span><span class="sxs-lookup"><span data-stu-id="34a60-108">Remarks</span></span>

<span data-ttu-id="34a60-109">這個屬性可讓元素根據不透明度設定的數量，以半透明的形式出現。</span><span class="sxs-lookup"><span data-stu-id="34a60-109">This attribute allows an element to appear semitransparent, depending on the amount of opacity set.</span></span> <span data-ttu-id="34a60-110">不透明度越少，就越透明地顯示元素。</span><span class="sxs-lookup"><span data-stu-id="34a60-110">The less opacity, the more transparent the element will appear.</span></span> <span data-ttu-id="34a60-111">面板中的每個專案都可以有不同的不透明度值，但 **BUTTONGROUP** 控制項中的按鈕元素除外。</span><span class="sxs-lookup"><span data-stu-id="34a60-111">Each element in the skin can have a separate opacity value except for button elements in a **BUTTONGROUP** control.</span></span> <span data-ttu-id="34a60-112">當 [ **AlphaBlend** ] 設定為 [ **VIEW**] 時，將會設定整個外觀的不透明度。</span><span class="sxs-lookup"><span data-stu-id="34a60-112">When **alphaBlend** is set in **VIEW**, the opacity of the entire skin will be set.</span></span> <span data-ttu-id="34a60-113">如果 [**無視窗**] 設定為 [false]) ，Alpha blend 將無法用於視窗型控制項，包括 **播放清單**、**效果**、 **LISTBOX**、 **POPUP**、**編輯方塊** 和 **VIDEO** (。</span><span class="sxs-lookup"><span data-stu-id="34a60-113">Alpha blend will not work for windowed controls, including **PLAYLIST**, **EFFECTS**, **LISTBOX**, **POPUP**, **EDITBOX**, and **VIDEO** (if **windowless** is set to false).</span></span> <span data-ttu-id="34a60-114">當 [ **AlphaBlend** ] 設定為 [ **VIEW**] 時，整個外觀就會變成透明。</span><span class="sxs-lookup"><span data-stu-id="34a60-114">When **alphaBlend** is set on **VIEW**, the whole skin becomes transparent.</span></span> <span data-ttu-id="34a60-115">**AlphaBlend** 不支援數個元素所使用的 **transparencyColor** 屬性。</span><span class="sxs-lookup"><span data-stu-id="34a60-115">The **transparencyColor** attributes used by several elements are not supported with **alphaBlend**.</span></span>

<span data-ttu-id="34a60-116">當您使用 **AlphaBlend** 搭配未指定 **backgroundColor** 的 **TEXT** 元素時，將會使用黑色的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="34a60-116">When you use **alphaBlend** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="34a60-117">如果前景色彩也是黑色 (這是 *文字* 的預設值。**foregroundColor**) ，您的文字可能會變成無法讀取。</span><span class="sxs-lookup"><span data-stu-id="34a60-117">If the foreground color is also black (which is the default value for *TEXT*.**foregroundColor**), your text may become unreadable.</span></span> <span data-ttu-id="34a60-118">若要避免這種情況，請一律指定 **backgroundColor** 屬性，或將 **foregroundColor** 設定為黑色以外的色彩。</span><span class="sxs-lookup"><span data-stu-id="34a60-118">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

> [!Note]  
> <span data-ttu-id="34a60-119">Windows 98 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="34a60-119">This attribute is not supported in Windows 98.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="34a60-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="34a60-120">Requirements</span></span>



| <span data-ttu-id="34a60-121">需求</span><span class="sxs-lookup"><span data-stu-id="34a60-121">Requirement</span></span> | <span data-ttu-id="34a60-122">值</span><span class="sxs-lookup"><span data-stu-id="34a60-122">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="34a60-123">版本</span><span class="sxs-lookup"><span data-stu-id="34a60-123">Version</span></span><br/> | <span data-ttu-id="34a60-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="34a60-124">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34a60-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34a60-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34a60-126">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="34a60-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="34a60-127">**AmbientAttributes.AlphaBlendTo**</span><span class="sxs-lookup"><span data-stu-id="34a60-127">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="34a60-128">**TEXT 元素**</span><span class="sxs-lookup"><span data-stu-id="34a60-128">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="34a60-129">**BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="34a60-129">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="34a60-130">**ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="34a60-130">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





