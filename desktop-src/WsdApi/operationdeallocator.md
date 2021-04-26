---
description: 指定作業存根函式所要使用的類型釋放器。
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: operationDeallocator 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3ae0d9f1d37a478ceca0895806ade6a011747e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994285"
---
# <a name="operationdeallocator-element"></a><span data-ttu-id="6fa29-103">operationDeallocator 元素</span><span class="sxs-lookup"><span data-stu-id="6fa29-103">operationDeallocator element</span></span>

<span data-ttu-id="6fa29-104">指定作業的存根函數所要使用的類型釋放器。</span><span class="sxs-lookup"><span data-stu-id="6fa29-104">Specifies the type deallocator to be used by an operation's stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="6fa29-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="6fa29-105">Usage</span></span>

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="6fa29-106">屬性</span><span class="sxs-lookup"><span data-stu-id="6fa29-106">Attributes</span></span>



| <span data-ttu-id="6fa29-107">屬性</span><span class="sxs-lookup"><span data-stu-id="6fa29-107">Attribute</span></span>                  | <span data-ttu-id="6fa29-108">類型</span><span class="sxs-lookup"><span data-stu-id="6fa29-108">Type</span></span>                         | <span data-ttu-id="6fa29-109">必要</span><span class="sxs-lookup"><span data-stu-id="6fa29-109">Required</span></span>       | <span data-ttu-id="6fa29-110">描述</span><span class="sxs-lookup"><span data-stu-id="6fa29-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa29-111">**釋放器**</span><span class="sxs-lookup"><span data-stu-id="6fa29-111">**deallocator**</span></span><br/> | <span data-ttu-id="6fa29-112">字元 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="6fa29-112">character\_string</span></span><br/> | <span data-ttu-id="6fa29-113">Yes</span><span class="sxs-lookup"><span data-stu-id="6fa29-113">Yes</span></span><br/> | <span data-ttu-id="6fa29-114">要用於作業的釋放器。</span><span class="sxs-lookup"><span data-stu-id="6fa29-114">The deallocator to use for the operation.</span></span><br/> <br/> <span data-ttu-id="6fa29-115">下列字串是有效的值。</span><span class="sxs-lookup"><span data-stu-id="6fa29-115">The following strings are valid values.</span></span><br/> <br/> <dl><span data-ttu-id="6fa29-116"><span id="none"></span><span id="NONE"></span><dt>\* \* \* \* 無 \*</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> \* \* *<dt>* \* \* \* WSDFreeLinkedMemory \*</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> \* \* *<dt>* \* \* \* CoTaskMemFree \*</dt> <span id="free"></span> <span id="FREE"></span> \* \* *<dt>* \* \* \* 免費 \*</dt> <span id="delete"></span> <span id="DELETE"></span> \* \* *<dt>* \* \* \* 刪除 \* \*</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> \* *<dt>* \* \* \* deleteArray \*</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> \* \* *<dt>* \* \* \* 發行 \*</dt> \* \*</span><span class="sxs-lookup"><span data-stu-id="6fa29-116"><span id="none"></span><span id="NONE"></span><dt>\*\*\*\*none\*\*\*\*</dt><span id="WSDFreeLinkedMemory"></span><span id="wsdfreelinkedmemory"></span><span id="WSDFREELINKEDMEMORY"></span><dt>\*\*\*\*WSDFreeLinkedMemory\*\*\*\*</dt><span id="CoTaskMemFree"></span><span id="cotaskmemfree"></span><span id="COTASKMEMFREE"></span><dt>\*\*\*\*CoTaskMemFree\*\*\*\*</dt><span id="free"></span><span id="FREE"></span><dt>\*\*\*\*free\*\*\*\*</dt><span id="delete"></span><span id="DELETE"></span><dt>\*\*\*\*delete\*\*\*\*</dt><span id="deleteArray"></span><span id="deletearray"></span><span id="DELETEARRAY"></span><dt>\*\*\*\*deleteArray\*\*\*\*</dt><span id="Release"></span><span id="release"></span><span id="RELEASE"></span><dt>\*\*\*\*Release\*\*\*\*</dt></span></span> </dl> |
| <span data-ttu-id="6fa29-117">**operation**</span><span class="sxs-lookup"><span data-stu-id="6fa29-117">**operation**</span></span><br/>   | <span data-ttu-id="6fa29-118">字元 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="6fa29-118">character\_string</span></span><br/> | <span data-ttu-id="6fa29-119">Yes</span><span class="sxs-lookup"><span data-stu-id="6fa29-119">Yes</span></span><br/> | <span data-ttu-id="6fa29-120">作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fa29-120">The name of the operation.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a><span data-ttu-id="6fa29-121">子元素</span><span class="sxs-lookup"><span data-stu-id="6fa29-121">Child elements</span></span>

<span data-ttu-id="6fa29-122">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="6fa29-122">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="6fa29-123">父元素</span><span class="sxs-lookup"><span data-stu-id="6fa29-123">Parent elements</span></span>



| <span data-ttu-id="6fa29-124">元素</span><span class="sxs-lookup"><span data-stu-id="6fa29-124">Element</span></span>                                               | <span data-ttu-id="6fa29-125">描述</span><span class="sxs-lookup"><span data-stu-id="6fa29-125">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6fa29-126">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="6fa29-126">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="6fa29-127">針對埠類型作業產生存根函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="6fa29-127">Generates implementations for stub functions for port type operations.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="6fa29-128">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6fa29-128">Element information</span></span>



| <span data-ttu-id="6fa29-129">標籤</span><span class="sxs-lookup"><span data-stu-id="6fa29-129">Label</span></span> | <span data-ttu-id="6fa29-130">值</span><span class="sxs-lookup"><span data-stu-id="6fa29-130">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="6fa29-131">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="6fa29-131">Minimum supported system</span></span><br/> | <span data-ttu-id="6fa29-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6fa29-132">Windows Vista</span></span> |
| <span data-ttu-id="6fa29-133">可以是空的</span><span class="sxs-lookup"><span data-stu-id="6fa29-133">Can be empty</span></span>                        | <span data-ttu-id="6fa29-134">是</span><span class="sxs-lookup"><span data-stu-id="6fa29-134">Yes</span></span>           |



 

 




