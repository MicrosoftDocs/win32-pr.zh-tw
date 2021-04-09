---
title: RegisteredTaskCollection 物件
description: 腳本物件，其中包含所有已註冊的工作。
ms.assetid: 0bd2010d-af25-4316-8829-62e4ec4761e2
keywords:
- RegisteredTaskCollection 物件工作排程器
- RegisteredTaskCollection 物件工作排程器，說明
topic_type:
- apiref
api_name:
- RegisteredTaskCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11c299bc8817cc1627c40b3c465cd182e0f4c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024773"
---
# <a name="registeredtaskcollection-object"></a><span data-ttu-id="7405b-105">RegisteredTaskCollection 物件</span><span class="sxs-lookup"><span data-stu-id="7405b-105">RegisteredTaskCollection object</span></span>

<span data-ttu-id="7405b-106">腳本物件，其中包含所有已註冊的工作。</span><span class="sxs-lookup"><span data-stu-id="7405b-106">Scripting object that contains all the tasks that are registered.</span></span>

## <a name="members"></a><span data-ttu-id="7405b-107">成員</span><span class="sxs-lookup"><span data-stu-id="7405b-107">Members</span></span>

<span data-ttu-id="7405b-108">**RegisteredTaskCollection** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7405b-108">The **RegisteredTaskCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="7405b-109">屬性</span><span class="sxs-lookup"><span data-stu-id="7405b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7405b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7405b-110">Properties</span></span>

<span data-ttu-id="7405b-111">**RegisteredTaskCollection** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7405b-111">The **RegisteredTaskCollection** object has these properties.</span></span>



| <span data-ttu-id="7405b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="7405b-112">Property</span></span>                                                   | <span data-ttu-id="7405b-113">存取類型</span><span class="sxs-lookup"><span data-stu-id="7405b-113">Access type</span></span>          | <span data-ttu-id="7405b-114">Description</span><span class="sxs-lookup"><span data-stu-id="7405b-114">Description</span></span>                                                        |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="7405b-115">**計數**</span><span class="sxs-lookup"><span data-stu-id="7405b-115">**Count**</span></span>](registeredtaskcollection-count.md)<br/> | <span data-ttu-id="7405b-116">唯讀</span><span class="sxs-lookup"><span data-stu-id="7405b-116">Read-only</span></span><br/> | <span data-ttu-id="7405b-117">取得集合中已註冊工作的數目。</span><span class="sxs-lookup"><span data-stu-id="7405b-117">Gets the number of registered tasks in the collection.</span></span><br/>  |
| [<span data-ttu-id="7405b-118">**項目**</span><span class="sxs-lookup"><span data-stu-id="7405b-118">**Item**</span></span>](registeredtaskcollection-item.md)<br/>   | <span data-ttu-id="7405b-119">唯讀</span><span class="sxs-lookup"><span data-stu-id="7405b-119">Read-only</span></span><br/> | <span data-ttu-id="7405b-120">從集合中取得指定的已註冊工作。</span><span class="sxs-lookup"><span data-stu-id="7405b-120">Gets the specified registered task from the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="7405b-121">範例</span><span class="sxs-lookup"><span data-stu-id="7405b-121">Examples</span></span>

<span data-ttu-id="7405b-122">如需此腳本物件的詳細資訊和程式碼範例，請參閱 [顯示工作名稱和狀態 (腳本) ](displaying-task-names-and-state--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="7405b-122">For more information and example code for this scripting object, see [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7405b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="7405b-123">Requirements</span></span>



| <span data-ttu-id="7405b-124">需求</span><span class="sxs-lookup"><span data-stu-id="7405b-124">Requirement</span></span> | <span data-ttu-id="7405b-125">值</span><span class="sxs-lookup"><span data-stu-id="7405b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7405b-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7405b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7405b-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7405b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7405b-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7405b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7405b-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7405b-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7405b-130">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="7405b-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="7405b-131"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7405b-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7405b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7405b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7405b-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7405b-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7405b-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7405b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7405b-135">**TaskFolder.GetTasks**</span><span class="sxs-lookup"><span data-stu-id="7405b-135">**TaskFolder.GetTasks**</span></span>](taskfolder-gettasks.md)
</dt> </dl>

 

 





