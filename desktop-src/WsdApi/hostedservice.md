---
description: 定義要在主機建立器函式中裝載的服務。
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: hostedService 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfcf2f4c67cadf90279221fd5bdfd518e285e844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848727"
---
# <a name="hostedservice-element"></a><span data-ttu-id="e1d8e-103">hostedService 元素</span><span class="sxs-lookup"><span data-stu-id="e1d8e-103">hostedService element</span></span>

<span data-ttu-id="e1d8e-104">定義要在主機建立器函式中裝載的服務。</span><span class="sxs-lookup"><span data-stu-id="e1d8e-104">Defines a service to be hosted in a host builder function.</span></span>

## <a name="usage"></a><span data-ttu-id="e1d8e-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="e1d8e-105">Usage</span></span>

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a><span data-ttu-id="e1d8e-106">屬性</span><span class="sxs-lookup"><span data-stu-id="e1d8e-106">Attributes</span></span>

<span data-ttu-id="e1d8e-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="e1d8e-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e1d8e-108">子元素</span><span class="sxs-lookup"><span data-stu-id="e1d8e-108">Child elements</span></span>



| <span data-ttu-id="e1d8e-109">元素</span><span class="sxs-lookup"><span data-stu-id="e1d8e-109">Element</span></span>                                     | <span data-ttu-id="e1d8e-110">描述</span><span class="sxs-lookup"><span data-stu-id="e1d8e-110">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1d8e-111">**代號**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="e1d8e-112">指定要在產生的程式碼中用於埠類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1d8e-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="e1d8e-113">根據預設，會從埠類型的限定名稱產生程式碼名稱。</span><span class="sxs-lookup"><span data-stu-id="e1d8e-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="e1d8e-114">**portType**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="e1d8e-115">要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="e1d8e-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                                       |
| [<span data-ttu-id="e1d8e-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="e1d8e-117">要從 builder 函式產生的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="e1d8e-117">Class name to generate from builder function.</span></span><br/> <br/>                                                                                                      |
| [<span data-ttu-id="e1d8e-118">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-118">**ServiceID**</span></span>](serviceid.md)<br/>   | <span data-ttu-id="e1d8e-119">表示服務識別碼的 URI。</span><span class="sxs-lookup"><span data-stu-id="e1d8e-119">A URI that represents the service identifier.</span></span><br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="e1d8e-120">子項目順序</span><span class="sxs-lookup"><span data-stu-id="e1d8e-120">Child element sequence</span></span>

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a><span data-ttu-id="e1d8e-121">父元素</span><span class="sxs-lookup"><span data-stu-id="e1d8e-121">Parent elements</span></span>



| <span data-ttu-id="e1d8e-122">元素</span><span class="sxs-lookup"><span data-stu-id="e1d8e-122">Element</span></span>                         | <span data-ttu-id="e1d8e-123">描述</span><span class="sxs-lookup"><span data-stu-id="e1d8e-123">Description</span></span>                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="e1d8e-124">**檔**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="e1d8e-125">程式碼產生器的輸出檔規格。</span><span class="sxs-lookup"><span data-stu-id="e1d8e-125">The output file specification for the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="e1d8e-126">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e1d8e-126">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="e1d8e-127">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="e1d8e-127">Minimum supported system</span></span><br/> | <span data-ttu-id="e1d8e-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1d8e-128">Windows Vista</span></span> |
| <span data-ttu-id="e1d8e-129">可以是空的</span><span class="sxs-lookup"><span data-stu-id="e1d8e-129">Can be empty</span></span>                        | <span data-ttu-id="e1d8e-130">否</span><span class="sxs-lookup"><span data-stu-id="e1d8e-130">No</span></span>            |



 

 




