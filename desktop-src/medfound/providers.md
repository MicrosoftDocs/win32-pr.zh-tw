---
description: 包含 MFTrace 的追蹤提供者清單。
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: providers 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e5aaedcd14d840cfdc0d85559f6a7981943593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191760"
---
# <a name="providers-element"></a><span data-ttu-id="07eff-103">providers 元素</span><span class="sxs-lookup"><span data-stu-id="07eff-103">providers element</span></span>

<span data-ttu-id="07eff-104">包含 [MFTrace](mftrace.md)的追蹤提供者清單。</span><span class="sxs-lookup"><span data-stu-id="07eff-104">Contains a list of trace providers for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="07eff-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="07eff-105">Usage</span></span>

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a><span data-ttu-id="07eff-106">屬性</span><span class="sxs-lookup"><span data-stu-id="07eff-106">Attributes</span></span>

<span data-ttu-id="07eff-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="07eff-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="07eff-108">子元素</span><span class="sxs-lookup"><span data-stu-id="07eff-108">Child elements</span></span>



| <span data-ttu-id="07eff-109">元素</span><span class="sxs-lookup"><span data-stu-id="07eff-109">Element</span></span>                                   | <span data-ttu-id="07eff-110">描述</span><span class="sxs-lookup"><span data-stu-id="07eff-110">Description</span></span>                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07eff-111">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="07eff-111">**mfdetours**</span></span>](mfdetours.md)<br/> | <span data-ttu-id="07eff-112">指定媒體基礎繞道提供者，此提供者會追蹤媒體基礎的 API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="07eff-112">Specifies the Media Foundation Detours provider, which traces Media Foundation API calls.</span></span><br/> <br/> |
| [<span data-ttu-id="07eff-113">**供應商**</span><span class="sxs-lookup"><span data-stu-id="07eff-113">**provider**</span></span>](provider.md)<br/>   | <span data-ttu-id="07eff-114">指定追蹤提供者 (ETW 或 WPP) 。</span><span class="sxs-lookup"><span data-stu-id="07eff-114">Specifies a trace provider (ETW or WPP).</span></span><br/> <br/>                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="07eff-115">子項目順序</span><span class="sxs-lookup"><span data-stu-id="07eff-115">Child element sequence</span></span>

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a><span data-ttu-id="07eff-116">父元素</span><span class="sxs-lookup"><span data-stu-id="07eff-116">Parent elements</span></span>

<span data-ttu-id="07eff-117">沒有父元素。</span><span class="sxs-lookup"><span data-stu-id="07eff-117">There are no parent elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="07eff-118">項目資訊</span><span class="sxs-lookup"><span data-stu-id="07eff-118">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="07eff-119">可以是空的</span><span class="sxs-lookup"><span data-stu-id="07eff-119">Can be empty</span></span> | <span data-ttu-id="07eff-120">Yes</span><span class="sxs-lookup"><span data-stu-id="07eff-120">Yes</span></span> |



## <a name="see-also"></a><span data-ttu-id="07eff-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07eff-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07eff-122">MFTrace 設定檔</span><span class="sxs-lookup"><span data-stu-id="07eff-122">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




