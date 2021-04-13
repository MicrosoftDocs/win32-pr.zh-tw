---
description: 包含要設定的電池資訊。
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: 'BATTERY_SET_INFORMATION 結構 (Poclass .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 0b23489bc5a7608e2e8afb297bb4be7ba35cecb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115557"
---
# <a name="battery_set_information-structure"></a><span data-ttu-id="63666-103">電池 \_ 設定 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="63666-103">BATTERY\_SET\_INFORMATION structure</span></span>

<span data-ttu-id="63666-104">包含要設定的電池資訊。</span><span class="sxs-lookup"><span data-stu-id="63666-104">Contains battery information to be set.</span></span> <span data-ttu-id="63666-105">此結構會與 [**IOCTL \_ 電池 \_ 設定 \_ 資訊**](ioctl-battery-set-information.md) 控制程式代碼搭配使用。</span><span class="sxs-lookup"><span data-stu-id="63666-105">This structure is used with the [**IOCTL\_BATTERY\_SET\_INFORMATION**](ioctl-battery-set-information.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="63666-106">語法</span><span class="sxs-lookup"><span data-stu-id="63666-106">Syntax</span></span>


```C++
typedef struct _BATTERY_SET_INFORMATION {
  ULONG                         BatteryTag;
  BATTERY_SET_INFORMATION_LEVEL InformationLevel;
  UCHAR                         Buffer[1];
} BATTERY_SET_INFORMATION, *PBATTERY_SET_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="63666-107">成員</span><span class="sxs-lookup"><span data-stu-id="63666-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="63666-108">**BatteryTag**</span><span class="sxs-lookup"><span data-stu-id="63666-108">**BatteryTag**</span></span>
</dt> <dd>

<span data-ttu-id="63666-109">電池目前的電池標記。</span><span class="sxs-lookup"><span data-stu-id="63666-109">The current battery tag for the battery.</span></span> <span data-ttu-id="63666-110">只會傳回符合標記之電池的資訊。</span><span class="sxs-lookup"><span data-stu-id="63666-110">Information for a battery matching the tag can only be returned.</span></span> <span data-ttu-id="63666-111">每當此值不符合電池的目前標記時，就會完成 IOCTL 要求，並找不到錯誤檔案 \_ \_ \_ ，這會向呼叫者指出其具有標記的電池已不存在。</span><span class="sxs-lookup"><span data-stu-id="63666-111">Whenever this value does not match the battery's current tag, the IOCTL request will be completed with ERROR\_FILE\_NOT\_FOUND, which indicates to the caller that the battery for which it has a tag for no longer exists.</span></span> <span data-ttu-id="63666-112">呼叫者可以選擇使用 [**IOCTL \_ 電池 \_ 查詢 \_ 標記**](ioctl-battery-query-tag.md) 作業來判斷新安裝的電池標記（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="63666-112">The caller may opt to use the [**IOCTL\_BATTERY\_QUERY\_TAG**](ioctl-battery-query-tag.md) operation to determine the tag of the newly installed battery, if one exists.</span></span> <span data-ttu-id="63666-113"> (查看 [電池標記](battery-information.md) 以取得詳細資訊。 ) </span><span class="sxs-lookup"><span data-stu-id="63666-113">(See [Battery Tags](battery-information.md) for more information.)</span></span>

<span data-ttu-id="63666-114">發出查詢資訊要求時，會驗證此值。</span><span class="sxs-lookup"><span data-stu-id="63666-114">When a query information request is made, this value is verified.</span></span> <span data-ttu-id="63666-115">此外，如果此值變更時，要求仍在進行中，則會中止要求，並出現「找不到錯誤檔案」的狀態 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="63666-115">In addition, if the request is in progress while this value changes, the request is aborted with the status of ERROR\_FILE\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="63666-116">**InformationLevel**</span><span class="sxs-lookup"><span data-stu-id="63666-116">**InformationLevel**</span></span>
</dt> <dd>

<span data-ttu-id="63666-117">要設定的電池資訊。</span><span class="sxs-lookup"><span data-stu-id="63666-117">The battery information to be set.</span></span> <span data-ttu-id="63666-118">**緩衝區** 成員中的資料類型取決於這個成員的值。</span><span class="sxs-lookup"><span data-stu-id="63666-118">The type of data in the **Buffer** member depends on the value of this member.</span></span> <span data-ttu-id="63666-119">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="63666-119">This member can be one of the following values.</span></span>



| <span data-ttu-id="63666-120">值</span><span class="sxs-lookup"><span data-stu-id="63666-120">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="63666-121">意義</span><span class="sxs-lookup"><span data-stu-id="63666-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <span data-ttu-id="63666-122"><dt>**BatteryCharge**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="63666-122"><dt>**BatteryCharge**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="63666-123">通知電池裝置，表示使用者已要求電池必須在這段時間充電。</span><span class="sxs-lookup"><span data-stu-id="63666-123">Informs the battery device that the user has requested that the battery should be charging at this time.</span></span> <span data-ttu-id="63666-124">例如，使用智慧型電池/充電器/選擇器時，應用程式可以一次收取一台電池的費用。</span><span class="sxs-lookup"><span data-stu-id="63666-124">For example, with a smart battery/charger/selector, the application could charge one battery at a time.</span></span> <span data-ttu-id="63666-125">忽略此結構的 **緩衝區** 成員。</span><span class="sxs-lookup"><span data-stu-id="63666-125">The **Buffer** member of this structure is ignored.</span></span><br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <span data-ttu-id="63666-126"><dt>**BatteryCriticalBias**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="63666-126"><dt>**BatteryCriticalBias**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="63666-127">設定電池的重大偏差調整。</span><span class="sxs-lookup"><span data-stu-id="63666-127">Sets the battery's critical bias adjustment.</span></span> <span data-ttu-id="63666-128">請注意，此值通常會由軟體變更，而且只會在介面中顯示為維護功能。</span><span class="sxs-lookup"><span data-stu-id="63666-128">Note it is not envisioned that this value would normally be changed by software, and is present in the interfaces only as a maintenance feature.</span></span> <span data-ttu-id="63666-129">並非所有電池都可以維持這種設定，而且應該閱讀電池資訊，以確認電池已接受設定。</span><span class="sxs-lookup"><span data-stu-id="63666-129">Not all batteries can maintain such a setting, and the battery information should be read to confirm that the battery accepted the setting.</span></span><br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <span data-ttu-id="63666-130"><dt>**BatteryDischarge**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="63666-130"><dt>**BatteryDischarge**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="63666-131">通知電池裝置，使用者目前已要求電池即將放電。</span><span class="sxs-lookup"><span data-stu-id="63666-131">Informs the battery device that the user has requested that the battery be discharging at this time.</span></span> <span data-ttu-id="63666-132">例如，這可以用來指出使用者目前要為系統提供哪些電池電力。</span><span class="sxs-lookup"><span data-stu-id="63666-132">For example, this could be used to indicate which battery the user currently wants to power the system.</span></span> <span data-ttu-id="63666-133">忽略此結構的 **緩衝區** 成員。</span><span class="sxs-lookup"><span data-stu-id="63666-133">The **Buffer** member of this structure is ignored.</span></span><br/>                                                                          |



 

</dd> <dt>

<span data-ttu-id="63666-134">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="63666-134">**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="63666-135">要設定的電池資訊。</span><span class="sxs-lookup"><span data-stu-id="63666-135">The battery information to be set.</span></span> <span data-ttu-id="63666-136">資料取決於 **InformationLevel** 的值。</span><span class="sxs-lookup"><span data-stu-id="63666-136">The data depends on the value of **InformationLevel**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63666-137">備註</span><span class="sxs-lookup"><span data-stu-id="63666-137">Remarks</span></span>

<span data-ttu-id="63666-138">**電池 \_ 設定 \_ 資訊** 結構是可變長度的結構，而且您必須配置適當大小的緩衝區，才能將資訊包含在結構中。</span><span class="sxs-lookup"><span data-stu-id="63666-138">The **BATTERY\_SET\_INFORMATION** structure is a variable-length structure, and you must allocate a buffer of suitable size for the information to be included in the structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="63666-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="63666-139">Requirements</span></span>



| <span data-ttu-id="63666-140">需求</span><span class="sxs-lookup"><span data-stu-id="63666-140">Requirement</span></span> | <span data-ttu-id="63666-141">值</span><span class="sxs-lookup"><span data-stu-id="63666-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63666-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63666-142">Minimum supported client</span></span><br/> | <span data-ttu-id="63666-143">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63666-143">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="63666-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63666-144">Minimum supported server</span></span><br/> | <span data-ttu-id="63666-145">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63666-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="63666-146">標頭</span><span class="sxs-lookup"><span data-stu-id="63666-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="63666-147"><dt>Poclass .h;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP 上的 Batclass .h</dt></span><span class="sxs-lookup"><span data-stu-id="63666-147"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63666-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63666-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63666-149">**IOCTL \_ 電池 \_ 設定 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="63666-149">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

 




