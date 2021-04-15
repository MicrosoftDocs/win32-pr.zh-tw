---
title: 'WM_PSD_MARGINRECT 訊息 (Commdlg .h) '
description: 通知頁面設定對話方塊（PagePaintHook）的攔截程式，對話方塊即將繪製範例頁面的邊界矩形。
ms.assetid: 81c057ab-6faf-4dd8-8b0c-34a2753e572c
keywords:
- WM_PSD_MARGINRECT 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_PSD_MARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4718cfbe16db53378544d9fca0ab44ade23ffb3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466141"
---
# <a name="wm_psd_marginrect-message"></a><span data-ttu-id="cfad3-104">WM \_ PSD \_ MARGINRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="cfad3-104">WM\_PSD\_MARGINRECT message</span></span>

<span data-ttu-id="cfad3-105">通知 **頁面設定** 對話方塊（ [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)）的攔截程式，對話方塊即將繪製範例頁面的邊界矩形。</span><span class="sxs-lookup"><span data-stu-id="cfad3-105">Notifies the hook procedure of a **Page Setup** dialog box, [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the margin rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_MARGINRECT       (WM_USER+3)
```



## <a name="parameters"></a><span data-ttu-id="cfad3-106">參數</span><span class="sxs-lookup"><span data-stu-id="cfad3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfad3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfad3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfad3-108">範例頁面的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="cfad3-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="cfad3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfad3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfad3-110">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，其中包含邊界矩形的座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="cfad3-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the margin rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfad3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cfad3-111">Return value</span></span>

<span data-ttu-id="cfad3-112">如果攔截程式傳回 **TRUE**，對話方塊就不會在範例頁面中繪製邊界矩形。</span><span class="sxs-lookup"><span data-stu-id="cfad3-112">If the hook procedure returns **TRUE**, the dialog box does not draw the margin rectangle in the sample page.</span></span>

<span data-ttu-id="cfad3-113">如果攔截程式傳回 **FALSE**，對話方塊會在範例頁面中繪製邊界矩形。</span><span class="sxs-lookup"><span data-stu-id="cfad3-113">If the hook procedure returns **FALSE**, the dialog box draws the margin rectangle in the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfad3-114">備註</span><span class="sxs-lookup"><span data-stu-id="cfad3-114">Remarks</span></span>

<span data-ttu-id="cfad3-115">[版面 **設定** ] 對話方塊包含範例頁面的影像，其中顯示使用者的選取專案如何影響列印輸出的外觀。</span><span class="sxs-lookup"><span data-stu-id="cfad3-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="cfad3-116">當您呼叫 [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) 函式時，您可以提供 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 攔截程式以自訂範例頁面的外觀。</span><span class="sxs-lookup"><span data-stu-id="cfad3-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="cfad3-117">每當對話方塊要繪製範例頁面的內容時，對話方塊會傳送一連串訊息給攔截程式。</span><span class="sxs-lookup"><span data-stu-id="cfad3-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfad3-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfad3-118">Requirements</span></span>



| <span data-ttu-id="cfad3-119">需求</span><span class="sxs-lookup"><span data-stu-id="cfad3-119">Requirement</span></span> | <span data-ttu-id="cfad3-120">值</span><span class="sxs-lookup"><span data-stu-id="cfad3-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfad3-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cfad3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cfad3-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfad3-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cfad3-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cfad3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cfad3-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfad3-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cfad3-125">標頭</span><span class="sxs-lookup"><span data-stu-id="cfad3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfad3-126"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="cfad3-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfad3-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfad3-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="cfad3-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="cfad3-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cfad3-129">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="cfad3-129">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="cfad3-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cfad3-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cfad3-131">**WM \_ PSD \_ PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="cfad3-131">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="cfad3-132">**概念**</span><span class="sxs-lookup"><span data-stu-id="cfad3-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cfad3-133">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="cfad3-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

