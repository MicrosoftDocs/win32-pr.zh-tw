---
description: 指定要針對合約資訊處理的 XSD 檔案。
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: xsd 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9628a078129446f51729c92c447f8da5736dab88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849400"
---
# <a name="xsd-element"></a><span data-ttu-id="22c93-103">xsd 元素</span><span class="sxs-lookup"><span data-stu-id="22c93-103">xsd element</span></span>

<span data-ttu-id="22c93-104">指定要針對合約資訊處理的 XSD 檔案。</span><span class="sxs-lookup"><span data-stu-id="22c93-104">Specifies an XSD file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="22c93-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="22c93-105">Usage</span></span>

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a><span data-ttu-id="22c93-106">屬性</span><span class="sxs-lookup"><span data-stu-id="22c93-106">Attributes</span></span>



| <span data-ttu-id="22c93-107">屬性</span><span class="sxs-lookup"><span data-stu-id="22c93-107">Attribute</span></span>           | <span data-ttu-id="22c93-108">類型</span><span class="sxs-lookup"><span data-stu-id="22c93-108">Type</span></span>                       | <span data-ttu-id="22c93-109">必要</span><span class="sxs-lookup"><span data-stu-id="22c93-109">Required</span></span>       | <span data-ttu-id="22c93-110">描述</span><span class="sxs-lookup"><span data-stu-id="22c93-110">Description</span></span>                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="22c93-111">**path**</span><span class="sxs-lookup"><span data-stu-id="22c93-111">**path**</span></span><br/> | <span data-ttu-id="22c93-112">pathname 字串</span><span class="sxs-lookup"><span data-stu-id="22c93-112">pathname string</span></span><br/> | <span data-ttu-id="22c93-113">Yes</span><span class="sxs-lookup"><span data-stu-id="22c93-113">Yes</span></span><br/> | <span data-ttu-id="22c93-114">XSD 輸入檔的檔案和路徑。</span><span class="sxs-lookup"><span data-stu-id="22c93-114">File and path of the XSD input file.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="22c93-115">子元素</span><span class="sxs-lookup"><span data-stu-id="22c93-115">Child elements</span></span>



| <span data-ttu-id="22c93-116">元素</span><span class="sxs-lookup"><span data-stu-id="22c93-116">Element</span></span>                               | <span data-ttu-id="22c93-117">描述</span><span class="sxs-lookup"><span data-stu-id="22c93-117">Description</span></span>                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="22c93-118">**typeUri**</span><span class="sxs-lookup"><span data-stu-id="22c93-118">**typeUri**</span></span>](typeuri.md)<br/> | <span data-ttu-id="22c93-119">指定要包含在 XSD 檔案中的類型。</span><span class="sxs-lookup"><span data-stu-id="22c93-119">Specifies a type to include from an XSD file.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="22c93-120">子項目順序</span><span class="sxs-lookup"><span data-stu-id="22c93-120">Child element sequence</span></span>

``` syntax
typeUri*
```

## <a name="parent-elements"></a><span data-ttu-id="22c93-121">父元素</span><span class="sxs-lookup"><span data-stu-id="22c93-121">Parent elements</span></span>



| <span data-ttu-id="22c93-122">元素</span><span class="sxs-lookup"><span data-stu-id="22c93-122">Element</span></span>                                     | <span data-ttu-id="22c93-123">描述</span><span class="sxs-lookup"><span data-stu-id="22c93-123">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="22c93-124">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="22c93-124">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="22c93-125">WSDAPI 程式碼產生器 XML 腳本檔的根項目。</span><span class="sxs-lookup"><span data-stu-id="22c93-125">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="22c93-126">備註</span><span class="sxs-lookup"><span data-stu-id="22c93-126">Remarks</span></span>

<span data-ttu-id="22c93-127">檔案名字串也應該包含完整的路徑資訊。</span><span class="sxs-lookup"><span data-stu-id="22c93-127">The filename string should include complete path information as well.</span></span>

## <a name="element-information"></a><span data-ttu-id="22c93-128">項目資訊</span><span class="sxs-lookup"><span data-stu-id="22c93-128">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="22c93-129">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="22c93-129">Minimum supported system</span></span><br/> | <span data-ttu-id="22c93-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22c93-130">Windows Vista</span></span> |
| <span data-ttu-id="22c93-131">可以是空的</span><span class="sxs-lookup"><span data-stu-id="22c93-131">Can be empty</span></span>                        | <span data-ttu-id="22c93-132">是</span><span class="sxs-lookup"><span data-stu-id="22c93-132">Yes</span></span>           |



 

 




