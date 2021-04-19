---
title: Principal. GroupId 屬性
description: 針對腳本，取得或設定執行與主體相關聯之工作所需之使用者群組的識別碼。
ms.assetid: be0b7cd1-0e17-4aa5-af8e-880c95b3e7dc
keywords:
- GroupId 屬性工作排程器
- GroupId 屬性工作排程器、Principal 物件
- Principal 物件工作排程器，GroupId 屬性
topic_type:
- apiref
api_name:
- Principal.GroupId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5acd17d32b0123723fe53f91e390c37f42d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995166"
---
# <a name="principalgroupid-property"></a><span data-ttu-id="1d887-106">Principal. GroupId 屬性</span><span class="sxs-lookup"><span data-stu-id="1d887-106">Principal.GroupId property</span></span>

<span data-ttu-id="1d887-107">針對腳本，取得或設定執行與主體相關聯之工作所需之使用者群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d887-107">For scripting, gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d887-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d887-108">Syntax</span></span>


```VB
Principal.GroupId As String
```



## <a name="property-value"></a><span data-ttu-id="1d887-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="1d887-109">Property value</span></span>

<span data-ttu-id="1d887-110">與此主體相關聯之使用者群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d887-110">The identifier of the user group that is associated with this principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d887-111">備註</span><span class="sxs-lookup"><span data-stu-id="1d887-111">Remarks</span></span>

<span data-ttu-id="1d887-112">如果在 [**UserId**](principal-userid.md) 屬性中指定使用者識別碼，請勿設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="1d887-112">Do not set this property if a user identifier is specified in the [**UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="1d887-113">讀取或寫入工作的 XML 時，會在工作排程器架構的 [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) 元素中指定主體的群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d887-113">When reading or writing XML for a task, the group identifier for a principal is specified in the [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d887-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d887-114">Requirements</span></span>



| <span data-ttu-id="1d887-115">需求</span><span class="sxs-lookup"><span data-stu-id="1d887-115">Requirement</span></span> | <span data-ttu-id="1d887-116">值</span><span class="sxs-lookup"><span data-stu-id="1d887-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d887-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d887-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1d887-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d887-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1d887-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d887-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1d887-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d887-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1d887-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1d887-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="1d887-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1d887-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1d887-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1d887-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d887-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d887-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d887-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d887-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d887-126">**UserId**</span><span class="sxs-lookup"><span data-stu-id="1d887-126">**UserId**</span></span>](principal-userid.md)
</dt> <dt>

[<span data-ttu-id="1d887-127">**主要**</span><span class="sxs-lookup"><span data-stu-id="1d887-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="1d887-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="1d887-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





