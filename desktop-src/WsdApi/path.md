---
description: 指定 WSDL 檔案的位置和檔案名。 路徑可以是檔案的絕對路徑或相對路徑，但不能是 URL。
ms.assetid: 0664dcc6-1e71-46cf-9084-1adc84861b52
title: '裝置上 (Web 服務的路徑元素) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48df5a156149f00b8b153ccc0d46d6d2d34a1ce
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994305"
---
# <a name="path-element"></a><span data-ttu-id="92de0-104">path 元素</span><span class="sxs-lookup"><span data-stu-id="92de0-104">path element</span></span>

<span data-ttu-id="92de0-105">指定 WSDL 檔案的位置和檔案名。</span><span class="sxs-lookup"><span data-stu-id="92de0-105">Specifies the location and filename of a WSDL file.</span></span> <span data-ttu-id="92de0-106">路徑可以是檔案的絕對路徑或相對路徑，但不能是 URL。</span><span class="sxs-lookup"><span data-stu-id="92de0-106">The path may be an absolute or relative path to the file, but must not be an URL.</span></span>

## <a name="usage"></a><span data-ttu-id="92de0-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="92de0-107">Usage</span></span>

``` syntax
<path/>
```

## <a name="attributes"></a><span data-ttu-id="92de0-108">屬性</span><span class="sxs-lookup"><span data-stu-id="92de0-108">Attributes</span></span>

<span data-ttu-id="92de0-109">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="92de0-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="92de0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="92de0-110">Child elements</span></span>

<span data-ttu-id="92de0-111">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="92de0-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="92de0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="92de0-112">Parent elements</span></span>



| <span data-ttu-id="92de0-113">元素</span><span class="sxs-lookup"><span data-stu-id="92de0-113">Element</span></span>                         | <span data-ttu-id="92de0-114">描述</span><span class="sxs-lookup"><span data-stu-id="92de0-114">Description</span></span>                                                             |
|---------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="92de0-115">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="92de0-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="92de0-116">要針對合約資訊處理的 WSDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="92de0-116">A WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="examples"></a><span data-ttu-id="92de0-117">範例</span><span class="sxs-lookup"><span data-stu-id="92de0-117">Examples</span></span>

<span data-ttu-id="92de0-118">下列 XML 會顯示有效的 **路徑** 元素。</span><span class="sxs-lookup"><span data-stu-id="92de0-118">The following XML shows a valid **path** element.</span></span>

``` syntax
<path>"..\wsdls\example.wsdl"</path>
```

## <a name="element-information"></a><span data-ttu-id="92de0-119">項目資訊</span><span class="sxs-lookup"><span data-stu-id="92de0-119">Element information</span></span>



| <span data-ttu-id="92de0-120">標籤</span><span class="sxs-lookup"><span data-stu-id="92de0-120">Label</span></span> | <span data-ttu-id="92de0-121">值</span><span class="sxs-lookup"><span data-stu-id="92de0-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="92de0-122">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="92de0-122">Minimum supported system</span></span><br/> | <span data-ttu-id="92de0-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92de0-123">Windows Vista</span></span> |
| <span data-ttu-id="92de0-124">可以是空的</span><span class="sxs-lookup"><span data-stu-id="92de0-124">Can be empty</span></span>                        | <span data-ttu-id="92de0-125">是</span><span class="sxs-lookup"><span data-stu-id="92de0-125">Yes</span></span>           |



 

 




