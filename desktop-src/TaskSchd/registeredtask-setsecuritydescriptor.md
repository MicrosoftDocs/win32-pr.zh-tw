---
title: RegisteredTask. SetSecurityDescriptor 方法
description: 針對腳本，設定用來作為已註冊工作認證的安全描述項。
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- SetSecurityDescriptor 方法工作排程器
- SetSecurityDescriptor 方法工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器，SetSecurityDescriptor 方法
topic_type:
- apiref
api_name:
- RegisteredTask.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 386c97c470b94686c0a1f654313c6ef1e0bca5a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105684"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a><span data-ttu-id="53b8c-106">RegisteredTask. SetSecurityDescriptor 方法</span><span class="sxs-lookup"><span data-stu-id="53b8c-106">RegisteredTask.SetSecurityDescriptor method</span></span>

<span data-ttu-id="53b8c-107">針對腳本，設定用來作為已註冊工作認證的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="53b8c-107">For scripting, sets the security descriptor that is used as credentials for the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="53b8c-108">語法</span><span class="sxs-lookup"><span data-stu-id="53b8c-108">Syntax</span></span>


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="53b8c-109">參數</span><span class="sxs-lookup"><span data-stu-id="53b8c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53b8c-110">*sddl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53b8c-110">*sddl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53b8c-111">用來作為已註冊工作之認證的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="53b8c-111">The security descriptor that is used as credentials for the registered task.</span></span>

> [!Note]  
> <span data-ttu-id="53b8c-112">如果本機系統帳戶拒絕存取某項工作，工作排程器服務可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="53b8c-112">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="53b8c-113">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53b8c-113">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53b8c-114">指定如何設定安全描述項的旗標。</span><span class="sxs-lookup"><span data-stu-id="53b8c-114">Flags that specify how to set the security descriptor.</span></span> <span data-ttu-id="53b8c-115">您 \_ \_ \_ \_ 可以指定工作 [**\_ 建立**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) 列舉 (0x10) 的工作不新增主體 ACE 旗標。</span><span class="sxs-lookup"><span data-stu-id="53b8c-115">The TASK\_DONT\_ADD\_PRINCIPAL\_ACE flag (0x10) from the [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) enumeration can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53b8c-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="53b8c-116">Return value</span></span>

<span data-ttu-id="53b8c-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="53b8c-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53b8c-118">備註</span><span class="sxs-lookup"><span data-stu-id="53b8c-118">Remarks</span></span>

<span data-ttu-id="53b8c-119">您可以在工作的安全描述項中指定 (ACL) 的存取控制清單，以允許或拒絕特定使用者和群組對工作的存取。</span><span class="sxs-lookup"><span data-stu-id="53b8c-119">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

## <a name="requirements"></a><span data-ttu-id="53b8c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="53b8c-120">Requirements</span></span>



| <span data-ttu-id="53b8c-121">需求</span><span class="sxs-lookup"><span data-stu-id="53b8c-121">Requirement</span></span> | <span data-ttu-id="53b8c-122">值</span><span class="sxs-lookup"><span data-stu-id="53b8c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53b8c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53b8c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="53b8c-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53b8c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="53b8c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53b8c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="53b8c-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53b8c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="53b8c-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="53b8c-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="53b8c-128"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="53b8c-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="53b8c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="53b8c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53b8c-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53b8c-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53b8c-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53b8c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53b8c-132">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="53b8c-132">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="53b8c-133">**TaskFolder. GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="53b8c-133">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="53b8c-134">**RegisteredTask.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="53b8c-134">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





