---
title: RunLevel (runLevelType) 元素
description: 包含指定執行工作之安全性內容層級的值。
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- RunLevel 元素工作排程器
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d374f5b9ad388f3ad0a626e1b99ecae96eeef1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317499"
---
# <a name="runlevel-runleveltype-element"></a><span data-ttu-id="302ba-104">RunLevel (runLevelType) 元素</span><span class="sxs-lookup"><span data-stu-id="302ba-104">RunLevel (runLevelType) Element</span></span>

<span data-ttu-id="302ba-105">包含指定執行工作之安全性內容層級的值。</span><span class="sxs-lookup"><span data-stu-id="302ba-105">Contains a value that specifies the security context level for running the task.</span></span> <span data-ttu-id="302ba-106">您可以指定使用最低許可權或更高的許可權來執行工作。</span><span class="sxs-lookup"><span data-stu-id="302ba-106">You can specify to run a task using least privileges or elevated privileges.</span></span> <span data-ttu-id="302ba-107">值為0會指定以最低許可權來執行工作，而值為1則指定以較高的許可權執行工作。</span><span class="sxs-lookup"><span data-stu-id="302ba-107">A value of 0 specifies to run the task with lowest privileges, and a value of 1 specifies to run the task with elevated privileges.</span></span>

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

<span data-ttu-id="302ba-108">**RunLevel** 元素是由 [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) simple 型別定義。</span><span class="sxs-lookup"><span data-stu-id="302ba-108">The **RunLevel** element is defined by the [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) simple type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="302ba-109">父元素</span><span class="sxs-lookup"><span data-stu-id="302ba-109">Parent element</span></span>



| <span data-ttu-id="302ba-110">元素</span><span class="sxs-lookup"><span data-stu-id="302ba-110">Element</span></span>                                                                                  | <span data-ttu-id="302ba-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="302ba-111">Derived from</span></span>                                                           | <span data-ttu-id="302ba-112">Description</span><span class="sxs-lookup"><span data-stu-id="302ba-112">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="302ba-113">**Principal (principalType)**</span><span class="sxs-lookup"><span data-stu-id="302ba-113">**Principal (principalType)**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="302ba-114">**principalType**</span><span class="sxs-lookup"><span data-stu-id="302ba-114">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="302ba-115">指定主體的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="302ba-115">Specifies the security credentials for a principal.</span></span> <span data-ttu-id="302ba-116">這些認證會定義工作執行所在的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="302ba-116">These credentials define the security context that a task runs under.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="302ba-117">備註</span><span class="sxs-lookup"><span data-stu-id="302ba-117">Remarks</span></span>

<span data-ttu-id="302ba-118">針對 c + + 開發，請參閱 [**IPrincipal 的 RunLevel 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel)。</span><span class="sxs-lookup"><span data-stu-id="302ba-118">For C++ development, see [**RunLevel Property of IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).</span></span>

<span data-ttu-id="302ba-119">如需腳本開發，請參閱 [**Principal. RunLevel**](principal-runlevel.md)。</span><span class="sxs-lookup"><span data-stu-id="302ba-119">For script development, see [**Principal.RunLevel**](principal-runlevel.md).</span></span>

<span data-ttu-id="302ba-120">如果工作是使用內 **建 \\ 系統管理員** 帳戶或 [LocalSystem](/windows/desktop/Services/localsystem-account) 或 [LocalService](/windows/desktop/Services/localservice-account) 帳戶來註冊的，則會忽略 [**RunLevel**](principal-runlevel.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="302ba-120">If a task is registered using the **Builtin\\Administrator** account or the [LocalSystem](/windows/desktop/Services/localsystem-account) or [LocalService](/windows/desktop/Services/localservice-account) accounts, the [**RunLevel**](principal-runlevel.md) property is ignored.</span></span> <span data-ttu-id="302ba-121">如果已關閉 [使用者帳戶控制](/windows/desktop/SecAuthZ/user-account-control) (UAC) ，也會忽略屬性值。</span><span class="sxs-lookup"><span data-stu-id="302ba-121">The attribute value will also be ignored if [User Account Control](/windows/desktop/SecAuthZ/user-account-control) (UAC) is turned off.</span></span>

<span data-ttu-id="302ba-122">如果工作是使用工作安全性內容的 **Administrators** 群組來註冊的，則您也必須將 [**RunLevel**](principal-runlevel.md) 屬性設定為 "HighestAvailable"，才能執行工作。</span><span class="sxs-lookup"><span data-stu-id="302ba-122">If a task is registered using the **Administrators** group for the security context of the task, then you must also set the [**RunLevel**](principal-runlevel.md) property to "HighestAvailable" to run the task.</span></span> <span data-ttu-id="302ba-123">如需詳細資訊，請參閱工作 [的安全性](security-contexts-for-running-tasks.md)內容。</span><span class="sxs-lookup"><span data-stu-id="302ba-123">For more information, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="302ba-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="302ba-124">Requirements</span></span>



| <span data-ttu-id="302ba-125">需求</span><span class="sxs-lookup"><span data-stu-id="302ba-125">Requirement</span></span> | <span data-ttu-id="302ba-126">值</span><span class="sxs-lookup"><span data-stu-id="302ba-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="302ba-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="302ba-127">Minimum supported client</span></span><br/> | <span data-ttu-id="302ba-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="302ba-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="302ba-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="302ba-129">Minimum supported server</span></span><br/> | <span data-ttu-id="302ba-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="302ba-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

