---
description: 針對埠類型作業產生 proxy 函式的 IDL 宣告。
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: idlFunctionDeclarations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1afa43676898231f739804185b8bf5d6e2b4faf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983565"
---
# <a name="idlfunctiondeclarations-element"></a><span data-ttu-id="c4af0-103">idlFunctionDeclarations 元素</span><span class="sxs-lookup"><span data-stu-id="c4af0-103">idlFunctionDeclarations element</span></span>

<span data-ttu-id="c4af0-104">針對埠類型作業產生 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="c4af0-104">Generates IDL declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="c4af0-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="c4af0-105">Usage</span></span>

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="c4af0-106">屬性</span><span class="sxs-lookup"><span data-stu-id="c4af0-106">Attributes</span></span>

<span data-ttu-id="c4af0-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="c4af0-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c4af0-108">子元素</span><span class="sxs-lookup"><span data-stu-id="c4af0-108">Child elements</span></span>



| <span data-ttu-id="c4af0-109">元素</span><span class="sxs-lookup"><span data-stu-id="c4af0-109">Element</span></span>                                   | <span data-ttu-id="c4af0-110">描述</span><span class="sxs-lookup"><span data-stu-id="c4af0-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4af0-111">**async**</span><span class="sxs-lookup"><span data-stu-id="c4af0-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="c4af0-112">指定產生的 proxy 函數中是否包含非同步作業。</span><span class="sxs-lookup"><span data-stu-id="c4af0-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="c4af0-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="c4af0-113">**eventArg**</span></span>](eventarg.md)<br/>   | <span data-ttu-id="c4af0-114">指定產生的函數中是否包含相關的事件引數。</span><span class="sxs-lookup"><span data-stu-id="c4af0-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="c4af0-115">**事件**</span><span class="sxs-lookup"><span data-stu-id="c4af0-115">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="c4af0-116">指定產生的函數中是否包含相關事件。</span><span class="sxs-lookup"><span data-stu-id="c4af0-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="c4af0-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="c4af0-117">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="c4af0-118">指定產生的函式中是否包含用來傳遞錯誤資訊的參數。</span><span class="sxs-lookup"><span data-stu-id="c4af0-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="c4af0-119">**操作**</span><span class="sxs-lookup"><span data-stu-id="c4af0-119">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="c4af0-120">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="c4af0-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="c4af0-121">**portType**</span><span class="sxs-lookup"><span data-stu-id="c4af0-121">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="c4af0-122">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="c4af0-122">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="c4af0-123">子項目順序</span><span class="sxs-lookup"><span data-stu-id="c4af0-123">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  eventArg?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="c4af0-124">父元素</span><span class="sxs-lookup"><span data-stu-id="c4af0-124">Parent elements</span></span>



| <span data-ttu-id="c4af0-125">元素</span><span class="sxs-lookup"><span data-stu-id="c4af0-125">Element</span></span>                         | <span data-ttu-id="c4af0-126">描述</span><span class="sxs-lookup"><span data-stu-id="c4af0-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="c4af0-127">**檔**</span><span class="sxs-lookup"><span data-stu-id="c4af0-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="c4af0-128">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="c4af0-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c4af0-129">備註</span><span class="sxs-lookup"><span data-stu-id="c4af0-129">Remarks</span></span>

<span data-ttu-id="c4af0-130">這個元素會產生對應至合約所呼叫之作業的成員函式宣告。</span><span class="sxs-lookup"><span data-stu-id="c4af0-130">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="c4af0-131">這些宣告的格式適合 MIDL 編譯器取用，而且通常會在 .idl 檔中使用。</span><span class="sxs-lookup"><span data-stu-id="c4af0-131">These declarations are in a form appropriate for consumption by the MIDL compiler and are generally used in .idl files.</span></span>

<span data-ttu-id="c4af0-132">範例：</span><span class="sxs-lookup"><span data-stu-id="c4af0-132">Example:</span></span>

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="c4af0-133">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c4af0-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="c4af0-134">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="c4af0-134">Minimum supported system</span></span><br/> | <span data-ttu-id="c4af0-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4af0-135">Windows Vista</span></span> |
| <span data-ttu-id="c4af0-136">可以是空的</span><span class="sxs-lookup"><span data-stu-id="c4af0-136">Can be empty</span></span>                        | <span data-ttu-id="c4af0-137">是</span><span class="sxs-lookup"><span data-stu-id="c4af0-137">Yes</span></span>           |



 

 




