---
title: RegisteredTask. GetInstances 方法
description: 針對腳本，會傳回已註冊工作的所有目前執行中實例。
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- GetInstances 方法工作排程器
- GetInstances 方法工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器，GetInstances 方法
topic_type:
- apiref
api_name:
- RegisteredTask.GetInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78b1579df1124fcd6d26ea658730190b5eb0f5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105245"
---
# <a name="registeredtaskgetinstances-method"></a><span data-ttu-id="aceac-106">RegisteredTask. GetInstances 方法</span><span class="sxs-lookup"><span data-stu-id="aceac-106">RegisteredTask.GetInstances method</span></span>

<span data-ttu-id="aceac-107">針對腳本，會傳回已註冊工作的所有目前執行中實例。</span><span class="sxs-lookup"><span data-stu-id="aceac-107">For scripting, returns all currently running instances of the registered task.</span></span>

> [!Note]  
> <span data-ttu-id="aceac-108">**RegisteredTask** 只會傳回目前正在執行之已註冊工作的實例，該工作是在使用者的安全性內容中執行。</span><span class="sxs-lookup"><span data-stu-id="aceac-108">**RegisteredTask.GetInstances** will only return instances of the currently running registered task that are running at or below a user's security context.</span></span> <span data-ttu-id="aceac-109">例如，針對 Administrators 群組的成員， **GetInstances** 會傳回目前正在執行之已註冊工作的所有實例，但是針對 users 群組的成員， **GetInstances** 只會傳回目前正在執行之已註冊工作的實例，該工作是在 users 群組的安全性內容下執行。</span><span class="sxs-lookup"><span data-stu-id="aceac-109">For example, for members of the Administrators group, **GetInstances** will return all instances of the currently running registered task, but for members of the Users group, **GetInstances** will only return instances of the currently running registered task that are running under the Users group security context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="aceac-110">語法</span><span class="sxs-lookup"><span data-stu-id="aceac-110">Syntax</span></span>


```VB
RegisteredTask.GetInstances( _
  ByVal flags, _
  ByRef runningTasks _
)
```



## <a name="parameters"></a><span data-ttu-id="aceac-111">參數</span><span class="sxs-lookup"><span data-stu-id="aceac-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aceac-112">*flags*</span><span class="sxs-lookup"><span data-stu-id="aceac-112">*flags*</span></span> 
</dt> <dd>

<span data-ttu-id="aceac-113">此參數會保留供日後使用，且必須設定為0。</span><span class="sxs-lookup"><span data-stu-id="aceac-113">This parameter is reserved for future use and must be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="aceac-114">*runningTasks* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="aceac-114">*runningTasks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aceac-115">[**RunningTaskCollection**](runningtaskcollection.md)物件，其中包含目前正在執行之工作的所有實例。</span><span class="sxs-lookup"><span data-stu-id="aceac-115">A [**RunningTaskCollection**](runningtaskcollection.md) object that contains all currently running instances of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aceac-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="aceac-116">Return value</span></span>

<span data-ttu-id="aceac-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="aceac-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="aceac-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="aceac-118">Requirements</span></span>



| <span data-ttu-id="aceac-119">需求</span><span class="sxs-lookup"><span data-stu-id="aceac-119">Requirement</span></span> | <span data-ttu-id="aceac-120">值</span><span class="sxs-lookup"><span data-stu-id="aceac-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aceac-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aceac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aceac-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aceac-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="aceac-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aceac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aceac-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aceac-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aceac-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="aceac-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="aceac-126"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aceac-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aceac-127">DLL</span><span class="sxs-lookup"><span data-stu-id="aceac-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aceac-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aceac-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aceac-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aceac-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aceac-130">工作排程器</span><span class="sxs-lookup"><span data-stu-id="aceac-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="aceac-131">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="aceac-131">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





