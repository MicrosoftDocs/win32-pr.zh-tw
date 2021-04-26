---
description: 針對埠類型作業產生 proxy 函式的 IDL 宣告。
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: idlFunctionDeclarations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf4d1648ac6d9c3ac6900826ebe90a64418822b6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994735"
---
# <a name="idlfunctiondeclarations-element"></a><span data-ttu-id="03354-103">idlFunctionDeclarations 元素</span><span class="sxs-lookup"><span data-stu-id="03354-103">idlFunctionDeclarations element</span></span>

<span data-ttu-id="03354-104">針對埠類型作業產生 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="03354-104">Generates IDL declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="03354-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="03354-105">Usage</span></span>

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="03354-106">屬性</span><span class="sxs-lookup"><span data-stu-id="03354-106">Attributes</span></span>

<span data-ttu-id="03354-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="03354-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="03354-108">子元素</span><span class="sxs-lookup"><span data-stu-id="03354-108">Child elements</span></span>



| <span data-ttu-id="03354-109">元素</span><span class="sxs-lookup"><span data-stu-id="03354-109">Element</span></span>                                   | <span data-ttu-id="03354-110">描述</span><span class="sxs-lookup"><span data-stu-id="03354-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03354-111">**async**</span><span class="sxs-lookup"><span data-stu-id="03354-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="03354-112">指定產生的 proxy 函數中是否包含非同步作業。</span><span class="sxs-lookup"><span data-stu-id="03354-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="03354-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="03354-113">**eventArg**</span></span>](eventarg.md)<br/>   | <span data-ttu-id="03354-114">指定產生的函數中是否包含相關的事件引數。</span><span class="sxs-lookup"><span data-stu-id="03354-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="03354-115">**事件**</span><span class="sxs-lookup"><span data-stu-id="03354-115">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="03354-116">指定產生的函數中是否包含相關事件。</span><span class="sxs-lookup"><span data-stu-id="03354-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="03354-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="03354-117">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="03354-118">指定產生的函式中是否包含用來傳遞錯誤資訊的參數。</span><span class="sxs-lookup"><span data-stu-id="03354-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="03354-119">**操作**</span><span class="sxs-lookup"><span data-stu-id="03354-119">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="03354-120">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="03354-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="03354-121">**portType**</span><span class="sxs-lookup"><span data-stu-id="03354-121">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="03354-122">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="03354-122">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="03354-123">子項目順序</span><span class="sxs-lookup"><span data-stu-id="03354-123">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="03354-124">父元素</span><span class="sxs-lookup"><span data-stu-id="03354-124">Parent elements</span></span>



| <span data-ttu-id="03354-125">元素</span><span class="sxs-lookup"><span data-stu-id="03354-125">Element</span></span>                         | <span data-ttu-id="03354-126">描述</span><span class="sxs-lookup"><span data-stu-id="03354-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="03354-127">**檔**</span><span class="sxs-lookup"><span data-stu-id="03354-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="03354-128">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="03354-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="03354-129">備註</span><span class="sxs-lookup"><span data-stu-id="03354-129">Remarks</span></span>

<span data-ttu-id="03354-130">這個元素會產生對應至合約所呼叫之作業的成員函式宣告。</span><span class="sxs-lookup"><span data-stu-id="03354-130">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="03354-131">這些宣告的格式適合 MIDL 編譯器取用，而且通常會在 .idl 檔中使用。</span><span class="sxs-lookup"><span data-stu-id="03354-131">These declarations are in a form appropriate for consumption by the MIDL compiler and are generally used in .idl files.</span></span>

<span data-ttu-id="03354-132">範例：</span><span class="sxs-lookup"><span data-stu-id="03354-132">Example:</span></span>

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="03354-133">項目資訊</span><span class="sxs-lookup"><span data-stu-id="03354-133">Element information</span></span>



| <span data-ttu-id="03354-134">標籤</span><span class="sxs-lookup"><span data-stu-id="03354-134">Label</span></span> | <span data-ttu-id="03354-135">值</span><span class="sxs-lookup"><span data-stu-id="03354-135">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="03354-136">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="03354-136">Minimum supported system</span></span><br/> | <span data-ttu-id="03354-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03354-137">Windows Vista</span></span> |
| <span data-ttu-id="03354-138">可以是空的</span><span class="sxs-lookup"><span data-stu-id="03354-138">Can be empty</span></span>                        | <span data-ttu-id="03354-139">是</span><span class="sxs-lookup"><span data-stu-id="03354-139">Yes</span></span>           |



 

 




