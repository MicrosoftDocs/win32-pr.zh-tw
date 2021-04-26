---
description: 針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的實作為宣告。
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: subscriptionFunctionDeclarations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7389b30ef7da17f9466fa8aefd24fa04f4c99f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995455"
---
# <a name="subscriptionfunctiondeclarations-element"></a><span data-ttu-id="74ea5-103">subscriptionFunctionDeclarations 元素</span><span class="sxs-lookup"><span data-stu-id="74ea5-103">subscriptionFunctionDeclarations element</span></span>

<span data-ttu-id="74ea5-104">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="74ea5-104">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="74ea5-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="74ea5-105">Usage</span></span>

``` syntax
<subscriptionFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="74ea5-106">屬性</span><span class="sxs-lookup"><span data-stu-id="74ea5-106">Attributes</span></span>



| <span data-ttu-id="74ea5-107">屬性</span><span class="sxs-lookup"><span data-stu-id="74ea5-107">Attribute</span></span>                 | <span data-ttu-id="74ea5-108">類型</span><span class="sxs-lookup"><span data-stu-id="74ea5-108">Type</span></span>               | <span data-ttu-id="74ea5-109">必要</span><span class="sxs-lookup"><span data-stu-id="74ea5-109">Required</span></span>      | <span data-ttu-id="74ea5-110">描述</span><span class="sxs-lookup"><span data-stu-id="74ea5-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74ea5-111">**擴展**</span><span class="sxs-lookup"><span data-stu-id="74ea5-111">**extensible**</span></span><br/> | <span data-ttu-id="74ea5-112">boolean</span><span class="sxs-lookup"><span data-stu-id="74ea5-112">boolean</span></span><br/> | <span data-ttu-id="74ea5-113">No</span><span class="sxs-lookup"><span data-stu-id="74ea5-113">No</span></span><br/> | <span data-ttu-id="74ea5-114">將擴充功能新增至函式和介面的能力。</span><span class="sxs-lookup"><span data-stu-id="74ea5-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="74ea5-115">此值一律設定為 true。</span><span class="sxs-lookup"><span data-stu-id="74ea5-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="74ea5-116">子元素</span><span class="sxs-lookup"><span data-stu-id="74ea5-116">Child elements</span></span>



| <span data-ttu-id="74ea5-117">元素</span><span class="sxs-lookup"><span data-stu-id="74ea5-117">Element</span></span>                                                           | <span data-ttu-id="74ea5-118">描述</span><span class="sxs-lookup"><span data-stu-id="74ea5-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74ea5-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="74ea5-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="74ea5-120">指定與事件訂閱搭配使用之通知介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="74ea5-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="74ea5-121">**操作**</span><span class="sxs-lookup"><span data-stu-id="74ea5-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="74ea5-122">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="74ea5-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="74ea5-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="74ea5-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="74ea5-124">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="74ea5-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="74ea5-125">子項目順序</span><span class="sxs-lookup"><span data-stu-id="74ea5-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="74ea5-126">父元素</span><span class="sxs-lookup"><span data-stu-id="74ea5-126">Parent elements</span></span>



| <span data-ttu-id="74ea5-127">元素</span><span class="sxs-lookup"><span data-stu-id="74ea5-127">Element</span></span>                         | <span data-ttu-id="74ea5-128">描述</span><span class="sxs-lookup"><span data-stu-id="74ea5-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="74ea5-129">**檔**</span><span class="sxs-lookup"><span data-stu-id="74ea5-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="74ea5-130">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="74ea5-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="74ea5-131">項目資訊</span><span class="sxs-lookup"><span data-stu-id="74ea5-131">Element information</span></span>



| <span data-ttu-id="74ea5-132">標籤</span><span class="sxs-lookup"><span data-stu-id="74ea5-132">Label</span></span> | <span data-ttu-id="74ea5-133">值</span><span class="sxs-lookup"><span data-stu-id="74ea5-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="74ea5-134">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="74ea5-134">Minimum supported system</span></span><br/> | <span data-ttu-id="74ea5-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74ea5-135">Windows Vista</span></span> |
| <span data-ttu-id="74ea5-136">可以是空的</span><span class="sxs-lookup"><span data-stu-id="74ea5-136">Can be empty</span></span>                        | <span data-ttu-id="74ea5-137">是</span><span class="sxs-lookup"><span data-stu-id="74ea5-137">Yes</span></span>           |



 

 




