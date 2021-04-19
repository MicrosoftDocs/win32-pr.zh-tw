---
description: LINEDIALTONEMODE \_ 位旗標常數描述不同類型的撥號音。 特殊的撥號音通常會攜帶特殊意義 (與訊息等候) 一樣。
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: 'LINEDIALTONEMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5128f2a176f3aeaf92bc3487b131b7720568085e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977609"
---
# <a name="linedialtonemode_-constants"></a><span data-ttu-id="5e1d9-104">LINEDIALTONEMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="5e1d9-104">LINEDIALTONEMODE\_ Constants</span></span>

<span data-ttu-id="5e1d9-105">**LINEDIALTONEMODE \_** 位旗標常數描述不同類型的撥號音。</span><span class="sxs-lookup"><span data-stu-id="5e1d9-105">The **LINEDIALTONEMODE\_** bit-flag constants describe different types of dial tones.</span></span> <span data-ttu-id="5e1d9-106">特殊的撥號音通常會攜帶特殊意義 (與訊息等候) 一樣。</span><span class="sxs-lookup"><span data-stu-id="5e1d9-106">A special dial tone typically carries a special meaning (as with message waiting).</span></span>

<dl> <dt>

<span data-ttu-id="5e1d9-107"><span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE \_ 外部**</span><span class="sxs-lookup"><span data-stu-id="5e1d9-107"><span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE\_EXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5e1d9-108">這是外部 (公用網路) 撥號音。</span><span class="sxs-lookup"><span data-stu-id="5e1d9-108">This is an external (public network) dial tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5e1d9-109"><span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE \_ 內部**</span><span class="sxs-lookup"><span data-stu-id="5e1d9-109"><span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5e1d9-110">這是在 PBX 內的內部撥號音。</span><span class="sxs-lookup"><span data-stu-id="5e1d9-110">This is an internal dial tone, as within a PBX.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5e1d9-111"><span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE \_ 正常**</span><span class="sxs-lookup"><span data-stu-id="5e1d9-111"><span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE\_NORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5e1d9-112">這是一般的撥號音，通常是連續的聲音。</span><span class="sxs-lookup"><span data-stu-id="5e1d9-112">This is a normal dial tone, which typically is a continuous tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5e1d9-113"><span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE \_ 特殊**</span><span class="sxs-lookup"><span data-stu-id="5e1d9-113"><span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE\_SPECIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5e1d9-114">這是特殊的撥號音，表示參數 (已知的特定條件或網路) 目前有效。</span><span class="sxs-lookup"><span data-stu-id="5e1d9-114">This is a special dial tone indicating that a certain condition (known by the switch or network) is currently in effect.</span></span> <span data-ttu-id="5e1d9-115">特殊撥號音通常會使用中斷的聲音。</span><span class="sxs-lookup"><span data-stu-id="5e1d9-115">Special dial tones typically use an interrupted tone.</span></span> <span data-ttu-id="5e1d9-116">如同一般的撥號音，這表示交換器已準備好接收要撥打的號碼。</span><span class="sxs-lookup"><span data-stu-id="5e1d9-116">As with a normal dial tone, this indicates that the switch is ready to receive the number to be dialed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5e1d9-117"><span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE \_ UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="5e1d9-117"><span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5e1d9-118">撥號音模式無法使用，而且將不會變成已知。</span><span class="sxs-lookup"><span data-stu-id="5e1d9-118">The dial tone mode is unavailable and will not become known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5e1d9-119"><span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="5e1d9-119"><span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5e1d9-120">撥號音模式目前不是已知的，但稍後可能會變成已知。</span><span class="sxs-lookup"><span data-stu-id="5e1d9-120">The dial tone mode is not currently known but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e1d9-121">備註</span><span class="sxs-lookup"><span data-stu-id="5e1d9-121">Remarks</span></span>

<span data-ttu-id="5e1d9-122">您可以為裝置專屬的延伸模組指派高序位16位。</span><span class="sxs-lookup"><span data-stu-id="5e1d9-122">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="5e1d9-123">低序位16位是保留的。</span><span class="sxs-lookup"><span data-stu-id="5e1d9-123">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="5e1d9-124">**LINEDIALTONEMODE \_ 常數** 是在 [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)資料結構內用於撥號程式狀態中的呼叫。</span><span class="sxs-lookup"><span data-stu-id="5e1d9-124">The **LINEDIALTONEMODE\_constants** are used within the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) data structure for a call in the dialtone state.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e1d9-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e1d9-125">Requirements</span></span>



| <span data-ttu-id="5e1d9-126">需求</span><span class="sxs-lookup"><span data-stu-id="5e1d9-126">Requirement</span></span> | <span data-ttu-id="5e1d9-127">值</span><span class="sxs-lookup"><span data-stu-id="5e1d9-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5e1d9-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="5e1d9-128">TAPI version</span></span><br/> | <span data-ttu-id="5e1d9-129">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5e1d9-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5e1d9-130">標頭</span><span class="sxs-lookup"><span data-stu-id="5e1d9-130">Header</span></span><br/>       | <dl> <span data-ttu-id="5e1d9-131"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="5e1d9-131"><dt>Tapi.h</dt></span></span> </dl> |



 

 




