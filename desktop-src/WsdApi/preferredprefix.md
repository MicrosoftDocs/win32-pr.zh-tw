---
description: 定義應對應命名空間的前置詞，以便讓 XML 更容易讀取。
ms.assetid: 955f4785-5657-4a89-9728-bce99a0a4234
title: preferredPrefix 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98fa0310872a43811ceb626ae0684fa45a2f6666
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996475"
---
# <a name="preferredprefix-element"></a><span data-ttu-id="c3a9c-103">preferredPrefix 元素</span><span class="sxs-lookup"><span data-stu-id="c3a9c-103">preferredPrefix element</span></span>

<span data-ttu-id="c3a9c-104">定義應對應命名空間的前置詞，以便讓 XML 更容易讀取。</span><span class="sxs-lookup"><span data-stu-id="c3a9c-104">Defines the prefix to which the namespace should be mapped to make the XML more readable.</span></span>

## <a name="usage"></a><span data-ttu-id="c3a9c-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="c3a9c-105">Usage</span></span>

``` syntax
<preferredPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="c3a9c-106">屬性</span><span class="sxs-lookup"><span data-stu-id="c3a9c-106">Attributes</span></span>

<span data-ttu-id="c3a9c-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="c3a9c-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c3a9c-108">子元素</span><span class="sxs-lookup"><span data-stu-id="c3a9c-108">Child elements</span></span>

<span data-ttu-id="c3a9c-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="c3a9c-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="c3a9c-110">父元素</span><span class="sxs-lookup"><span data-stu-id="c3a9c-110">Parent elements</span></span>



| <span data-ttu-id="c3a9c-111">元素</span><span class="sxs-lookup"><span data-stu-id="c3a9c-111">Element</span></span>                                   | <span data-ttu-id="c3a9c-112">描述</span><span class="sxs-lookup"><span data-stu-id="c3a9c-112">Description</span></span>                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="c3a9c-113">**命名 空間**</span><span class="sxs-lookup"><span data-stu-id="c3a9c-113">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="c3a9c-114">要用於產生程式碼的命名空間。</span><span class="sxs-lookup"><span data-stu-id="c3a9c-114">A namespace to be used for code generation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c3a9c-115">備註</span><span class="sxs-lookup"><span data-stu-id="c3a9c-115">Remarks</span></span>

<span data-ttu-id="c3a9c-116">這個元素會覆寫用於產生之程式碼的預設 URI 前置詞。</span><span class="sxs-lookup"><span data-stu-id="c3a9c-116">This element overrides the default URI prefix used for generated code.</span></span> <span data-ttu-id="c3a9c-117">例如，媒體相關的命名空間可能會有適用于音訊/視覺效果) 的慣用首碼 "av" (。</span><span class="sxs-lookup"><span data-stu-id="c3a9c-117">For example, a media-related namespace might have the preferred prefix "av" (for audio/visual).</span></span>

<span data-ttu-id="c3a9c-118">根據預設，產生的程式碼會從 URI 建立慣用的前置詞。</span><span class="sxs-lookup"><span data-stu-id="c3a9c-118">By default, the code generated creates a preferred prefix from the URI.</span></span>

## <a name="element-information"></a><span data-ttu-id="c3a9c-119">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c3a9c-119">Element information</span></span>



| <span data-ttu-id="c3a9c-120">標籤</span><span class="sxs-lookup"><span data-stu-id="c3a9c-120">Label</span></span> | <span data-ttu-id="c3a9c-121">值</span><span class="sxs-lookup"><span data-stu-id="c3a9c-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="c3a9c-122">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="c3a9c-122">Minimum supported system</span></span><br/> | <span data-ttu-id="c3a9c-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3a9c-123">Windows Vista</span></span> |
| <span data-ttu-id="c3a9c-124">可以是空的</span><span class="sxs-lookup"><span data-stu-id="c3a9c-124">Can be empty</span></span>                        | <span data-ttu-id="c3a9c-125">是</span><span class="sxs-lookup"><span data-stu-id="c3a9c-125">Yes</span></span>           |



 

 




