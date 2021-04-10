---
description: 針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的 IDL 宣告。
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: subscriptionIdlFunctionDeclarations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e1eba60e327778efb1589436a09e62d043d2960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851487"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a><span data-ttu-id="8bd3c-103">subscriptionIdlFunctionDeclarations 元素</span><span class="sxs-lookup"><span data-stu-id="8bd3c-103">subscriptionIdlFunctionDeclarations element</span></span>

<span data-ttu-id="8bd3c-104">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="8bd3c-104">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="8bd3c-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="8bd3c-105">Usage</span></span>

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="8bd3c-106">屬性</span><span class="sxs-lookup"><span data-stu-id="8bd3c-106">Attributes</span></span>



| <span data-ttu-id="8bd3c-107">屬性</span><span class="sxs-lookup"><span data-stu-id="8bd3c-107">Attribute</span></span>                 | <span data-ttu-id="8bd3c-108">類型</span><span class="sxs-lookup"><span data-stu-id="8bd3c-108">Type</span></span>               | <span data-ttu-id="8bd3c-109">必要</span><span class="sxs-lookup"><span data-stu-id="8bd3c-109">Required</span></span>      | <span data-ttu-id="8bd3c-110">描述</span><span class="sxs-lookup"><span data-stu-id="8bd3c-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bd3c-111">**擴展**</span><span class="sxs-lookup"><span data-stu-id="8bd3c-111">**extensible**</span></span><br/> | <span data-ttu-id="8bd3c-112">boolean</span><span class="sxs-lookup"><span data-stu-id="8bd3c-112">boolean</span></span><br/> | <span data-ttu-id="8bd3c-113">No</span><span class="sxs-lookup"><span data-stu-id="8bd3c-113">No</span></span><br/> | <span data-ttu-id="8bd3c-114">將擴充功能新增至函式和介面的能力。</span><span class="sxs-lookup"><span data-stu-id="8bd3c-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="8bd3c-115">此值一律設定為 true。</span><span class="sxs-lookup"><span data-stu-id="8bd3c-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="8bd3c-116">子元素</span><span class="sxs-lookup"><span data-stu-id="8bd3c-116">Child elements</span></span>



| <span data-ttu-id="8bd3c-117">元素</span><span class="sxs-lookup"><span data-stu-id="8bd3c-117">Element</span></span>                                                           | <span data-ttu-id="8bd3c-118">描述</span><span class="sxs-lookup"><span data-stu-id="8bd3c-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8bd3c-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="8bd3c-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="8bd3c-120">指定與事件訂閱搭配使用之通知介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="8bd3c-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="8bd3c-121">**操作**</span><span class="sxs-lookup"><span data-stu-id="8bd3c-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="8bd3c-122">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="8bd3c-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="8bd3c-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="8bd3c-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="8bd3c-124">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="8bd3c-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="8bd3c-125">子項目順序</span><span class="sxs-lookup"><span data-stu-id="8bd3c-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="8bd3c-126">父元素</span><span class="sxs-lookup"><span data-stu-id="8bd3c-126">Parent elements</span></span>



| <span data-ttu-id="8bd3c-127">元素</span><span class="sxs-lookup"><span data-stu-id="8bd3c-127">Element</span></span>                         | <span data-ttu-id="8bd3c-128">描述</span><span class="sxs-lookup"><span data-stu-id="8bd3c-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="8bd3c-129">**檔**</span><span class="sxs-lookup"><span data-stu-id="8bd3c-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="8bd3c-130">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="8bd3c-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="8bd3c-131">項目資訊</span><span class="sxs-lookup"><span data-stu-id="8bd3c-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="8bd3c-132">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="8bd3c-132">Minimum supported system</span></span><br/> | <span data-ttu-id="8bd3c-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8bd3c-133">Windows Vista</span></span> |
| <span data-ttu-id="8bd3c-134">可以是空的</span><span class="sxs-lookup"><span data-stu-id="8bd3c-134">Can be empty</span></span>                        | <span data-ttu-id="8bd3c-135">是</span><span class="sxs-lookup"><span data-stu-id="8bd3c-135">Yes</span></span>           |



 

 




