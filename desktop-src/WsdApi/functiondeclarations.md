---
description: 針對埠類型作業產生 proxy 函式的實作為宣告。
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: functionDeclarations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508cbac6d220c0ebdee0c6306d5f8a8ab5f26770
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998815"
---
# <a name="functiondeclarations-element"></a><span data-ttu-id="4d8b6-103">functionDeclarations 元素</span><span class="sxs-lookup"><span data-stu-id="4d8b6-103">functionDeclarations element</span></span>

<span data-ttu-id="4d8b6-104">針對埠類型作業產生 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="4d8b6-104">Generates implementation declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="4d8b6-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="4d8b6-105">Usage</span></span>

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="4d8b6-106">屬性</span><span class="sxs-lookup"><span data-stu-id="4d8b6-106">Attributes</span></span>

<span data-ttu-id="4d8b6-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="4d8b6-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4d8b6-108">子元素</span><span class="sxs-lookup"><span data-stu-id="4d8b6-108">Child elements</span></span>



| <span data-ttu-id="4d8b6-109">元素</span><span class="sxs-lookup"><span data-stu-id="4d8b6-109">Element</span></span>                                   | <span data-ttu-id="4d8b6-110">描述</span><span class="sxs-lookup"><span data-stu-id="4d8b6-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d8b6-111">**async**</span><span class="sxs-lookup"><span data-stu-id="4d8b6-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="4d8b6-112">指定產生的 proxy 函數中是否包含非同步作業。</span><span class="sxs-lookup"><span data-stu-id="4d8b6-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="4d8b6-113">**事件**</span><span class="sxs-lookup"><span data-stu-id="4d8b6-113">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="4d8b6-114">指定產生的函數中是否包含相關事件。</span><span class="sxs-lookup"><span data-stu-id="4d8b6-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="4d8b6-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="4d8b6-115">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="4d8b6-116">指定產生的函式中是否包含用來傳遞錯誤資訊的參數。</span><span class="sxs-lookup"><span data-stu-id="4d8b6-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="4d8b6-117">**操作**</span><span class="sxs-lookup"><span data-stu-id="4d8b6-117">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="4d8b6-118">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="4d8b6-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="4d8b6-119">**portType**</span><span class="sxs-lookup"><span data-stu-id="4d8b6-119">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="4d8b6-120">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="4d8b6-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="4d8b6-121">子項目順序</span><span class="sxs-lookup"><span data-stu-id="4d8b6-121">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="4d8b6-122">父元素</span><span class="sxs-lookup"><span data-stu-id="4d8b6-122">Parent elements</span></span>



| <span data-ttu-id="4d8b6-123">元素</span><span class="sxs-lookup"><span data-stu-id="4d8b6-123">Element</span></span>                         | <span data-ttu-id="4d8b6-124">描述</span><span class="sxs-lookup"><span data-stu-id="4d8b6-124">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="4d8b6-125">**檔**</span><span class="sxs-lookup"><span data-stu-id="4d8b6-125">**file**</span></span>](file.md)<br/> | <span data-ttu-id="4d8b6-126">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="4d8b6-126">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4d8b6-127">備註</span><span class="sxs-lookup"><span data-stu-id="4d8b6-127">Remarks</span></span>

<span data-ttu-id="4d8b6-128">這個元素會產生對應至合約所呼叫之作業的成員函式宣告。</span><span class="sxs-lookup"><span data-stu-id="4d8b6-128">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="4d8b6-129">這些宣告的格式適合 c + + 編譯器取用，通常用於 .cpp 檔案中。</span><span class="sxs-lookup"><span data-stu-id="4d8b6-129">These declarations are in a form appropriate for consumption by a C++ compiler and are generally used in .cpp files.</span></span>

<span data-ttu-id="4d8b6-130">範例：</span><span class="sxs-lookup"><span data-stu-id="4d8b6-130">Example:</span></span>

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="4d8b6-131">項目資訊</span><span class="sxs-lookup"><span data-stu-id="4d8b6-131">Element information</span></span>



| <span data-ttu-id="4d8b6-132">標籤</span><span class="sxs-lookup"><span data-stu-id="4d8b6-132">Label</span></span> | <span data-ttu-id="4d8b6-133">值</span><span class="sxs-lookup"><span data-stu-id="4d8b6-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="4d8b6-134">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="4d8b6-134">Minimum supported system</span></span><br/> | <span data-ttu-id="4d8b6-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d8b6-135">Windows Vista</span></span> |
| <span data-ttu-id="4d8b6-136">可以是空的</span><span class="sxs-lookup"><span data-stu-id="4d8b6-136">Can be empty</span></span>                        | <span data-ttu-id="4d8b6-137">是</span><span class="sxs-lookup"><span data-stu-id="4d8b6-137">Yes</span></span>           |



 

 




