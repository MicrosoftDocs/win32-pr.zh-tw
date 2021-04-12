---
title: 'EM_SETTABSTOPS 訊息 (Winuser .h) '
description: EM \_ SETTABSTOPS 訊息會設定多行編輯控制項中的定位停駐點。
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- EM_SETTABSTOPS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d076dea415f169eff46101fd7cfe632d73d976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104213"
---
# <a name="em_settabstops-message"></a><span data-ttu-id="cdd0e-104">EM \_ SETTABSTOPS 訊息</span><span class="sxs-lookup"><span data-stu-id="cdd0e-104">EM\_SETTABSTOPS message</span></span>

<span data-ttu-id="cdd0e-105">**EM \_ SETTABSTOPS** 訊息會設定多行編輯控制項中的定位停駐點。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-105">The **EM\_SETTABSTOPS** message sets the tab stops in a multiline edit control.</span></span> <span data-ttu-id="cdd0e-106">當文字複製到控制項時，文字中的任何定位字元都會產生空間，直到下一個索引標籤停止為止。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-106">When text is copied to the control, any tab character in the text causes space to be generated up to the next tab stop.</span></span>

<span data-ttu-id="cdd0e-107">此訊息只會由多行編輯控制項處理。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-107">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="cdd0e-108">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-108">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cdd0e-109">參數</span><span class="sxs-lookup"><span data-stu-id="cdd0e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdd0e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cdd0e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cdd0e-111">陣列中包含的定位停駐點數目。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-111">The number of tab stops contained in the array.</span></span> <span data-ttu-id="cdd0e-112">如果此參數為零，則會忽略 *lParam* 參數，並在每個32對話方塊範本單位上設定預設索引標籤停止。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-112">If this parameter is zero, the *lParam* parameter is ignored and default tab stops are set at every 32 dialog template units.</span></span> <span data-ttu-id="cdd0e-113">如果這個參數是1，就會在每個 *n* 個對話方塊範本單位設定 tab 鍵停止，其中 *n* 是 *lParam* 參數所指向的距離。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-113">If this parameter is 1, tab stops are set at every *n* dialog template units, where *n* is the distance pointed to by the *lParam* parameter.</span></span> <span data-ttu-id="cdd0e-114">如果此參數大於1， *lParam* 就會是定位點的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-114">If this parameter is greater than 1, *lParam* is a pointer to an array of tab stops.</span></span>

</dd> <dt>

<span data-ttu-id="cdd0e-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cdd0e-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cdd0e-116">在對話方塊範本單位中指定索引標籤的不帶正負號的整數陣列指標。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-116">A pointer to an array of unsigned integers specifying the tab stops, in dialog template units.</span></span> <span data-ttu-id="cdd0e-117">如果 *wParam* 參數為1，這個參數就是不帶正負號整數的指標，其中包含對話方塊範本單位中所有制表位之間的距離。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-117">If the *wParam* parameter is 1, this parameter is a pointer to an unsigned integer containing the distance between all tab stops, in dialog template units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdd0e-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="cdd0e-118">Return value</span></span>

<span data-ttu-id="cdd0e-119">如果設定了所有索引標籤，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-119">If all the tabs are set, the return value is **TRUE**.</span></span>

<span data-ttu-id="cdd0e-120">如果未設定所有索引標籤，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-120">If all the tabs are not set, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdd0e-121">備註</span><span class="sxs-lookup"><span data-stu-id="cdd0e-121">Remarks</span></span>

<span data-ttu-id="cdd0e-122">**EM \_ SETTABSTOPS** 訊息不會自動重新繪製編輯控制項視窗。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-122">The **EM\_SETTABSTOPS** message does not automatically redraw the edit control window.</span></span> <span data-ttu-id="cdd0e-123">如果應用程式正在變更已在編輯控制項中之文字的定位停駐點，它應該呼叫 [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) 函式來重繪編輯控制項視窗。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-123">If the application is changing the tab stops for text already in the edit control, it should call the [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function to redraw the edit control window.</span></span>

<span data-ttu-id="cdd0e-124">陣列中指定的值位於對話方塊範本單位中，也就是對話方塊範本中使用的裝置獨立單位。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-124">The values specified in the array are in dialog template units, which are the device-independent units used in dialog box templates.</span></span> <span data-ttu-id="cdd0e-125">若要將度量從對話方塊範本單位轉換為螢幕單位 (圖元) ，請使用 [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) 函數。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-125">To convert measurements from dialog template units to screen units (pixels), use the [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) function.</span></span>

<span data-ttu-id="cdd0e-126">**Rich Edit：** Microsoft Rich Edit 3.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-126">**Rich Edit:** Supported in Microsoft Rich Edit 3.0 and later.</span></span> <span data-ttu-id="cdd0e-127">Rich edit 控制項可具有最大索引標籤停止指定的最大 tab 鍵數目 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-127">A rich edit control can have the maximum number of tab stops specified by MAX\_TAB\_STOPS.</span></span> <span data-ttu-id="cdd0e-128">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="cdd0e-128">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cdd0e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="cdd0e-129">Requirements</span></span>



| <span data-ttu-id="cdd0e-130">需求</span><span class="sxs-lookup"><span data-stu-id="cdd0e-130">Requirement</span></span> | <span data-ttu-id="cdd0e-131">值</span><span class="sxs-lookup"><span data-stu-id="cdd0e-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd0e-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cdd0e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cdd0e-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdd0e-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cdd0e-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cdd0e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cdd0e-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdd0e-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cdd0e-136">標頭</span><span class="sxs-lookup"><span data-stu-id="cdd0e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdd0e-137"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="cdd0e-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdd0e-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cdd0e-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="cdd0e-139">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="cdd0e-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="cdd0e-140">**InvalidateRect**</span><span class="sxs-lookup"><span data-stu-id="cdd0e-140">**InvalidateRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[<span data-ttu-id="cdd0e-141">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="cdd0e-141">**MapDialogRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

