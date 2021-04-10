---
title: 'WM_CHOOSEFONT_SETLOGFONT 訊息 (Commdlg .h) '
description: 應用程式會將 WM \_ CHOOSEFONT \_ SETLOGFONT 訊息傳送至 [字型] 對話方塊，以設定目前的邏輯字型資訊。
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- WM_CHOOSEFONT_SETLOGFONT 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a588ebff7c8e56bb559a2cc9faa1d6290fbd8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686178"
---
# <a name="wm_choosefont_setlogfont-message"></a><span data-ttu-id="b568b-104">WM \_ CHOOSEFONT \_ SETLOGFONT 訊息</span><span class="sxs-lookup"><span data-stu-id="b568b-104">WM\_CHOOSEFONT\_SETLOGFONT message</span></span>

<span data-ttu-id="b568b-105">應用程式會將 **WM \_ CHOOSEFONT \_ SETLOGFONT** 訊息傳送至 [ **字型** ] 對話方塊，以設定目前的邏輯字型資訊。</span><span class="sxs-lookup"><span data-stu-id="b568b-105">An application sends the **WM\_CHOOSEFONT\_SETLOGFONT** message to a **Font** dialog box to set the current logical font information.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETLOGFONT      (WM_USER + 101)
```



## <a name="parameters"></a><span data-ttu-id="b568b-106">參數</span><span class="sxs-lookup"><span data-stu-id="b568b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b568b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b568b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b568b-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="b568b-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b568b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b568b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b568b-110">[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的指標，其中包含目前邏輯字型的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b568b-110">A pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that contains information about the current logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b568b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b568b-111">Return value</span></span>

<span data-ttu-id="b568b-112">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="b568b-112">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b568b-113">備註</span><span class="sxs-lookup"><span data-stu-id="b568b-113">Remarks</span></span>

<span data-ttu-id="b568b-114">當您呼叫 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)函式來建立 [**字型**] 對話方塊時，可以使用 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構的 **lpLogFont** 成員來指定包含對話方塊初始值的 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構。</span><span class="sxs-lookup"><span data-stu-id="b568b-114">When you call the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function to create a **Font** dialog box, you can use the **lpLogFont** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to specify a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure containing initial values for the dialog box.</span></span> <span data-ttu-id="b568b-115">在 [**字型**] 對話方塊開啟時，使用 **WM \_ CHOOSEFONT \_ SETLOGFONT** 訊息來指定具有不同值的 **LOGFONT** 結構。</span><span class="sxs-lookup"><span data-stu-id="b568b-115">Use the **WM\_CHOOSEFONT\_SETLOGFONT** message to specify a **LOGFONT** structure with different values while the **Font** dialog box is open.</span></span>

<span data-ttu-id="b568b-116">一般來說，您會從 [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)攔截程式傳送 **WM \_ CHOOSEFONT \_ SETLOGFONT** 訊息。</span><span class="sxs-lookup"><span data-stu-id="b568b-116">Typically, you would send the **WM\_CHOOSEFONT\_SETLOGFONT** message from a [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure.</span></span> <span data-ttu-id="b568b-117">攔截程式也可以傳送 [**wm \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md) 和 [**wm \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="b568b-117">The hook procedure can also send the [**WM\_CHOOSEFONT\_GETLOGFONT**](wm-choosefont-getlogfont.md) and [**WM\_CHOOSEFONT\_SETFLAGS**](wm-choosefont-setflags.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="b568b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b568b-118">Requirements</span></span>



| <span data-ttu-id="b568b-119">需求</span><span class="sxs-lookup"><span data-stu-id="b568b-119">Requirement</span></span> | <span data-ttu-id="b568b-120">值</span><span class="sxs-lookup"><span data-stu-id="b568b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b568b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b568b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b568b-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b568b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b568b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b568b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b568b-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b568b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b568b-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b568b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b568b-126"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b568b-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b568b-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b568b-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="b568b-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="b568b-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b568b-129">**CFHookProc**</span><span class="sxs-lookup"><span data-stu-id="b568b-129">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="b568b-130">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="b568b-130">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="b568b-131">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="b568b-131">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="b568b-132">**WM \_ CHOOSEFONT \_ GETLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="b568b-132">**WM\_CHOOSEFONT\_GETLOGFONT**</span></span>](wm-choosefont-getlogfont.md)
</dt> <dt>

[<span data-ttu-id="b568b-133">**WM \_ CHOOSEFONT \_ SETFLAGS**</span><span class="sxs-lookup"><span data-stu-id="b568b-133">**WM\_CHOOSEFONT\_SETFLAGS**</span></span>](wm-choosefont-setflags.md)
</dt> <dt>

<span data-ttu-id="b568b-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="b568b-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b568b-135">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="b568b-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="b568b-136">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="b568b-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b568b-137">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="b568b-137">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

