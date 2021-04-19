---
title: AmbientAttributes。可見
description: Visible 屬性會指定或抓取控制項的可見度。
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- AmbientAttributes visible Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72794b7bbba0237a687dc70bda761c505b839e59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999664"
---
# <a name="ambientattributesvisible"></a><span data-ttu-id="667a9-104">AmbientAttributes。可見</span><span class="sxs-lookup"><span data-stu-id="667a9-104">AmbientAttributes.visible</span></span>

<span data-ttu-id="667a9-105">**Visible** 屬性會指定或抓取控制項的可見度。</span><span class="sxs-lookup"><span data-stu-id="667a9-105">The **visible** attribute specifies or retrieves the visibility for the control.</span></span>

``` syntax
        elementID.visible
```

## <a name="possible-values"></a><span data-ttu-id="667a9-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="667a9-106">Possible Values</span></span>

<span data-ttu-id="667a9-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="667a9-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="667a9-108">值</span><span class="sxs-lookup"><span data-stu-id="667a9-108">Value</span></span> | <span data-ttu-id="667a9-109">描述</span><span class="sxs-lookup"><span data-stu-id="667a9-109">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="667a9-110">true</span><span class="sxs-lookup"><span data-stu-id="667a9-110">true</span></span>  | <span data-ttu-id="667a9-111">預設值。</span><span class="sxs-lookup"><span data-stu-id="667a9-111">Default.</span></span> <span data-ttu-id="667a9-112">可以看到控制項。</span><span class="sxs-lookup"><span data-stu-id="667a9-112">The control is visible.</span></span> |
| <span data-ttu-id="667a9-113">false</span><span class="sxs-lookup"><span data-stu-id="667a9-113">false</span></span> | <span data-ttu-id="667a9-114">控制項是不可見的。</span><span class="sxs-lookup"><span data-stu-id="667a9-114">The control is not visible.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="667a9-115">備註</span><span class="sxs-lookup"><span data-stu-id="667a9-115">Remarks</span></span>

<span data-ttu-id="667a9-116">這個屬性適用于隱藏控制項，例如，當您交換播放按鈕的 [暫停] 按鈕時。</span><span class="sxs-lookup"><span data-stu-id="667a9-116">This attribute is useful for hiding controls, for example when swapping a pause button for a play button.</span></span>

<span data-ttu-id="667a9-117">如果值為 false，則不會顯示控制項，而是將事件傳遞給其後方的控制項。</span><span class="sxs-lookup"><span data-stu-id="667a9-117">If the value is false, the control is not visible and click events are passed to the control behind it.</span></span> <span data-ttu-id="667a9-118">如果值為 true，就會顯示控制項，並接收 click 事件本身。</span><span class="sxs-lookup"><span data-stu-id="667a9-118">If the value is true, the control is visible and receives the click event itself.</span></span>

<span data-ttu-id="667a9-119">**AUTOMENU** 元素的預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="667a9-119">The default value for the **AUTOMENU** element is false.</span></span>

## <a name="requirements"></a><span data-ttu-id="667a9-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="667a9-120">Requirements</span></span>



| <span data-ttu-id="667a9-121">需求</span><span class="sxs-lookup"><span data-stu-id="667a9-121">Requirement</span></span> | <span data-ttu-id="667a9-122">值</span><span class="sxs-lookup"><span data-stu-id="667a9-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="667a9-123">版本</span><span class="sxs-lookup"><span data-stu-id="667a9-123">Version</span></span><br/> | <span data-ttu-id="667a9-124">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="667a9-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="667a9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="667a9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="667a9-126">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="667a9-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





