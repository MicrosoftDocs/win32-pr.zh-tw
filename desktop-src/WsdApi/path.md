---
description: 指定 WSDL 檔案的位置和檔案名。 路徑可以是檔案的絕對路徑或相對路徑，但不能是 URL。
ms.assetid: 0664dcc6-1e71-46cf-9084-1adc84861b52
title: '裝置上 (Web 服務的路徑元素) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 763ad1479c20553fb7e62ab29e504d56bfa6d950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991865"
---
# <a name="path-element"></a><span data-ttu-id="a53d5-104">path 元素</span><span class="sxs-lookup"><span data-stu-id="a53d5-104">path element</span></span>

<span data-ttu-id="a53d5-105">指定 WSDL 檔案的位置和檔案名。</span><span class="sxs-lookup"><span data-stu-id="a53d5-105">Specifies the location and filename of a WSDL file.</span></span> <span data-ttu-id="a53d5-106">路徑可以是檔案的絕對路徑或相對路徑，但不能是 URL。</span><span class="sxs-lookup"><span data-stu-id="a53d5-106">The path may be an absolute or relative path to the file, but must not be an URL.</span></span>

## <a name="usage"></a><span data-ttu-id="a53d5-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="a53d5-107">Usage</span></span>

``` syntax
<path/>
```

## <a name="attributes"></a><span data-ttu-id="a53d5-108">屬性</span><span class="sxs-lookup"><span data-stu-id="a53d5-108">Attributes</span></span>

<span data-ttu-id="a53d5-109">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="a53d5-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a53d5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a53d5-110">Child elements</span></span>

<span data-ttu-id="a53d5-111">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="a53d5-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a53d5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a53d5-112">Parent elements</span></span>



| <span data-ttu-id="a53d5-113">元素</span><span class="sxs-lookup"><span data-stu-id="a53d5-113">Element</span></span>                         | <span data-ttu-id="a53d5-114">描述</span><span class="sxs-lookup"><span data-stu-id="a53d5-114">Description</span></span>                                                             |
|---------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="a53d5-115">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="a53d5-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="a53d5-116">要針對合約資訊處理的 WSDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="a53d5-116">A WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="examples"></a><span data-ttu-id="a53d5-117">範例</span><span class="sxs-lookup"><span data-stu-id="a53d5-117">Examples</span></span>

<span data-ttu-id="a53d5-118">下列 XML 會顯示有效的 **路徑** 元素。</span><span class="sxs-lookup"><span data-stu-id="a53d5-118">The following XML shows a valid **path** element.</span></span>

``` syntax
<path>"..\wsdls\example.wsdl"</path>
```

## <a name="element-information"></a><span data-ttu-id="a53d5-119">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a53d5-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="a53d5-120">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="a53d5-120">Minimum supported system</span></span><br/> | <span data-ttu-id="a53d5-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a53d5-121">Windows Vista</span></span> |
| <span data-ttu-id="a53d5-122">可以是空的</span><span class="sxs-lookup"><span data-stu-id="a53d5-122">Can be empty</span></span>                        | <span data-ttu-id="a53d5-123">是</span><span class="sxs-lookup"><span data-stu-id="a53d5-123">Yes</span></span>           |



 

 




