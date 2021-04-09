---
title: 'WM_PSD_FULLPAGERECT 訊息 (Commdlg .h) '
description: 在 [版面設定] 對話方塊中，通知範例頁面矩形座標的 PagePaintHook 勾點程式。 當此對話方塊即將繪製範例頁面的內容時，就會傳送此訊息。
ms.assetid: 88ca1d60-3335-480a-b874-c6f248a3c23a
keywords:
- WM_PSD_FULLPAGERECT 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_PSD_FULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5265144822ba1f46c470b71169e0b27f2e1c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934751"
---
# <a name="wm_psd_fullpagerect-message"></a><span data-ttu-id="4b000-105">WM \_ PSD \_ FULLPAGERECT 訊息</span><span class="sxs-lookup"><span data-stu-id="4b000-105">WM\_PSD\_FULLPAGERECT message</span></span>

<span data-ttu-id="4b000-106">在 [版面設定] 對話方塊中，通知範例頁面矩形座標的 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 勾點 **程式** 。</span><span class="sxs-lookup"><span data-stu-id="4b000-106">Notifies a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure of the coordinates of the sample page rectangle in the **Page Setup** dialog box.</span></span> <span data-ttu-id="4b000-107">當此對話方塊即將繪製範例頁面的內容時，就會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="4b000-107">The dialog box sends this message when it is about to draw the contents of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_FULLPAGERECT     (WM_USER+1)
```



## <a name="parameters"></a><span data-ttu-id="4b000-108">參數</span><span class="sxs-lookup"><span data-stu-id="4b000-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b000-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b000-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b000-110">範例頁面的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="4b000-110">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="4b000-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b000-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b000-112">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，其中包含範例頁面的座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="4b000-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the sample page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b000-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b000-113">Return value</span></span>

<span data-ttu-id="4b000-114">如果攔截程式傳回 **TRUE**，對話方塊將不再傳送任何訊息，而且在下一次系統需要重新繪製範例頁面之前，不會在範例頁面中繪製。</span><span class="sxs-lookup"><span data-stu-id="4b000-114">If the hook procedure returns **TRUE**, the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page.</span></span>

<span data-ttu-id="4b000-115">如果攔截程式傳回 **FALSE**，對話方塊會傳送繪圖順序的其餘訊息。</span><span class="sxs-lookup"><span data-stu-id="4b000-115">If the hook procedure returns **FALSE**, the dialog box sends the remaining messages of the drawing sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b000-116">備註</span><span class="sxs-lookup"><span data-stu-id="4b000-116">Remarks</span></span>

<span data-ttu-id="4b000-117">[版面 **設定** ] 對話方塊包含範例頁面的影像，其中顯示使用者的選取專案如何影響列印輸出的外觀。</span><span class="sxs-lookup"><span data-stu-id="4b000-117">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="4b000-118">當您呼叫 [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) 函式時，您可以提供 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 攔截程式以自訂範例頁面的外觀。</span><span class="sxs-lookup"><span data-stu-id="4b000-118">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="4b000-119">每當對話方塊要繪製範例頁面的內容時，對話方塊會傳送一連串訊息給攔截程式。</span><span class="sxs-lookup"><span data-stu-id="4b000-119">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b000-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b000-120">Requirements</span></span>



| <span data-ttu-id="4b000-121">需求</span><span class="sxs-lookup"><span data-stu-id="4b000-121">Requirement</span></span> | <span data-ttu-id="4b000-122">值</span><span class="sxs-lookup"><span data-stu-id="4b000-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b000-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4b000-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4b000-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b000-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4b000-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4b000-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4b000-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b000-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4b000-127">標頭</span><span class="sxs-lookup"><span data-stu-id="4b000-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b000-128"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4b000-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b000-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b000-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="4b000-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="4b000-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4b000-131">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="4b000-131">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="4b000-132">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4b000-132">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4b000-133">**WM \_ PSD \_ PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="4b000-133">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="4b000-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="4b000-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4b000-135">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="4b000-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

