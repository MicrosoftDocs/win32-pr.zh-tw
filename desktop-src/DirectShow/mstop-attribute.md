---
description: Mstop 屬性會指定剪輯的停止時間（相對於原始媒體檔案）。
ms.assetid: 01559d29-9c7b-4842-a1f7-16552adbda43
title: mstop 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a63f52a1b912392165293e008074cf64a03b9751
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108480"
---
# <a name="mstop-attribute"></a><span data-ttu-id="44e10-103">mstop 屬性</span><span class="sxs-lookup"><span data-stu-id="44e10-103">mstop Attribute</span></span>

> [!Note]  
> <span data-ttu-id="44e10-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="44e10-104">\[Deprecated.</span></span> <span data-ttu-id="44e10-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="44e10-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="44e10-106">`mstop`屬性會指定相對於原始媒體檔案的剪輯停止時間。</span><span class="sxs-lookup"><span data-stu-id="44e10-106">The `mstop` attribute specifies the stop time of a clip, relative to the original media file.</span></span>

## <a name="applies-to"></a><span data-ttu-id="44e10-107">套用至</span><span class="sxs-lookup"><span data-stu-id="44e10-107">Applies To</span></span>

[<span data-ttu-id="44e10-108">**clip**</span><span class="sxs-lookup"><span data-stu-id="44e10-108">**clip**</span></span>](clip-element.md)

## <a name="possible-values"></a><span data-ttu-id="44e10-109">可能的值</span><span class="sxs-lookup"><span data-stu-id="44e10-109">Possible Values</span></span>

<span data-ttu-id="44e10-110">必須是格式為 *hh： mm： ss* 格式的字串，其中 *hh* = hours， *mm* = 分鐘， *ss* = 秒，而 *ff* = 秒數的分數。</span><span class="sxs-lookup"><span data-stu-id="44e10-110">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="44e10-111">範例：1：04：30.512。</span><span class="sxs-lookup"><span data-stu-id="44e10-111">Example: 1:04:30.512.</span></span> <span data-ttu-id="44e10-112">您可以省略前置單位。</span><span class="sxs-lookup"><span data-stu-id="44e10-112">Leading units can be omitted.</span></span> <span data-ttu-id="44e10-113">例如，3:00 (三分鐘) 和 45 (45 秒) 都有效。</span><span class="sxs-lookup"><span data-stu-id="44e10-113">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="see-also"></a><span data-ttu-id="44e10-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44e10-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44e10-115">XTL 屬性</span><span class="sxs-lookup"><span data-stu-id="44e10-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="44e10-116">**IAMTimelineSrc::SetMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="44e10-116">**IAMTimelineSrc::SetMediaTimes**</span></span>](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



