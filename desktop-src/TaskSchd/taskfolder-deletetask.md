---
title: TaskFolder. DeleteTask 方法
description: 針對腳本，會從資料夾中刪除工作。
ms.assetid: c030b2bf-fbde-4b8b-b38b-763938855d12
keywords:
- DeleteTask 方法工作排程器
- DeleteTask 方法工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器，DeleteTask 方法
topic_type:
- apiref
api_name:
- TaskFolder.DeleteTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad4cf0a881a62cf5e9c1600653e5df58f3000f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686076"
---
# <a name="taskfolderdeletetask-method"></a><span data-ttu-id="78de1-106">TaskFolder. DeleteTask 方法</span><span class="sxs-lookup"><span data-stu-id="78de1-106">TaskFolder.DeleteTask method</span></span>

<span data-ttu-id="78de1-107">針對腳本，會從資料夾中刪除工作。</span><span class="sxs-lookup"><span data-stu-id="78de1-107">For scripting, deletes a task from the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="78de1-108">語法</span><span class="sxs-lookup"><span data-stu-id="78de1-108">Syntax</span></span>


```VB
TaskFolder.DeleteTask( _
  ByVal Name, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="78de1-109">參數</span><span class="sxs-lookup"><span data-stu-id="78de1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78de1-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="78de1-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78de1-111">註冊工作時所指定的工作名稱。</span><span class="sxs-lookup"><span data-stu-id="78de1-111">The name of the task that is specified when the task was registered.</span></span> <span data-ttu-id="78de1-112">'. ' 字元不能用來指定目前的工作資料夾與 ' ... '</span><span class="sxs-lookup"><span data-stu-id="78de1-112">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="78de1-113">字元不能用來指定路徑中的父工作資料夾。</span><span class="sxs-lookup"><span data-stu-id="78de1-113">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="78de1-114">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="78de1-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78de1-115">不支援。</span><span class="sxs-lookup"><span data-stu-id="78de1-115">Not supported.</span></span> <span data-ttu-id="78de1-116">值為0</span><span class="sxs-lookup"><span data-stu-id="78de1-116">Value is 0</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78de1-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="78de1-117">Return value</span></span>

<span data-ttu-id="78de1-118">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="78de1-118">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="78de1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="78de1-119">Requirements</span></span>



| <span data-ttu-id="78de1-120">需求</span><span class="sxs-lookup"><span data-stu-id="78de1-120">Requirement</span></span> | <span data-ttu-id="78de1-121">值</span><span class="sxs-lookup"><span data-stu-id="78de1-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78de1-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78de1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="78de1-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78de1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="78de1-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78de1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="78de1-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78de1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="78de1-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="78de1-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="78de1-127"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="78de1-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="78de1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="78de1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78de1-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78de1-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78de1-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78de1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78de1-131">工作排程器</span><span class="sxs-lookup"><span data-stu-id="78de1-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





