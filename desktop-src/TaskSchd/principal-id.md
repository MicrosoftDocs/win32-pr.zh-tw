---
title: Principal.Id 屬性
description: 針對腳本，取得或設定主體的識別碼。
ms.assetid: 54112977-9c30-4c52-bffd-7625eeb79f82
keywords:
- Id 屬性工作排程器
- Id 屬性工作排程器、Principal 物件
- Principal 物件工作排程器、Id 屬性
topic_type:
- apiref
api_name:
- Principal.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fb3561bb5266a649dc230f84b9e35e68e005d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385009"
---
# <a name="principalid-property"></a><span data-ttu-id="33921-106">Principal.Id 屬性</span><span class="sxs-lookup"><span data-stu-id="33921-106">Principal.Id property</span></span>

<span data-ttu-id="33921-107">針對腳本，取得或設定主體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="33921-107">For scripting, gets or sets the identifier of the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="33921-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="33921-108">Syntax</span></span>


```VB
Principal.Id As String
```



## <a name="property-value"></a><span data-ttu-id="33921-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="33921-109">Property value</span></span>

<span data-ttu-id="33921-110">主體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="33921-110">The identifier of the principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="33921-111">備註</span><span class="sxs-lookup"><span data-stu-id="33921-111">Remarks</span></span>

<span data-ttu-id="33921-112">指定 [**actioncollection 動作**](actioncollection-context.md) 時，也會使用這個識別碼。</span><span class="sxs-lookup"><span data-stu-id="33921-112">This identifier is also used when specifying the [**ActionCollection.Context**](actioncollection-context.md) property.</span></span>

<span data-ttu-id="33921-113">讀取或寫入工作的 XML 時，主體的識別碼會指定于工作排程器架構之 [**principal**](taskschedulerschema-principal-principaltype-element.md) 元素的 Id 屬性中。</span><span class="sxs-lookup"><span data-stu-id="33921-113">When reading or writing XML for a task, the identifier of the principal is specified in the Id attribute of the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="33921-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="33921-114">Requirements</span></span>



| <span data-ttu-id="33921-115">需求</span><span class="sxs-lookup"><span data-stu-id="33921-115">Requirement</span></span> | <span data-ttu-id="33921-116">值</span><span class="sxs-lookup"><span data-stu-id="33921-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33921-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33921-117">Minimum supported client</span></span><br/> | <span data-ttu-id="33921-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33921-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="33921-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33921-119">Minimum supported server</span></span><br/> | <span data-ttu-id="33921-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33921-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="33921-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="33921-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="33921-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="33921-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="33921-123">DLL</span><span class="sxs-lookup"><span data-stu-id="33921-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33921-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33921-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33921-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33921-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33921-126">**Actioncollection 動作。內容**</span><span class="sxs-lookup"><span data-stu-id="33921-126">**ActionCollection.Context**</span></span>](actioncollection-context.md)
</dt> <dt>

[<span data-ttu-id="33921-127">**主要**</span><span class="sxs-lookup"><span data-stu-id="33921-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="33921-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="33921-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





