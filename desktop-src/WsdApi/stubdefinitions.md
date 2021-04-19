---
description: 針對埠類型作業產生存根函式的實作為。
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: stubDefinitions 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6676cfc6cf55aa9c9961bd614506500d847def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980307"
---
# <a name="stubdefinitions-element"></a><span data-ttu-id="b08fe-103">stubDefinitions 元素</span><span class="sxs-lookup"><span data-stu-id="b08fe-103">stubDefinitions element</span></span>

<span data-ttu-id="b08fe-104">針對埠類型作業產生存根函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="b08fe-104">Generates implementations for stub functions for port-type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="b08fe-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="b08fe-105">Usage</span></span>

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="b08fe-106">屬性</span><span class="sxs-lookup"><span data-stu-id="b08fe-106">Attributes</span></span>

<span data-ttu-id="b08fe-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="b08fe-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b08fe-108">子元素</span><span class="sxs-lookup"><span data-stu-id="b08fe-108">Child elements</span></span>



| <span data-ttu-id="b08fe-109">元素</span><span class="sxs-lookup"><span data-stu-id="b08fe-109">Element</span></span>                                                         | <span data-ttu-id="b08fe-110">描述</span><span class="sxs-lookup"><span data-stu-id="b08fe-110">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b08fe-111">**釋放器**</span><span class="sxs-lookup"><span data-stu-id="b08fe-111">**deallocator**</span></span>](deallocator.md)<br/>                   | <span data-ttu-id="b08fe-112">指定存根函式所要使用的釋放器類型。</span><span class="sxs-lookup"><span data-stu-id="b08fe-112">Specifies the type of deallocator to be used by a stub function.</span></span><br/> <br/>                                 |
| [<span data-ttu-id="b08fe-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="b08fe-113">**eventArg**</span></span>](eventarg.md)<br/>                         | <span data-ttu-id="b08fe-114">指定產生的函數中是否包含相關的事件引數。</span><span class="sxs-lookup"><span data-stu-id="b08fe-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="b08fe-115">**事件**</span><span class="sxs-lookup"><span data-stu-id="b08fe-115">**events**</span></span>](events.md)<br/>                             | <span data-ttu-id="b08fe-116">指定產生的函數中是否包含相關事件。</span><span class="sxs-lookup"><span data-stu-id="b08fe-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="b08fe-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="b08fe-117">**faultInfo**</span></span>](faultinfo.md)<br/>                       | <span data-ttu-id="b08fe-118">指定產生的函式中是否包含用來傳遞錯誤資訊的參數。</span><span class="sxs-lookup"><span data-stu-id="b08fe-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="b08fe-119">**操作**</span><span class="sxs-lookup"><span data-stu-id="b08fe-119">**operation**</span></span>](operation.md)<br/>                       | <span data-ttu-id="b08fe-120">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="b08fe-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="b08fe-121">**operationDeallocator**</span><span class="sxs-lookup"><span data-stu-id="b08fe-121">**operationDeallocator**</span></span>](operationdeallocator.md)<br/> | <span data-ttu-id="b08fe-122">指定作業的存根函數所要使用的釋放器類型。</span><span class="sxs-lookup"><span data-stu-id="b08fe-122">Specifies the type of deallocator to be used by an operation's stub function.</span></span><br/> <br/>                    |
| [<span data-ttu-id="b08fe-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="b08fe-123">**portType**</span></span>](porttype.md)<br/>                         | <span data-ttu-id="b08fe-124">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="b08fe-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="b08fe-125">**serverClass**</span><span class="sxs-lookup"><span data-stu-id="b08fe-125">**serverClass**</span></span>](serverclass.md)<br/>                   | <span data-ttu-id="b08fe-126">指定主機端伺服器類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="b08fe-126">Specifies the name of the host-side server class.</span></span><br/> <br/>                                                |



### <a name="child-element-sequence"></a><span data-ttu-id="b08fe-127">子項目順序</span><span class="sxs-lookup"><span data-stu-id="b08fe-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  serverClass, 
  eventArg?, 
  events?, 
  operationDeallocator*, 
  deallocator?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="b08fe-128">父元素</span><span class="sxs-lookup"><span data-stu-id="b08fe-128">Parent elements</span></span>



| <span data-ttu-id="b08fe-129">元素</span><span class="sxs-lookup"><span data-stu-id="b08fe-129">Element</span></span>                         | <span data-ttu-id="b08fe-130">描述</span><span class="sxs-lookup"><span data-stu-id="b08fe-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="b08fe-131">**檔**</span><span class="sxs-lookup"><span data-stu-id="b08fe-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="b08fe-132">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="b08fe-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="b08fe-133">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b08fe-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b08fe-134">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="b08fe-134">Minimum supported system</span></span><br/> | <span data-ttu-id="b08fe-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b08fe-135">Windows Vista</span></span> |
| <span data-ttu-id="b08fe-136">可以是空的</span><span class="sxs-lookup"><span data-stu-id="b08fe-136">Can be empty</span></span>                        | <span data-ttu-id="b08fe-137">否</span><span class="sxs-lookup"><span data-stu-id="b08fe-137">No</span></span>            |



 

 




