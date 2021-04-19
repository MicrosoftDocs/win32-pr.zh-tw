---
description: 防止針對 WSDL 檔中 wsdl： import 專案所命名的指定目標產生 import 語句。
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: excludeImport 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf511a24ad4007deb886900843991364fcf03a5a
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380772"
---
# <a name="excludeimport-element"></a><span data-ttu-id="c1b97-103">excludeImport 元素</span><span class="sxs-lookup"><span data-stu-id="c1b97-103">excludeImport element</span></span>

<span data-ttu-id="c1b97-104">防止在 WSDL 檔案中的元素中，針對指定的目標產生 import 語句 \<wsdl:import> 。</span><span class="sxs-lookup"><span data-stu-id="c1b97-104">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="c1b97-105">這可以用來防止 WsdCodeGen 匯入已知的目標，例如 WS-Addressing 和 WS-Eventing 的規格，即使 WSDL 中參考了這些目標也是一樣。</span><span class="sxs-lookup"><span data-stu-id="c1b97-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="c1b97-106">這個元素的值必須設定為要排除的元素中所指定的命名空間 \<wsdl:import> 。</span><span class="sxs-lookup"><span data-stu-id="c1b97-106">The value of this element must be set to the namespace named in the \<wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="c1b97-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="c1b97-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="c1b97-108">屬性</span><span class="sxs-lookup"><span data-stu-id="c1b97-108">Attributes</span></span>

<span data-ttu-id="c1b97-109">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="c1b97-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c1b97-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c1b97-110">Child elements</span></span>

<span data-ttu-id="c1b97-111">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="c1b97-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="c1b97-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c1b97-112">Parent elements</span></span>



| <span data-ttu-id="c1b97-113">元素</span><span class="sxs-lookup"><span data-stu-id="c1b97-113">Element</span></span>                         | <span data-ttu-id="c1b97-114">描述</span><span class="sxs-lookup"><span data-stu-id="c1b97-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="c1b97-115">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="c1b97-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="c1b97-116">指定要針對合約資訊處理的 WSDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="c1b97-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="c1b97-117">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c1b97-117">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="c1b97-118">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="c1b97-118">Minimum supported system</span></span><br/> | <span data-ttu-id="c1b97-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1b97-119">Windows Vista</span></span> |
| <span data-ttu-id="c1b97-120">可以是空的</span><span class="sxs-lookup"><span data-stu-id="c1b97-120">Can be empty</span></span>                        | <span data-ttu-id="c1b97-121">是</span><span class="sxs-lookup"><span data-stu-id="c1b97-121">Yes</span></span>           |



 

 




