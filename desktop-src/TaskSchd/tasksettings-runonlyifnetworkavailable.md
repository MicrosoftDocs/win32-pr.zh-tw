---
title: TaskSettings. RunOnlyIfNetworkAvailable 屬性
description: 針對腳本，取得或設定布林值，指出工作排程器只有在有可用的網路時才會執行工作。
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- RunOnlyIfNetworkAvailable 屬性工作排程器
- RunOnlyIfNetworkAvailable 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、RunOnlyIfNetworkAvailable 屬性
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8225d836e5bc87abd5ce9b6c311b4af527561d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844060"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a><span data-ttu-id="17ce9-106">TaskSettings. RunOnlyIfNetworkAvailable 屬性</span><span class="sxs-lookup"><span data-stu-id="17ce9-106">TaskSettings.RunOnlyIfNetworkAvailable property</span></span>

<span data-ttu-id="17ce9-107">針對腳本，取得或設定布林值，指出工作排程器只有在有可用的網路時才會執行工作。</span><span class="sxs-lookup"><span data-stu-id="17ce9-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will run the task only when a network is available.</span></span>

<span data-ttu-id="17ce9-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="17ce9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="17ce9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="17ce9-109">Syntax</span></span>


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a><span data-ttu-id="17ce9-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="17ce9-110">Property value</span></span>

<span data-ttu-id="17ce9-111">若為 True，則屬性會指出工作排程器只有在有可用的網路時才會執行工作。</span><span class="sxs-lookup"><span data-stu-id="17ce9-111">If True, the property indicates that the Task Scheduler will run the task only when a network is available.</span></span> <span data-ttu-id="17ce9-112">預設值是 False。</span><span class="sxs-lookup"><span data-stu-id="17ce9-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="17ce9-113">備註</span><span class="sxs-lookup"><span data-stu-id="17ce9-113">Remarks</span></span>

<span data-ttu-id="17ce9-114">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="17ce9-114">When reading or writing XML for a task, this setting is specified in the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="17ce9-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="17ce9-115">Requirements</span></span>



| <span data-ttu-id="17ce9-116">需求</span><span class="sxs-lookup"><span data-stu-id="17ce9-116">Requirement</span></span> | <span data-ttu-id="17ce9-117">值</span><span class="sxs-lookup"><span data-stu-id="17ce9-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17ce9-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17ce9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="17ce9-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17ce9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="17ce9-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17ce9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="17ce9-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17ce9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="17ce9-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="17ce9-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="17ce9-123"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="17ce9-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="17ce9-124">DLL</span><span class="sxs-lookup"><span data-stu-id="17ce9-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17ce9-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17ce9-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17ce9-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17ce9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17ce9-127">工作排程器</span><span class="sxs-lookup"><span data-stu-id="17ce9-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





