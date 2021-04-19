---
description: 產生已知類型的 C 結構定義。
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: structDefinitions 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33ca9ac9ce3f9e868646c0bfff260238c30e572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971865"
---
# <a name="structdefinitions-element"></a><span data-ttu-id="7b69d-103">structDefinitions 元素</span><span class="sxs-lookup"><span data-stu-id="7b69d-103">structDefinitions element</span></span>

<span data-ttu-id="7b69d-104">產生已知類型的 C 結構定義。</span><span class="sxs-lookup"><span data-stu-id="7b69d-104">Generates C structure definitions for known types.</span></span>

## <a name="usage"></a><span data-ttu-id="7b69d-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="7b69d-105">Usage</span></span>

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a><span data-ttu-id="7b69d-106">屬性</span><span class="sxs-lookup"><span data-stu-id="7b69d-106">Attributes</span></span>

<span data-ttu-id="7b69d-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="7b69d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7b69d-108">子元素</span><span class="sxs-lookup"><span data-stu-id="7b69d-108">Child elements</span></span>

<span data-ttu-id="7b69d-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="7b69d-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7b69d-110">父元素</span><span class="sxs-lookup"><span data-stu-id="7b69d-110">Parent elements</span></span>



| <span data-ttu-id="7b69d-111">元素</span><span class="sxs-lookup"><span data-stu-id="7b69d-111">Element</span></span>                         | <span data-ttu-id="7b69d-112">描述</span><span class="sxs-lookup"><span data-stu-id="7b69d-112">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="7b69d-113">**檔**</span><span class="sxs-lookup"><span data-stu-id="7b69d-113">**file**</span></span>](file.md)<br/> | <span data-ttu-id="7b69d-114">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="7b69d-114">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7b69d-115">備註</span><span class="sxs-lookup"><span data-stu-id="7b69d-115">Remarks</span></span>

<span data-ttu-id="7b69d-116">已知類型的結構會由許多產生的程式碼和應用程式程式碼所參考。</span><span class="sxs-lookup"><span data-stu-id="7b69d-116">Structures for known types are referenced by much of the generated code and by application code.</span></span> <span data-ttu-id="7b69d-117">此元素用來產生 include 檔案。</span><span class="sxs-lookup"><span data-stu-id="7b69d-117">This element is used to generate include files.</span></span> <span data-ttu-id="7b69d-118">這個元素應該會在 [**structDeclarations**](structdeclarations.md) 元素之後發生，以便妥善處理結構之間的參考。</span><span class="sxs-lookup"><span data-stu-id="7b69d-118">This element should occur after a [**structDeclarations**](structdeclarations.md) element so that references between structures are handled properly.</span></span>

## <a name="element-information"></a><span data-ttu-id="7b69d-119">項目資訊</span><span class="sxs-lookup"><span data-stu-id="7b69d-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="7b69d-120">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="7b69d-120">Minimum supported system</span></span><br/> | <span data-ttu-id="7b69d-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b69d-121">Windows Vista</span></span> |
| <span data-ttu-id="7b69d-122">可以是空的</span><span class="sxs-lookup"><span data-stu-id="7b69d-122">Can be empty</span></span>                        | <span data-ttu-id="7b69d-123">是</span><span class="sxs-lookup"><span data-stu-id="7b69d-123">Yes</span></span>           |



 

 




