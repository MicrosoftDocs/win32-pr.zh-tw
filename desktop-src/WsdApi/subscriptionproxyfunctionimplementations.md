---
description: 針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的執行。
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: subscriptionProxyFunctionImplementations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb57fa21910f9b39440257bc72918519b35c6a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112984"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a><span data-ttu-id="623d3-103">subscriptionProxyFunctionImplementations 元素</span><span class="sxs-lookup"><span data-stu-id="623d3-103">subscriptionProxyFunctionImplementations element</span></span>

<span data-ttu-id="623d3-104">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="623d3-104">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="623d3-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="623d3-105">Usage</span></span>

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="623d3-106">屬性</span><span class="sxs-lookup"><span data-stu-id="623d3-106">Attributes</span></span>



| <span data-ttu-id="623d3-107">屬性</span><span class="sxs-lookup"><span data-stu-id="623d3-107">Attribute</span></span>                 | <span data-ttu-id="623d3-108">類型</span><span class="sxs-lookup"><span data-stu-id="623d3-108">Type</span></span>               | <span data-ttu-id="623d3-109">必要</span><span class="sxs-lookup"><span data-stu-id="623d3-109">Required</span></span>      | <span data-ttu-id="623d3-110">描述</span><span class="sxs-lookup"><span data-stu-id="623d3-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="623d3-111">**擴展**</span><span class="sxs-lookup"><span data-stu-id="623d3-111">**extensible**</span></span><br/> | <span data-ttu-id="623d3-112">boolean</span><span class="sxs-lookup"><span data-stu-id="623d3-112">boolean</span></span><br/> | <span data-ttu-id="623d3-113">No</span><span class="sxs-lookup"><span data-stu-id="623d3-113">No</span></span><br/> | <span data-ttu-id="623d3-114">將擴充功能新增至函式和介面的能力。</span><span class="sxs-lookup"><span data-stu-id="623d3-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="623d3-115">此值一律設定為 true。</span><span class="sxs-lookup"><span data-stu-id="623d3-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="623d3-116">子元素</span><span class="sxs-lookup"><span data-stu-id="623d3-116">Child elements</span></span>



| <span data-ttu-id="623d3-117">元素</span><span class="sxs-lookup"><span data-stu-id="623d3-117">Element</span></span>                                                           | <span data-ttu-id="623d3-118">描述</span><span class="sxs-lookup"><span data-stu-id="623d3-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="623d3-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="623d3-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="623d3-120">指定與事件訂閱搭配使用之通知介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="623d3-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="623d3-121">**操作**</span><span class="sxs-lookup"><span data-stu-id="623d3-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="623d3-122">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="623d3-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="623d3-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="623d3-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="623d3-124">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="623d3-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |
| [<span data-ttu-id="623d3-125">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="623d3-125">**proxyClass**</span></span>](proxyclass.md)<br/>                       | <span data-ttu-id="623d3-126">指定用戶端 proxy 類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="623d3-126">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                              |



### <a name="child-element-sequence"></a><span data-ttu-id="623d3-127">子項目順序</span><span class="sxs-lookup"><span data-stu-id="623d3-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="623d3-128">父元素</span><span class="sxs-lookup"><span data-stu-id="623d3-128">Parent elements</span></span>



| <span data-ttu-id="623d3-129">元素</span><span class="sxs-lookup"><span data-stu-id="623d3-129">Element</span></span>                         | <span data-ttu-id="623d3-130">描述</span><span class="sxs-lookup"><span data-stu-id="623d3-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="623d3-131">**檔**</span><span class="sxs-lookup"><span data-stu-id="623d3-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="623d3-132">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="623d3-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="623d3-133">項目資訊</span><span class="sxs-lookup"><span data-stu-id="623d3-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="623d3-134">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="623d3-134">Minimum supported system</span></span><br/> | <span data-ttu-id="623d3-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="623d3-135">Windows Vista</span></span> |
| <span data-ttu-id="623d3-136">可以是空的</span><span class="sxs-lookup"><span data-stu-id="623d3-136">Can be empty</span></span>                        | <span data-ttu-id="623d3-137">是</span><span class="sxs-lookup"><span data-stu-id="623d3-137">Yes</span></span>           |



 

 




