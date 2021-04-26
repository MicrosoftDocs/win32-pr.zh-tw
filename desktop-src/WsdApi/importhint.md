---
description: 指定未明確指定位置之 wsdl： import 指示詞的下載位置。
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: importHint 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c874879ee0a608c100f32a0520a85efe76080cc2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998755"
---
# <a name="importhint-element"></a><span data-ttu-id="c5bf2-103">importHint 元素</span><span class="sxs-lookup"><span data-stu-id="c5bf2-103">importHint element</span></span>

<span data-ttu-id="c5bf2-104">指定 \<wsdl:import> 未明確指定位置之指示詞的下載位置。</span><span class="sxs-lookup"><span data-stu-id="c5bf2-104">Specifies the download location for a \<wsdl:import> directive that does not explicitly specify a location.</span></span>

## <a name="usage"></a><span data-ttu-id="c5bf2-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="c5bf2-105">Usage</span></span>

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a><span data-ttu-id="c5bf2-106">屬性</span><span class="sxs-lookup"><span data-stu-id="c5bf2-106">Attributes</span></span>

<span data-ttu-id="c5bf2-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="c5bf2-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c5bf2-108">子元素</span><span class="sxs-lookup"><span data-stu-id="c5bf2-108">Child elements</span></span>



| <span data-ttu-id="c5bf2-109">元素</span><span class="sxs-lookup"><span data-stu-id="c5bf2-109">Element</span></span>                                   | <span data-ttu-id="c5bf2-110">描述</span><span class="sxs-lookup"><span data-stu-id="c5bf2-110">Description</span></span>                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5bf2-111">**位置**</span><span class="sxs-lookup"><span data-stu-id="c5bf2-111">**location**</span></span>](location.md)<br/>   | <span data-ttu-id="c5bf2-112">要匯入之檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="c5bf2-112">The location of the file to import.</span></span> <span data-ttu-id="c5bf2-113">位置可以是相對路徑、絕對路徑或 HTTP URL。</span><span class="sxs-lookup"><span data-stu-id="c5bf2-113">The location may be a relative path, an absolute path, or an HTTP URL.</span></span><br/> <br/> |
| [<span data-ttu-id="c5bf2-114">**命名 空間**</span><span class="sxs-lookup"><span data-stu-id="c5bf2-114">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="c5bf2-115">要匯入的命名空間。</span><span class="sxs-lookup"><span data-stu-id="c5bf2-115">The namespace to import.</span></span> <span data-ttu-id="c5bf2-116">這應該符合元素中指定的命名空間 \<wsdl:import> 。</span><span class="sxs-lookup"><span data-stu-id="c5bf2-116">This should match the namespace specified in the \<wsdl:import> element.</span></span><br/> <br/>     |



### <a name="child-element-sequence"></a><span data-ttu-id="c5bf2-117">子項目順序</span><span class="sxs-lookup"><span data-stu-id="c5bf2-117">Child element sequence</span></span>

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a><span data-ttu-id="c5bf2-118">父元素</span><span class="sxs-lookup"><span data-stu-id="c5bf2-118">Parent elements</span></span>



| <span data-ttu-id="c5bf2-119">元素</span><span class="sxs-lookup"><span data-stu-id="c5bf2-119">Element</span></span>                         | <span data-ttu-id="c5bf2-120">描述</span><span class="sxs-lookup"><span data-stu-id="c5bf2-120">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="c5bf2-121">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="c5bf2-121">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="c5bf2-122">指定要針對合約資訊處理的 WSDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="c5bf2-122">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="c5bf2-123">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c5bf2-123">Element information</span></span>



| <span data-ttu-id="c5bf2-124">標籤</span><span class="sxs-lookup"><span data-stu-id="c5bf2-124">Label</span></span> | <span data-ttu-id="c5bf2-125">值</span><span class="sxs-lookup"><span data-stu-id="c5bf2-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="c5bf2-126">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="c5bf2-126">Minimum supported system</span></span><br/> | <span data-ttu-id="c5bf2-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5bf2-127">Windows Vista</span></span> |
| <span data-ttu-id="c5bf2-128">可以是空的</span><span class="sxs-lookup"><span data-stu-id="c5bf2-128">Can be empty</span></span>                        | <span data-ttu-id="c5bf2-129">否</span><span class="sxs-lookup"><span data-stu-id="c5bf2-129">No</span></span>            |



 

 




