---
title: IdleSettings. RestartOnIdle 屬性
description: 針對腳本，取得或設定布林值，這個值會指出當電腦迴圈進入閒置條件超過一次時，是否要重新開機工作。
ms.assetid: c77b6f5f-659c-4aa0-a5f7-39c01e5ca65e
keywords:
- RestartOnIdle 屬性工作排程器
- RestartOnIdle 屬性工作排程器，IdleSettings 物件
- IdleSettings 物件工作排程器、RestartOnIdle 屬性
topic_type:
- apiref
api_name:
- IdleSettings.RestartOnIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e80b2e523f2f19222292eac7752847a72291c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967973"
---
# <a name="idlesettingsrestartonidle-property"></a><span data-ttu-id="8ac35-106">IdleSettings. RestartOnIdle 屬性</span><span class="sxs-lookup"><span data-stu-id="8ac35-106">IdleSettings.RestartOnIdle property</span></span>

<span data-ttu-id="8ac35-107">針對腳本，取得或設定布林值，這個值會指出當電腦迴圈進入閒置條件超過一次時，是否要重新開機工作。</span><span class="sxs-lookup"><span data-stu-id="8ac35-107">For scripting, gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ac35-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ac35-108">Syntax</span></span>


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a><span data-ttu-id="8ac35-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="8ac35-109">Property value</span></span>

<span data-ttu-id="8ac35-110">布林值，指出當電腦迴圈進入閒置條件超過一次時，是否必須重新開機工作。</span><span class="sxs-lookup"><span data-stu-id="8ac35-110">A Boolean value that indicates whether the task must be restarted when the computer cycles into an idle condition more than once.</span></span> <span data-ttu-id="8ac35-111">預設值是 False。</span><span class="sxs-lookup"><span data-stu-id="8ac35-111">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ac35-112">備註</span><span class="sxs-lookup"><span data-stu-id="8ac35-112">Remarks</span></span>

<span data-ttu-id="8ac35-113">只有當 [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md) 屬性設定為 True 時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8ac35-113">This property is only used if the [**IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md) property is set to True.</span></span>

<span data-ttu-id="8ac35-114">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="8ac35-114">When reading or writing XML for a task, this setting is specified in the [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ac35-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ac35-115">Requirements</span></span>



| <span data-ttu-id="8ac35-116">需求</span><span class="sxs-lookup"><span data-stu-id="8ac35-116">Requirement</span></span> | <span data-ttu-id="8ac35-117">值</span><span class="sxs-lookup"><span data-stu-id="8ac35-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ac35-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ac35-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8ac35-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ac35-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8ac35-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ac35-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8ac35-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ac35-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8ac35-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8ac35-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="8ac35-123"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8ac35-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8ac35-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8ac35-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ac35-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ac35-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ac35-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ac35-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ac35-127">工作排程器</span><span class="sxs-lookup"><span data-stu-id="8ac35-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="8ac35-128">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="8ac35-128">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





