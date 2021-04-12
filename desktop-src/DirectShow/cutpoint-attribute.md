---
description: Cutpoint 屬性會指定當轉換轉譯為剪下時，轉換會從某個來源減少到下一個來源。 值相對於轉換開始。
ms.assetid: bdb0b8cd-025f-4b56-9cd4-f71c58ee809a
title: cutpoint 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd516bd67577906a0a06d8da692ffbd7563ce32f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109232"
---
# <a name="cutpoint-attribute"></a><span data-ttu-id="1dce7-104">cutpoint 屬性</span><span class="sxs-lookup"><span data-stu-id="1dce7-104">cutpoint Attribute</span></span>

> [!Note]  
> <span data-ttu-id="1dce7-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="1dce7-105">\[Deprecated.</span></span> <span data-ttu-id="1dce7-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="1dce7-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1dce7-107">當轉換轉譯 `cutpoint` 為剪下時，屬性會指定當轉換從某個來源減少到下一個來源時。</span><span class="sxs-lookup"><span data-stu-id="1dce7-107">The `cutpoint` attribute specifies when a transition cuts from one source to the next, if the transition is rendered as a cut.</span></span> <span data-ttu-id="1dce7-108">值相對於轉換開始。</span><span class="sxs-lookup"><span data-stu-id="1dce7-108">The value is relative to the start of the transition.</span></span>

## <a name="possible-values"></a><span data-ttu-id="1dce7-109">可能的值</span><span class="sxs-lookup"><span data-stu-id="1dce7-109">Possible Values</span></span>

<span data-ttu-id="1dce7-110">必須是格式為 *hh： mm： ss* 格式的字串，其中 *hh* = hours， *mm* = 分鐘， *ss* = 秒，而 *ff* = 秒數的分數。</span><span class="sxs-lookup"><span data-stu-id="1dce7-110">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="1dce7-111">範例：1：04：30.512。</span><span class="sxs-lookup"><span data-stu-id="1dce7-111">Example: 1:04:30.512.</span></span> <span data-ttu-id="1dce7-112">您可以省略前置單位。</span><span class="sxs-lookup"><span data-stu-id="1dce7-112">Leading units can be omitted.</span></span> <span data-ttu-id="1dce7-113">例如，3:00 (三分鐘) 和 45 (45 秒) 都有效。</span><span class="sxs-lookup"><span data-stu-id="1dce7-113">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1dce7-114">套用至</span><span class="sxs-lookup"><span data-stu-id="1dce7-114">Applies To</span></span>

[<span data-ttu-id="1dce7-115">**過渡**</span><span class="sxs-lookup"><span data-stu-id="1dce7-115">**transition**</span></span>](transition-element.md)

## <a name="see-also"></a><span data-ttu-id="1dce7-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1dce7-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dce7-117">XTL 屬性</span><span class="sxs-lookup"><span data-stu-id="1dce7-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="1dce7-118">**IAMTimelineTrans::SetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="1dce7-118">**IAMTimelineTrans::SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)
</dt> </dl>

 

 



