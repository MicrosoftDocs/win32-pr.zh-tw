---
description: 描述 Windows 裝置) 的安全模式 (S 模式。
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: 'WLDP_WINDOWS_LOCKDOWN_MODE 列舉 (Wldp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_WINDOWS_LOCKDOWN_MODE
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 438a44bec0745ea67b2b40c3f8aa9c0dd6bd0072
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990802"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a><span data-ttu-id="08ce5-103">WLDP \_ WINDOWS \_ 鎖定 \_ 模式列舉</span><span class="sxs-lookup"><span data-stu-id="08ce5-103">WLDP\_WINDOWS\_LOCKDOWN\_MODE enumeration</span></span>

<span data-ttu-id="08ce5-104">描述 Windows 裝置) 的安全模式 (S 模式。</span><span class="sxs-lookup"><span data-stu-id="08ce5-104">Describes the secure modes (S modes) for a Windows device.</span></span> <span data-ttu-id="08ce5-105">主要用於 [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md)。</span><span class="sxs-lookup"><span data-stu-id="08ce5-105">Used primarily in [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="08ce5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="08ce5-106">Syntax</span></span>


```C++
typedef enum _WLDP_WINDOWS_LOCKDOWN_MODE { 
  WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED  = 0,
  WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL     = 1,
  WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED    = 2,
  WLDP_WINDOWS_LOCKDOWN_MODE_MAX       = 3
} WLDP_WINDOWS_LOCKDOWN_MODE, *PWLDP_WINDOWS_LOCKDOWN_MODE;
```



## <a name="constants"></a><span data-ttu-id="08ce5-107">常數</span><span class="sxs-lookup"><span data-stu-id="08ce5-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="08ce5-108"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**WLDP \_ WINDOWS \_ 鎖定 \_ 模式已 \_ 解除鎖定**</span><span class="sxs-lookup"><span data-stu-id="08ce5-108"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_UNLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="08ce5-109">解 鎖。</span><span class="sxs-lookup"><span data-stu-id="08ce5-109">Unlocked.</span></span> <span data-ttu-id="08ce5-110">主要用於沒有 S 模式的 Windows 裝置。</span><span class="sxs-lookup"><span data-stu-id="08ce5-110">Used primarily for Windows devices without the S mode.</span></span>

</dd> <dt>

<span data-ttu-id="08ce5-111"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**WLDP \_ WINDOWS \_ 鎖定 \_ 模式 \_ 試用版**</span><span class="sxs-lookup"><span data-stu-id="08ce5-111"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_TRIAL**</span></span>
</dt> <dd>

<span data-ttu-id="08ce5-112">試驗。</span><span class="sxs-lookup"><span data-stu-id="08ce5-112">Trial.</span></span> <span data-ttu-id="08ce5-113">主要用於具有 S 模式的 Windows 10 試用版裝置。</span><span class="sxs-lookup"><span data-stu-id="08ce5-113">Used primarily for a Windows 10 trial device with the S mode.</span></span> <span data-ttu-id="08ce5-114">試用模式是以 S 模式 Windows 10 裝置的特殊案例：原則會強制執行，但沒有強制執行原則的復原保護。</span><span class="sxs-lookup"><span data-stu-id="08ce5-114">Trial mode is a special case for Windows 10 devices with the S mode: policies are enforced, but there is no anti-rollback protection for the enforcement of the policy.</span></span>

</dd> <dt>

<span data-ttu-id="08ce5-115"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP \_ WINDOWS \_ 鎖定 \_ 模式已 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="08ce5-115"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_LOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="08ce5-116">鎖。</span><span class="sxs-lookup"><span data-stu-id="08ce5-116">Locked.</span></span> <span data-ttu-id="08ce5-117">主要用於具有 S 模式的 Windows 10 裝置。</span><span class="sxs-lookup"><span data-stu-id="08ce5-117">Used primarily for a Windows 10 device with the S mode.</span></span> <span data-ttu-id="08ce5-118">鎖定的裝置將會強制執行以 S 模式隨附 Windows 10 OS 映射的已簽署 Device Guard 原則。</span><span class="sxs-lookup"><span data-stu-id="08ce5-118">A device that is locked will enforce the signed Device Guard policies shipped with the Windows 10 OS image with the S mode.</span></span>

</dd> <dt>

<span data-ttu-id="08ce5-119"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP \_ WINDOWS \_ 鎖定 \_ 模式 \_ 最大值**</span><span class="sxs-lookup"><span data-stu-id="08ce5-119"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="08ce5-120">最大的列舉值。</span><span class="sxs-lookup"><span data-stu-id="08ce5-120">The maximum enumeration value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08ce5-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="08ce5-121">Requirements</span></span>



| <span data-ttu-id="08ce5-122">需求</span><span class="sxs-lookup"><span data-stu-id="08ce5-122">Requirement</span></span> | <span data-ttu-id="08ce5-123">值</span><span class="sxs-lookup"><span data-stu-id="08ce5-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="08ce5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="08ce5-124">Header</span></span><br/> | <dl> <span data-ttu-id="08ce5-125"><dt>Wldp。h</dt></span><span class="sxs-lookup"><span data-stu-id="08ce5-125"><dt>Wldp.h</dt></span></span> </dl> |



 

 




