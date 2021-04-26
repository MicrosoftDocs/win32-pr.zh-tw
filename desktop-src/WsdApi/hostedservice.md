---
description: 定義要在主機建立器函式中裝載的服務。
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: hostedService 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96c9f6e010989f4844d93299bb34f1ab8893236
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994785"
---
# <a name="hostedservice-element"></a><span data-ttu-id="e0933-103">hostedService 元素</span><span class="sxs-lookup"><span data-stu-id="e0933-103">hostedService element</span></span>

<span data-ttu-id="e0933-104">定義要在主機建立器函式中裝載的服務。</span><span class="sxs-lookup"><span data-stu-id="e0933-104">Defines a service to be hosted in a host builder function.</span></span>

## <a name="usage"></a><span data-ttu-id="e0933-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="e0933-105">Usage</span></span>

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a><span data-ttu-id="e0933-106">屬性</span><span class="sxs-lookup"><span data-stu-id="e0933-106">Attributes</span></span>

<span data-ttu-id="e0933-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="e0933-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e0933-108">子元素</span><span class="sxs-lookup"><span data-stu-id="e0933-108">Child elements</span></span>



| <span data-ttu-id="e0933-109">元素</span><span class="sxs-lookup"><span data-stu-id="e0933-109">Element</span></span>                                     | <span data-ttu-id="e0933-110">描述</span><span class="sxs-lookup"><span data-stu-id="e0933-110">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0933-111">**代號**</span><span class="sxs-lookup"><span data-stu-id="e0933-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="e0933-112">指定要在產生的程式碼中用於埠類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0933-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="e0933-113">根據預設，會從埠類型的限定名稱產生程式碼名稱。</span><span class="sxs-lookup"><span data-stu-id="e0933-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="e0933-114">**portType**</span><span class="sxs-lookup"><span data-stu-id="e0933-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="e0933-115">要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="e0933-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                                       |
| [<span data-ttu-id="e0933-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="e0933-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="e0933-117">要從 builder 函式產生的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="e0933-117">Class name to generate from builder function.</span></span><br/> <br/>                                                                                                      |
| [<span data-ttu-id="e0933-118">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="e0933-118">**ServiceID**</span></span>](serviceid.md)<br/>   | <span data-ttu-id="e0933-119">表示服務識別碼的 URI。</span><span class="sxs-lookup"><span data-stu-id="e0933-119">A URI that represents the service identifier.</span></span><br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="e0933-120">子項目順序</span><span class="sxs-lookup"><span data-stu-id="e0933-120">Child element sequence</span></span>

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a><span data-ttu-id="e0933-121">父元素</span><span class="sxs-lookup"><span data-stu-id="e0933-121">Parent elements</span></span>



| <span data-ttu-id="e0933-122">元素</span><span class="sxs-lookup"><span data-stu-id="e0933-122">Element</span></span>                         | <span data-ttu-id="e0933-123">描述</span><span class="sxs-lookup"><span data-stu-id="e0933-123">Description</span></span>                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="e0933-124">**檔**</span><span class="sxs-lookup"><span data-stu-id="e0933-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="e0933-125">程式碼產生器的輸出檔規格。</span><span class="sxs-lookup"><span data-stu-id="e0933-125">The output file specification for the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="e0933-126">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e0933-126">Element information</span></span>



| <span data-ttu-id="e0933-127">標籤</span><span class="sxs-lookup"><span data-stu-id="e0933-127">Label</span></span> | <span data-ttu-id="e0933-128">值</span><span class="sxs-lookup"><span data-stu-id="e0933-128">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="e0933-129">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="e0933-129">Minimum supported system</span></span><br/> | <span data-ttu-id="e0933-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0933-130">Windows Vista</span></span> |
| <span data-ttu-id="e0933-131">可以是空的</span><span class="sxs-lookup"><span data-stu-id="e0933-131">Can be empty</span></span>                        | <span data-ttu-id="e0933-132">否</span><span class="sxs-lookup"><span data-stu-id="e0933-132">No</span></span>            |



 

 




