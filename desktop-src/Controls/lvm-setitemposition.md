---
title: 'LVM_SETITEMPOSITION 訊息 (Commctrl .h) '
description: 將專案移至清單視圖控制項中的指定位置 (必須是圖示或小圖示視圖) 。 您可以明確地傳送此訊息，或使用 ListView \_ SetItemPosition 宏來傳送。
ms.assetid: dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01
keywords:
- LVM_SETITEMPOSITION message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95fcf2949f1e19677bd445c0f6c5f762db078d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843667"
---
# <a name="lvm_setitemposition-message"></a><span data-ttu-id="bdbc8-105">LVM \_ SETITEMPOSITION 訊息</span><span class="sxs-lookup"><span data-stu-id="bdbc8-105">LVM\_SETITEMPOSITION message</span></span>

<span data-ttu-id="bdbc8-106">將專案移至清單視圖控制項中的指定位置 (必須是圖示或小圖示視圖) 。</span><span class="sxs-lookup"><span data-stu-id="bdbc8-106">Moves an item to a specified position in a list-view control (must be in icon or small icon view).</span></span> <span data-ttu-id="bdbc8-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="bdbc8-107">You can send this message explicitly or by using the [**ListView\_SetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bdbc8-108">參數</span><span class="sxs-lookup"><span data-stu-id="bdbc8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdbc8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdbc8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbc8-110">清單視圖專案的索引。</span><span class="sxs-lookup"><span data-stu-id="bdbc8-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="bdbc8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdbc8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbc8-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會在 view 座標中指定專案左上角的新 x 位置。</span><span class="sxs-lookup"><span data-stu-id="bdbc8-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the new x-position of the item's upper-left corner, in view coordinates.</span></span> <span data-ttu-id="bdbc8-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會在 view 座標中指定專案左上角的新 y 位置。</span><span class="sxs-lookup"><span data-stu-id="bdbc8-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the new y-position of the item's upper-left corner, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdbc8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="bdbc8-114">Return value</span></span>

<span data-ttu-id="bdbc8-115">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="bdbc8-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdbc8-116">備註</span><span class="sxs-lookup"><span data-stu-id="bdbc8-116">Remarks</span></span>

<span data-ttu-id="bdbc8-117">如果清單視圖控制項有 [**lvs) \_ AUTOARRANGE**](list-view-window-styles.md) 樣式，則會在設定專案的位置之後排列清單視圖控制項中的專案。</span><span class="sxs-lookup"><span data-stu-id="bdbc8-117">If the list-view control has the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style, the items in the list-view control are arranged after the position of the item is set.</span></span>

<span data-ttu-id="bdbc8-118">在 Windows Vista 上，將此訊息傳送至具有 [**lvs) \_ AUTOARRANGE**](list-view-window-styles.md) 樣式的清單視圖控制項不會執行任何動作，且傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="bdbc8-118">On Windows Vista, sending this message to a list-view control with the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style does nothing, and the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdbc8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="bdbc8-119">Requirements</span></span>



| <span data-ttu-id="bdbc8-120">需求</span><span class="sxs-lookup"><span data-stu-id="bdbc8-120">Requirement</span></span> | <span data-ttu-id="bdbc8-121">值</span><span class="sxs-lookup"><span data-stu-id="bdbc8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdbc8-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bdbc8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bdbc8-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bdbc8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bdbc8-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bdbc8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bdbc8-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bdbc8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bdbc8-126">標頭</span><span class="sxs-lookup"><span data-stu-id="bdbc8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdbc8-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="bdbc8-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

