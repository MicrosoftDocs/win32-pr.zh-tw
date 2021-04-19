---
description: '[指定值] 會定義在圖形建立期間，篩選圖形管理員嘗試新增篩選的順序。'
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: " (Dshow 的) "
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947a13d78f58c12c236ec31f0eeee1dc6d44f1d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991510"
---
# <a name="merit"></a><span data-ttu-id="6ad9a-103">優點</span><span class="sxs-lookup"><span data-stu-id="6ad9a-103">Merit</span></span>

<span data-ttu-id="6ad9a-104">[指定值] 會定義在圖形建立期間，篩選圖形管理員嘗試新增篩選的順序。</span><span class="sxs-lookup"><span data-stu-id="6ad9a-104">Merit values define the order in which the Filter Graph Manager tries to add filters during graph building.</span></span>

<dl> <span data-ttu-id="6ad9a-105"><span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**業績 \_慣用** 的 (0x800000) 獲得 <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **\_ 正常** 的 (0x600000) <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> 不 **\_ 太可能** 獲得 (0x400000) <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> **\_ \_ 未 \_ 使用** (0x200000) 找出 <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> **\_ 軟體 \_ 壓縮** (0x100000) <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **\_ 硬體 \_ 壓縮**</span><span class="sxs-lookup"><span data-stu-id="6ad9a-105"><span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**MERIT\_PREFERRED** (0x800000) <span id="MERIT_NORMAL"></span><span id="merit_normal"></span>**MERIT\_NORMAL** (0x600000) <span id="MERIT_UNLIKELY"></span><span id="merit_unlikely"></span>**MERIT\_UNLIKELY** (0x400000) <span id="MERIT_DO_NOT_USE"></span><span id="merit_do_not_use"></span>**MERIT\_DO\_NOT\_USE** (0x200000) <span id="MERIT_SW_COMPRESSOR"></span><span id="merit_sw_compressor"></span>**MERIT\_SW\_COMPRESSOR** (0x100000) <span id="MERIT_HW_COMPRESSOR"></span><span id="merit_hw_compressor"></span>**MERIT\_HW\_COMPRESSOR** (0x100050)</span></span>
</dl>

## <a name="remarks"></a><span data-ttu-id="6ad9a-106">備註</span><span class="sxs-lookup"><span data-stu-id="6ad9a-106">Remarks</span></span>

<span data-ttu-id="6ad9a-107">每個篩選器都是以「價值」值註冊。</span><span class="sxs-lookup"><span data-stu-id="6ad9a-107">Each filter is registered with a merit value.</span></span> <span data-ttu-id="6ad9a-108">當篩選圖形管理員建立圖形時，會列舉以正確媒體類型註冊的所有篩選準則。</span><span class="sxs-lookup"><span data-stu-id="6ad9a-108">When the filter graph manager builds a graph, it enumerates all the filters registered with the correct media type.</span></span> <span data-ttu-id="6ad9a-109">然後，它會以最高至最低的方式來嘗試進行。</span><span class="sxs-lookup"><span data-stu-id="6ad9a-109">Then it tries them in order of merit, from highest to lowest.</span></span> <span data-ttu-id="6ad9a-110"> (它會使用其他準則，在具有相同相關的篩選準則之間進行選擇。 ) 它永遠不會嘗試值小於或等於 [ **\_ \_ 未 \_ 使用**] 的篩選。</span><span class="sxs-lookup"><span data-stu-id="6ad9a-110">(It uses additional criteria to choose between filters with equal merit.) It never tries filters with a merit value less than or equal to **MERIT\_DO\_NOT\_USE**.</span></span>

<span data-ttu-id="6ad9a-111">永遠不會被視為一般播放的篩選準則應該 **\_ \_ 不 \_** 會有較多的考慮。</span><span class="sxs-lookup"><span data-stu-id="6ad9a-111">A filter that should never be considered for ordinary playback should have a merit of **MERIT\_DO\_NOT\_USE** or less.</span></span> <span data-ttu-id="6ad9a-112">您可以使用未由此列舉定義的中繼值來註冊篩選準則，例如， **\_ 一般** 的 + 1。</span><span class="sxs-lookup"><span data-stu-id="6ad9a-112">Filters can be registered with intermediate values not defined by this enumeration, such as **MERIT\_NORMAL** + 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ad9a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ad9a-113">Requirements</span></span>



| <span data-ttu-id="6ad9a-114">需求</span><span class="sxs-lookup"><span data-stu-id="6ad9a-114">Requirement</span></span> | <span data-ttu-id="6ad9a-115">值</span><span class="sxs-lookup"><span data-stu-id="6ad9a-115">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ad9a-116">標頭</span><span class="sxs-lookup"><span data-stu-id="6ad9a-116">Header</span></span><br/> | <dl> <span data-ttu-id="6ad9a-117"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="6ad9a-117"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ad9a-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ad9a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ad9a-119">常數和 Guid</span><span class="sxs-lookup"><span data-stu-id="6ad9a-119">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="6ad9a-120">註冊篩選準則的指導方針</span><span class="sxs-lookup"><span data-stu-id="6ad9a-120">Guidelines for Registering Filters</span></span>](guidelines-for-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="6ad9a-121">智慧型連接</span><span class="sxs-lookup"><span data-stu-id="6ad9a-121">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 




