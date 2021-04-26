---
description: 產生已知類型的 C 結構定義。
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: structDefinitions 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f680db18b06253362f932cc7d34d5b85f7c1b5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996455"
---
# <a name="structdefinitions-element"></a><span data-ttu-id="8fa3e-103">structDefinitions 元素</span><span class="sxs-lookup"><span data-stu-id="8fa3e-103">structDefinitions element</span></span>

<span data-ttu-id="8fa3e-104">產生已知類型的 C 結構定義。</span><span class="sxs-lookup"><span data-stu-id="8fa3e-104">Generates C structure definitions for known types.</span></span>

## <a name="usage"></a><span data-ttu-id="8fa3e-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="8fa3e-105">Usage</span></span>

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a><span data-ttu-id="8fa3e-106">屬性</span><span class="sxs-lookup"><span data-stu-id="8fa3e-106">Attributes</span></span>

<span data-ttu-id="8fa3e-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="8fa3e-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8fa3e-108">子元素</span><span class="sxs-lookup"><span data-stu-id="8fa3e-108">Child elements</span></span>

<span data-ttu-id="8fa3e-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="8fa3e-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="8fa3e-110">父元素</span><span class="sxs-lookup"><span data-stu-id="8fa3e-110">Parent elements</span></span>



| <span data-ttu-id="8fa3e-111">元素</span><span class="sxs-lookup"><span data-stu-id="8fa3e-111">Element</span></span>                         | <span data-ttu-id="8fa3e-112">描述</span><span class="sxs-lookup"><span data-stu-id="8fa3e-112">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="8fa3e-113">**檔**</span><span class="sxs-lookup"><span data-stu-id="8fa3e-113">**file**</span></span>](file.md)<br/> | <span data-ttu-id="8fa3e-114">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="8fa3e-114">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8fa3e-115">備註</span><span class="sxs-lookup"><span data-stu-id="8fa3e-115">Remarks</span></span>

<span data-ttu-id="8fa3e-116">已知類型的結構會由許多產生的程式碼和應用程式程式碼所參考。</span><span class="sxs-lookup"><span data-stu-id="8fa3e-116">Structures for known types are referenced by much of the generated code and by application code.</span></span> <span data-ttu-id="8fa3e-117">此元素用來產生 include 檔案。</span><span class="sxs-lookup"><span data-stu-id="8fa3e-117">This element is used to generate include files.</span></span> <span data-ttu-id="8fa3e-118">這個元素應該會在 [**structDeclarations**](structdeclarations.md) 元素之後發生，以便妥善處理結構之間的參考。</span><span class="sxs-lookup"><span data-stu-id="8fa3e-118">This element should occur after a [**structDeclarations**](structdeclarations.md) element so that references between structures are handled properly.</span></span>

## <a name="element-information"></a><span data-ttu-id="8fa3e-119">項目資訊</span><span class="sxs-lookup"><span data-stu-id="8fa3e-119">Element information</span></span>



| <span data-ttu-id="8fa3e-120">標籤</span><span class="sxs-lookup"><span data-stu-id="8fa3e-120">Label</span></span> | <span data-ttu-id="8fa3e-121">值</span><span class="sxs-lookup"><span data-stu-id="8fa3e-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="8fa3e-122">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="8fa3e-122">Minimum supported system</span></span><br/> | <span data-ttu-id="8fa3e-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8fa3e-123">Windows Vista</span></span> |
| <span data-ttu-id="8fa3e-124">可以是空的</span><span class="sxs-lookup"><span data-stu-id="8fa3e-124">Can be empty</span></span>                        | <span data-ttu-id="8fa3e-125">是</span><span class="sxs-lookup"><span data-stu-id="8fa3e-125">Yes</span></span>           |



 

 




