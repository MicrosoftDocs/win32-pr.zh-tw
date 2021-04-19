---
description: 定義針對命名空間中的宏名稱所產生的程式碼中所使用的前置詞。
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: macroPrefix 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76c88dc48505e3344db1467463a9a99639edd881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985634"
---
# <a name="macroprefix-element"></a><span data-ttu-id="d06c9-103">macroPrefix 元素</span><span class="sxs-lookup"><span data-stu-id="d06c9-103">macroPrefix element</span></span>

<span data-ttu-id="d06c9-104">定義針對命名空間中的宏名稱所產生的程式碼中所使用的前置詞。</span><span class="sxs-lookup"><span data-stu-id="d06c9-104">Defines the prefix to be used in the generated code for names of macros in the namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="d06c9-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="d06c9-105">Usage</span></span>

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="d06c9-106">屬性</span><span class="sxs-lookup"><span data-stu-id="d06c9-106">Attributes</span></span>

<span data-ttu-id="d06c9-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="d06c9-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d06c9-108">子元素</span><span class="sxs-lookup"><span data-stu-id="d06c9-108">Child elements</span></span>

<span data-ttu-id="d06c9-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="d06c9-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d06c9-110">父元素</span><span class="sxs-lookup"><span data-stu-id="d06c9-110">Parent elements</span></span>



| <span data-ttu-id="d06c9-111">元素</span><span class="sxs-lookup"><span data-stu-id="d06c9-111">Element</span></span>                                   | <span data-ttu-id="d06c9-112">描述</span><span class="sxs-lookup"><span data-stu-id="d06c9-112">Description</span></span>                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="d06c9-113">**命名 空間**</span><span class="sxs-lookup"><span data-stu-id="d06c9-113">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="d06c9-114">要用於產生程式碼的命名空間。</span><span class="sxs-lookup"><span data-stu-id="d06c9-114">A namespace to be used for code generation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d06c9-115">備註</span><span class="sxs-lookup"><span data-stu-id="d06c9-115">Remarks</span></span>

<span data-ttu-id="d06c9-116">這個元素會覆寫用於產生之宏的預設 URI 前置詞。</span><span class="sxs-lookup"><span data-stu-id="d06c9-116">This element overrides the default URI prefix used for generated macros.</span></span> <span data-ttu-id="d06c9-117">例如，如果宏前置詞為 "AV \_ " 且名稱為 "調諧器"，則為限定名稱產生的宏將會是 "av \_ 調諧器"。</span><span class="sxs-lookup"><span data-stu-id="d06c9-117">For example, if the macro prefix is "AV\_" and the name is "Tuner", the macro generated for the qualified name will be "AV\_Tuner".</span></span>

<span data-ttu-id="d06c9-118">根據預設，產生的程式碼會從 URI 建立慣用的宏前置詞。</span><span class="sxs-lookup"><span data-stu-id="d06c9-118">By default, the code generated creates a preferred macro prefix from the URI.</span></span>

## <a name="element-information"></a><span data-ttu-id="d06c9-119">項目資訊</span><span class="sxs-lookup"><span data-stu-id="d06c9-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="d06c9-120">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="d06c9-120">Minimum supported system</span></span><br/> | <span data-ttu-id="d06c9-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d06c9-121">Windows Vista</span></span> |
| <span data-ttu-id="d06c9-122">可以是空的</span><span class="sxs-lookup"><span data-stu-id="d06c9-122">Can be empty</span></span>                        | <span data-ttu-id="d06c9-123">是</span><span class="sxs-lookup"><span data-stu-id="d06c9-123">Yes</span></span>           |



 

 




