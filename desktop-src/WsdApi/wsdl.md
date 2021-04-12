---
description: 指定要針對合約資訊處理的 WSDL 檔案。
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: wsdl 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb54f946f32fb4962b8384dea7c6cf4b3c0ebe3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192895"
---
# <a name="wsdl-element"></a><span data-ttu-id="639e8-103">wsdl 元素</span><span class="sxs-lookup"><span data-stu-id="639e8-103">wsdl element</span></span>

<span data-ttu-id="639e8-104">指定要針對合約資訊處理的 WSDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="639e8-104">Specifies a WSDL file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="639e8-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="639e8-105">Usage</span></span>

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a><span data-ttu-id="639e8-106">屬性</span><span class="sxs-lookup"><span data-stu-id="639e8-106">Attributes</span></span>

<span data-ttu-id="639e8-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="639e8-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="639e8-108">子元素</span><span class="sxs-lookup"><span data-stu-id="639e8-108">Child elements</span></span>



| <span data-ttu-id="639e8-109">元素</span><span class="sxs-lookup"><span data-stu-id="639e8-109">Element</span></span>                                           | <span data-ttu-id="639e8-110">描述</span><span class="sxs-lookup"><span data-stu-id="639e8-110">Description</span></span>                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="639e8-111">**excludeImport**</span><span class="sxs-lookup"><span data-stu-id="639e8-111">**excludeImport**</span></span>](excludeimport.md)<br/> | <span data-ttu-id="639e8-112">防止在 WSDL 檔案的 <wsdl： import> 專案中，為指定的目標產生 import 語句。</span><span class="sxs-lookup"><span data-stu-id="639e8-112">Prevents the generation of import statements for specified targets named in a <wsdl:import> element in a WSDL file.</span></span> <br/> <br/> |
| [<span data-ttu-id="639e8-113">**importHint**</span><span class="sxs-lookup"><span data-stu-id="639e8-113">**importHint**</span></span>](importhint.md)<br/>       | <span data-ttu-id="639e8-114">指定未明確指定位置之 <wsdl： import> 指示詞的下載位置。</span><span class="sxs-lookup"><span data-stu-id="639e8-114">Specifies the download location for a <wsdl:import> directive that does not explicitly specify a location.</span></span><br/> <br/>           |
| [<span data-ttu-id="639e8-115">**路徑**</span><span class="sxs-lookup"><span data-stu-id="639e8-115">**path**</span></span>](path.md)<br/>                   | <span data-ttu-id="639e8-116">WSDL 輸入檔的檔案和路徑。</span><span class="sxs-lookup"><span data-stu-id="639e8-116">File and path of the WSDL input file.</span></span><br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="639e8-117">子項目順序</span><span class="sxs-lookup"><span data-stu-id="639e8-117">Child element sequence</span></span>

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a><span data-ttu-id="639e8-118">父元素</span><span class="sxs-lookup"><span data-stu-id="639e8-118">Parent elements</span></span>



| <span data-ttu-id="639e8-119">元素</span><span class="sxs-lookup"><span data-stu-id="639e8-119">Element</span></span>                                     | <span data-ttu-id="639e8-120">描述</span><span class="sxs-lookup"><span data-stu-id="639e8-120">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="639e8-121">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="639e8-121">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="639e8-122">WSDAPI 程式碼產生器 XML 腳本檔的根項目。</span><span class="sxs-lookup"><span data-stu-id="639e8-122">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="639e8-123">備註</span><span class="sxs-lookup"><span data-stu-id="639e8-123">Remarks</span></span>

<span data-ttu-id="639e8-124">在 XML 設定檔案中的 [**path**](path.md)元素後面出現的任何 [**importHint**](importhint.md)或 [**excludeImport**](excludeimport.md)元素都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="639e8-124">Any [**importHint**](importhint.md) or [**excludeImport**](excludeimport.md) elements appearing after the [**path**](path.md) element in an XML configuration file will be ignored.</span></span>

## <a name="element-information"></a><span data-ttu-id="639e8-125">項目資訊</span><span class="sxs-lookup"><span data-stu-id="639e8-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="639e8-126">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="639e8-126">Minimum supported system</span></span><br/> | <span data-ttu-id="639e8-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="639e8-127">Windows Vista</span></span> |
| <span data-ttu-id="639e8-128">可以是空的</span><span class="sxs-lookup"><span data-stu-id="639e8-128">Can be empty</span></span>                        | <span data-ttu-id="639e8-129">否</span><span class="sxs-lookup"><span data-stu-id="639e8-129">No</span></span>            |



 

 




