---
title: RegisteredTask. Stop 方法
description: 若為腳本，請立即停止已註冊的工作。
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- Stop 方法工作排程器
- Stop 方法工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器，Stop 方法
topic_type:
- apiref
api_name:
- RegisteredTask.Stop
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d51cf748bb65a9db38c56fded102ddeb5b40fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385186"
---
# <a name="registeredtaskstop-method"></a><span data-ttu-id="08ea6-106">RegisteredTask. Stop 方法</span><span class="sxs-lookup"><span data-stu-id="08ea6-106">RegisteredTask.Stop method</span></span>

<span data-ttu-id="08ea6-107">若為腳本，請立即停止已註冊的工作。</span><span class="sxs-lookup"><span data-stu-id="08ea6-107">For scripting, stops the registered task immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="08ea6-108">語法</span><span class="sxs-lookup"><span data-stu-id="08ea6-108">Syntax</span></span>


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="08ea6-109">參數</span><span class="sxs-lookup"><span data-stu-id="08ea6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08ea6-110">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="08ea6-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ea6-111">保留的。</span><span class="sxs-lookup"><span data-stu-id="08ea6-111">Reserved.</span></span> <span data-ttu-id="08ea6-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="08ea6-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08ea6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="08ea6-113">Return value</span></span>

<span data-ttu-id="08ea6-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="08ea6-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08ea6-115">備註</span><span class="sxs-lookup"><span data-stu-id="08ea6-115">Remarks</span></span>

<span data-ttu-id="08ea6-116">**RegisteredTask** 停止函式會停止工作的所有實例。</span><span class="sxs-lookup"><span data-stu-id="08ea6-116">The **RegisteredTask.Stop** function stops all instances of the task.</span></span>

<span data-ttu-id="08ea6-117">系統帳戶使用者可以停止工作，具有系統管理員群組許可權的使用者可以停止工作，且如果使用者有權執行和讀取工作，則使用者可以停止工作。</span><span class="sxs-lookup"><span data-stu-id="08ea6-117">System account users can stop a task, users with Administrator group privileges can stop a task, and if a user has rights to execute and read a task, then the user can stop the task.</span></span> <span data-ttu-id="08ea6-118">使用者可以停止在與使用者帳戶相同的認證下執行的工作實例。</span><span class="sxs-lookup"><span data-stu-id="08ea6-118">A user can stop the task instances that are running under the same credentials as the user account.</span></span> <span data-ttu-id="08ea6-119">在所有其他情況下，使用者會被拒絕存取來停止工作。</span><span class="sxs-lookup"><span data-stu-id="08ea6-119">In all other cases, the user is denied access to stop the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="08ea6-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="08ea6-120">Requirements</span></span>



| <span data-ttu-id="08ea6-121">需求</span><span class="sxs-lookup"><span data-stu-id="08ea6-121">Requirement</span></span> | <span data-ttu-id="08ea6-122">值</span><span class="sxs-lookup"><span data-stu-id="08ea6-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08ea6-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="08ea6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="08ea6-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08ea6-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="08ea6-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="08ea6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="08ea6-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08ea6-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08ea6-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="08ea6-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="08ea6-128"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="08ea6-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="08ea6-129">DLL</span><span class="sxs-lookup"><span data-stu-id="08ea6-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08ea6-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08ea6-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08ea6-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08ea6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08ea6-132">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="08ea6-132">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





