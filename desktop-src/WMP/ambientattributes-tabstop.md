---
title: AmbientAttributes
description: TabStop 屬性會指定或抓取值，指出控制項是否為定位順序。 您可以藉由將控制項放在其他控制項標記之前或之後的整體腳本，來設定定位順序。
ms.assetid: 3d4b7fe4-1032-44e1-bae5-f253d00881bf
keywords:
- AmbientAttributes Windows Media Player 的 tabStop
topic_type:
- apiref
api_name:
- AmbientAttributes.tabStop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4005fc26a2bc5f928cde0f5ed67ec2098cf3e6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996039"
---
# <a name="ambientattributestabstop"></a><span data-ttu-id="b0304-105">AmbientAttributes</span><span class="sxs-lookup"><span data-stu-id="b0304-105">AmbientAttributes.tabStop</span></span>

<span data-ttu-id="b0304-106">**TabStop** 屬性會指定或抓取值，指出控制項是否為定位順序。</span><span class="sxs-lookup"><span data-stu-id="b0304-106">The **tabStop** attribute specifies or retrieves a value indicating whether the control is in the tabbing order.</span></span> <span data-ttu-id="b0304-107">您可以藉由將控制項放在其他控制項標記之前或之後的整體腳本，來設定定位順序。</span><span class="sxs-lookup"><span data-stu-id="b0304-107">You set the tabbing order by placing the control in the overall script before or after other control tags.</span></span>

``` syntax
        elementID.tabStop
```

## <a name="possible-values"></a><span data-ttu-id="b0304-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="b0304-108">Possible Values</span></span>

<span data-ttu-id="b0304-109">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="b0304-109">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="b0304-110">值</span><span class="sxs-lookup"><span data-stu-id="b0304-110">Value</span></span> | <span data-ttu-id="b0304-111">描述</span><span class="sxs-lookup"><span data-stu-id="b0304-111">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0304-112">true</span><span class="sxs-lookup"><span data-stu-id="b0304-112">true</span></span>  | <span data-ttu-id="b0304-113">控制項處於 [定位順序] (控制項將會有一個索引標籤停止： [協助工具需求]) 。</span><span class="sxs-lookup"><span data-stu-id="b0304-113">Control is in the tabbing order (control will have a tab stop: accessibility requirement).</span></span> |
| <span data-ttu-id="b0304-114">false</span><span class="sxs-lookup"><span data-stu-id="b0304-114">false</span></span> | <span data-ttu-id="b0304-115">控制項不在定位順序中。</span><span class="sxs-lookup"><span data-stu-id="b0304-115">Control is not in the tabbing order.</span></span>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="b0304-116">備註</span><span class="sxs-lookup"><span data-stu-id="b0304-116">Remarks</span></span>

<span data-ttu-id="b0304-117">**TabStop** 屬性不適用於 **效果** 元素。</span><span class="sxs-lookup"><span data-stu-id="b0304-117">The **tabStop** attribute is not applicable to the **EFFECTS** element.</span></span>

<span data-ttu-id="b0304-118">除了 **AUTOMENU** 和 **TEXT** 以外的所有元素（預設值為 false），此屬性的預設值都是 true。</span><span class="sxs-lookup"><span data-stu-id="b0304-118">The default value for this attribute is true for all elements except **AUTOMENU** and **TEXT**, which have a default value of false.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0304-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0304-119">Requirements</span></span>



| <span data-ttu-id="b0304-120">需求</span><span class="sxs-lookup"><span data-stu-id="b0304-120">Requirement</span></span> | <span data-ttu-id="b0304-121">值</span><span class="sxs-lookup"><span data-stu-id="b0304-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b0304-122">版本</span><span class="sxs-lookup"><span data-stu-id="b0304-122">Version</span></span><br/> | <span data-ttu-id="b0304-123">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="b0304-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0304-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0304-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0304-125">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="b0304-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





