---
title: 'LVM_GETSTRINGWIDTH 訊息 (Commctrl .h) '
description: 使用指定的清單視圖控制項目前字型，判斷指定之字串的寬度。 您可以明確地傳送此訊息，或使用 ListView \_ GetStringWidth 宏來傳送。
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- LVM_GETSTRINGWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETSTRINGWIDTH
- LVM_GETSTRINGWIDTHA
- LVM_GETSTRINGWIDTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e27512eb7a2a260976356ed2a128b48975f9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509159"
---
# <a name="lvm_getstringwidth-message"></a><span data-ttu-id="3135f-105">LVM \_ GETSTRINGWIDTH 訊息</span><span class="sxs-lookup"><span data-stu-id="3135f-105">LVM\_GETSTRINGWIDTH message</span></span>

<span data-ttu-id="3135f-106">使用指定的清單視圖控制項目前字型，判斷指定之字串的寬度。</span><span class="sxs-lookup"><span data-stu-id="3135f-106">Determines the width of a specified string using the specified list-view control's current font.</span></span> <span data-ttu-id="3135f-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetStringWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="3135f-107">You can send this message explicitly or by using the [**ListView\_GetStringWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3135f-108">參數</span><span class="sxs-lookup"><span data-stu-id="3135f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3135f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3135f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3135f-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3135f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3135f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3135f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3135f-112">以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="3135f-112">Pointer to a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3135f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3135f-113">Return value</span></span>

<span data-ttu-id="3135f-114">如果成功，則傳回字串寬度，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="3135f-114">Returns the string width if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3135f-115">備註</span><span class="sxs-lookup"><span data-stu-id="3135f-115">Remarks</span></span>

<span data-ttu-id="3135f-116">LVM \_ GETSTRINGWIDTH 訊息會傳回指定字串的確切寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="3135f-116">The LVM\_GETSTRINGWIDTH message returns the exact width, in pixels, of the specified string.</span></span> <span data-ttu-id="3135f-117">如果您使用傳回的字串寬度做為 [**LVM \_ SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) 訊息中的資料行寬度，則會截斷字串。</span><span class="sxs-lookup"><span data-stu-id="3135f-117">If you use the returned string width as the column width in the [**LVM\_SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) message, the string will be truncated.</span></span> <span data-ttu-id="3135f-118">若要在不截斷的情況下，取得可包含字串的資料行寬度，您必須在傳回的字串寬度加上填補。</span><span class="sxs-lookup"><span data-stu-id="3135f-118">To retrieve the column width that can contain the string without truncating it, you must add padding to the returned string width.</span></span>

## <a name="requirements"></a><span data-ttu-id="3135f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3135f-119">Requirements</span></span>



| <span data-ttu-id="3135f-120">需求</span><span class="sxs-lookup"><span data-stu-id="3135f-120">Requirement</span></span> | <span data-ttu-id="3135f-121">值</span><span class="sxs-lookup"><span data-stu-id="3135f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3135f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3135f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3135f-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3135f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3135f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3135f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3135f-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3135f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3135f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="3135f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3135f-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3135f-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3135f-128">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="3135f-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3135f-129">**LVM \_GETSTRINGWIDTHW** (Unicode) 和 **LVM \_ GETSTRINGWIDTHA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="3135f-129">**LVM\_GETSTRINGWIDTHW** (Unicode) and **LVM\_GETSTRINGWIDTHA** (ANSI)</span></span><br/>     |



 

 





