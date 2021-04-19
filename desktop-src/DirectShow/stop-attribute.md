---
description: Stop 屬性會指定相對於父物件之物件的停止時間。
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: stop 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6deb3f2a422cb8100da32c0427caf6436e72fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985037"
---
# <a name="stop-attribute"></a><span data-ttu-id="d4c96-103">stop 屬性</span><span class="sxs-lookup"><span data-stu-id="d4c96-103">stop Attribute</span></span>

> [!Note]  
> <span data-ttu-id="d4c96-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="d4c96-104">\[Deprecated.</span></span> <span data-ttu-id="d4c96-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="d4c96-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d4c96-106">`stop`屬性會指定相對於父物件之物件的停止時間。</span><span class="sxs-lookup"><span data-stu-id="d4c96-106">The `stop` attribute specifies the stop time of an object, relative to the parent object.</span></span>

## <a name="possible-values"></a><span data-ttu-id="d4c96-107">可能的值</span><span class="sxs-lookup"><span data-stu-id="d4c96-107">Possible Values</span></span>

<span data-ttu-id="d4c96-108">必須是格式為 *hh： mm： ss* 格式的字串，其中 *hh* = hours， *mm* = 分鐘， *ss* = 秒，而 *ff* = 秒數的分數。</span><span class="sxs-lookup"><span data-stu-id="d4c96-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="d4c96-109">範例：1：04：30.512。</span><span class="sxs-lookup"><span data-stu-id="d4c96-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="d4c96-110">您可以省略前置單位。</span><span class="sxs-lookup"><span data-stu-id="d4c96-110">Leading units can be omitted.</span></span> <span data-ttu-id="d4c96-111">例如，3:00 (三分鐘) 和 45 (45 秒) 都有效。</span><span class="sxs-lookup"><span data-stu-id="d4c96-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="d4c96-112">套用至</span><span class="sxs-lookup"><span data-stu-id="d4c96-112">Applies To</span></span>

<span data-ttu-id="d4c96-113">[**剪輯**](clip-element.md)、 [**效果**](effect-element.md)、 [**轉換**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="d4c96-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="d4c96-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4c96-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c96-115">XTL 屬性</span><span class="sxs-lookup"><span data-stu-id="d4c96-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="d4c96-116">**IAMTimelineObj::SetStartStop**</span><span class="sxs-lookup"><span data-stu-id="d4c96-116">**IAMTimelineObj::SetStartStop**</span></span>](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



