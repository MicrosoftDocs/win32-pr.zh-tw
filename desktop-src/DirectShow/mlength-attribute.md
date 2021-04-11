---
description: Mlength 屬性會指定原始程式檔的持續時間。 此值必須是實際的持續時間，否則可能會發生轉譯錯誤。
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: mlength 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eadc288e29d99df0e6af7f06e1404d86f6a938
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935604"
---
# <a name="mlength-attribute"></a><span data-ttu-id="9e415-104">mlength 屬性</span><span class="sxs-lookup"><span data-stu-id="9e415-104">mlength Attribute</span></span>

> [!Note]  
> <span data-ttu-id="9e415-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="9e415-105">\[Deprecated.</span></span> <span data-ttu-id="9e415-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="9e415-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9e415-107">`mlength`屬性指定原始程式檔的持續時間。</span><span class="sxs-lookup"><span data-stu-id="9e415-107">The `mlength` attribute specifies the duration of a source file.</span></span> <span data-ttu-id="9e415-108">此值必須是實際的持續時間，否則可能會發生轉譯錯誤。</span><span class="sxs-lookup"><span data-stu-id="9e415-108">This value must be the actual duration, or rendering errors may occur.</span></span>

## <a name="applies-to"></a><span data-ttu-id="9e415-109">套用至</span><span class="sxs-lookup"><span data-stu-id="9e415-109">Applies To</span></span>

[<span data-ttu-id="9e415-110">**clip**</span><span class="sxs-lookup"><span data-stu-id="9e415-110">**clip**</span></span>](clip-element.md)

## <a name="possible-values"></a><span data-ttu-id="9e415-111">可能的值</span><span class="sxs-lookup"><span data-stu-id="9e415-111">Possible Values</span></span>

<span data-ttu-id="9e415-112">必須是格式為 *hh： mm： ss* 格式的字串，其中 *hh* = hours， *mm* = 分鐘， *ss* = 秒，而 *ff* = 秒數的分數。</span><span class="sxs-lookup"><span data-stu-id="9e415-112">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="9e415-113">範例：1：04：30.512。</span><span class="sxs-lookup"><span data-stu-id="9e415-113">Example: 1:04:30.512.</span></span> <span data-ttu-id="9e415-114">您可以省略前置單位。</span><span class="sxs-lookup"><span data-stu-id="9e415-114">Leading units can be omitted.</span></span> <span data-ttu-id="9e415-115">例如，3:00 (三分鐘) 和 45 (45 秒) 都有效。</span><span class="sxs-lookup"><span data-stu-id="9e415-115">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e415-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e415-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e415-117">XTL 屬性</span><span class="sxs-lookup"><span data-stu-id="9e415-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="9e415-118">**IAMTimelineSrc::SetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="9e415-118">**IAMTimelineSrc::SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



