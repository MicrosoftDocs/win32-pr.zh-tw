---
title: Windows 多媒體) 滑杆 (
description: 滑桿
ms.assetid: cfd82672-5b22-4b59-82b5-15ca68a451fc
keywords:
- 音訊 mixers，控制項
- 音訊 mixers、滑杆
- mixers，控制項
- mixers、滑杆
- 滑桿
- MIXERCONTROLDETAILS_SIGNED 結構
- 平移控制項
- QSound pan 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d7644255e2fa9ee6384cbb5102df81c2a1eb0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383630"
---
# <a name="sliders-windows-multimedia"></a><span data-ttu-id="d24f5-111">Windows 多媒體) 滑杆 (</span><span class="sxs-lookup"><span data-stu-id="d24f5-111">Sliders (Windows Multimedia)</span></span>

<span data-ttu-id="d24f5-112">滑杆控制項通常是可向左或向右調整的水準控制項。</span><span class="sxs-lookup"><span data-stu-id="d24f5-112">The slider controls are typically horizontal controls that can be adjusted to the left or right.</span></span> <span data-ttu-id="d24f5-113">這些控制項使用 [**MIXERCONTROLDETAILS \_ 簽署**](/previous-versions//dd757297(v=vs.85)) 的結構來抓取和設定控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="d24f5-113">These controls use the [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="d24f5-114">下表描述滑杆的類型。</span><span class="sxs-lookup"><span data-stu-id="d24f5-114">The following table describes the types of sliders.</span></span>



| <span data-ttu-id="d24f5-115">控制</span><span class="sxs-lookup"><span data-stu-id="d24f5-115">Control</span></span>    | <span data-ttu-id="d24f5-116">描述</span><span class="sxs-lookup"><span data-stu-id="d24f5-116">Description</span></span>                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d24f5-117">滑桿</span><span class="sxs-lookup"><span data-stu-id="d24f5-117">Slider</span></span>     | <span data-ttu-id="d24f5-118">的範圍為–32768到32767。</span><span class="sxs-lookup"><span data-stu-id="d24f5-118">Has a range of –32,768 through 32,767.</span></span> <span data-ttu-id="d24f5-119">混音器驅動程式會定義此控制項的限制。</span><span class="sxs-lookup"><span data-stu-id="d24f5-119">The mixer driver defines the limits of this control.</span></span>                               |
| <span data-ttu-id="d24f5-120">移動瀏覽</span><span class="sxs-lookup"><span data-stu-id="d24f5-120">Pan</span></span>        | <span data-ttu-id="d24f5-121">的範圍為–32768到32767。</span><span class="sxs-lookup"><span data-stu-id="d24f5-121">Has a range of –32,768 through 32,767.</span></span> <span data-ttu-id="d24f5-122">混音器驅動程式會定義此控制項的限制，並以0作為中型值。</span><span class="sxs-lookup"><span data-stu-id="d24f5-122">The mixer driver defines the limits of this control, with 0 as the midrange value.</span></span> |
| <span data-ttu-id="d24f5-123">QSound Pan</span><span class="sxs-lookup"><span data-stu-id="d24f5-123">QSound Pan</span></span> | <span data-ttu-id="d24f5-124">提供透過 QSound 展開的音效控制項。</span><span class="sxs-lookup"><span data-stu-id="d24f5-124">Provides expanded sound control through QSound.</span></span> <span data-ttu-id="d24f5-125">此控制項的範圍為–15到15。</span><span class="sxs-lookup"><span data-stu-id="d24f5-125">This control has a range of –15 through 15.</span></span>                               |



 

 

 
