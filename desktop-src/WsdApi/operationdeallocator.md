---
description: 指定作業存根函式所要使用的類型釋放器。
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: operationDeallocator 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c214b5dbc3245f63797c55880fe052d5c3ced15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974468"
---
# <a name="operationdeallocator-element"></a><span data-ttu-id="563cc-103">operationDeallocator 元素</span><span class="sxs-lookup"><span data-stu-id="563cc-103">operationDeallocator element</span></span>

<span data-ttu-id="563cc-104">指定作業的存根函數所要使用的類型釋放器。</span><span class="sxs-lookup"><span data-stu-id="563cc-104">Specifies the type deallocator to be used by an operation's stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="563cc-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="563cc-105">Usage</span></span>

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="563cc-106">屬性</span><span class="sxs-lookup"><span data-stu-id="563cc-106">Attributes</span></span>



| <span data-ttu-id="563cc-107">屬性</span><span class="sxs-lookup"><span data-stu-id="563cc-107">Attribute</span></span>                  | <span data-ttu-id="563cc-108">類型</span><span class="sxs-lookup"><span data-stu-id="563cc-108">Type</span></span>                         | <span data-ttu-id="563cc-109">必要</span><span class="sxs-lookup"><span data-stu-id="563cc-109">Required</span></span>       | <span data-ttu-id="563cc-110">描述</span><span class="sxs-lookup"><span data-stu-id="563cc-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="563cc-111">**釋放器**</span><span class="sxs-lookup"><span data-stu-id="563cc-111">**deallocator**</span></span><br/> | <span data-ttu-id="563cc-112">字元 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="563cc-112">character\_string</span></span><br/> | <span data-ttu-id="563cc-113">Yes</span><span class="sxs-lookup"><span data-stu-id="563cc-113">Yes</span></span><br/> | <span data-ttu-id="563cc-114">要用於作業的釋放器。</span><span class="sxs-lookup"><span data-stu-id="563cc-114">The deallocator to use for the operation.</span></span><br/> <br/> <span data-ttu-id="563cc-115">下列字串是有效的值。</span><span class="sxs-lookup"><span data-stu-id="563cc-115">The following strings are valid values.</span></span><br/> <br/> <dl><span data-ttu-id="563cc-116"><span id="none"></span><span id="NONE"></span><dt>\* \* \* \* 無 \*</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> \* \* *<dt>* \* \* \* WSDFreeLinkedMemory \*</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> \* \* *<dt>* \* \* \* CoTaskMemFree \*</dt> <span id="free"></span> <span id="FREE"></span> \* \* *<dt>* \* \* \* 免費 \*</dt> <span id="delete"></span> <span id="DELETE"></span> \* \* *<dt>* \* \* \* 刪除 \* \*</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> \* *<dt>* \* \* \* deleteArray \*</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> \* \* *<dt>* \* \* \* 發行 \*</dt> \* \*</span><span class="sxs-lookup"><span data-stu-id="563cc-116"><span id="none"></span><span id="NONE"></span><dt>\*\*\*\*none\*\*\*\*</dt><span id="WSDFreeLinkedMemory"></span><span id="wsdfreelinkedmemory"></span><span id="WSDFREELINKEDMEMORY"></span><dt>\*\*\*\*WSDFreeLinkedMemory\*\*\*\*</dt><span id="CoTaskMemFree"></span><span id="cotaskmemfree"></span><span id="COTASKMEMFREE"></span><dt>\*\*\*\*CoTaskMemFree\*\*\*\*</dt><span id="free"></span><span id="FREE"></span><dt>\*\*\*\*free\*\*\*\*</dt><span id="delete"></span><span id="DELETE"></span><dt>\*\*\*\*delete\*\*\*\*</dt><span id="deleteArray"></span><span id="deletearray"></span><span id="DELETEARRAY"></span><dt>\*\*\*\*deleteArray\*\*\*\*</dt><span id="Release"></span><span id="release"></span><span id="RELEASE"></span><dt>\*\*\*\*Release\*\*\*\*</dt></span></span> </dl> |
| <span data-ttu-id="563cc-117">**operation**</span><span class="sxs-lookup"><span data-stu-id="563cc-117">**operation**</span></span><br/>   | <span data-ttu-id="563cc-118">字元 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="563cc-118">character\_string</span></span><br/> | <span data-ttu-id="563cc-119">Yes</span><span class="sxs-lookup"><span data-stu-id="563cc-119">Yes</span></span><br/> | <span data-ttu-id="563cc-120">作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="563cc-120">The name of the operation.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a><span data-ttu-id="563cc-121">子元素</span><span class="sxs-lookup"><span data-stu-id="563cc-121">Child elements</span></span>

<span data-ttu-id="563cc-122">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="563cc-122">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="563cc-123">父元素</span><span class="sxs-lookup"><span data-stu-id="563cc-123">Parent elements</span></span>



| <span data-ttu-id="563cc-124">元素</span><span class="sxs-lookup"><span data-stu-id="563cc-124">Element</span></span>                                               | <span data-ttu-id="563cc-125">描述</span><span class="sxs-lookup"><span data-stu-id="563cc-125">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="563cc-126">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="563cc-126">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="563cc-127">針對埠類型作業產生存根函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="563cc-127">Generates implementations for stub functions for port type operations.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="563cc-128">項目資訊</span><span class="sxs-lookup"><span data-stu-id="563cc-128">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="563cc-129">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="563cc-129">Minimum supported system</span></span><br/> | <span data-ttu-id="563cc-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="563cc-130">Windows Vista</span></span> |
| <span data-ttu-id="563cc-131">可以是空的</span><span class="sxs-lookup"><span data-stu-id="563cc-131">Can be empty</span></span>                        | <span data-ttu-id="563cc-132">是</span><span class="sxs-lookup"><span data-stu-id="563cc-132">Yes</span></span>           |



 

 




