---
title: TaskSettings： Hidden 屬性
description: 針對腳本，取得或設定布林值，指出工作將不會顯示在 UI 中。
ms.assetid: 84a3d0b3-30f0-4356-b6cf-9bee3091612f
keywords:
- Hidden 屬性工作排程器
- Hidden 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器，隱藏的屬性
topic_type:
- apiref
api_name:
- TaskSettings.Hidden
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057a3d920ba70260d23ad13a5888072ab5b07767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686217"
---
# <a name="tasksettingshidden-property"></a><span data-ttu-id="a0d7e-106">TaskSettings： Hidden 屬性</span><span class="sxs-lookup"><span data-stu-id="a0d7e-106">TaskSettings.Hidden property</span></span>

<span data-ttu-id="a0d7e-107">針對腳本，取得或設定布林值，指出工作將不會顯示在 UI 中。</span><span class="sxs-lookup"><span data-stu-id="a0d7e-107">For scripting, gets or sets a Boolean value that indicates that the task will not be visible in the UI.</span></span> <span data-ttu-id="a0d7e-108">不過，系統管理員可以使用「主要交換器」來覆寫這項設定，讓所有工作都顯示在 UI 中。</span><span class="sxs-lookup"><span data-stu-id="a0d7e-108">However, administrators can override this setting through the use of a "master switch" that makes all tasks visible in the UI.</span></span>

<span data-ttu-id="a0d7e-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="a0d7e-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0d7e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0d7e-110">Syntax</span></span>


```VB
TaskSettings.Hidden As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a0d7e-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="a0d7e-111">Property value</span></span>

<span data-ttu-id="a0d7e-112">若 **為 True**，此值表示工作將不會顯示在 UI 中。</span><span class="sxs-lookup"><span data-stu-id="a0d7e-112">If **True**, the value indicates that the task will not be visible in the UI.</span></span> <span data-ttu-id="a0d7e-113">如果 **為 False**，則工作會顯示在 UI 中。</span><span class="sxs-lookup"><span data-stu-id="a0d7e-113">If **False**, the task will be visible in the UI.</span></span> <span data-ttu-id="a0d7e-114">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="a0d7e-114">The default is **False**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0d7e-115">備註</span><span class="sxs-lookup"><span data-stu-id="a0d7e-115">Remarks</span></span>

<span data-ttu-id="a0d7e-116">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**Hidden (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="a0d7e-116">When reading or writing XML for a task, this setting is specified in the [**Hidden (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0d7e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0d7e-117">Requirements</span></span>



| <span data-ttu-id="a0d7e-118">需求</span><span class="sxs-lookup"><span data-stu-id="a0d7e-118">Requirement</span></span> | <span data-ttu-id="a0d7e-119">值</span><span class="sxs-lookup"><span data-stu-id="a0d7e-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d7e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0d7e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a0d7e-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0d7e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a0d7e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0d7e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a0d7e-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0d7e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a0d7e-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a0d7e-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="a0d7e-125"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a0d7e-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a0d7e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a0d7e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0d7e-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0d7e-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0d7e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0d7e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0d7e-129">工作排程器</span><span class="sxs-lookup"><span data-stu-id="a0d7e-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





