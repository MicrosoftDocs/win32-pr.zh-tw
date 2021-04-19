---
description: 產生 QueryInterface、AddRef 和 Release 函數的實作為。
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: IUnknownDefinitions 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ca92338e3dc97a12e04228510fc17eb2ef2483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977845"
---
# <a name="iunknowndefinitions-element"></a><span data-ttu-id="91042-103">IUnknownDefinitions 元素</span><span class="sxs-lookup"><span data-stu-id="91042-103">IUnknownDefinitions element</span></span>

<span data-ttu-id="91042-104">產生 QueryInterface、AddRef 和 Release 函數的實作為。</span><span class="sxs-lookup"><span data-stu-id="91042-104">Generates implementations for the QueryInterface, AddRef and Release functions.</span></span>

## <a name="usage"></a><span data-ttu-id="91042-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="91042-105">Usage</span></span>

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="91042-106">屬性</span><span class="sxs-lookup"><span data-stu-id="91042-106">Attributes</span></span>



| <span data-ttu-id="91042-107">屬性</span><span class="sxs-lookup"><span data-stu-id="91042-107">Attribute</span></span>                  | <span data-ttu-id="91042-108">類型</span><span class="sxs-lookup"><span data-stu-id="91042-108">Type</span></span>                         | <span data-ttu-id="91042-109">必要</span><span class="sxs-lookup"><span data-stu-id="91042-109">Required</span></span>       | <span data-ttu-id="91042-110">描述</span><span class="sxs-lookup"><span data-stu-id="91042-110">Description</span></span>                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| <span data-ttu-id="91042-111">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="91042-111">**proxyClass**</span></span><br/>  | <span data-ttu-id="91042-112">字元 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="91042-112">character\_string</span></span><br/> | <span data-ttu-id="91042-113">Yes</span><span class="sxs-lookup"><span data-stu-id="91042-113">Yes</span></span><br/> | <span data-ttu-id="91042-114">執行類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="91042-114">The name of the implementing class.</span></span><br/> <br/> |
| <span data-ttu-id="91042-115">**refCountVar**</span><span class="sxs-lookup"><span data-stu-id="91042-115">**refCountVar**</span></span><br/> | <span data-ttu-id="91042-116">字元 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="91042-116">character\_string</span></span><br/> | <span data-ttu-id="91042-117">Yes</span><span class="sxs-lookup"><span data-stu-id="91042-117">Yes</span></span><br/> | <span data-ttu-id="91042-118">參考計數變數名稱。</span><span class="sxs-lookup"><span data-stu-id="91042-118">The reference count variable name.</span></span><br/> <br/>  |



## <a name="child-elements"></a><span data-ttu-id="91042-119">子元素</span><span class="sxs-lookup"><span data-stu-id="91042-119">Child elements</span></span>



| <span data-ttu-id="91042-120">元素</span><span class="sxs-lookup"><span data-stu-id="91042-120">Element</span></span>                                   | <span data-ttu-id="91042-121">描述</span><span class="sxs-lookup"><span data-stu-id="91042-121">Description</span></span>                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="91042-122">**介面**</span><span class="sxs-lookup"><span data-stu-id="91042-122">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="91042-123">QueryInterface 要傳回的介面名稱。</span><span class="sxs-lookup"><span data-stu-id="91042-123">The name of the interface to be returned by QueryInterface.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="91042-124">子項目順序</span><span class="sxs-lookup"><span data-stu-id="91042-124">Child element sequence</span></span>

``` syntax
interface
```

## <a name="parent-elements"></a><span data-ttu-id="91042-125">父元素</span><span class="sxs-lookup"><span data-stu-id="91042-125">Parent elements</span></span>



| <span data-ttu-id="91042-126">元素</span><span class="sxs-lookup"><span data-stu-id="91042-126">Element</span></span>                         | <span data-ttu-id="91042-127">描述</span><span class="sxs-lookup"><span data-stu-id="91042-127">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="91042-128">**檔**</span><span class="sxs-lookup"><span data-stu-id="91042-128">**file**</span></span>](file.md)<br/> | <span data-ttu-id="91042-129">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="91042-129">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="91042-130">項目資訊</span><span class="sxs-lookup"><span data-stu-id="91042-130">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="91042-131">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="91042-131">Minimum supported system</span></span><br/> | <span data-ttu-id="91042-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91042-132">Windows Vista</span></span> |
| <span data-ttu-id="91042-133">可以是空的</span><span class="sxs-lookup"><span data-stu-id="91042-133">Can be empty</span></span>                        | <span data-ttu-id="91042-134">否</span><span class="sxs-lookup"><span data-stu-id="91042-134">No</span></span>            |



 

 




