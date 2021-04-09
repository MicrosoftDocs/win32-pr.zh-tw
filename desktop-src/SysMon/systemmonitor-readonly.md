---
title: SystemMonitor ReadOnly 屬性
description: 抓取或設定值，這個值會決定使用者是否可以修改控制項的屬性值。
ms.assetid: 6ecfd63a-09b1-46eb-803f-6cb05bdecc25
keywords:
- ReadOnly 屬性 SysMon
- ReadOnly 屬性 SysMon，SystemMonitor 類別
- SystemMonitor 類別 SysMon，ReadOnly 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.ReadOnly
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f42481e1bb0df0966f09ee354421af6378969f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934335"
---
# <a name="systemmonitorreadonly-property"></a><span data-ttu-id="e5321-106">SystemMonitor ReadOnly 屬性</span><span class="sxs-lookup"><span data-stu-id="e5321-106">SystemMonitor.ReadOnly property</span></span>

<span data-ttu-id="e5321-107">抓取或設定值，這個值會決定使用者是否可以修改控制項的屬性值。</span><span class="sxs-lookup"><span data-stu-id="e5321-107">Retrieves or sets a value that determines whether a user can modify the property values of the control.</span></span>

<span data-ttu-id="e5321-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e5321-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5321-109">語法</span><span class="sxs-lookup"><span data-stu-id="e5321-109">Syntax</span></span>


```VB
Property ReadOnly As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e5321-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e5321-110">Property value</span></span>

<span data-ttu-id="e5321-111">如果您不想讓使用者修改控制項的屬性值，則為 True。否則為 false。</span><span class="sxs-lookup"><span data-stu-id="e5321-111">True if you do not want the user to modify the property values of the control; otherwise, false.</span></span> <span data-ttu-id="e5321-112">預設值為 false，表示使用者可以修改控制項的屬性值。</span><span class="sxs-lookup"><span data-stu-id="e5321-112">The default value is false, meaning that users can modify the property values of the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5321-113">備註</span><span class="sxs-lookup"><span data-stu-id="e5321-113">Remarks</span></span>

<span data-ttu-id="e5321-114">當此屬性的值為 True 時，下列條件就會生效：</span><span class="sxs-lookup"><span data-stu-id="e5321-114">When the value of this property is True, the following conditions are in effect:</span></span>

-   <span data-ttu-id="e5321-115">使用者無法使用內容功能表。</span><span class="sxs-lookup"><span data-stu-id="e5321-115">The user cannot use the context menu.</span></span>
-   <span data-ttu-id="e5321-116">下列工具列按鈕已停用：</span><span class="sxs-lookup"><span data-stu-id="e5321-116">The following toolbar buttons are disabled:</span></span>
    -   <span data-ttu-id="e5321-117">新的計數器集合</span><span class="sxs-lookup"><span data-stu-id="e5321-117">New Counter Set</span></span>
    -   <span data-ttu-id="e5321-118">檢視目前的活動</span><span class="sxs-lookup"><span data-stu-id="e5321-118">View Current Activity</span></span>
    -   <span data-ttu-id="e5321-119">檢視記錄檔資料</span><span class="sxs-lookup"><span data-stu-id="e5321-119">View Log File Data</span></span>
    -   <span data-ttu-id="e5321-120">加</span><span class="sxs-lookup"><span data-stu-id="e5321-120">Add</span></span>
    -   <span data-ttu-id="e5321-121">刪除</span><span class="sxs-lookup"><span data-stu-id="e5321-121">Delete</span></span>
    -   <span data-ttu-id="e5321-122">貼上計數器清單</span><span class="sxs-lookup"><span data-stu-id="e5321-122">Paste Counter List</span></span>
    -   <span data-ttu-id="e5321-123">屬性</span><span class="sxs-lookup"><span data-stu-id="e5321-123">Properties</span></span>

<span data-ttu-id="e5321-124">請注意，此屬性只會影響使用者透過使用者介面修改屬性值的能力，而不會讓您無法以程式設計方式修改屬性值或計數器。</span><span class="sxs-lookup"><span data-stu-id="e5321-124">Note that this property affects only the user's ability to modify property values through the user interface, it does not prevent you from programmatically modifying property values or counters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5321-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5321-125">Requirements</span></span>



| <span data-ttu-id="e5321-126">需求</span><span class="sxs-lookup"><span data-stu-id="e5321-126">Requirement</span></span> | <span data-ttu-id="e5321-127">值</span><span class="sxs-lookup"><span data-stu-id="e5321-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5321-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5321-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e5321-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5321-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e5321-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5321-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e5321-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5321-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e5321-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e5321-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5321-133"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e5321-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5321-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5321-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5321-135">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="e5321-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





