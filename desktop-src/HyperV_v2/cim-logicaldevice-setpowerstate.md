---
description: 設定裝置的電源狀態。 這種方法的用法已被取代。 請改為在相關聯的 PowerManagementService 類別中使用 SetPowerState 方法。
ms.assetid: 2f53a8bd-18a8-45aa-92ad-68a33b6a42ab
title: 'CIM_LogicalDevice 類別的 SetPowerState 方法 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SetPowerState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a29f71806747e6d63f53618acd09d472ac8bdea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944771"
---
# <a name="setpowerstate-method-of-the-cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="a4ae8-105">CIM_LogicalDevice 類別的 SetPowerState 方法 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="a4ae8-105">SetPowerState method of the CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="a4ae8-106">設定裝置的電源狀態。</span><span class="sxs-lookup"><span data-stu-id="a4ae8-106">Sets the power state of the Device.</span></span> <span data-ttu-id="a4ae8-107">這種方法的用法已被取代。</span><span class="sxs-lookup"><span data-stu-id="a4ae8-107">The use of this method has been deprecated.</span></span> <span data-ttu-id="a4ae8-108">請改為在相關聯的 **PowerManagementService** 類別中使用 **SetPowerState** 方法。</span><span class="sxs-lookup"><span data-stu-id="a4ae8-108">Instead, use the **SetPowerState** method in the associated **PowerManagementService** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4ae8-109">語法</span><span class="sxs-lookup"><span data-stu-id="a4ae8-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="a4ae8-110">參數</span><span class="sxs-lookup"><span data-stu-id="a4ae8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4ae8-111">*>powerstate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4ae8-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4ae8-112">要設定的電源狀態。</span><span class="sxs-lookup"><span data-stu-id="a4ae8-112">The power state to set.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="a4ae8-113">**Full Power** (1) </span><span class="sxs-lookup"><span data-stu-id="a4ae8-113">**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a4ae8-114">省 **電-低電源模式** (2) </span><span class="sxs-lookup"><span data-stu-id="a4ae8-114">**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a4ae8-115">省 **電-待命** (3) </span><span class="sxs-lookup"><span data-stu-id="a4ae8-115">**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="a4ae8-116">省 **電-其他** (4) </span><span class="sxs-lookup"><span data-stu-id="a4ae8-116">**Power Save - Other** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a4ae8-117">**電源週期** (5) </span><span class="sxs-lookup"><span data-stu-id="a4ae8-117">**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a4ae8-118">**關閉** (6) 的電源</span><span class="sxs-lookup"><span data-stu-id="a4ae8-118">**Power Off** (6)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="a4ae8-119">*時間* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4ae8-119">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4ae8-120">Time 指出應該設定電源狀態的時間，可以是一般的日期時間值，或做為間隔值， (在) 收到方法調用時的間隔開始時間。</span><span class="sxs-lookup"><span data-stu-id="a4ae8-120">Time indicates when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4ae8-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4ae8-121">Return value</span></span>

<span data-ttu-id="a4ae8-122">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a4ae8-122">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4ae8-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4ae8-123">Requirements</span></span>



| <span data-ttu-id="a4ae8-124">需求</span><span class="sxs-lookup"><span data-stu-id="a4ae8-124">Requirement</span></span> | <span data-ttu-id="a4ae8-125">值</span><span class="sxs-lookup"><span data-stu-id="a4ae8-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4ae8-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4ae8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a4ae8-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a4ae8-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a4ae8-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4ae8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a4ae8-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a4ae8-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a4ae8-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="a4ae8-130">Namespace</span></span><br/>                | <span data-ttu-id="a4ae8-131">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="a4ae8-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a4ae8-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a4ae8-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4ae8-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a4ae8-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4ae8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a4ae8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4ae8-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a4ae8-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a4ae8-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4ae8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4ae8-137">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="a4ae8-137">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




