---
description: 下列清單描述放電原則常數。
ms.assetid: a085709e-1c61-4ae2-832e-fda59479cef6
title: " (WinNT. h) 釋出原則常數"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 052d07a5fe538543b66ec8d48c940f63fe82a682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971794"
---
# <a name="discharge-policy-constants"></a><span data-ttu-id="1e6a6-103">放電原則常數</span><span class="sxs-lookup"><span data-stu-id="1e6a6-103">Discharge Policy Constants</span></span>

<span data-ttu-id="1e6a6-104">下列清單描述放電原則常數。</span><span class="sxs-lookup"><span data-stu-id="1e6a6-104">The following list describes the discharge policy constants.</span></span>



| <span data-ttu-id="1e6a6-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="1e6a6-105">Constant/value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="1e6a6-106">Description</span><span class="sxs-lookup"><span data-stu-id="1e6a6-106">Description</span></span>                                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISCHARGE_POLICY_CRITICAL"></span><span id="discharge_policy_critical"></span><dl> <span data-ttu-id="1e6a6-107"><dt>**放電 \_原則 \_ 關鍵性**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1e6a6-107"><dt>**DISCHARGE\_POLICY\_CRITICAL**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="1e6a6-108">當電池出院低於 [重大臨界值] 時，會使用哪一個電池放電原則設定 ([**系統 \_ 電源 \_ 等級**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) 結構) 。</span><span class="sxs-lookup"><span data-stu-id="1e6a6-108">Which of the battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) is used when the battery discharges below the critical threshold.</span></span><br/> |
| <span id="DISCHARGE_POLICY_LOW"></span><span id="discharge_policy_low"></span><dl> <span data-ttu-id="1e6a6-109"><dt>**放電 \_原則 \_ 低**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1e6a6-109"><dt>**DISCHARGE\_POLICY\_LOW**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="1e6a6-110">當電池出院低於低閾值時，會使用) 的電池放電原則設定 ([**系統 \_ 電源 \_ 等級**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) 結構。</span><span class="sxs-lookup"><span data-stu-id="1e6a6-110">Which of the battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) is used when the battery discharges below the low threshold.</span></span><br/>      |
| <span id="NUM_DISCHARGE_POLICIES"></span><span id="num_discharge_policies"></span><dl> <span data-ttu-id="1e6a6-111"><dt>**NUM \_放電 \_ 原則**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1e6a6-111"><dt>**NUM\_DISCHARGE\_POLICIES**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="1e6a6-112">) 指定 ([**系統 \_ 電源 \_ 等級**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) 結構的電池放電原則設定數目。</span><span class="sxs-lookup"><span data-stu-id="1e6a6-112">Number of battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) specified.</span></span><br/>                                                           |



## <a name="requirements"></a><span data-ttu-id="1e6a6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e6a6-113">Requirements</span></span>



| <span data-ttu-id="1e6a6-114">需求</span><span class="sxs-lookup"><span data-stu-id="1e6a6-114">Requirement</span></span> | <span data-ttu-id="1e6a6-115">值</span><span class="sxs-lookup"><span data-stu-id="1e6a6-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e6a6-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e6a6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1e6a6-117">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e6a6-117">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1e6a6-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e6a6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1e6a6-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e6a6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1e6a6-120">標頭</span><span class="sxs-lookup"><span data-stu-id="1e6a6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e6a6-121"><dt>WinNT (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1e6a6-121"><dt>WinNT.h (include Windows.h)</dt></span></span> </dl> |



 

 




