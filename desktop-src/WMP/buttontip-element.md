---
title: ButtonTip 元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 |ButtonTip 元素
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- ButtonTip 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ab94794232ade6f924b87fd3f4d73d4452d544
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989275"
---
# <a name="buttontip-element"></a><span data-ttu-id="5d2c3-105">ButtonTip 元素</span><span class="sxs-lookup"><span data-stu-id="5d2c3-105">ButtonTip Element</span></span>

> [!Note]  
> <span data-ttu-id="5d2c3-106">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="5d2c3-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5d2c3-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="5d2c3-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5d2c3-108">**ButtonTip** 元素會指定當使用者指向工作窗格按鈕時所顯示的文字字串。</span><span class="sxs-lookup"><span data-stu-id="5d2c3-108">The **ButtonTip** element specifies the text string that is displayed when the user points to a task pane button.</span></span>

``` syntax
<ButtonTip>
   text string
</ButtonTip>
```

## <a name="attributes"></a><span data-ttu-id="5d2c3-109">屬性</span><span class="sxs-lookup"><span data-stu-id="5d2c3-109">Attributes</span></span>

<span data-ttu-id="5d2c3-110">這個元素沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="5d2c3-110">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="5d2c3-111">父/子項目</span><span class="sxs-lookup"><span data-stu-id="5d2c3-111">Parent/Child Elements</span></span>



| <span data-ttu-id="5d2c3-112">階層</span><span class="sxs-lookup"><span data-stu-id="5d2c3-112">Hierarchy</span></span>       | <span data-ttu-id="5d2c3-113">元素</span><span class="sxs-lookup"><span data-stu-id="5d2c3-113">Element</span></span>                                              |
|-----------------|------------------------------------------------------|
| <span data-ttu-id="5d2c3-114">父元素</span><span class="sxs-lookup"><span data-stu-id="5d2c3-114">Parent elements</span></span> | <span data-ttu-id="5d2c3-115">**ServiceTask1**、 **ServiceTask2**、 **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="5d2c3-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |
| <span data-ttu-id="5d2c3-116">子元素</span><span class="sxs-lookup"><span data-stu-id="5d2c3-116">Child elements</span></span>  | <span data-ttu-id="5d2c3-117">無</span><span class="sxs-lookup"><span data-stu-id="5d2c3-117">None</span></span>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="5d2c3-118">備註</span><span class="sxs-lookup"><span data-stu-id="5d2c3-118">Remarks</span></span>

<span data-ttu-id="5d2c3-119">針對 **ServiceTask1**、 **ServiceTask2** 或 **ServiceTask3** 的每個實例，這個元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="5d2c3-119">This element is optional for each instance of **ServiceTask1**, **ServiceTask2**, or **ServiceTask3**.</span></span> <span data-ttu-id="5d2c3-120">如果未提供此元素，Windows Media Player 會使用按鈕文字作為預設值。</span><span class="sxs-lookup"><span data-stu-id="5d2c3-120">If this element is not supplied, Windows Media Player uses the button text as the default value.</span></span>

> [!Note]  
> <span data-ttu-id="5d2c3-121">Windows Media Player 10 有三個工作窗格，可讓線上商店顯示其網頁。</span><span class="sxs-lookup"><span data-stu-id="5d2c3-121">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="5d2c3-122">線上商店可以選擇使用一個、兩個或三個工作窗格。</span><span class="sxs-lookup"><span data-stu-id="5d2c3-122">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="5d2c3-123">Windows Media Player 11 只有一個工作窗格，使用者可以按一下 [ **線上商店** ] 索引標籤來查看。 Windows Media Player 11 會忽略 **ServiceTask2** 和 **ServiceTask3** 元素。</span><span class="sxs-lookup"><span data-stu-id="5d2c3-123">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d2c3-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d2c3-124">Requirements</span></span>



| <span data-ttu-id="5d2c3-125">需求</span><span class="sxs-lookup"><span data-stu-id="5d2c3-125">Requirement</span></span> | <span data-ttu-id="5d2c3-126">值</span><span class="sxs-lookup"><span data-stu-id="5d2c3-126">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="5d2c3-127">版本</span><span class="sxs-lookup"><span data-stu-id="5d2c3-127">Version</span></span><br/> | <span data-ttu-id="5d2c3-128">Windows Media Player 10 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="5d2c3-128">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5d2c3-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d2c3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d2c3-130">**類型1線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="5d2c3-130">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="5d2c3-131">**Type 2 線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="5d2c3-131">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="5d2c3-132">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="5d2c3-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





