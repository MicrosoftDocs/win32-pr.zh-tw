---
description: At 元素會在特定時間定義 param 專案的值，相對於包含參數的轉換或效果的開頭。
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: at 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb539331519fb23b6b8aa45b374457229f807a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688308"
---
# <a name="at-element"></a><span data-ttu-id="b1ae3-103">at 元素</span><span class="sxs-lookup"><span data-stu-id="b1ae3-103">at Element</span></span>

> [!Note]  
> <span data-ttu-id="b1ae3-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="b1ae3-104">\[Deprecated.</span></span> <span data-ttu-id="b1ae3-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="b1ae3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b1ae3-106">專案 `at` 會在特定時間定義 [**param**](param-element.md) 專案的值，相對於包含參數的轉換或效果的開頭。</span><span class="sxs-lookup"><span data-stu-id="b1ae3-106">The `at` element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the parameter.</span></span> <span data-ttu-id="b1ae3-107">`at`元素會在指定的時間，讓參數跳到新值。</span><span class="sxs-lookup"><span data-stu-id="b1ae3-107">The `at` element causes the parameter to jump abruptly to the new value at the given time.</span></span> <span data-ttu-id="b1ae3-108">若要讓新值的進展順利進行，請使用 [**線性**](linear-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="b1ae3-108">For a smooth progression to a new value, use the [**linear**](linear-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="b1ae3-109">屬性</span><span class="sxs-lookup"><span data-stu-id="b1ae3-109">Attributes</span></span>

<span data-ttu-id="b1ae3-110">[**時間**](time-attribute.md)、 [**值**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="b1ae3-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="b1ae3-111">父系/子系資訊</span><span class="sxs-lookup"><span data-stu-id="b1ae3-111">Parent/Child Information</span></span>



|          |                                |
|----------|--------------------------------|
| <span data-ttu-id="b1ae3-112">父代</span><span class="sxs-lookup"><span data-stu-id="b1ae3-112">Parent</span></span>   | [<span data-ttu-id="b1ae3-113">**參數**</span><span class="sxs-lookup"><span data-stu-id="b1ae3-113">**param**</span></span>](param-element.md) |
| <span data-ttu-id="b1ae3-114">Children</span><span class="sxs-lookup"><span data-stu-id="b1ae3-114">Children</span></span> | <span data-ttu-id="b1ae3-115">無</span><span class="sxs-lookup"><span data-stu-id="b1ae3-115">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="b1ae3-116">範例</span><span class="sxs-lookup"><span data-stu-id="b1ae3-116">Examples</span></span>


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a><span data-ttu-id="b1ae3-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1ae3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1ae3-118">XTL 元素</span><span class="sxs-lookup"><span data-stu-id="b1ae3-118">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



