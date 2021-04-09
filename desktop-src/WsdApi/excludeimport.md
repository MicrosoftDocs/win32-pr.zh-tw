---
description: 防止在 WSDL 檔案的 <wsdl： import> 專案中，為指定的目標產生 import 語句。
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: excludeImport 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c08d8880029d9e03917e48b61561e3ab3eb2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848731"
---
# <a name="excludeimport-element"></a><span data-ttu-id="1178d-103">excludeImport 元素</span><span class="sxs-lookup"><span data-stu-id="1178d-103">excludeImport element</span></span>

<span data-ttu-id="1178d-104">防止在 WSDL 檔案的 <wsdl： import> 專案中，為指定的目標產生 import 語句。</span><span class="sxs-lookup"><span data-stu-id="1178d-104">Prevents the generation of import statements for specified targets named in a <wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="1178d-105">這可以用來防止 WsdCodeGen 匯入已知的目標，例如 WS-Addressing 和 WS-Eventing 的規格，即使 WSDL 中參考了這些目標也是一樣。</span><span class="sxs-lookup"><span data-stu-id="1178d-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="1178d-106">這個元素的值必須設定為要排除的 <wsdl： import> 元素中所命名的命名空間。</span><span class="sxs-lookup"><span data-stu-id="1178d-106">The value of this element must be set to the namespace named in the <wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="1178d-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="1178d-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="1178d-108">屬性</span><span class="sxs-lookup"><span data-stu-id="1178d-108">Attributes</span></span>

<span data-ttu-id="1178d-109">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="1178d-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1178d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1178d-110">Child elements</span></span>

<span data-ttu-id="1178d-111">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="1178d-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="1178d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1178d-112">Parent elements</span></span>



| <span data-ttu-id="1178d-113">元素</span><span class="sxs-lookup"><span data-stu-id="1178d-113">Element</span></span>                         | <span data-ttu-id="1178d-114">描述</span><span class="sxs-lookup"><span data-stu-id="1178d-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="1178d-115">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="1178d-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="1178d-116">指定要針對合約資訊處理的 WSDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="1178d-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="1178d-117">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1178d-117">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="1178d-118">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="1178d-118">Minimum supported system</span></span><br/> | <span data-ttu-id="1178d-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1178d-119">Windows Vista</span></span> |
| <span data-ttu-id="1178d-120">可以是空的</span><span class="sxs-lookup"><span data-stu-id="1178d-120">Can be empty</span></span>                        | <span data-ttu-id="1178d-121">是</span><span class="sxs-lookup"><span data-stu-id="1178d-121">Yes</span></span>           |



 

 




