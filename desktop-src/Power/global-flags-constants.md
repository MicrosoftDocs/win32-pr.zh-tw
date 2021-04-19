---
description: 全域旗標常數可用來啟用或停用使用者電源原則選項。
ms.assetid: d98190ef-f70e-4796-960e-ff32d2cf6f4f
title: '全域旗標常數 (PowrProf .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd31340e3e7daf4f9dd034c3fa2db333680a626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987534"
---
# <a name="global-flags-constants"></a><span data-ttu-id="e1bcb-103">全域旗標常數</span><span class="sxs-lookup"><span data-stu-id="e1bcb-103">Global Flags Constants</span></span>

<span data-ttu-id="e1bcb-104">全域旗標常數可用來啟用或停用使用者電源原則選項。</span><span class="sxs-lookup"><span data-stu-id="e1bcb-104">The global flags constants are used to enable or disable user power policy options.</span></span>



| <span data-ttu-id="e1bcb-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="e1bcb-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="e1bcb-106">Description</span><span class="sxs-lookup"><span data-stu-id="e1bcb-106">Description</span></span>                                                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EnableMultiBatteryDisplay"></span><span id="enablemultibatterydisplay"></span><span id="ENABLEMULTIBATTERYDISPLAY"></span><dl> <span data-ttu-id="e1bcb-107"><dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="e1bcb-107"><dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="e1bcb-108">啟用或停用系統電源計量表中的多個電池顯示器。</span><span class="sxs-lookup"><span data-stu-id="e1bcb-108">Enables or disables multiple battery display in the system Power Meter.</span></span><br/>                                                                 |
| <span id="EnablePasswordLogon"></span><span id="enablepasswordlogon"></span><span id="ENABLEPASSWORDLOGON"></span><dl> <span data-ttu-id="e1bcb-109"><dt>**EnablePasswordLogon**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="e1bcb-109"><dt>**EnablePasswordLogon**</dt> <dt>0x04</dt></span></span> </dl>                         | <span data-ttu-id="e1bcb-110">當系統從待命或休眠狀態恢復時，啟用或停用需要密碼登入。</span><span class="sxs-lookup"><span data-stu-id="e1bcb-110">Enables or disables requiring password logon when the system resumes from standby or hibernate.</span></span><br/>                                         |
| <span id="EnableSysTrayBatteryMeter"></span><span id="enablesystraybatterymeter"></span><span id="ENABLESYSTRAYBATTERYMETER"></span><dl> <span data-ttu-id="e1bcb-111"><dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="e1bcb-111"><dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="e1bcb-112">啟用或停用系統匣中的電池計量表圖示。</span><span class="sxs-lookup"><span data-stu-id="e1bcb-112">Enables or disables the battery meter icon in the system tray.</span></span> <span data-ttu-id="e1bcb-113">清除此旗標時，不會顯示電池計量表圖示。</span><span class="sxs-lookup"><span data-stu-id="e1bcb-113">When this flag is cleared, the battery meter icon is not displayed.</span></span><br/>      |
| <span id="EnableVideoDimDisplay"></span><span id="enablevideodimdisplay"></span><span id="ENABLEVIDEODIMDISPLAY"></span><dl> <span data-ttu-id="e1bcb-114"><dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="e1bcb-114"><dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt></span></span> </dl>                 | <span data-ttu-id="e1bcb-115">啟用或停用在系統從 AC 電源上執行變更為以電池電源執行時，讓影片顯示變暗的支援。</span><span class="sxs-lookup"><span data-stu-id="e1bcb-115">Enables or disables support for dimming the video display when the system changes from running on AC power to running on battery power.</span></span><br/> |
| <span id="EnableWakeOnRing"></span><span id="enablewakeonring"></span><span id="ENABLEWAKEONRING"></span><dl> <span data-ttu-id="e1bcb-116"><dt>**EnableWakeOnRing**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="e1bcb-116"><dt>**EnableWakeOnRing**</dt> <dt>0x08</dt></span></span> </dl>                                     | <span data-ttu-id="e1bcb-117">啟用或停用喚醒功能支援。</span><span class="sxs-lookup"><span data-stu-id="e1bcb-117">Enables or disables wake on ring support.</span></span><br/>                                                                                               |



## <a name="requirements"></a><span data-ttu-id="e1bcb-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1bcb-118">Requirements</span></span>



| <span data-ttu-id="e1bcb-119">需求</span><span class="sxs-lookup"><span data-stu-id="e1bcb-119">Requirement</span></span> | <span data-ttu-id="e1bcb-120">值</span><span class="sxs-lookup"><span data-stu-id="e1bcb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1bcb-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e1bcb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e1bcb-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1bcb-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e1bcb-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e1bcb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e1bcb-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1bcb-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1bcb-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e1bcb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1bcb-126"><dt>PowrProf。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1bcb-126"><dt>PowrProf.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1bcb-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1bcb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1bcb-128">**全域 \_ 使用者 \_ 電源 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="e1bcb-128">**GLOBAL\_USER\_POWER\_POLICY**</span></span>](/windows/desktop/api/PowrProf/ns-powrprof-global_user_power_policy)
</dt> </dl>

 

 




