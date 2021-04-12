---
title: Principal. RunLevel 屬性
description: 針對腳本，取得或設定用來指定執行與主體相關聯之工作所需之許可權等級的識別碼。
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- RunLevel 屬性工作排程器
- RunLevel 屬性工作排程器、Principal 物件
- Principal 物件工作排程器，RunLevel 屬性
topic_type:
- apiref
api_name:
- Principal.RunLevel
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acb6c4c86215312b2df73f7bf85847ef61a4b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508660"
---
# <a name="principalrunlevel-property"></a><span data-ttu-id="6f59a-106">Principal. RunLevel 屬性</span><span class="sxs-lookup"><span data-stu-id="6f59a-106">Principal.RunLevel property</span></span>

<span data-ttu-id="6f59a-107">針對腳本，取得或設定用來指定執行與主體相關聯之工作所需之許可權等級的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f59a-107">For scripting, gets or sets the identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span>

<span data-ttu-id="6f59a-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f59a-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f59a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f59a-109">Syntax</span></span>


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="6f59a-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="6f59a-110">Property value</span></span>

<span data-ttu-id="6f59a-111">用來指定執行與主體相關聯之工作所需之許可權層級的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f59a-111">The identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span>



| <span data-ttu-id="6f59a-112">值</span><span class="sxs-lookup"><span data-stu-id="6f59a-112">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="6f59a-113">意義</span><span class="sxs-lookup"><span data-stu-id="6f59a-113">Meaning</span></span>                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <span data-ttu-id="6f59a-114"><dt>**工作 \_RUNLEVEL \_ LUA**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6f59a-114"><dt>**TASK\_RUNLEVEL\_LUA**</dt> <dt>0</dt></span></span> </dl>             | <span data-ttu-id="6f59a-115">工作會以最少的許可權執行， (LUA) 。</span><span class="sxs-lookup"><span data-stu-id="6f59a-115">Tasks will be run with the least privileges (LUA).</span></span><br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <span data-ttu-id="6f59a-116"><dt>**工作 \_RUNLEVEL \_ 最高**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6f59a-116"><dt>**TASK\_RUNLEVEL\_HIGHEST**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="6f59a-117">工作會以最高的許可權執行。</span><span class="sxs-lookup"><span data-stu-id="6f59a-117">Tasks will be run with the highest privileges.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="6f59a-118">備註</span><span class="sxs-lookup"><span data-stu-id="6f59a-118">Remarks</span></span>

<span data-ttu-id="6f59a-119">如果工作是使用內建 \\ 系統管理員帳戶或本機系統或本地服務帳戶來註冊的，則會忽略 **RunLevel** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6f59a-119">If a task is registered using the Builtin\\Administrator account or the Local System or Local Service accounts, then the **RunLevel** property will be ignored.</span></span> <span data-ttu-id="6f59a-120">如果已關閉使用者帳戶控制 (UAC) ，也會忽略屬性值。</span><span class="sxs-lookup"><span data-stu-id="6f59a-120">The property value will also be ignored if User Account Control (UAC) is turned off.</span></span>

<span data-ttu-id="6f59a-121">如果工作是使用工作安全性內容的 Administrators 群組來註冊的，則您也必須將 [ [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) ] 屬性設定為 [ **task \_ RunLevel \_** ] （如果您想要執行此工作）。</span><span class="sxs-lookup"><span data-stu-id="6f59a-121">If a task is registered using the Administrators group for the security context of the task, then you must also set the [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) property to **TASK\_RUNLEVEL\_HIGHEST** if you want to run the task.</span></span> <span data-ttu-id="6f59a-122">如需詳細資訊，請參閱工作 [的安全性](security-contexts-for-running-tasks.md)內容。</span><span class="sxs-lookup"><span data-stu-id="6f59a-122">For more information, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f59a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f59a-123">Requirements</span></span>



| <span data-ttu-id="6f59a-124">需求</span><span class="sxs-lookup"><span data-stu-id="6f59a-124">Requirement</span></span> | <span data-ttu-id="6f59a-125">值</span><span class="sxs-lookup"><span data-stu-id="6f59a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f59a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f59a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6f59a-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f59a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6f59a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f59a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6f59a-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f59a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6f59a-130">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6f59a-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f59a-131"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6f59a-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6f59a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6f59a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f59a-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f59a-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f59a-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f59a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f59a-135">**主要**</span><span class="sxs-lookup"><span data-stu-id="6f59a-135">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





