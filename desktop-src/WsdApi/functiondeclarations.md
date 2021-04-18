---
description: 針對埠類型作業產生 proxy 函式的實作為宣告。
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: functionDeclarations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b82aca30f94fc8fcec80701a74b56e83ab674c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192912"
---
# <a name="functiondeclarations-element"></a><span data-ttu-id="16d9f-103">functionDeclarations 元素</span><span class="sxs-lookup"><span data-stu-id="16d9f-103">functionDeclarations element</span></span>

<span data-ttu-id="16d9f-104">針對埠類型作業產生 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="16d9f-104">Generates implementation declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="16d9f-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="16d9f-105">Usage</span></span>

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="16d9f-106">屬性</span><span class="sxs-lookup"><span data-stu-id="16d9f-106">Attributes</span></span>

<span data-ttu-id="16d9f-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="16d9f-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="16d9f-108">子元素</span><span class="sxs-lookup"><span data-stu-id="16d9f-108">Child elements</span></span>



| <span data-ttu-id="16d9f-109">元素</span><span class="sxs-lookup"><span data-stu-id="16d9f-109">Element</span></span>                                   | <span data-ttu-id="16d9f-110">描述</span><span class="sxs-lookup"><span data-stu-id="16d9f-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16d9f-111">**async**</span><span class="sxs-lookup"><span data-stu-id="16d9f-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="16d9f-112">指定產生的 proxy 函數中是否包含非同步作業。</span><span class="sxs-lookup"><span data-stu-id="16d9f-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="16d9f-113">**事件**</span><span class="sxs-lookup"><span data-stu-id="16d9f-113">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="16d9f-114">指定產生的函數中是否包含相關事件。</span><span class="sxs-lookup"><span data-stu-id="16d9f-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="16d9f-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="16d9f-115">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="16d9f-116">指定產生的函式中是否包含用來傳遞錯誤資訊的參數。</span><span class="sxs-lookup"><span data-stu-id="16d9f-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="16d9f-117">**操作**</span><span class="sxs-lookup"><span data-stu-id="16d9f-117">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="16d9f-118">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="16d9f-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="16d9f-119">**portType**</span><span class="sxs-lookup"><span data-stu-id="16d9f-119">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="16d9f-120">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="16d9f-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="16d9f-121">子項目順序</span><span class="sxs-lookup"><span data-stu-id="16d9f-121">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="16d9f-122">父元素</span><span class="sxs-lookup"><span data-stu-id="16d9f-122">Parent elements</span></span>



| <span data-ttu-id="16d9f-123">元素</span><span class="sxs-lookup"><span data-stu-id="16d9f-123">Element</span></span>                         | <span data-ttu-id="16d9f-124">描述</span><span class="sxs-lookup"><span data-stu-id="16d9f-124">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="16d9f-125">**檔**</span><span class="sxs-lookup"><span data-stu-id="16d9f-125">**file**</span></span>](file.md)<br/> | <span data-ttu-id="16d9f-126">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="16d9f-126">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="16d9f-127">備註</span><span class="sxs-lookup"><span data-stu-id="16d9f-127">Remarks</span></span>

<span data-ttu-id="16d9f-128">這個元素會產生對應至合約所呼叫之作業的成員函式宣告。</span><span class="sxs-lookup"><span data-stu-id="16d9f-128">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="16d9f-129">這些宣告的格式適合 c + + 編譯器取用，通常用於 .cpp 檔案中。</span><span class="sxs-lookup"><span data-stu-id="16d9f-129">These declarations are in a form appropriate for consumption by a C++ compiler and are generally used in .cpp files.</span></span>

<span data-ttu-id="16d9f-130">範例：</span><span class="sxs-lookup"><span data-stu-id="16d9f-130">Example:</span></span>

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="16d9f-131">項目資訊</span><span class="sxs-lookup"><span data-stu-id="16d9f-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="16d9f-132">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="16d9f-132">Minimum supported system</span></span><br/> | <span data-ttu-id="16d9f-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16d9f-133">Windows Vista</span></span> |
| <span data-ttu-id="16d9f-134">可以是空的</span><span class="sxs-lookup"><span data-stu-id="16d9f-134">Can be empty</span></span>                        | <span data-ttu-id="16d9f-135">是</span><span class="sxs-lookup"><span data-stu-id="16d9f-135">Yes</span></span>           |



 

 




