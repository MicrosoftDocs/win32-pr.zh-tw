---
description: LINEROAMMODE \_ 位旗標常數描述線路裝置的漫遊狀態。
ms.assetid: af0eb263-8deb-44ab-8acb-00e4ff7930ab
title: 'LINEROAMMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e40c40291567e7800b53070f882bf1e0bdac93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995263"
---
# <a name="lineroammode_-constants"></a><span data-ttu-id="278c2-103">LINEROAMMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="278c2-103">LINEROAMMODE\_ Constants</span></span>

<span data-ttu-id="278c2-104">**LINEROAMMODE \_** 位旗標常數描述線路裝置的漫遊狀態。</span><span class="sxs-lookup"><span data-stu-id="278c2-104">The **LINEROAMMODE\_** bit-flag constants describe the roaming status of a line device.</span></span>

<dl> <dt>

<span data-ttu-id="278c2-105"><span id="LINEROAMMODE_HOME"></span><span id="lineroammode_home"></span>**LINEROAMMODE \_ 首頁**</span><span class="sxs-lookup"><span data-stu-id="278c2-105"><span id="LINEROAMMODE_HOME"></span><span id="lineroammode_home"></span>**LINEROAMMODE\_HOME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="278c2-106">這一行連接到 [家用網路] 節點。</span><span class="sxs-lookup"><span data-stu-id="278c2-106">The line is connected to the home network node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="278c2-107"><span id="LINEROAMMODE_ROAMA"></span><span id="lineroammode_roama"></span>**LINEROAMMODE \_ ROAMA**</span><span class="sxs-lookup"><span data-stu-id="278c2-107"><span id="LINEROAMMODE_ROAMA"></span><span id="lineroammode_roama"></span>**LINEROAMMODE\_ROAMA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="278c2-108">線路會連接到「漫遊」-「貨運公司」和通話會據以收費。</span><span class="sxs-lookup"><span data-stu-id="278c2-108">The line is connected to the Roam-A carrier and calls are charged accordingly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="278c2-109"><span id="LINEROAMMODE_ROAMB"></span><span id="lineroammode_roamb"></span>**LINEROAMMODE \_ ROAMB**</span><span class="sxs-lookup"><span data-stu-id="278c2-109"><span id="LINEROAMMODE_ROAMB"></span><span id="lineroammode_roamb"></span>**LINEROAMMODE\_ROAMB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="278c2-110">線路會連接到「漫遊-B」貨運公司，並據此收費通話。</span><span class="sxs-lookup"><span data-stu-id="278c2-110">The line is connected to the Roam-B carrier and calls are charged accordingly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="278c2-111"><span id="LINEROAMMODE_UNAVAIL"></span><span id="lineroammode_unavail"></span>**LINEROAMMODE \_ UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="278c2-111"><span id="LINEROAMMODE_UNAVAIL"></span><span id="lineroammode_unavail"></span>**LINEROAMMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="278c2-112">漫遊模式無法使用，也不會知道。</span><span class="sxs-lookup"><span data-stu-id="278c2-112">The roam mode is unavailable and will not be known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="278c2-113"><span id="LINEROAMMODE_UNKNOWN"></span><span id="lineroammode_unknown"></span>**LINEROAMMODE \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="278c2-113"><span id="LINEROAMMODE_UNKNOWN"></span><span id="lineroammode_unknown"></span>**LINEROAMMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="278c2-114">漫遊模式目前是未知的，但稍後可能會變成已知。</span><span class="sxs-lookup"><span data-stu-id="278c2-114">The roam mode is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="278c2-115">備註</span><span class="sxs-lookup"><span data-stu-id="278c2-115">Remarks</span></span>

<span data-ttu-id="278c2-116">無延伸。</span><span class="sxs-lookup"><span data-stu-id="278c2-116">No extensibility.</span></span> <span data-ttu-id="278c2-117">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="278c2-117">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="278c2-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="278c2-118">Requirements</span></span>



| <span data-ttu-id="278c2-119">需求</span><span class="sxs-lookup"><span data-stu-id="278c2-119">Requirement</span></span> | <span data-ttu-id="278c2-120">值</span><span class="sxs-lookup"><span data-stu-id="278c2-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="278c2-121">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="278c2-121">TAPI version</span></span><br/> | <span data-ttu-id="278c2-122">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="278c2-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="278c2-123">標頭</span><span class="sxs-lookup"><span data-stu-id="278c2-123">Header</span></span><br/>       | <dl> <span data-ttu-id="278c2-124"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="278c2-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




