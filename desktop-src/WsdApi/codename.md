---
description: 定義用來在產生的程式碼中識別命名空間的名稱。
ms.assetid: 4e476be2-fa73-4b3e-b0cc-799c8d16b5de
title: codeName 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44c10b937f503c2d3994543db8852b5d7ee923b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985300"
---
# <a name="codename-element"></a><span data-ttu-id="f7145-103">codeName 元素</span><span class="sxs-lookup"><span data-stu-id="f7145-103">codeName element</span></span>

<span data-ttu-id="f7145-104">定義用來在產生的程式碼中識別命名空間的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7145-104">Defines the name to be used to identify the namespace in generated code.</span></span>

## <a name="usage"></a><span data-ttu-id="f7145-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="f7145-105">Usage</span></span>

``` syntax
<codeName/>
```

## <a name="attributes"></a><span data-ttu-id="f7145-106">屬性</span><span class="sxs-lookup"><span data-stu-id="f7145-106">Attributes</span></span>

<span data-ttu-id="f7145-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="f7145-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f7145-108">子元素</span><span class="sxs-lookup"><span data-stu-id="f7145-108">Child elements</span></span>

<span data-ttu-id="f7145-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="f7145-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f7145-110">父元素</span><span class="sxs-lookup"><span data-stu-id="f7145-110">Parent elements</span></span>



| <span data-ttu-id="f7145-111">元素</span><span class="sxs-lookup"><span data-stu-id="f7145-111">Element</span></span>                                                         | <span data-ttu-id="f7145-112">描述</span><span class="sxs-lookup"><span data-stu-id="f7145-112">Description</span></span>                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="f7145-113">**命名 空間**</span><span class="sxs-lookup"><span data-stu-id="f7145-113">**nameSpace**</span></span>](namespace.md)<br/>                       | <span data-ttu-id="f7145-114">要用於產生程式碼的命名空間。</span><span class="sxs-lookup"><span data-stu-id="f7145-114">A namespace to be used for code generation.</span></span><br/> <br/>       |
| [<span data-ttu-id="f7145-115">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="f7145-115">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/> | <span data-ttu-id="f7145-116">產生埠類型的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="f7145-116">Generates C constant declarations for port types.</span></span><br/> <br/> |
| [<span data-ttu-id="f7145-117">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="f7145-117">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>   | <span data-ttu-id="f7145-118">產生埠類型的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="f7145-118">Generates C constants for port types.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="f7145-119">備註</span><span class="sxs-lookup"><span data-stu-id="f7145-119">Remarks</span></span>

<span data-ttu-id="f7145-120">這個元素會覆寫用於產生之程式碼的預設程式碼名稱。</span><span class="sxs-lookup"><span data-stu-id="f7145-120">This element overrides the default code name used for generated code.</span></span> <span data-ttu-id="f7145-121">根據預設，產生的程式碼會從 URI 或限定名稱建立程式碼名稱。</span><span class="sxs-lookup"><span data-stu-id="f7145-121">By default, the code generated creates a code name from the URI or qualified name.</span></span>

## <a name="element-information"></a><span data-ttu-id="f7145-122">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f7145-122">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="f7145-123">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="f7145-123">Minimum supported system</span></span><br/> | <span data-ttu-id="f7145-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7145-124">Windows Vista</span></span> |
| <span data-ttu-id="f7145-125">可以是空的</span><span class="sxs-lookup"><span data-stu-id="f7145-125">Can be empty</span></span>                        | <span data-ttu-id="f7145-126">是</span><span class="sxs-lookup"><span data-stu-id="f7145-126">Yes</span></span>           |



 

 




