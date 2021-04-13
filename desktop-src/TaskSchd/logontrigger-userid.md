---
title: LogonTrigger。 UserId 屬性
description: 針對腳本，取得或設定使用者的識別碼。
ms.assetid: d28eea9b-8238-49e7-afec-5a96281b3063
keywords:
- UserId 屬性工作排程器
- UserId 屬性工作排程器，LogonTrigger 物件
- LogonTrigger 物件工作排程器，UserId 屬性
topic_type:
- apiref
api_name:
- LogonTrigger.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dde08f82742325303e62e405cd13d2b9e7c1191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384106"
---
# <a name="logontriggeruserid-property"></a><span data-ttu-id="7bc16-106">LogonTrigger。 UserId 屬性</span><span class="sxs-lookup"><span data-stu-id="7bc16-106">LogonTrigger.UserId property</span></span>

<span data-ttu-id="7bc16-107">針對腳本，取得或設定使用者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7bc16-107">For scripting, gets or sets the identifier of the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bc16-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bc16-108">Syntax</span></span>


```VB
LogonTrigger.UserId As String
```



## <a name="property-value"></a><span data-ttu-id="7bc16-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="7bc16-109">Property value</span></span>

<span data-ttu-id="7bc16-110">使用者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7bc16-110">The identifier of the user.</span></span> <span data-ttu-id="7bc16-111">例如，"MyDomain \\ MyName" 或本機帳戶 "Administrator"。</span><span class="sxs-lookup"><span data-stu-id="7bc16-111">For example, "MyDomain\\MyName" or for a local account, "Administrator".</span></span>

<span data-ttu-id="7bc16-112">這個屬性可以是下列其中一種格式：</span><span class="sxs-lookup"><span data-stu-id="7bc16-112">This property can be in one of the following formats:</span></span>

-   <span data-ttu-id="7bc16-113">使用者名稱或 SID：當使用者登入電腦時，就會啟動工作。</span><span class="sxs-lookup"><span data-stu-id="7bc16-113">User name or SID: The task is started when the user logs on to the computer.</span></span>
-   <span data-ttu-id="7bc16-114">Null：當任何使用者登入電腦時，就會啟動工作。</span><span class="sxs-lookup"><span data-stu-id="7bc16-114">NULL: The task is started when any user logs on to the computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bc16-115">備註</span><span class="sxs-lookup"><span data-stu-id="7bc16-115">Remarks</span></span>

<span data-ttu-id="7bc16-116">如果您想要在群組的任何成員登入電腦而非特定使用者登入時觸發工作，則不要將值指派給 **LogonTrigger。 UserId** 屬性。</span><span class="sxs-lookup"><span data-stu-id="7bc16-116">If you want a task to be triggered when any member of a group logs on to the computer rather than when a specific user logs on, then do not assign a value to the **LogonTrigger.UserId** property.</span></span> <span data-ttu-id="7bc16-117">相反地，請使用 **LogonTrigger 的 UserId** 屬性建立登入觸發程式，並使用 [**principal**](principal-groupid.md) 屬性將值指派給工作的主體。</span><span class="sxs-lookup"><span data-stu-id="7bc16-117">Instead, create a logon trigger with an empty **LogonTrigger.UserId** property and assign a value to the principal for the task using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="7bc16-118">讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) 元素來指定登入使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="7bc16-118">When reading or writing XML for a task, the logon user identifier is specified using the [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bc16-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="7bc16-119">Requirements</span></span>



| <span data-ttu-id="7bc16-120">需求</span><span class="sxs-lookup"><span data-stu-id="7bc16-120">Requirement</span></span> | <span data-ttu-id="7bc16-121">值</span><span class="sxs-lookup"><span data-stu-id="7bc16-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bc16-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7bc16-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7bc16-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7bc16-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7bc16-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7bc16-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7bc16-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7bc16-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7bc16-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="7bc16-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="7bc16-127"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7bc16-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7bc16-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7bc16-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bc16-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bc16-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bc16-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7bc16-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bc16-131">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="7bc16-131">**LogonTrigger**</span></span>](logontrigger.md)
</dt> <dt>

[<span data-ttu-id="7bc16-132">工作排程器</span><span class="sxs-lookup"><span data-stu-id="7bc16-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





