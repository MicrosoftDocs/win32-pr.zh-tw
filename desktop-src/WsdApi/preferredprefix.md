---
description: 定義應對應命名空間的前置詞，以便讓 XML 更容易讀取。
ms.assetid: 955f4785-5657-4a89-9728-bce99a0a4234
title: preferredPrefix 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71f124756f29aaf29ba30d254f9b03ab4495f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974385"
---
# <a name="preferredprefix-element"></a><span data-ttu-id="5e0d1-103">preferredPrefix 元素</span><span class="sxs-lookup"><span data-stu-id="5e0d1-103">preferredPrefix element</span></span>

<span data-ttu-id="5e0d1-104">定義應對應命名空間的前置詞，以便讓 XML 更容易讀取。</span><span class="sxs-lookup"><span data-stu-id="5e0d1-104">Defines the prefix to which the namespace should be mapped to make the XML more readable.</span></span>

## <a name="usage"></a><span data-ttu-id="5e0d1-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="5e0d1-105">Usage</span></span>

``` syntax
<preferredPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="5e0d1-106">屬性</span><span class="sxs-lookup"><span data-stu-id="5e0d1-106">Attributes</span></span>

<span data-ttu-id="5e0d1-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="5e0d1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5e0d1-108">子元素</span><span class="sxs-lookup"><span data-stu-id="5e0d1-108">Child elements</span></span>

<span data-ttu-id="5e0d1-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="5e0d1-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="5e0d1-110">父元素</span><span class="sxs-lookup"><span data-stu-id="5e0d1-110">Parent elements</span></span>



| <span data-ttu-id="5e0d1-111">元素</span><span class="sxs-lookup"><span data-stu-id="5e0d1-111">Element</span></span>                                   | <span data-ttu-id="5e0d1-112">描述</span><span class="sxs-lookup"><span data-stu-id="5e0d1-112">Description</span></span>                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="5e0d1-113">**命名 空間**</span><span class="sxs-lookup"><span data-stu-id="5e0d1-113">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="5e0d1-114">要用於產生程式碼的命名空間。</span><span class="sxs-lookup"><span data-stu-id="5e0d1-114">A namespace to be used for code generation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5e0d1-115">備註</span><span class="sxs-lookup"><span data-stu-id="5e0d1-115">Remarks</span></span>

<span data-ttu-id="5e0d1-116">這個元素會覆寫用於產生之程式碼的預設 URI 前置詞。</span><span class="sxs-lookup"><span data-stu-id="5e0d1-116">This element overrides the default URI prefix used for generated code.</span></span> <span data-ttu-id="5e0d1-117">例如，媒體相關的命名空間可能會有適用于音訊/視覺效果) 的慣用首碼 "av" (。</span><span class="sxs-lookup"><span data-stu-id="5e0d1-117">For example, a media-related namespace might have the preferred prefix "av" (for audio/visual).</span></span>

<span data-ttu-id="5e0d1-118">根據預設，產生的程式碼會從 URI 建立慣用的前置詞。</span><span class="sxs-lookup"><span data-stu-id="5e0d1-118">By default, the code generated creates a preferred prefix from the URI.</span></span>

## <a name="element-information"></a><span data-ttu-id="5e0d1-119">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5e0d1-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="5e0d1-120">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="5e0d1-120">Minimum supported system</span></span><br/> | <span data-ttu-id="5e0d1-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e0d1-121">Windows Vista</span></span> |
| <span data-ttu-id="5e0d1-122">可以是空的</span><span class="sxs-lookup"><span data-stu-id="5e0d1-122">Can be empty</span></span>                        | <span data-ttu-id="5e0d1-123">是</span><span class="sxs-lookup"><span data-stu-id="5e0d1-123">Yes</span></span>           |



 

 




