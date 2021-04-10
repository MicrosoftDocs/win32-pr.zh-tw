---
description: 針對訊息類型產生 XML 架構資料表的 C 常數宣告。
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: messageTypeDeclarations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 700511d3c0a83badcb15b0e07491a14ade53f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944929"
---
# <a name="messagetypedeclarations-element"></a><span data-ttu-id="ac214-103">messageTypeDeclarations 元素</span><span class="sxs-lookup"><span data-stu-id="ac214-103">messageTypeDeclarations element</span></span>

<span data-ttu-id="ac214-104">針對訊息類型產生 XML 架構資料表的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="ac214-104">Generates C constant declarations for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="ac214-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="ac214-105">Usage</span></span>

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="ac214-106">屬性</span><span class="sxs-lookup"><span data-stu-id="ac214-106">Attributes</span></span>

<span data-ttu-id="ac214-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ac214-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ac214-108">子元素</span><span class="sxs-lookup"><span data-stu-id="ac214-108">Child elements</span></span>



| <span data-ttu-id="ac214-109">元素</span><span class="sxs-lookup"><span data-stu-id="ac214-109">Element</span></span>                                   | <span data-ttu-id="ac214-110">描述</span><span class="sxs-lookup"><span data-stu-id="ac214-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="ac214-111">**操作**</span><span class="sxs-lookup"><span data-stu-id="ac214-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="ac214-112">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="ac214-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="ac214-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="ac214-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="ac214-114">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="ac214-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="ac214-115">子項目順序</span><span class="sxs-lookup"><span data-stu-id="ac214-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="ac214-116">父元素</span><span class="sxs-lookup"><span data-stu-id="ac214-116">Parent elements</span></span>



| <span data-ttu-id="ac214-117">元素</span><span class="sxs-lookup"><span data-stu-id="ac214-117">Element</span></span>                         | <span data-ttu-id="ac214-118">描述</span><span class="sxs-lookup"><span data-stu-id="ac214-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="ac214-119">**檔**</span><span class="sxs-lookup"><span data-stu-id="ac214-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="ac214-120">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="ac214-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ac214-121">備註</span><span class="sxs-lookup"><span data-stu-id="ac214-121">Remarks</span></span>

<span data-ttu-id="ac214-122">架構資料表是由埠類型定義所參考。</span><span class="sxs-lookup"><span data-stu-id="ac214-122">Schema tables are referenced by port type definitions.</span></span> <span data-ttu-id="ac214-123">因此，這個元素通常會在 [**portTypeDefinitions**](porttypedefinitions.md) 元素之前使用。</span><span class="sxs-lookup"><span data-stu-id="ac214-123">This element is therefore generally used just prior to [**portTypeDefinitions**](porttypedefinitions.md) elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="ac214-124">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ac214-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="ac214-125">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="ac214-125">Minimum supported system</span></span><br/> | <span data-ttu-id="ac214-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ac214-126">Windows Vista</span></span> |
| <span data-ttu-id="ac214-127">可以是空的</span><span class="sxs-lookup"><span data-stu-id="ac214-127">Can be empty</span></span>                        | <span data-ttu-id="ac214-128">是</span><span class="sxs-lookup"><span data-stu-id="ac214-128">Yes</span></span>           |



 

 




