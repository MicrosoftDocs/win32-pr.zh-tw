---
description: Time 屬性指定參數採用新值的時間（相對於轉換或效果的開頭）。
ms.assetid: bb478215-cbd5-4fea-9d88-a1f2b002f3da
title: 時間屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15a84d40c5e38ed81f8c17cd2d931e3f85e389a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195445"
---
# <a name="time-attribute"></a><span data-ttu-id="19262-103">時間屬性</span><span class="sxs-lookup"><span data-stu-id="19262-103">time Attribute</span></span>

> [!Note]  
> <span data-ttu-id="19262-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="19262-104">\[Deprecated.</span></span> <span data-ttu-id="19262-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="19262-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="19262-106">`time`屬性指定參數採用新值的時間（相對於轉換或效果的開頭）。</span><span class="sxs-lookup"><span data-stu-id="19262-106">The `time` attribute specifies the time at which a parameter assumes a new value, relative to the start of the transition or effect.</span></span>

## <a name="possible-values"></a><span data-ttu-id="19262-107">可能的值</span><span class="sxs-lookup"><span data-stu-id="19262-107">Possible Values</span></span>

<span data-ttu-id="19262-108">必須是格式為 *hh： mm： ss* 格式的字串，其中 *hh* = hours， *mm* = 分鐘， *ss* = 秒，而 *ff* = 秒數的分數。</span><span class="sxs-lookup"><span data-stu-id="19262-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="19262-109">範例：1：04：30.512。</span><span class="sxs-lookup"><span data-stu-id="19262-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="19262-110">您可以省略前置單位。</span><span class="sxs-lookup"><span data-stu-id="19262-110">Leading units can be omitted.</span></span> <span data-ttu-id="19262-111">例如，3:00 (三分鐘) 和 45 (45 秒) 都有效。</span><span class="sxs-lookup"><span data-stu-id="19262-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="19262-112">套用至</span><span class="sxs-lookup"><span data-stu-id="19262-112">Applies To</span></span>

<span data-ttu-id="19262-113">[**at**](at-element.md)、 [**線性**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="19262-113">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="19262-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19262-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19262-115">XTL 屬性</span><span class="sxs-lookup"><span data-stu-id="19262-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> </dl>

 

 



