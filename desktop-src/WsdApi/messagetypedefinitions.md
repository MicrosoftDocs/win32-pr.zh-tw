---
description: 針對訊息類型產生 XML 架構資料表的 C 常數。
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: messageTypeDefinitions 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f1b6563254a93122960b4a990fe0bd18ab1453
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998705"
---
# <a name="messagetypedefinitions-element"></a><span data-ttu-id="6aeb6-103">messageTypeDefinitions 元素</span><span class="sxs-lookup"><span data-stu-id="6aeb6-103">messageTypeDefinitions element</span></span>

<span data-ttu-id="6aeb6-104">針對訊息類型產生 XML 架構資料表的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="6aeb6-104">Generates C constants for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="6aeb6-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="6aeb6-105">Usage</span></span>

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="6aeb6-106">屬性</span><span class="sxs-lookup"><span data-stu-id="6aeb6-106">Attributes</span></span>

<span data-ttu-id="6aeb6-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="6aeb6-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6aeb6-108">子元素</span><span class="sxs-lookup"><span data-stu-id="6aeb6-108">Child elements</span></span>



| <span data-ttu-id="6aeb6-109">元素</span><span class="sxs-lookup"><span data-stu-id="6aeb6-109">Element</span></span>                                   | <span data-ttu-id="6aeb6-110">描述</span><span class="sxs-lookup"><span data-stu-id="6aeb6-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="6aeb6-111">**操作**</span><span class="sxs-lookup"><span data-stu-id="6aeb6-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="6aeb6-112">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="6aeb6-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="6aeb6-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="6aeb6-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="6aeb6-114">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="6aeb6-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="6aeb6-115">子項目順序</span><span class="sxs-lookup"><span data-stu-id="6aeb6-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="6aeb6-116">父元素</span><span class="sxs-lookup"><span data-stu-id="6aeb6-116">Parent elements</span></span>



| <span data-ttu-id="6aeb6-117">元素</span><span class="sxs-lookup"><span data-stu-id="6aeb6-117">Element</span></span>                         | <span data-ttu-id="6aeb6-118">描述</span><span class="sxs-lookup"><span data-stu-id="6aeb6-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="6aeb6-119">**檔**</span><span class="sxs-lookup"><span data-stu-id="6aeb6-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="6aeb6-120">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="6aeb6-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6aeb6-121">備註</span><span class="sxs-lookup"><span data-stu-id="6aeb6-121">Remarks</span></span>

<span data-ttu-id="6aeb6-122">此元素通常用於 C 來源檔案，以提供 [**messageTypeDeclarations**](messagetypedeclarations.md)所宣告的架構資料表。</span><span class="sxs-lookup"><span data-stu-id="6aeb6-122">This element is generally used in C source files to provide the schema tables declared by [**messageTypeDeclarations**](messagetypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="6aeb6-123">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6aeb6-123">Element information</span></span>



| <span data-ttu-id="6aeb6-124">標籤</span><span class="sxs-lookup"><span data-stu-id="6aeb6-124">Label</span></span> | <span data-ttu-id="6aeb6-125">值</span><span class="sxs-lookup"><span data-stu-id="6aeb6-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="6aeb6-126">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="6aeb6-126">Minimum supported system</span></span><br/> | <span data-ttu-id="6aeb6-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6aeb6-127">Windows Vista</span></span> |
| <span data-ttu-id="6aeb6-128">可以是空的</span><span class="sxs-lookup"><span data-stu-id="6aeb6-128">Can be empty</span></span>                        | <span data-ttu-id="6aeb6-129">是</span><span class="sxs-lookup"><span data-stu-id="6aeb6-129">Yes</span></span>           |



 

 




