---
title: 'WM_CHOOSEFONT_SETFLAGS 訊息 (Commdlg .h) '
description: 應用程式會將 WM \_ CHOOSEFONT \_ SETFLAGS 訊息傳送至 [字型] 對話方塊，以設定對話方塊的顯示選項。
ms.assetid: 945ebc07-440d-4466-8255-ad344bdc568a
keywords:
- WM_CHOOSEFONT_SETFLAGS 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETFLAGS
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7abf436311f8a3868b1471c2a10a7ee2e4a3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104880"
---
# <a name="wm_choosefont_setflags-message"></a><span data-ttu-id="b1909-104">WM \_ CHOOSEFONT \_ SETFLAGS 訊息</span><span class="sxs-lookup"><span data-stu-id="b1909-104">WM\_CHOOSEFONT\_SETFLAGS message</span></span>

<span data-ttu-id="b1909-105">應用程式會將 **WM \_ CHOOSEFONT \_ SETFLAGS** 訊息傳送至 [ **字型** ] 對話方塊，以設定對話方塊的顯示選項。</span><span class="sxs-lookup"><span data-stu-id="b1909-105">An application sends the **WM\_CHOOSEFONT\_SETFLAGS** message to a **Font** dialog box to set the display options for the dialog box.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETFLAGS        (WM_USER + 102)
```



## <a name="parameters"></a><span data-ttu-id="b1909-106">參數</span><span class="sxs-lookup"><span data-stu-id="b1909-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1909-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1909-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1909-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="b1909-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b1909-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1909-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1909-110">[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構的指標，其中包含 **旗標** 成員中的新設定。</span><span class="sxs-lookup"><span data-stu-id="b1909-110">A pointer to a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure that contains new settings in the **Flags** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1909-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1909-111">Return value</span></span>

<span data-ttu-id="b1909-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="b1909-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1909-113">備註</span><span class="sxs-lookup"><span data-stu-id="b1909-113">Remarks</span></span>

<span data-ttu-id="b1909-114">[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)函式會建立 [**字型**] 對話方塊，並使用 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構來指定 **旗標** 成員的初始值。</span><span class="sxs-lookup"><span data-stu-id="b1909-114">The [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function creates a **Font** dialog box and uses a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to specify the initial values for the **Flags** member.</span></span> <span data-ttu-id="b1909-115">使用 **WM \_ CHOOSEFONT \_ SETFLAGS** 訊息，在 [**字型**] 對話方塊開啟時，為 **旗標** 成員指定不同的值。</span><span class="sxs-lookup"><span data-stu-id="b1909-115">Use the **WM\_CHOOSEFONT\_SETFLAGS** message to specify different values for the **Flags** member while the **Font** dialog box is open.</span></span>

<span data-ttu-id="b1909-116">一般來說，您應該從 [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)攔截程式傳送 **WM \_ CHOOSEFONT \_ SETFLAGS** 訊息。</span><span class="sxs-lookup"><span data-stu-id="b1909-116">Typically, you should send the **WM\_CHOOSEFONT\_SETFLAGS** message from a [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1909-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1909-117">Requirements</span></span>



| <span data-ttu-id="b1909-118">需求</span><span class="sxs-lookup"><span data-stu-id="b1909-118">Requirement</span></span> | <span data-ttu-id="b1909-119">值</span><span class="sxs-lookup"><span data-stu-id="b1909-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1909-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1909-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b1909-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1909-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b1909-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1909-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b1909-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1909-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b1909-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b1909-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1909-125"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b1909-125"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1909-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1909-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b1909-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="b1909-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b1909-128">**CFHookProc**</span><span class="sxs-lookup"><span data-stu-id="b1909-128">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="b1909-129">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="b1909-129">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="b1909-130">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="b1909-130">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

<span data-ttu-id="b1909-131">**概念**</span><span class="sxs-lookup"><span data-stu-id="b1909-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b1909-132">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="b1909-132">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

