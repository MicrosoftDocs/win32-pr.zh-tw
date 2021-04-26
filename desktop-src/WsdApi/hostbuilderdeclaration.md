---
description: 產生函式的宣告，這個函式會建立具類型的主控制項。
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: hostBuilderDeclaration 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf3ddd474b4000b053b49157f1fc4b2eb399d34
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994905"
---
# <a name="hostbuilderdeclaration-element"></a><span data-ttu-id="30a2c-103">hostBuilderDeclaration 元素</span><span class="sxs-lookup"><span data-stu-id="30a2c-103">hostBuilderDeclaration element</span></span>

<span data-ttu-id="30a2c-104">產生函式的宣告，這個函式會建立具類型的主控制項。</span><span class="sxs-lookup"><span data-stu-id="30a2c-104">Generates a declaration for a function that creates a typed host.</span></span>

## <a name="usage"></a><span data-ttu-id="30a2c-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="30a2c-105">Usage</span></span>

``` syntax
<hostBuilderDeclaration>
  child elements
</hostBuilderDeclaration>
```

## <a name="attributes"></a><span data-ttu-id="30a2c-106">屬性</span><span class="sxs-lookup"><span data-stu-id="30a2c-106">Attributes</span></span>

<span data-ttu-id="30a2c-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="30a2c-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="30a2c-108">子元素</span><span class="sxs-lookup"><span data-stu-id="30a2c-108">Child elements</span></span>



| <span data-ttu-id="30a2c-109">元素</span><span class="sxs-lookup"><span data-stu-id="30a2c-109">Element</span></span>                                   | <span data-ttu-id="30a2c-110">描述</span><span class="sxs-lookup"><span data-stu-id="30a2c-110">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30a2c-111">**介面**</span><span class="sxs-lookup"><span data-stu-id="30a2c-111">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="30a2c-112">要為主機包含的服務介面名稱。</span><span class="sxs-lookup"><span data-stu-id="30a2c-112">The name of service interface to be included for host.</span></span> <span data-ttu-id="30a2c-113">此元素的值必須符合 [**hostedService**](hostedservice.md)的 [**介面**](interface.md)子項目值。</span><span class="sxs-lookup"><span data-stu-id="30a2c-113">The value of this element must match the value of the [**interface**](interface.md) child element of [**hostedService**](hostedservice.md).</span></span> <br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="30a2c-114">子項目順序</span><span class="sxs-lookup"><span data-stu-id="30a2c-114">Child element sequence</span></span>

``` syntax
interface+
```

## <a name="parent-elements"></a><span data-ttu-id="30a2c-115">父元素</span><span class="sxs-lookup"><span data-stu-id="30a2c-115">Parent elements</span></span>



| <span data-ttu-id="30a2c-116">元素</span><span class="sxs-lookup"><span data-stu-id="30a2c-116">Element</span></span>                         | <span data-ttu-id="30a2c-117">描述</span><span class="sxs-lookup"><span data-stu-id="30a2c-117">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="30a2c-118">**檔**</span><span class="sxs-lookup"><span data-stu-id="30a2c-118">**file**</span></span>](file.md)<br/> | <span data-ttu-id="30a2c-119">從程式碼產生器輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="30a2c-119">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="30a2c-120">項目資訊</span><span class="sxs-lookup"><span data-stu-id="30a2c-120">Element information</span></span>



| <span data-ttu-id="30a2c-121">標籤</span><span class="sxs-lookup"><span data-stu-id="30a2c-121">Label</span></span> | <span data-ttu-id="30a2c-122">值</span><span class="sxs-lookup"><span data-stu-id="30a2c-122">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="30a2c-123">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="30a2c-123">Minimum supported system</span></span><br/> | <span data-ttu-id="30a2c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30a2c-124">Windows Vista</span></span> |
| <span data-ttu-id="30a2c-125">可以是空的</span><span class="sxs-lookup"><span data-stu-id="30a2c-125">Can be empty</span></span>                        | <span data-ttu-id="30a2c-126">否</span><span class="sxs-lookup"><span data-stu-id="30a2c-126">No</span></span>            |



 

 




