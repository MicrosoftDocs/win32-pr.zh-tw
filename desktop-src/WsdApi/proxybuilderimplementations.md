---
description: 產生函數以建立具類型的 proxy。
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: proxyBuilderImplementations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2cb64a6ea87b1083871931359a4f7c01ece9b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000160"
---
# <a name="proxybuilderimplementations-element"></a><span data-ttu-id="93f3a-103">proxyBuilderImplementations 元素</span><span class="sxs-lookup"><span data-stu-id="93f3a-103">proxyBuilderImplementations element</span></span>

<span data-ttu-id="93f3a-104">產生函數以建立具類型的 proxy。</span><span class="sxs-lookup"><span data-stu-id="93f3a-104">Generates functions to create typed proxies.</span></span>

## <a name="usage"></a><span data-ttu-id="93f3a-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="93f3a-105">Usage</span></span>

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a><span data-ttu-id="93f3a-106">屬性</span><span class="sxs-lookup"><span data-stu-id="93f3a-106">Attributes</span></span>

<span data-ttu-id="93f3a-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="93f3a-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="93f3a-108">子元素</span><span class="sxs-lookup"><span data-stu-id="93f3a-108">Child elements</span></span>



| <span data-ttu-id="93f3a-109">元素</span><span class="sxs-lookup"><span data-stu-id="93f3a-109">Element</span></span>                                     | <span data-ttu-id="93f3a-110">描述</span><span class="sxs-lookup"><span data-stu-id="93f3a-110">Description</span></span>                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93f3a-111">**代號**</span><span class="sxs-lookup"><span data-stu-id="93f3a-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="93f3a-112">要在產生的程式碼中用於埠類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="93f3a-112">The name to be used for the port type in the generated code.</span></span> <span data-ttu-id="93f3a-113">根據預設，會從埠類型的限定名稱產生程式碼名稱。</span><span class="sxs-lookup"><span data-stu-id="93f3a-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="93f3a-114">**portType**</span><span class="sxs-lookup"><span data-stu-id="93f3a-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="93f3a-115">要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="93f3a-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                             |
| [<span data-ttu-id="93f3a-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="93f3a-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="93f3a-117">要從 proxy 產生器函數產生的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="93f3a-117">Class name to generate from the proxy builder function.</span></span><br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="93f3a-118">子項目順序</span><span class="sxs-lookup"><span data-stu-id="93f3a-118">Child element sequence</span></span>

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a><span data-ttu-id="93f3a-119">父元素</span><span class="sxs-lookup"><span data-stu-id="93f3a-119">Parent elements</span></span>



| <span data-ttu-id="93f3a-120">元素</span><span class="sxs-lookup"><span data-stu-id="93f3a-120">Element</span></span>                         | <span data-ttu-id="93f3a-121">描述</span><span class="sxs-lookup"><span data-stu-id="93f3a-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="93f3a-122">**檔**</span><span class="sxs-lookup"><span data-stu-id="93f3a-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="93f3a-123">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="93f3a-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="93f3a-124">項目資訊</span><span class="sxs-lookup"><span data-stu-id="93f3a-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="93f3a-125">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="93f3a-125">Minimum supported system</span></span><br/> | <span data-ttu-id="93f3a-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93f3a-126">Windows Vista</span></span> |
| <span data-ttu-id="93f3a-127">可以是空的</span><span class="sxs-lookup"><span data-stu-id="93f3a-127">Can be empty</span></span>                        | <span data-ttu-id="93f3a-128">否</span><span class="sxs-lookup"><span data-stu-id="93f3a-128">No</span></span>            |



 

 




