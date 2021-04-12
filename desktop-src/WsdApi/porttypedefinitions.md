---
description: 產生埠類型的 C 常數。
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: portTypeDefinitions 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60f55408df938ed95af14c69b2676473ac1bda71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192907"
---
# <a name="porttypedefinitions-element"></a><span data-ttu-id="bbc2b-103">portTypeDefinitions 元素</span><span class="sxs-lookup"><span data-stu-id="bbc2b-103">portTypeDefinitions element</span></span>

<span data-ttu-id="bbc2b-104">產生埠類型的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="bbc2b-104">Generates C constants for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="bbc2b-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="bbc2b-105">Usage</span></span>

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="bbc2b-106">屬性</span><span class="sxs-lookup"><span data-stu-id="bbc2b-106">Attributes</span></span>

<span data-ttu-id="bbc2b-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="bbc2b-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="bbc2b-108">子元素</span><span class="sxs-lookup"><span data-stu-id="bbc2b-108">Child elements</span></span>



| <span data-ttu-id="bbc2b-109">元素</span><span class="sxs-lookup"><span data-stu-id="bbc2b-109">Element</span></span>                                                   | <span data-ttu-id="bbc2b-110">描述</span><span class="sxs-lookup"><span data-stu-id="bbc2b-110">Description</span></span>                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbc2b-111">**代號**</span><span class="sxs-lookup"><span data-stu-id="bbc2b-111">**codeName**</span></span>](codename.md)<br/>                   | <span data-ttu-id="bbc2b-112">指定要在產生的程式碼中用於埠類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="bbc2b-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="bbc2b-113">根據預設，會從埠類型的限定名稱產生程式碼名稱。</span><span class="sxs-lookup"><span data-stu-id="bbc2b-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/>         |
| [<span data-ttu-id="bbc2b-114">**eventStubFunction**</span><span class="sxs-lookup"><span data-stu-id="bbc2b-114">**eventStubFunction**</span></span>](eventstubfunction.md)<br/> | <span data-ttu-id="bbc2b-115">指定存根函數參考是否應該包含在通知作業的埠類型定義中的作業結構中。</span><span class="sxs-lookup"><span data-stu-id="bbc2b-115">Specifies whether stub function references should be included in the operation structures in the port type definitions for notification operations.</span></span><br/> <br/>        |
| [<span data-ttu-id="bbc2b-116">**操作**</span><span class="sxs-lookup"><span data-stu-id="bbc2b-116">**operation**</span></span>](operation.md)<br/>                 | <span data-ttu-id="bbc2b-117">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="bbc2b-117">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                                  |
| [<span data-ttu-id="bbc2b-118">**portType**</span><span class="sxs-lookup"><span data-stu-id="bbc2b-118">**portType**</span></span>](porttype.md)<br/>                   | <span data-ttu-id="bbc2b-119">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="bbc2b-119">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                                 |
| [<span data-ttu-id="bbc2b-120">**stubFunction**</span><span class="sxs-lookup"><span data-stu-id="bbc2b-120">**stubFunction**</span></span>](stubfunction.md)<br/>           | <span data-ttu-id="bbc2b-121">指定存根函式參考是否應該包含在單向和雙向作業的埠類型定義中的作業結構中。</span><span class="sxs-lookup"><span data-stu-id="bbc2b-121">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="bbc2b-122">子項目順序</span><span class="sxs-lookup"><span data-stu-id="bbc2b-122">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="bbc2b-123">父元素</span><span class="sxs-lookup"><span data-stu-id="bbc2b-123">Parent elements</span></span>



| <span data-ttu-id="bbc2b-124">元素</span><span class="sxs-lookup"><span data-stu-id="bbc2b-124">Element</span></span>                         | <span data-ttu-id="bbc2b-125">描述</span><span class="sxs-lookup"><span data-stu-id="bbc2b-125">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="bbc2b-126">**檔**</span><span class="sxs-lookup"><span data-stu-id="bbc2b-126">**file**</span></span>](file.md)<br/> | <span data-ttu-id="bbc2b-127">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="bbc2b-127">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="bbc2b-128">備註</span><span class="sxs-lookup"><span data-stu-id="bbc2b-128">Remarks</span></span>

<span data-ttu-id="bbc2b-129">此元素通常用於 C 來源檔案，以提供 [**portTypeDeclarations**](porttypedeclarations.md)所宣告的埠類型常數。</span><span class="sxs-lookup"><span data-stu-id="bbc2b-129">This element is generally used in C source files to provide the port type constants declared by [**portTypeDeclarations**](porttypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="bbc2b-130">項目資訊</span><span class="sxs-lookup"><span data-stu-id="bbc2b-130">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="bbc2b-131">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="bbc2b-131">Minimum supported system</span></span><br/> | <span data-ttu-id="bbc2b-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbc2b-132">Windows Vista</span></span> |
| <span data-ttu-id="bbc2b-133">可以是空的</span><span class="sxs-lookup"><span data-stu-id="bbc2b-133">Can be empty</span></span>                        | <span data-ttu-id="bbc2b-134">是</span><span class="sxs-lookup"><span data-stu-id="bbc2b-134">Yes</span></span>           |



 

 




