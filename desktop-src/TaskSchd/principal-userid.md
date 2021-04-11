---
title: Principal. UserId 屬性
description: 針對腳本，取得或設定執行與主體相關聯之工作所需的使用者識別碼。
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- UserId 屬性工作排程器
- UserId 屬性工作排程器、Principal 物件
- Principal 物件工作排程器，UserId 屬性
topic_type:
- apiref
api_name:
- Principal.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6fce7fcfdf235ba8a83f262161c2e0f2afc71c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104357"
---
# <a name="principaluserid-property"></a><span data-ttu-id="56202-106">Principal. UserId 屬性</span><span class="sxs-lookup"><span data-stu-id="56202-106">Principal.UserId property</span></span>

<span data-ttu-id="56202-107">針對腳本，取得或設定執行與主體相關聯之工作所需的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="56202-107">For scripting, gets or sets the user identifier that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="56202-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="56202-108">Syntax</span></span>


```VB
Principal.UserId As String
```



## <a name="property-value"></a><span data-ttu-id="56202-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="56202-109">Property value</span></span>

<span data-ttu-id="56202-110">執行工作所需的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="56202-110">The user identifier that is required to run the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="56202-111">備註</span><span class="sxs-lookup"><span data-stu-id="56202-111">Remarks</span></span>

<span data-ttu-id="56202-112">如果在 [**GroupId**](principal-groupid.md) 屬性中指定群組識別碼，請勿設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="56202-112">Do not set this property if a group identifier is specified in the [**GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="56202-113">讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**UserId**](taskschedulerschema-userid-principaltype-element.md) 元素來指定主體的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="56202-113">When reading or writing XML for a task, the user identifier for the principal is specified using the [**UserId**](taskschedulerschema-userid-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="56202-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="56202-114">Requirements</span></span>



| <span data-ttu-id="56202-115">需求</span><span class="sxs-lookup"><span data-stu-id="56202-115">Requirement</span></span> | <span data-ttu-id="56202-116">值</span><span class="sxs-lookup"><span data-stu-id="56202-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56202-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56202-117">Minimum supported client</span></span><br/> | <span data-ttu-id="56202-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56202-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="56202-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56202-119">Minimum supported server</span></span><br/> | <span data-ttu-id="56202-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56202-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="56202-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="56202-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="56202-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="56202-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="56202-123">DLL</span><span class="sxs-lookup"><span data-stu-id="56202-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56202-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56202-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56202-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56202-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56202-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="56202-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="56202-127">**主要**</span><span class="sxs-lookup"><span data-stu-id="56202-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="56202-128">**Principal**</span><span class="sxs-lookup"><span data-stu-id="56202-128">**Principal.GroupId**</span></span>](principal-groupid.md)
</dt> </dl>

 

 





