---
description: 定義用來在產生的程式碼中識別命名空間的名稱。
ms.assetid: 4e476be2-fa73-4b3e-b0cc-799c8d16b5de
title: codeName 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9be7292135e79477d0a66d2a0667ebd51bd7567c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994945"
---
# <a name="codename-element"></a><span data-ttu-id="b41c3-103">codeName 元素</span><span class="sxs-lookup"><span data-stu-id="b41c3-103">codeName element</span></span>

<span data-ttu-id="b41c3-104">定義用來在產生的程式碼中識別命名空間的名稱。</span><span class="sxs-lookup"><span data-stu-id="b41c3-104">Defines the name to be used to identify the namespace in generated code.</span></span>

## <a name="usage"></a><span data-ttu-id="b41c3-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="b41c3-105">Usage</span></span>

``` syntax
<codeName/>
```

## <a name="attributes"></a><span data-ttu-id="b41c3-106">屬性</span><span class="sxs-lookup"><span data-stu-id="b41c3-106">Attributes</span></span>

<span data-ttu-id="b41c3-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="b41c3-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b41c3-108">子元素</span><span class="sxs-lookup"><span data-stu-id="b41c3-108">Child elements</span></span>

<span data-ttu-id="b41c3-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="b41c3-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b41c3-110">父元素</span><span class="sxs-lookup"><span data-stu-id="b41c3-110">Parent elements</span></span>



| <span data-ttu-id="b41c3-111">元素</span><span class="sxs-lookup"><span data-stu-id="b41c3-111">Element</span></span>                                                         | <span data-ttu-id="b41c3-112">描述</span><span class="sxs-lookup"><span data-stu-id="b41c3-112">Description</span></span>                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="b41c3-113">**命名 空間**</span><span class="sxs-lookup"><span data-stu-id="b41c3-113">**nameSpace**</span></span>](namespace.md)<br/>                       | <span data-ttu-id="b41c3-114">要用於產生程式碼的命名空間。</span><span class="sxs-lookup"><span data-stu-id="b41c3-114">A namespace to be used for code generation.</span></span><br/> <br/>       |
| [<span data-ttu-id="b41c3-115">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b41c3-115">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/> | <span data-ttu-id="b41c3-116">產生埠類型的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="b41c3-116">Generates C constant declarations for port types.</span></span><br/> <br/> |
| [<span data-ttu-id="b41c3-117">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="b41c3-117">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>   | <span data-ttu-id="b41c3-118">產生埠類型的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="b41c3-118">Generates C constants for port types.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="b41c3-119">備註</span><span class="sxs-lookup"><span data-stu-id="b41c3-119">Remarks</span></span>

<span data-ttu-id="b41c3-120">這個元素會覆寫用於產生之程式碼的預設程式碼名稱。</span><span class="sxs-lookup"><span data-stu-id="b41c3-120">This element overrides the default code name used for generated code.</span></span> <span data-ttu-id="b41c3-121">根據預設，產生的程式碼會從 URI 或限定名稱建立程式碼名稱。</span><span class="sxs-lookup"><span data-stu-id="b41c3-121">By default, the code generated creates a code name from the URI or qualified name.</span></span>

## <a name="element-information"></a><span data-ttu-id="b41c3-122">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b41c3-122">Element information</span></span>



| <span data-ttu-id="b41c3-123">標籤</span><span class="sxs-lookup"><span data-stu-id="b41c3-123">Label</span></span> | <span data-ttu-id="b41c3-124">值</span><span class="sxs-lookup"><span data-stu-id="b41c3-124">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="b41c3-125">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="b41c3-125">Minimum supported system</span></span><br/> | <span data-ttu-id="b41c3-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b41c3-126">Windows Vista</span></span> |
| <span data-ttu-id="b41c3-127">可以是空的</span><span class="sxs-lookup"><span data-stu-id="b41c3-127">Can be empty</span></span>                        | <span data-ttu-id="b41c3-128">是</span><span class="sxs-lookup"><span data-stu-id="b41c3-128">Yes</span></span>           |



 

 




