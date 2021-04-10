---
title: RegisteredTask. NextRunTime 屬性
description: 針對腳本，取得下次排程執行的已註冊工作的時間。
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- NextRunTime 屬性工作排程器
- NextRunTime 屬性工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器、NextRunTime 屬性
topic_type:
- apiref
api_name:
- RegisteredTask.NextRunTime
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94db26c023ddd2c146586fbc433548517a84f234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686227"
---
# <a name="registeredtasknextruntime-property"></a><span data-ttu-id="1bf3b-106">RegisteredTask. NextRunTime 屬性</span><span class="sxs-lookup"><span data-stu-id="1bf3b-106">RegisteredTask.NextRunTime property</span></span>

<span data-ttu-id="1bf3b-107">針對腳本，取得下次排程執行的已註冊工作的時間。</span><span class="sxs-lookup"><span data-stu-id="1bf3b-107">For scripting, gets the time when the registered task is next scheduled to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bf3b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bf3b-108">Syntax</span></span>


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a><span data-ttu-id="1bf3b-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="1bf3b-109">Property value</span></span>

<span data-ttu-id="1bf3b-110">下次排定要執行的已註冊工作時間。</span><span class="sxs-lookup"><span data-stu-id="1bf3b-110">The time when the registered task is next scheduled to run.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bf3b-111">備註</span><span class="sxs-lookup"><span data-stu-id="1bf3b-111">Remarks</span></span>

<span data-ttu-id="1bf3b-112">如果已註冊的工作包含個別停用的觸發程式，這些觸發程式仍會影響下一次所傳回的排程執行時間（即使已停用）。</span><span class="sxs-lookup"><span data-stu-id="1bf3b-112">If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bf3b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bf3b-113">Requirements</span></span>



| <span data-ttu-id="1bf3b-114">需求</span><span class="sxs-lookup"><span data-stu-id="1bf3b-114">Requirement</span></span> | <span data-ttu-id="1bf3b-115">值</span><span class="sxs-lookup"><span data-stu-id="1bf3b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bf3b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1bf3b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1bf3b-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1bf3b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1bf3b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1bf3b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1bf3b-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1bf3b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1bf3b-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1bf3b-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="1bf3b-121"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1bf3b-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1bf3b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1bf3b-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bf3b-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bf3b-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bf3b-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1bf3b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bf3b-125">工作排程器</span><span class="sxs-lookup"><span data-stu-id="1bf3b-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="1bf3b-126">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="1bf3b-126">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





