---
description: 針對埠類型作業產生 proxy 函式的執行。
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: proxyFunctionImplementations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9f03834ca59ede41f2f3c3dff00d7dacdd54db
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995755"
---
# <a name="proxyfunctionimplementations-element"></a><span data-ttu-id="23c93-103">proxyFunctionImplementations 元素</span><span class="sxs-lookup"><span data-stu-id="23c93-103">proxyFunctionImplementations element</span></span>

<span data-ttu-id="23c93-104">針對埠類型作業產生 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="23c93-104">Generates implementations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="23c93-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="23c93-105">Usage</span></span>

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="23c93-106">屬性</span><span class="sxs-lookup"><span data-stu-id="23c93-106">Attributes</span></span>

<span data-ttu-id="23c93-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="23c93-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="23c93-108">子元素</span><span class="sxs-lookup"><span data-stu-id="23c93-108">Child elements</span></span>



| <span data-ttu-id="23c93-109">元素</span><span class="sxs-lookup"><span data-stu-id="23c93-109">Element</span></span>                                     | <span data-ttu-id="23c93-110">描述</span><span class="sxs-lookup"><span data-stu-id="23c93-110">Description</span></span>                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23c93-111">**async**</span><span class="sxs-lookup"><span data-stu-id="23c93-111">**async**</span></span>](async.md)<br/>           | <span data-ttu-id="23c93-112">指定產生的 proxy 函數中是否包含非同步作業。</span><span class="sxs-lookup"><span data-stu-id="23c93-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="23c93-113">**事件**</span><span class="sxs-lookup"><span data-stu-id="23c93-113">**events**</span></span>](events.md)<br/>         | <span data-ttu-id="23c93-114">指定產生的函數中是否包含相關事件。</span><span class="sxs-lookup"><span data-stu-id="23c93-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="23c93-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="23c93-115">**faultInfo**</span></span>](faultinfo.md)<br/>   | <span data-ttu-id="23c93-116">指定產生的函式中是否包含用來傳遞錯誤資訊的參數。</span><span class="sxs-lookup"><span data-stu-id="23c93-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="23c93-117">**操作**</span><span class="sxs-lookup"><span data-stu-id="23c93-117">**operation**</span></span>](operation.md)<br/>   | <span data-ttu-id="23c93-118">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="23c93-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="23c93-119">**portType**</span><span class="sxs-lookup"><span data-stu-id="23c93-119">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="23c93-120">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="23c93-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="23c93-121">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="23c93-121">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="23c93-122">指定用戶端 proxy 類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="23c93-122">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                                               |



### <a name="child-element-sequence"></a><span data-ttu-id="23c93-123">子項目順序</span><span class="sxs-lookup"><span data-stu-id="23c93-123">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="23c93-124">父元素</span><span class="sxs-lookup"><span data-stu-id="23c93-124">Parent elements</span></span>



| <span data-ttu-id="23c93-125">元素</span><span class="sxs-lookup"><span data-stu-id="23c93-125">Element</span></span>                         | <span data-ttu-id="23c93-126">描述</span><span class="sxs-lookup"><span data-stu-id="23c93-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="23c93-127">**檔**</span><span class="sxs-lookup"><span data-stu-id="23c93-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="23c93-128">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="23c93-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="23c93-129">項目資訊</span><span class="sxs-lookup"><span data-stu-id="23c93-129">Element information</span></span>



| <span data-ttu-id="23c93-130">標籤</span><span class="sxs-lookup"><span data-stu-id="23c93-130">Label</span></span> | <span data-ttu-id="23c93-131">值</span><span class="sxs-lookup"><span data-stu-id="23c93-131">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="23c93-132">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="23c93-132">Minimum supported system</span></span><br/> | <span data-ttu-id="23c93-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23c93-133">Windows Vista</span></span> |
| <span data-ttu-id="23c93-134">可以是空的</span><span class="sxs-lookup"><span data-stu-id="23c93-134">Can be empty</span></span>                        | <span data-ttu-id="23c93-135">是</span><span class="sxs-lookup"><span data-stu-id="23c93-135">Yes</span></span>           |



 

 




