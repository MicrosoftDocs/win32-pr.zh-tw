---
description: 針對埠類型作業產生存根函式的宣告。
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: stubDeclarations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1543883b4d41e7571cd4a4725e2aeab181530d30
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996405"
---
# <a name="stubdeclarations-element"></a><span data-ttu-id="39b1f-103">stubDeclarations 元素</span><span class="sxs-lookup"><span data-stu-id="39b1f-103">stubDeclarations element</span></span>

<span data-ttu-id="39b1f-104">針對埠類型作業產生存根函式的宣告。</span><span class="sxs-lookup"><span data-stu-id="39b1f-104">Generates declarations for stub functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="39b1f-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="39b1f-105">Usage</span></span>

``` syntax
<stubDeclarations>
  child elements
</stubDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="39b1f-106">屬性</span><span class="sxs-lookup"><span data-stu-id="39b1f-106">Attributes</span></span>

<span data-ttu-id="39b1f-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="39b1f-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="39b1f-108">子元素</span><span class="sxs-lookup"><span data-stu-id="39b1f-108">Child elements</span></span>



| <span data-ttu-id="39b1f-109">元素</span><span class="sxs-lookup"><span data-stu-id="39b1f-109">Element</span></span>                                   | <span data-ttu-id="39b1f-110">描述</span><span class="sxs-lookup"><span data-stu-id="39b1f-110">Description</span></span>                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39b1f-111">**事件**</span><span class="sxs-lookup"><span data-stu-id="39b1f-111">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="39b1f-112">指定產生的函數中是否包含相關事件。</span><span class="sxs-lookup"><span data-stu-id="39b1f-112">Specifies whether related events are included in the generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="39b1f-113">**操作**</span><span class="sxs-lookup"><span data-stu-id="39b1f-113">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="39b1f-114">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="39b1f-114">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                 |
| [<span data-ttu-id="39b1f-115">**portType**</span><span class="sxs-lookup"><span data-stu-id="39b1f-115">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="39b1f-116">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="39b1f-116">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                |



### <a name="child-element-sequence"></a><span data-ttu-id="39b1f-117">子項目順序</span><span class="sxs-lookup"><span data-stu-id="39b1f-117">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?
)
```

## <a name="parent-elements"></a><span data-ttu-id="39b1f-118">父元素</span><span class="sxs-lookup"><span data-stu-id="39b1f-118">Parent elements</span></span>



| <span data-ttu-id="39b1f-119">元素</span><span class="sxs-lookup"><span data-stu-id="39b1f-119">Element</span></span>                         | <span data-ttu-id="39b1f-120">描述</span><span class="sxs-lookup"><span data-stu-id="39b1f-120">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="39b1f-121">**檔**</span><span class="sxs-lookup"><span data-stu-id="39b1f-121">**file**</span></span>](file.md)<br/> | <span data-ttu-id="39b1f-122">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="39b1f-122">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="39b1f-123">項目資訊</span><span class="sxs-lookup"><span data-stu-id="39b1f-123">Element information</span></span>



| <span data-ttu-id="39b1f-124">標籤</span><span class="sxs-lookup"><span data-stu-id="39b1f-124">Label</span></span> | <span data-ttu-id="39b1f-125">值</span><span class="sxs-lookup"><span data-stu-id="39b1f-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="39b1f-126">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="39b1f-126">Minimum supported system</span></span><br/> | <span data-ttu-id="39b1f-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39b1f-127">Windows Vista</span></span> |
| <span data-ttu-id="39b1f-128">可以是空的</span><span class="sxs-lookup"><span data-stu-id="39b1f-128">Can be empty</span></span>                        | <span data-ttu-id="39b1f-129">是</span><span class="sxs-lookup"><span data-stu-id="39b1f-129">Yes</span></span>           |



 

 




