---
title: 'TVM_SETBORDER 訊息 (Commctrl .h) '
description: 針對樹狀檢視控制項中的專案，設定框線的大小。 您可以使用 TreeView SetBorder 宏明確地傳送訊息 \_ 。
ms.assetid: 468b46ae-2ab2-4753-a0af-7c644f75ce62
keywords:
- TVM_SETBORDER message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b4401959e2579caab7f2cb4b6eed1ea34481ffa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843784"
---
# <a name="tvm_setborder-message"></a><span data-ttu-id="d82b3-105">TVM \_ SETBORDER 訊息</span><span class="sxs-lookup"><span data-stu-id="d82b3-105">TVM\_SETBORDER message</span></span>

<span data-ttu-id="d82b3-106">**適用于內部用途;不建議在應用程式中使用。**</span><span class="sxs-lookup"><span data-stu-id="d82b3-106">**Intended for internal use; not recommended for use in applications.**</span></span>

<span data-ttu-id="d82b3-107">針對樹狀檢視控制項中的專案，設定框線的大小。</span><span class="sxs-lookup"><span data-stu-id="d82b3-107">Sets the size of the border for the items in a tree-view control.</span></span> <span data-ttu-id="d82b3-108">您可以使用 [**TreeView \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) 宏明確地傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="d82b3-108">You can send the message explicitly or by using the [**TreeView\_SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d82b3-109">參數</span><span class="sxs-lookup"><span data-stu-id="d82b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d82b3-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d82b3-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d82b3-111">動作旗標。</span><span class="sxs-lookup"><span data-stu-id="d82b3-111">Action flags.</span></span> <span data-ttu-id="d82b3-112">這個參數可以是下列其中一個或多個值：</span><span class="sxs-lookup"><span data-stu-id="d82b3-112">This parameter can be one or more of the following values:</span></span>



| <span data-ttu-id="d82b3-113">值</span><span class="sxs-lookup"><span data-stu-id="d82b3-113">Value</span></span>                                                                                                                                                         | <span data-ttu-id="d82b3-114">意義</span><span class="sxs-lookup"><span data-stu-id="d82b3-114">Meaning</span></span>                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="TVSBF_XBORDER"></span><span id="tvsbf_xborder"></span><dl> <span data-ttu-id="d82b3-115"><dt>**TVSBF \_ XBORDER**</dt></span><span class="sxs-lookup"><span data-stu-id="d82b3-115"><dt>**TVSBF\_XBORDER**</dt></span></span> </dl> | <span data-ttu-id="d82b3-116">將指定的框線大小套用至樹狀檢視控制項中專案的左邊。</span><span class="sxs-lookup"><span data-stu-id="d82b3-116">Applies the specified border size to the left side of the items in the tree-view control.</span></span> <br/> |
| <span id="TVSBF_YBORDER"></span><span id="tvsbf_yborder"></span><dl> <span data-ttu-id="d82b3-117"><dt>**TVSBF \_ YBORDER**</dt></span><span class="sxs-lookup"><span data-stu-id="d82b3-117"><dt>**TVSBF\_YBORDER**</dt></span></span> </dl> | <span data-ttu-id="d82b3-118">將指定的框線大小套用至樹狀檢視控制項中的專案頂端。</span><span class="sxs-lookup"><span data-stu-id="d82b3-118">Applies the specified border size to the top of the items in the tree-view control.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="d82b3-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d82b3-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d82b3-120">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是指定左邊框線大小的 **簡短** 值（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d82b3-120">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **SHORT** that specifies the size of the left border, in pixels.</span></span> <span data-ttu-id="d82b3-121">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))是指定上框線大小的 **簡短** 值（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d82b3-121">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **SHORT** that specifies the size of the top border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d82b3-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="d82b3-122">Return value</span></span>

<span data-ttu-id="d82b3-123">傳回包含先前框線大小的 **長** 數值（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d82b3-123">Returns a **LONG** value that contains the previous border size, in pixels.</span></span> <span data-ttu-id="d82b3-124">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含水準框線的先前大小，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))包含垂直框線的先前大小。</span><span class="sxs-lookup"><span data-stu-id="d82b3-124">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the previous size of the horizontal border, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the previous size of the vertical border.</span></span>

## <a name="remarks"></a><span data-ttu-id="d82b3-125">備註</span><span class="sxs-lookup"><span data-stu-id="d82b3-125">Remarks</span></span>

<span data-ttu-id="d82b3-126">**安全性警告：** 使用此訊息可能會危害程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="d82b3-126">**Security Warning:** Using this message might compromise the security of your program.</span></span>

<span data-ttu-id="d82b3-127">專案框線的設定只是為了間距之用。</span><span class="sxs-lookup"><span data-stu-id="d82b3-127">The item border is set just for spacing purposes.</span></span> <span data-ttu-id="d82b3-128">成功的設定會觸發捲軸的重新計算。</span><span class="sxs-lookup"><span data-stu-id="d82b3-128">A successful setting triggers a recalculation of the scroll bars.</span></span>

<span data-ttu-id="d82b3-129">未來的 Comctl32.dll 版本可能不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="d82b3-129">This message may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="d82b3-130">此外，commctrl 中並未定義此訊息。</span><span class="sxs-lookup"><span data-stu-id="d82b3-130">Also, this message is not defined in commctrl.h.</span></span> <span data-ttu-id="d82b3-131">將下列定義新增至您應用程式的原始程式檔，以使用訊息：</span><span class="sxs-lookup"><span data-stu-id="d82b3-131">Add the following definitions to the source files of your application to use the message:</span></span>

``` syntax
#define TVM_SETBORDER (TV_FIRST + 35)
#define TVSBF_XBORDER 0x00000001
#define TVSBF_YBORDER 0x00000002 
```

## <a name="requirements"></a><span data-ttu-id="d82b3-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="d82b3-132">Requirements</span></span>



| <span data-ttu-id="d82b3-133">需求</span><span class="sxs-lookup"><span data-stu-id="d82b3-133">Requirement</span></span> | <span data-ttu-id="d82b3-134">值</span><span class="sxs-lookup"><span data-stu-id="d82b3-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d82b3-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d82b3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d82b3-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d82b3-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d82b3-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d82b3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d82b3-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d82b3-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d82b3-139">標頭</span><span class="sxs-lookup"><span data-stu-id="d82b3-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d82b3-140"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d82b3-140"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d82b3-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d82b3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d82b3-142">**TreeView \_ SetBorder**</span><span class="sxs-lookup"><span data-stu-id="d82b3-142">**TreeView\_SetBorder**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 

