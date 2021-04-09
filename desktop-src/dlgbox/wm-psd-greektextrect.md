---
title: 'WM_PSD_GREEKTEXTRECT 訊息 (Commdlg .h) '
description: 通知頁面設定對話方塊 PagePaintHook 的攔截程式，對話方塊即將在範例頁面的邊界矩形內繪製希臘文文字。
ms.assetid: ad0a200d-5626-4768-b3bd-73d4e3f0d548
keywords:
- WM_PSD_GREEKTEXTRECT 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_PSD_GREEKTEXTRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0853720bea8cadc8df40d8fa649f644fd00694
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025299"
---
# <a name="wm_psd_greektextrect-message"></a><span data-ttu-id="4edd8-104">WM \_ PSD \_ GREEKTEXTRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="4edd8-104">WM\_PSD\_GREEKTEXTRECT message</span></span>

<span data-ttu-id="4edd8-105">通知 **頁面設定** 對話方塊 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)的攔截程式，對話方塊即將在範例頁面的邊界矩形內繪製希臘文文字。</span><span class="sxs-lookup"><span data-stu-id="4edd8-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw Greek text inside the margin rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_GREEKTEXTRECT    (WM_USER+4)
```



## <a name="parameters"></a><span data-ttu-id="4edd8-106">參數</span><span class="sxs-lookup"><span data-stu-id="4edd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4edd8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4edd8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4edd8-108">範例頁面的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="4edd8-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="4edd8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4edd8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4edd8-110">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，其中包含希臘文文字矩形的座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="4edd8-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the Greek text rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4edd8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4edd8-111">Return value</span></span>

<span data-ttu-id="4edd8-112">如果攔截程式傳回 **TRUE**，對話方塊就不會繪製範例頁面的希臘文文字部分。</span><span class="sxs-lookup"><span data-stu-id="4edd8-112">If the hook procedure returns **TRUE**, the dialog box does not draw the Greek text portion of the sample page.</span></span>

<span data-ttu-id="4edd8-113">如果攔截程式傳回 **FALSE**，對話方塊會繪製範例頁面的希臘文文字部分。</span><span class="sxs-lookup"><span data-stu-id="4edd8-113">If the hook procedure returns **FALSE**, the dialog box draws the Greek text portion of the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="4edd8-114">備註</span><span class="sxs-lookup"><span data-stu-id="4edd8-114">Remarks</span></span>

<span data-ttu-id="4edd8-115">[版面 **設定** ] 對話方塊包含範例頁面的影像，其中顯示使用者的選取專案如何影響列印輸出的外觀。</span><span class="sxs-lookup"><span data-stu-id="4edd8-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="4edd8-116">當您呼叫 [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) 函式時，您可以提供 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 攔截程式以自訂範例頁面的外觀。</span><span class="sxs-lookup"><span data-stu-id="4edd8-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="4edd8-117">每當對話方塊要繪製範例頁面的內容時，對話方塊會傳送一連串訊息給攔截程式。</span><span class="sxs-lookup"><span data-stu-id="4edd8-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4edd8-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4edd8-118">Requirements</span></span>



| <span data-ttu-id="4edd8-119">需求</span><span class="sxs-lookup"><span data-stu-id="4edd8-119">Requirement</span></span> | <span data-ttu-id="4edd8-120">值</span><span class="sxs-lookup"><span data-stu-id="4edd8-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4edd8-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4edd8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4edd8-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4edd8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4edd8-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4edd8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4edd8-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4edd8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4edd8-125">標頭</span><span class="sxs-lookup"><span data-stu-id="4edd8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4edd8-126"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4edd8-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4edd8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4edd8-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="4edd8-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="4edd8-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4edd8-129">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="4edd8-129">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="4edd8-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4edd8-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4edd8-131">**WM \_ PSD \_ PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="4edd8-131">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="4edd8-132">**概念**</span><span class="sxs-lookup"><span data-stu-id="4edd8-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4edd8-133">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="4edd8-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

