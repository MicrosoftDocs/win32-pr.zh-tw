---
description: 針對埠類型作業產生 proxy 函式的執行。
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: proxyFunctionImplementations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a27e217cfa3d0a9efd204a1b18c7b2f0ca16f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851228"
---
# <a name="proxyfunctionimplementations-element"></a><span data-ttu-id="63a04-103">proxyFunctionImplementations 元素</span><span class="sxs-lookup"><span data-stu-id="63a04-103">proxyFunctionImplementations element</span></span>

<span data-ttu-id="63a04-104">針對埠類型作業產生 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="63a04-104">Generates implementations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="63a04-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="63a04-105">Usage</span></span>

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="63a04-106">屬性</span><span class="sxs-lookup"><span data-stu-id="63a04-106">Attributes</span></span>

<span data-ttu-id="63a04-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="63a04-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="63a04-108">子元素</span><span class="sxs-lookup"><span data-stu-id="63a04-108">Child elements</span></span>



| <span data-ttu-id="63a04-109">元素</span><span class="sxs-lookup"><span data-stu-id="63a04-109">Element</span></span>                                     | <span data-ttu-id="63a04-110">描述</span><span class="sxs-lookup"><span data-stu-id="63a04-110">Description</span></span>                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63a04-111">**async**</span><span class="sxs-lookup"><span data-stu-id="63a04-111">**async**</span></span>](async.md)<br/>           | <span data-ttu-id="63a04-112">指定產生的 proxy 函數中是否包含非同步作業。</span><span class="sxs-lookup"><span data-stu-id="63a04-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="63a04-113">**事件**</span><span class="sxs-lookup"><span data-stu-id="63a04-113">**events**</span></span>](events.md)<br/>         | <span data-ttu-id="63a04-114">指定產生的函數中是否包含相關事件。</span><span class="sxs-lookup"><span data-stu-id="63a04-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="63a04-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="63a04-115">**faultInfo**</span></span>](faultinfo.md)<br/>   | <span data-ttu-id="63a04-116">指定產生的函式中是否包含用來傳遞錯誤資訊的參數。</span><span class="sxs-lookup"><span data-stu-id="63a04-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="63a04-117">**操作**</span><span class="sxs-lookup"><span data-stu-id="63a04-117">**operation**</span></span>](operation.md)<br/>   | <span data-ttu-id="63a04-118">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="63a04-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="63a04-119">**portType**</span><span class="sxs-lookup"><span data-stu-id="63a04-119">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="63a04-120">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="63a04-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="63a04-121">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="63a04-121">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="63a04-122">指定用戶端 proxy 類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="63a04-122">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                                               |



### <a name="child-element-sequence"></a><span data-ttu-id="63a04-123">子項目順序</span><span class="sxs-lookup"><span data-stu-id="63a04-123">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="63a04-124">父元素</span><span class="sxs-lookup"><span data-stu-id="63a04-124">Parent elements</span></span>



| <span data-ttu-id="63a04-125">元素</span><span class="sxs-lookup"><span data-stu-id="63a04-125">Element</span></span>                         | <span data-ttu-id="63a04-126">描述</span><span class="sxs-lookup"><span data-stu-id="63a04-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="63a04-127">**檔**</span><span class="sxs-lookup"><span data-stu-id="63a04-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="63a04-128">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="63a04-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="63a04-129">項目資訊</span><span class="sxs-lookup"><span data-stu-id="63a04-129">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="63a04-130">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="63a04-130">Minimum supported system</span></span><br/> | <span data-ttu-id="63a04-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63a04-131">Windows Vista</span></span> |
| <span data-ttu-id="63a04-132">可以是空的</span><span class="sxs-lookup"><span data-stu-id="63a04-132">Can be empty</span></span>                        | <span data-ttu-id="63a04-133">是</span><span class="sxs-lookup"><span data-stu-id="63a04-133">Yes</span></span>           |



 

 




