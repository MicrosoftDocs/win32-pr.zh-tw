---
description: 防止針對 WSDL 檔中 wsdl： import 專案所命名的指定目標產生 import 語句。
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: excludeImport 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e14d79576151fbb3dc266621c3fa34816cea55e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995875"
---
# <a name="excludeimport-element"></a><span data-ttu-id="a603f-103">excludeImport 元素</span><span class="sxs-lookup"><span data-stu-id="a603f-103">excludeImport element</span></span>

<span data-ttu-id="a603f-104">防止在 WSDL 檔案中的元素中，針對指定的目標產生 import 語句 \<wsdl:import> 。</span><span class="sxs-lookup"><span data-stu-id="a603f-104">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="a603f-105">這可以用來防止 WsdCodeGen 匯入已知的目標，例如 WS-Addressing 和 WS-Eventing 的規格，即使 WSDL 中參考了這些目標也是一樣。</span><span class="sxs-lookup"><span data-stu-id="a603f-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="a603f-106">這個元素的值必須設定為要排除的元素中所指定的命名空間 \<wsdl:import> 。</span><span class="sxs-lookup"><span data-stu-id="a603f-106">The value of this element must be set to the namespace named in the \<wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="a603f-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="a603f-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="a603f-108">屬性</span><span class="sxs-lookup"><span data-stu-id="a603f-108">Attributes</span></span>

<span data-ttu-id="a603f-109">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="a603f-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a603f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a603f-110">Child elements</span></span>

<span data-ttu-id="a603f-111">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="a603f-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a603f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a603f-112">Parent elements</span></span>



| <span data-ttu-id="a603f-113">元素</span><span class="sxs-lookup"><span data-stu-id="a603f-113">Element</span></span>                         | <span data-ttu-id="a603f-114">描述</span><span class="sxs-lookup"><span data-stu-id="a603f-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="a603f-115">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="a603f-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="a603f-116">指定要針對合約資訊處理的 WSDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="a603f-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="a603f-117">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a603f-117">Element information</span></span>



| <span data-ttu-id="a603f-118">標籤</span><span class="sxs-lookup"><span data-stu-id="a603f-118">Label</span></span> | <span data-ttu-id="a603f-119">值</span><span class="sxs-lookup"><span data-stu-id="a603f-119">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="a603f-120">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="a603f-120">Minimum supported system</span></span><br/> | <span data-ttu-id="a603f-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a603f-121">Windows Vista</span></span> |
| <span data-ttu-id="a603f-122">可以是空的</span><span class="sxs-lookup"><span data-stu-id="a603f-122">Can be empty</span></span>                        | <span data-ttu-id="a603f-123">是</span><span class="sxs-lookup"><span data-stu-id="a603f-123">Yes</span></span>           |



 

 




