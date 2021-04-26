---
description: 指定要包含在 XSD 檔案中的類型。
ms.assetid: dd3894a8-1848-4ae0-ba6c-42ac4fe36ff3
title: typeUri 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9ef0a2482354fcfd962a7e41a7c2b94b54f5cb
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998685"
---
# <a name="typeuri-element"></a><span data-ttu-id="b6da9-103">typeUri 元素</span><span class="sxs-lookup"><span data-stu-id="b6da9-103">typeUri element</span></span>

<span data-ttu-id="b6da9-104">指定要包含在 XSD 檔案中的類型。</span><span class="sxs-lookup"><span data-stu-id="b6da9-104">Specifies a type to include from an XSD file.</span></span>

## <a name="usage"></a><span data-ttu-id="b6da9-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="b6da9-105">Usage</span></span>

``` syntax
<typeUri
  type = "character_string"
  uri = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="b6da9-106">屬性</span><span class="sxs-lookup"><span data-stu-id="b6da9-106">Attributes</span></span>



| <span data-ttu-id="b6da9-107">屬性</span><span class="sxs-lookup"><span data-stu-id="b6da9-107">Attribute</span></span>           | <span data-ttu-id="b6da9-108">類型</span><span class="sxs-lookup"><span data-stu-id="b6da9-108">Type</span></span>                         | <span data-ttu-id="b6da9-109">必要</span><span class="sxs-lookup"><span data-stu-id="b6da9-109">Required</span></span>       | <span data-ttu-id="b6da9-110">描述</span><span class="sxs-lookup"><span data-stu-id="b6da9-110">Description</span></span>                                                            |
|---------------------|------------------------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="b6da9-111">**type**</span><span class="sxs-lookup"><span data-stu-id="b6da9-111">**type**</span></span><br/> | <span data-ttu-id="b6da9-112">字元 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="b6da9-112">character\_string</span></span><br/> | <span data-ttu-id="b6da9-113">Yes</span><span class="sxs-lookup"><span data-stu-id="b6da9-113">Yes</span></span><br/> | <span data-ttu-id="b6da9-114">型別的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6da9-114">The name of the type.</span></span><br/> <br/>                           |
| <span data-ttu-id="b6da9-115">**uri**</span><span class="sxs-lookup"><span data-stu-id="b6da9-115">**uri**</span></span><br/>  | <span data-ttu-id="b6da9-116">字元 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="b6da9-116">character\_string</span></span><br/> | <span data-ttu-id="b6da9-117">Yes</span><span class="sxs-lookup"><span data-stu-id="b6da9-117">Yes</span></span><br/> | <span data-ttu-id="b6da9-118">型別的命名空間。</span><span class="sxs-lookup"><span data-stu-id="b6da9-118">The namespace of the type.</span></span> <span data-ttu-id="b6da9-119">必須是有效的 URI。</span><span class="sxs-lookup"><span data-stu-id="b6da9-119">Must be a valid URI.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="b6da9-120">子元素</span><span class="sxs-lookup"><span data-stu-id="b6da9-120">Child elements</span></span>

<span data-ttu-id="b6da9-121">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="b6da9-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b6da9-122">父元素</span><span class="sxs-lookup"><span data-stu-id="b6da9-122">Parent elements</span></span>



| <span data-ttu-id="b6da9-123">元素</span><span class="sxs-lookup"><span data-stu-id="b6da9-123">Element</span></span>                       | <span data-ttu-id="b6da9-124">描述</span><span class="sxs-lookup"><span data-stu-id="b6da9-124">Description</span></span>                                                                       |
|-------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="b6da9-125">**Xsd**</span><span class="sxs-lookup"><span data-stu-id="b6da9-125">**xsd**</span></span>](xsd.md)<br/> | <span data-ttu-id="b6da9-126">指定要針對合約資訊處理的 XSD 檔案。</span><span class="sxs-lookup"><span data-stu-id="b6da9-126">Specifies an XSD file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="b6da9-127">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b6da9-127">Element information</span></span>



| <span data-ttu-id="b6da9-128">標籤</span><span class="sxs-lookup"><span data-stu-id="b6da9-128">Label</span></span> | <span data-ttu-id="b6da9-129">值</span><span class="sxs-lookup"><span data-stu-id="b6da9-129">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="b6da9-130">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="b6da9-130">Minimum supported system</span></span><br/> | <span data-ttu-id="b6da9-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6da9-131">Windows Vista</span></span> |
| <span data-ttu-id="b6da9-132">可以是空的</span><span class="sxs-lookup"><span data-stu-id="b6da9-132">Can be empty</span></span>                        | <span data-ttu-id="b6da9-133">是</span><span class="sxs-lookup"><span data-stu-id="b6da9-133">Yes</span></span>           |



 

 




