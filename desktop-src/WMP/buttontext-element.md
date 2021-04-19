---
title: ButtonText 項目
description: 請注意，本節將說明針對線上商店使用而設計的功能。 |ButtonText 元素
ms.assetid: 1afe1626-769a-40c8-883a-968ebd995a93
keywords:
- ButtonText 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ButtonText Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c94577ad772a5c6fa198bd43f2475d53821da72c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984481"
---
# <a name="buttontext-element"></a><span data-ttu-id="f84db-105">ButtonText 項目</span><span class="sxs-lookup"><span data-stu-id="f84db-105">ButtonText Element</span></span>

> [!Note]  
> <span data-ttu-id="f84db-106">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="f84db-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="f84db-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="f84db-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="f84db-108">**ButtonText** 元素會指定 Windows Media Player 針對工作窗格按鈕顯示的文字字串。</span><span class="sxs-lookup"><span data-stu-id="f84db-108">The **ButtonText** element specifies the text string that Windows Media Player displays for a task pane button.</span></span>

``` syntax
<ButtonText>
   text string
</ButtonText>
```

## <a name="attributes"></a><span data-ttu-id="f84db-109">屬性</span><span class="sxs-lookup"><span data-stu-id="f84db-109">Attributes</span></span>

<span data-ttu-id="f84db-110">這個元素沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="f84db-110">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="f84db-111">父/子項目</span><span class="sxs-lookup"><span data-stu-id="f84db-111">Parent/Child Elements</span></span>



| <span data-ttu-id="f84db-112">階層</span><span class="sxs-lookup"><span data-stu-id="f84db-112">Hierarchy</span></span>       | <span data-ttu-id="f84db-113">元素</span><span class="sxs-lookup"><span data-stu-id="f84db-113">Element</span></span>                                              |
|-----------------|------------------------------------------------------|
| <span data-ttu-id="f84db-114">父元素</span><span class="sxs-lookup"><span data-stu-id="f84db-114">Parent elements</span></span> | <span data-ttu-id="f84db-115">**ServiceTask1**、 **ServiceTask2**、 **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="f84db-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |
| <span data-ttu-id="f84db-116">子元素</span><span class="sxs-lookup"><span data-stu-id="f84db-116">Child elements</span></span>  | <span data-ttu-id="f84db-117">無</span><span class="sxs-lookup"><span data-stu-id="f84db-117">None</span></span>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="f84db-118">備註</span><span class="sxs-lookup"><span data-stu-id="f84db-118">Remarks</span></span>

<span data-ttu-id="f84db-119">每個 **ServiceTask1**、 **ServiceTask2** 或 **ServiceTask3** 實例都需要這個元素。</span><span class="sxs-lookup"><span data-stu-id="f84db-119">This element is required for each instance of **ServiceTask1**, **ServiceTask2**, or **ServiceTask3**.</span></span>

> [!Note]  
> <span data-ttu-id="f84db-120">Windows Media Player 10 有三個工作窗格，可讓線上商店顯示其網頁。</span><span class="sxs-lookup"><span data-stu-id="f84db-120">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="f84db-121">線上商店可以選擇使用一個、兩個或三個工作窗格。</span><span class="sxs-lookup"><span data-stu-id="f84db-121">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="f84db-122">Windows Media Player 11 只有一個工作窗格，使用者可以按一下 [ **線上商店** ] 索引標籤來查看。 Windows Media Player 11 會忽略 **ServiceTask2** 和 **ServiceTask3** 元素。</span><span class="sxs-lookup"><span data-stu-id="f84db-122">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

<span data-ttu-id="f84db-123">Windows Media Player 可能會裁剪按鈕文字以符合可用空間。</span><span class="sxs-lookup"><span data-stu-id="f84db-123">Windows Media Player may crop button text to fit the available space.</span></span> <span data-ttu-id="f84db-124">播放程式一律會使用 Tahoma 粗體的8點字型作為此文字。</span><span class="sxs-lookup"><span data-stu-id="f84db-124">The Player always uses the Tahoma bold 8-point font for this text.</span></span> <span data-ttu-id="f84db-125">有兩行可用來顯示按鈕文字，但播放程式不會自動將第一行的文字換行到第二行。</span><span class="sxs-lookup"><span data-stu-id="f84db-125">There are two lines available to display button text, but the Player does not automatically wrap text from the first line to the second.</span></span> <span data-ttu-id="f84db-126">若要在按鈕文字中指定分行符號，請在文字字串中插入新的行 escape 序列 " \\ n"。</span><span class="sxs-lookup"><span data-stu-id="f84db-126">To specify a line break in the button text, insert the new line escape sequence "\\n" in your text string.</span></span>

<span data-ttu-id="f84db-127">文字字串也會顯示在 Windows Media Player 使用者介面的 **GoTo** 功能表中。</span><span class="sxs-lookup"><span data-stu-id="f84db-127">The text string is also displayed in the **GoTo** menu in the Windows Media Player user interface.</span></span>

<span data-ttu-id="f84db-128">您應使用各種不同的顯示設定來測試您的線上商店，以確保文字如預期般顯示。</span><span class="sxs-lookup"><span data-stu-id="f84db-128">You should test your online store using a variety of display settings to ensure that text displays as you expect.</span></span>

## <a name="requirements"></a><span data-ttu-id="f84db-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="f84db-129">Requirements</span></span>



| <span data-ttu-id="f84db-130">需求</span><span class="sxs-lookup"><span data-stu-id="f84db-130">Requirement</span></span> | <span data-ttu-id="f84db-131">值</span><span class="sxs-lookup"><span data-stu-id="f84db-131">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="f84db-132">版本</span><span class="sxs-lookup"><span data-stu-id="f84db-132">Version</span></span><br/> | <span data-ttu-id="f84db-133">Windows Media Player 10 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="f84db-133">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f84db-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f84db-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f84db-135">**類型1線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="f84db-135">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="f84db-136">**Type 2 線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="f84db-136">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="f84db-137">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="f84db-137">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





