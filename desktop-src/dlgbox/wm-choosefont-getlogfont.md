---
title: 'WM_CHOOSEFONT_GETLOGFONT 訊息 (Commdlg .h) '
description: 應用程式會將 WM \_ CHOOSEFONT \_ GETLOGFONT 訊息傳送至 [字型] 對話方塊，以取得使用者目前字型選取專案的相關資訊。
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- WM_CHOOSEFONT_GETLOGFONT 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_GETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696246d26c2b87e9b299844a9dc7e78d39ac632f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966520"
---
# <a name="wm_choosefont_getlogfont-message"></a><span data-ttu-id="776d7-104">WM \_ CHOOSEFONT \_ GETLOGFONT 訊息</span><span class="sxs-lookup"><span data-stu-id="776d7-104">WM\_CHOOSEFONT\_GETLOGFONT message</span></span>

<span data-ttu-id="776d7-105">應用程式會將 **WM \_ CHOOSEFONT \_ GETLOGFONT** 訊息傳送至 [ **字型** ] 對話方塊，以取得使用者目前字型選取專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="776d7-105">An application sends the **WM\_CHOOSEFONT\_GETLOGFONT** message to a **Font** dialog box to retrieve information about the user's current font selections.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_GETLOGFONT      (WM_USER + 1)
```



## <a name="parameters"></a><span data-ttu-id="776d7-106">參數</span><span class="sxs-lookup"><span data-stu-id="776d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="776d7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="776d7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="776d7-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="776d7-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="776d7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="776d7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="776d7-110">[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的指標，此結構會接收使用者目前字型選取範圍的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="776d7-110">A pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that receives information about the user's current font selections.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="776d7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="776d7-111">Return value</span></span>

<span data-ttu-id="776d7-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="776d7-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="776d7-113">備註</span><span class="sxs-lookup"><span data-stu-id="776d7-113">Remarks</span></span>

<span data-ttu-id="776d7-114">[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)函式會建立 [**字型**] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="776d7-114">The [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function creates a **Font** dialog box.</span></span> <span data-ttu-id="776d7-115">當使用者關閉 [ **字型** ] 對話方塊時， **ChooseFont** 函式會傳回使用者在 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 結構中選取之字型的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="776d7-115">When the user closes the **Font** dialog box, the **ChooseFont** function returns information about the user's font selections in the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure.</span></span> <span data-ttu-id="776d7-116">**CHOOSEFONT** 結構的 **LpLogFont** 成員是 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="776d7-116">The **lpLogFont** member of the **CHOOSEFONT** structure is a pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

<span data-ttu-id="776d7-117">在 [**字型**] 對話方塊開啟時，使用 **WM \_ CHOOSEFONT \_ GETLOGFONT** 訊息來取得使用者目前字型選取範圍的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="776d7-117">Use the **WM\_CHOOSEFONT\_GETLOGFONT** message to get information about the user's current font selections while the **Font** dialog box is open.</span></span> <span data-ttu-id="776d7-118">例如，如果您啟用 [**字型**] 對話方塊中的 [套用 **] 按鈕，** 請傳送訊息以取得要套用至目前文字選取範圍的字型資訊。</span><span class="sxs-lookup"><span data-stu-id="776d7-118">For example, if you enable the **Apply** button in the **Font** dialog box, send the message to get the font information to apply to the current text selection.</span></span>

<span data-ttu-id="776d7-119">一般來說，您會啟用 [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)攔截程式，以處理 **適用于**[套用] 按鈕的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command)訊息。</span><span class="sxs-lookup"><span data-stu-id="776d7-119">Typically, you enable a [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure to process [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages for the **Apply** button.</span></span> <span data-ttu-id="776d7-120">當使用者按一下 [套用 **] 按鈕時** ，攔截程式會將 **WM \_ CHOOSEFONT \_ GETLOGFONT** 訊息傳送至對話方塊。</span><span class="sxs-lookup"><span data-stu-id="776d7-120">When the user clicks the **Apply** button, the hook procedure sends the **WM\_CHOOSEFONT\_GETLOGFONT** message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="776d7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="776d7-121">Requirements</span></span>



| <span data-ttu-id="776d7-122">需求</span><span class="sxs-lookup"><span data-stu-id="776d7-122">Requirement</span></span> | <span data-ttu-id="776d7-123">值</span><span class="sxs-lookup"><span data-stu-id="776d7-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="776d7-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="776d7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="776d7-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="776d7-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="776d7-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="776d7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="776d7-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="776d7-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="776d7-128">標頭</span><span class="sxs-lookup"><span data-stu-id="776d7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="776d7-129"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="776d7-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="776d7-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="776d7-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="776d7-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="776d7-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="776d7-132">**CFHookProc**</span><span class="sxs-lookup"><span data-stu-id="776d7-132">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="776d7-133">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="776d7-133">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="776d7-134">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="776d7-134">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="776d7-135">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="776d7-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> <dt>

<span data-ttu-id="776d7-136">**概念**</span><span class="sxs-lookup"><span data-stu-id="776d7-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="776d7-137">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="776d7-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="776d7-138">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="776d7-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="776d7-139">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="776d7-139">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

