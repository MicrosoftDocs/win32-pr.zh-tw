---
title: 'LVM_SETCOLUMNWIDTH 訊息 (Commctrl .h) '
description: 變更報表檢視模式中的資料行寬度，或在清單視圖模式中變更所有資料行的寬度。 您可以明確地傳送此訊息，或使用 ListView \_ SetColumnWidth 宏。
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- LVM_SETCOLUMNWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529e989b3d66562acc7b6f91c3b3b06527235e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093840"
---
# <a name="lvm_setcolumnwidth-message"></a><span data-ttu-id="7655f-105">LVM \_ SETCOLUMNWIDTH 訊息</span><span class="sxs-lookup"><span data-stu-id="7655f-105">LVM\_SETCOLUMNWIDTH message</span></span>

<span data-ttu-id="7655f-106">變更報表檢視模式中的資料行寬度，或在清單視圖模式中變更所有資料行的寬度。</span><span class="sxs-lookup"><span data-stu-id="7655f-106">Changes the width of a column in report-view mode or the width of all columns in list-view mode.</span></span> <span data-ttu-id="7655f-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) 宏。</span><span class="sxs-lookup"><span data-stu-id="7655f-107">You can send this message explicitly or use the [**ListView\_SetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7655f-108">參數</span><span class="sxs-lookup"><span data-stu-id="7655f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7655f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7655f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7655f-110">有效資料行以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="7655f-110">Zero-based index of a valid column.</span></span> <span data-ttu-id="7655f-111">若為清單視圖模式，此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="7655f-111">For list-view mode, this parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7655f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7655f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7655f-113">資料行的新寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="7655f-113">New width of the column, in pixels.</span></span> <span data-ttu-id="7655f-114">針對報表檢視模式，支援下列特殊值：</span><span class="sxs-lookup"><span data-stu-id="7655f-114">For report-view mode, the following special values are supported:</span></span>



| <span data-ttu-id="7655f-115">值</span><span class="sxs-lookup"><span data-stu-id="7655f-115">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="7655f-116">意義</span><span class="sxs-lookup"><span data-stu-id="7655f-116">Meaning</span></span>                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <span data-ttu-id="7655f-117"><dt>**LVSCW \_ AUTOSIZE**</dt></span><span class="sxs-lookup"><span data-stu-id="7655f-117"><dt>**LVSCW\_AUTOSIZE**</dt></span></span> </dl>                                | <span data-ttu-id="7655f-118">自動調整資料行的大小。</span><span class="sxs-lookup"><span data-stu-id="7655f-118">Automatically sizes the column.</span></span><br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <span data-ttu-id="7655f-119"><dt>**LVSCW \_ AUTOSIZE \_ USEHEADER**</dt></span><span class="sxs-lookup"><span data-stu-id="7655f-119"><dt>**LVSCW\_AUTOSIZE\_USEHEADER**</dt></span></span> </dl> | <span data-ttu-id="7655f-120">自動調整資料行大小以符合標頭文字。</span><span class="sxs-lookup"><span data-stu-id="7655f-120">Automatically sizes the column to fit the header text.</span></span> <span data-ttu-id="7655f-121">如果您使用此值與最後一個資料行，它的寬度會設定為填滿清單視圖控制項的剩餘寬度。</span><span class="sxs-lookup"><span data-stu-id="7655f-121">If you use this value with the last column, its width is set to fill the remaining width of the list-view control.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7655f-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="7655f-122">Return value</span></span>

<span data-ttu-id="7655f-123">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="7655f-123">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7655f-124">備註</span><span class="sxs-lookup"><span data-stu-id="7655f-124">Remarks</span></span>

<span data-ttu-id="7655f-125">假設您有一個寬度為500圖元的2個數據行清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="7655f-125">Assume that you have a 2-column list-view control with a width of 500 pixels.</span></span> <span data-ttu-id="7655f-126">如果資料行零的寬度設定為200圖元，且您使用 *wParam* = 1 和 *lParam* = LVSCW AUTOSIZE USEHEADER 來傳送此訊息， \_ \_ 則第二個 (和最後一個) 資料行將會是300圖元寬。</span><span class="sxs-lookup"><span data-stu-id="7655f-126">If the width of column zero is set to 200 pixels, and you send this message with *wParam* = 1 and *lParam* = LVSCW\_AUTOSIZE\_USEHEADER, the second (and last) column will be 300 pixels wide.</span></span>

## <a name="requirements"></a><span data-ttu-id="7655f-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="7655f-127">Requirements</span></span>



| <span data-ttu-id="7655f-128">需求</span><span class="sxs-lookup"><span data-stu-id="7655f-128">Requirement</span></span> | <span data-ttu-id="7655f-129">值</span><span class="sxs-lookup"><span data-stu-id="7655f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7655f-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7655f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7655f-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7655f-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7655f-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7655f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7655f-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7655f-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7655f-134">標頭</span><span class="sxs-lookup"><span data-stu-id="7655f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7655f-135"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7655f-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





