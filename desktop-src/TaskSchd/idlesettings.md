---
title: IdleSettings 物件
description: 腳本物件，指定當電腦處於閒置狀態時，工作排程器如何執行工作。
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- IdleSettings 物件工作排程器
- IdleSettings 物件工作排程器，說明
topic_type:
- apiref
api_name:
- IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 819ff226386f30483de96fac6213b35d7dd51a52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384366"
---
# <a name="idlesettings-object"></a><span data-ttu-id="615d2-105">IdleSettings 物件</span><span class="sxs-lookup"><span data-stu-id="615d2-105">IdleSettings object</span></span>

<span data-ttu-id="615d2-106">腳本物件，指定當電腦處於閒置狀態時，工作排程器如何執行工作。</span><span class="sxs-lookup"><span data-stu-id="615d2-106">A scripting object that specifies how the Task Scheduler performs tasks when the computer is in an idle condition.</span></span> <span data-ttu-id="615d2-107">如需有關閒置條件的詳細資訊，請參閱工作 [閒置條件](task-idle-conditions.md)。</span><span class="sxs-lookup"><span data-stu-id="615d2-107">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

## <a name="members"></a><span data-ttu-id="615d2-108">成員</span><span class="sxs-lookup"><span data-stu-id="615d2-108">Members</span></span>

<span data-ttu-id="615d2-109">**IdleSettings** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="615d2-109">The **IdleSettings** object has these types of members:</span></span>

- [<span data-ttu-id="615d2-110">屬性</span><span class="sxs-lookup"><span data-stu-id="615d2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="615d2-111">屬性</span><span class="sxs-lookup"><span data-stu-id="615d2-111">Properties</span></span>

<span data-ttu-id="615d2-112">**IdleSettings** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="615d2-112">The **IdleSettings** object has these properties.</span></span>

> [!NOTE]
> <span data-ttu-id="615d2-113">*IdleDuration* 和 *WaitTimeout* 設定已淘汰。</span><span class="sxs-lookup"><span data-stu-id="615d2-113">The *IdleDuration* and *WaitTimeout* settings are deprecated.</span></span> <span data-ttu-id="615d2-114">它們仍然存在於工作排程器的使用者介面中，而且其介面方法可能仍會傳回有效值，但不再使用這些值。</span><span class="sxs-lookup"><span data-stu-id="615d2-114">They're still present in the Task Scheduler user interface, and their interface methods may still return valid values, but they're no longer used.</span></span>

| <span data-ttu-id="615d2-115">屬性</span><span class="sxs-lookup"><span data-stu-id="615d2-115">Property</span></span>                                                       | <span data-ttu-id="615d2-116">存取類型</span><span class="sxs-lookup"><span data-stu-id="615d2-116">Access type</span></span>           | <span data-ttu-id="615d2-117">Description</span><span class="sxs-lookup"><span data-stu-id="615d2-117">Description</span></span>                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="615d2-118">**RestartOnIdle**</span><span class="sxs-lookup"><span data-stu-id="615d2-118">**RestartOnIdle**</span></span>](idlesettings-restartonidle.md)<br/> | <span data-ttu-id="615d2-119">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="615d2-119">Read/write</span></span><br/> | <span data-ttu-id="615d2-120">取得或設定布林值，這個值表示當電腦迴圈進入閒置條件超過一次時，是否重新開機工作。</span><span class="sxs-lookup"><span data-stu-id="615d2-120">Gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.</span></span><br/>            |
| [<span data-ttu-id="615d2-121">**StopOnIdleEnd**</span><span class="sxs-lookup"><span data-stu-id="615d2-121">**StopOnIdleEnd**</span></span>](idlesettings-stoponidleend.md)<br/> | <span data-ttu-id="615d2-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="615d2-122">Read/write</span></span><br/> | <span data-ttu-id="615d2-123">取得或設定布林值，這個值表示如果閒置條件在工作完成之前結束，工作排程器將終止工作。</span><span class="sxs-lookup"><span data-stu-id="615d2-123">Gets or sets a Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span><br/> |
| <span data-ttu-id="615d2-124">已 **淘汰**： [ **IdleDuration**](idlesettings-idleduration.md)</span><span class="sxs-lookup"><span data-stu-id="615d2-124">**Deprecated**: [**IdleDuration**](idlesettings-idleduration.md)</span></span><br/>   | <span data-ttu-id="615d2-125">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="615d2-125">Read/write</span></span><br/> | <span data-ttu-id="615d2-126">取得或設定值，這個值表示在工作執行之前，電腦必須處於閒置狀態的時間量。</span><span class="sxs-lookup"><span data-stu-id="615d2-126">Gets or sets a value that indicates the amount of time that the computer must be in an idle state before the task is run.</span></span><br/>                            |
| <span data-ttu-id="615d2-127">已 **淘汰**： [ **WaitTimeout**](idlesettings-waittimeout.md)</span><span class="sxs-lookup"><span data-stu-id="615d2-127">**Deprecated**: [**WaitTimeout**](idlesettings-waittimeout.md)</span></span><br/>     | <span data-ttu-id="615d2-128">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="615d2-128">Read/write</span></span><br/> | <span data-ttu-id="615d2-129">取得或設定值，這個值會指出工作排程器等候閒置條件發生的時間量。</span><span class="sxs-lookup"><span data-stu-id="615d2-129">Gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span><br/>                             |

## <a name="remarks"></a><span data-ttu-id="615d2-130">備註</span><span class="sxs-lookup"><span data-stu-id="615d2-130">Remarks</span></span>

<span data-ttu-id="615d2-131">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="615d2-131">When reading or writing XML for a task, this setting is specified in the [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="615d2-132">如果工作是由閒置觸發程式觸發，則會忽略 [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="615d2-132">If a task is triggered by an idle trigger, then the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property is ignored.</span></span>

> [!NOTE]
> <span data-ttu-id="615d2-133">*IdleSettings. IdleDuration* 和 *IdleSettings. WaitTimeout* 已被取代。</span><span class="sxs-lookup"><span data-stu-id="615d2-133">*IdleSettings.IdleDuration* and *IdleSettings.WaitTimeout* are deprecated.</span></span>

## <a name="requirements"></a><span data-ttu-id="615d2-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="615d2-134">Requirements</span></span>

| <span data-ttu-id="615d2-135">需求</span><span class="sxs-lookup"><span data-stu-id="615d2-135">Requirement</span></span> | <span data-ttu-id="615d2-136">值</span><span class="sxs-lookup"><span data-stu-id="615d2-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="615d2-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="615d2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="615d2-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="615d2-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="615d2-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="615d2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="615d2-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="615d2-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="615d2-141">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="615d2-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="615d2-142"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="615d2-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="615d2-143">DLL</span><span class="sxs-lookup"><span data-stu-id="615d2-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="615d2-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="615d2-144"><dt>Taskschd.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="615d2-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="615d2-145">See also</span></span>

[<span data-ttu-id="615d2-146">工作排程器物件</span><span class="sxs-lookup"><span data-stu-id="615d2-146">Task Scheduler Objects</span></span>](task-scheduler-objects.md)

[<span data-ttu-id="615d2-147">工作排程器</span><span class="sxs-lookup"><span data-stu-id="615d2-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
