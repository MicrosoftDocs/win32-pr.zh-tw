---
title: 'LVM_INSERTCOLUMN 訊息 (Commctrl .h) '
description: 在清單視圖控制項中插入新的資料行。 您可以明確地傳送此訊息，或使用 ListView \_ InsertColumn 宏來傳送。
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- LVM_INSERTCOLUMN message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be89ff0b4ef417a715085582544112cb90cb6b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509155"
---
# <a name="lvm_insertcolumn-message"></a><span data-ttu-id="eecf2-105">LVM \_ INSERTCOLUMN 訊息</span><span class="sxs-lookup"><span data-stu-id="eecf2-105">LVM\_INSERTCOLUMN message</span></span>

<span data-ttu-id="eecf2-106">在清單視圖控制項中插入新的資料行。</span><span class="sxs-lookup"><span data-stu-id="eecf2-106">Inserts a new column in a list-view control.</span></span> <span data-ttu-id="eecf2-107">您可以明確地傳送此訊息，或使用 [**ListView \_ InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="eecf2-107">You can send this message explicitly or by using the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="eecf2-108">參數</span><span class="sxs-lookup"><span data-stu-id="eecf2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eecf2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eecf2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eecf2-110">新資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="eecf2-110">Index of the new column.</span></span>

</dd> <dt>

<span data-ttu-id="eecf2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eecf2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eecf2-112">[**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna)結構的指標，其中包含新資料行的屬性。</span><span class="sxs-lookup"><span data-stu-id="eecf2-112">Pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that contains the attributes of the new column.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eecf2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="eecf2-113">Return value</span></span>

<span data-ttu-id="eecf2-114">如果成功，則傳回新資料行的索引，否則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="eecf2-114">Returns the index of the new column if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="eecf2-115">備註</span><span class="sxs-lookup"><span data-stu-id="eecf2-115">Remarks</span></span>

<span data-ttu-id="eecf2-116">只有在報表 (詳細資料) 視圖中，才會顯示資料行。</span><span class="sxs-lookup"><span data-stu-id="eecf2-116">Columns are visible only in report (details) view.</span></span>

## <a name="requirements"></a><span data-ttu-id="eecf2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="eecf2-117">Requirements</span></span>



| <span data-ttu-id="eecf2-118">需求</span><span class="sxs-lookup"><span data-stu-id="eecf2-118">Requirement</span></span> | <span data-ttu-id="eecf2-119">值</span><span class="sxs-lookup"><span data-stu-id="eecf2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eecf2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eecf2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eecf2-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eecf2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eecf2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eecf2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eecf2-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eecf2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eecf2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="eecf2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="eecf2-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="eecf2-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





