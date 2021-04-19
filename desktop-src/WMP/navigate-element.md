---
title: 導覽元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 導覽元素會指定呼叫外部. NavigateTaskPaneURL 所使用的 URL。
ms.assetid: 3898e381-baf8-481a-90ee-d64e55b319a0
keywords:
- 導覽元素 Windows Media Player
topic_type:
- apiref
api_name:
- Navigate Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab3a76fba522332f1414b02d3e317f2793e88292
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994701"
---
# <a name="navigate-element"></a><span data-ttu-id="90c64-106">導覽元素</span><span class="sxs-lookup"><span data-stu-id="90c64-106">Navigate Element</span></span>

> [!Note]  
> <span data-ttu-id="90c64-107">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="90c64-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="90c64-108">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="90c64-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="90c64-109">**導覽** 元素會指定呼叫 **外部. NavigateTaskPaneURL** 所使用的 URL。</span><span class="sxs-lookup"><span data-stu-id="90c64-109">The **Navigate** element specifies a URL used by calls to **External.NavigateTaskPaneURL**.</span></span>

``` syntax
<Navigate
    BaseURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="90c64-110">屬性</span><span class="sxs-lookup"><span data-stu-id="90c64-110">Attributes</span></span>



| <span data-ttu-id="90c64-111">詞彙</span><span class="sxs-lookup"><span data-stu-id="90c64-111">Term</span></span>                                                                                                                                             | <span data-ttu-id="90c64-112">描述</span><span class="sxs-lookup"><span data-stu-id="90c64-112">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90c64-113"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (必要) </span><span class="sxs-lookup"><span data-stu-id="90c64-113"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (required)</span></span><br/> | <span data-ttu-id="90c64-114">要導覽之網頁的完整 URL。</span><span class="sxs-lookup"><span data-stu-id="90c64-114">Fully qualified URL for the webpage to which to navigate.</span></span> <span data-ttu-id="90c64-115">**NavigateTaskPaneURL** 可以將查詢字串附加至此 URL。</span><span class="sxs-lookup"><span data-stu-id="90c64-115">**NavigateTaskPaneURL** can append a query string to this URL.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="90c64-116">父/子項目</span><span class="sxs-lookup"><span data-stu-id="90c64-116">Parent/Child Elements</span></span>



| <span data-ttu-id="90c64-117">階層</span><span class="sxs-lookup"><span data-stu-id="90c64-117">Hierarchy</span></span>       | <span data-ttu-id="90c64-118">元素</span><span class="sxs-lookup"><span data-stu-id="90c64-118">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="90c64-119">父元素</span><span class="sxs-lookup"><span data-stu-id="90c64-119">Parent elements</span></span> | <span data-ttu-id="90c64-120">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="90c64-120">**ServiceInfo**</span></span> |
| <span data-ttu-id="90c64-121">子元素</span><span class="sxs-lookup"><span data-stu-id="90c64-121">Child elements</span></span>  | <span data-ttu-id="90c64-122">無</span><span class="sxs-lookup"><span data-stu-id="90c64-122">None</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="90c64-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="90c64-123">Requirements</span></span>



| <span data-ttu-id="90c64-124">需求</span><span class="sxs-lookup"><span data-stu-id="90c64-124">Requirement</span></span> | <span data-ttu-id="90c64-125">值</span><span class="sxs-lookup"><span data-stu-id="90c64-125">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="90c64-126">版本</span><span class="sxs-lookup"><span data-stu-id="90c64-126">Version</span></span><br/> | <span data-ttu-id="90c64-127">Windows Media Player 10 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="90c64-127">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="90c64-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90c64-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90c64-129">**類型1線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="90c64-129">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="90c64-130">**Type 2 線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="90c64-130">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="90c64-131">**NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="90c64-131">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="90c64-132">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="90c64-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





