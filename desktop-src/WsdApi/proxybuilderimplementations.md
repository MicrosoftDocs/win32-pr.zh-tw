---
description: 產生函數以建立具類型的 proxy。
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: proxyBuilderImplementations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ad22348b33c60689adf60c029e3a08c2f4d417c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996465"
---
# <a name="proxybuilderimplementations-element"></a><span data-ttu-id="b2e11-103">proxyBuilderImplementations 元素</span><span class="sxs-lookup"><span data-stu-id="b2e11-103">proxyBuilderImplementations element</span></span>

<span data-ttu-id="b2e11-104">產生函數以建立具類型的 proxy。</span><span class="sxs-lookup"><span data-stu-id="b2e11-104">Generates functions to create typed proxies.</span></span>

## <a name="usage"></a><span data-ttu-id="b2e11-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="b2e11-105">Usage</span></span>

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a><span data-ttu-id="b2e11-106">屬性</span><span class="sxs-lookup"><span data-stu-id="b2e11-106">Attributes</span></span>

<span data-ttu-id="b2e11-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="b2e11-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b2e11-108">子元素</span><span class="sxs-lookup"><span data-stu-id="b2e11-108">Child elements</span></span>



| <span data-ttu-id="b2e11-109">元素</span><span class="sxs-lookup"><span data-stu-id="b2e11-109">Element</span></span>                                     | <span data-ttu-id="b2e11-110">描述</span><span class="sxs-lookup"><span data-stu-id="b2e11-110">Description</span></span>                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2e11-111">**代號**</span><span class="sxs-lookup"><span data-stu-id="b2e11-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="b2e11-112">要在產生的程式碼中用於埠類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2e11-112">The name to be used for the port type in the generated code.</span></span> <span data-ttu-id="b2e11-113">根據預設，會從埠類型的限定名稱產生程式碼名稱。</span><span class="sxs-lookup"><span data-stu-id="b2e11-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="b2e11-114">**portType**</span><span class="sxs-lookup"><span data-stu-id="b2e11-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="b2e11-115">要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="b2e11-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                             |
| [<span data-ttu-id="b2e11-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="b2e11-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="b2e11-117">要從 proxy 產生器函數產生的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="b2e11-117">Class name to generate from the proxy builder function.</span></span><br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="b2e11-118">子項目順序</span><span class="sxs-lookup"><span data-stu-id="b2e11-118">Child element sequence</span></span>

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a><span data-ttu-id="b2e11-119">父元素</span><span class="sxs-lookup"><span data-stu-id="b2e11-119">Parent elements</span></span>



| <span data-ttu-id="b2e11-120">元素</span><span class="sxs-lookup"><span data-stu-id="b2e11-120">Element</span></span>                         | <span data-ttu-id="b2e11-121">描述</span><span class="sxs-lookup"><span data-stu-id="b2e11-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="b2e11-122">**檔**</span><span class="sxs-lookup"><span data-stu-id="b2e11-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="b2e11-123">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="b2e11-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="b2e11-124">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b2e11-124">Element information</span></span>



| <span data-ttu-id="b2e11-125">標籤</span><span class="sxs-lookup"><span data-stu-id="b2e11-125">Label</span></span> | <span data-ttu-id="b2e11-126">值</span><span class="sxs-lookup"><span data-stu-id="b2e11-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="b2e11-127">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="b2e11-127">Minimum supported system</span></span><br/> | <span data-ttu-id="b2e11-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2e11-128">Windows Vista</span></span> |
| <span data-ttu-id="b2e11-129">可以是空的</span><span class="sxs-lookup"><span data-stu-id="b2e11-129">Can be empty</span></span>                        | <span data-ttu-id="b2e11-130">否</span><span class="sxs-lookup"><span data-stu-id="b2e11-130">No</span></span>            |



 

 




