---
title: 'WM_PSD_YAFULLPAGERECT 訊息 (Commdlg .h) '
description: 通知 PagePaintHook 頁面設定對話方塊的攔截程式，此對話方塊即將繪製信封範例頁面的傳回位址部分。
ms.assetid: 1f6aea69-a1bd-41ea-b508-44b4f5c38757
keywords:
- WM_PSD_YAFULLPAGERECT 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_PSD_YAFULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb325a8d408724cd865f5f9b70cfe7369fe6ffe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025449"
---
# <a name="wm_psd_yafullpagerect-message"></a><span data-ttu-id="6e622-104">WM \_ PSD \_ YAFULLPAGERECT 訊息</span><span class="sxs-lookup"><span data-stu-id="6e622-104">WM\_PSD\_YAFULLPAGERECT message</span></span>

<span data-ttu-id="6e622-105">通知 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)**頁面設定** 對話方塊的攔截程式，此對話方塊即將繪製信封範例頁面的傳回位址部分。</span><span class="sxs-lookup"><span data-stu-id="6e622-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the return address portion of an envelope sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_YAFULLPAGERECT   (WM_USER+6)
```



## <a name="parameters"></a><span data-ttu-id="6e622-106">參數</span><span class="sxs-lookup"><span data-stu-id="6e622-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e622-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e622-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e622-108">範例頁面的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="6e622-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="6e622-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e622-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e622-110">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，其中包含範例頁面的座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="6e622-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the sample page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e622-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e622-111">Return value</span></span>

<span data-ttu-id="6e622-112">如果攔截程式傳回 **TRUE**，對話方塊就不會繪製信封範例頁面的傳回位址部分。</span><span class="sxs-lookup"><span data-stu-id="6e622-112">If the hook procedure returns **TRUE**, the dialog box does not draw the return address portion of an envelope sample page.</span></span>

<span data-ttu-id="6e622-113">如果攔截程式傳回 **FALSE**，則對話方塊會繪製信封範例頁面的傳回位址部分。</span><span class="sxs-lookup"><span data-stu-id="6e622-113">If the hook procedure returns **FALSE**, the dialog box draws the return address portion of an envelope sample page.</span></span>

<span data-ttu-id="6e622-114">如果紙張類型不是信封，則傳回值沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="6e622-114">If the paper type is not an envelope, the return value has no effect.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e622-115">備註</span><span class="sxs-lookup"><span data-stu-id="6e622-115">Remarks</span></span>

<span data-ttu-id="6e622-116">[版面 **設定** ] 對話方塊包含範例頁面的影像，其中顯示使用者的選取專案如何影響列印輸出的外觀。</span><span class="sxs-lookup"><span data-stu-id="6e622-116">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="6e622-117">當您呼叫 [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) 函式時，您可以提供 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 攔截程式以自訂範例頁面的外觀。</span><span class="sxs-lookup"><span data-stu-id="6e622-117">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="6e622-118">每當對話方塊要繪製範例頁面的內容時，對話方塊會傳送一連串訊息給攔截程式。</span><span class="sxs-lookup"><span data-stu-id="6e622-118">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e622-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e622-119">Requirements</span></span>



| <span data-ttu-id="6e622-120">需求</span><span class="sxs-lookup"><span data-stu-id="6e622-120">Requirement</span></span> | <span data-ttu-id="6e622-121">值</span><span class="sxs-lookup"><span data-stu-id="6e622-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e622-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e622-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6e622-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e622-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6e622-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e622-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6e622-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e622-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6e622-126">標頭</span><span class="sxs-lookup"><span data-stu-id="6e622-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e622-127"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6e622-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e622-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e622-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="6e622-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="6e622-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6e622-130">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="6e622-130">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="6e622-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e622-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6e622-132">**WM \_ PSD \_ PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="6e622-132">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="6e622-133">**概念**</span><span class="sxs-lookup"><span data-stu-id="6e622-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6e622-134">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="6e622-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

