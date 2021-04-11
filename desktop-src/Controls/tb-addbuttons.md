---
title: 'TB_ADDBUTTONS 訊息 (Commctrl .h) '
description: 將一或多個按鈕加入至工具列。
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- TB_ADDBUTTONS message Windows 控制項
topic_type:
- apiref
api_name:
- TB_ADDBUTTONS
- TB_ADDBUTTONSA
- TB_ADDBUTTONSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f954e9a133f78a9415358d1c7f61d68008cd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935162"
---
# <a name="tb_addbuttons-message"></a><span data-ttu-id="edff6-104">TB \_ ADDBUTTONS 訊息</span><span class="sxs-lookup"><span data-stu-id="edff6-104">TB\_ADDBUTTONS message</span></span>

<span data-ttu-id="edff6-105">將一或多個按鈕加入至工具列。</span><span class="sxs-lookup"><span data-stu-id="edff6-105">Adds one or more buttons to a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="edff6-106">參數</span><span class="sxs-lookup"><span data-stu-id="edff6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edff6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="edff6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="edff6-108">要加入的按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="edff6-108">Number of buttons to add.</span></span>

</dd> <dt>

<span data-ttu-id="edff6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="edff6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="edff6-110">[**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構陣列的指標，其中包含要加入之按鈕的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="edff6-110">Pointer to an array of [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structures that contain information about the buttons to add.</span></span> <span data-ttu-id="edff6-111">陣列中的元素數目必須與 *wParam* 所指定的按鈕相同。</span><span class="sxs-lookup"><span data-stu-id="edff6-111">There must be the same number of elements in the array as buttons specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edff6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="edff6-112">Return value</span></span>

<span data-ttu-id="edff6-113">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="edff6-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="edff6-114">備註</span><span class="sxs-lookup"><span data-stu-id="edff6-114">Remarks</span></span>

<span data-ttu-id="edff6-115">如果工具列是使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式所建立，您必須先將 [**tb \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) 訊息傳送至工具列，然後再傳送 **tb \_ ADDBUTTONS**。</span><span class="sxs-lookup"><span data-stu-id="edff6-115">If the toolbar was created using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, you must send the [**TB\_BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) message to the toolbar before sending **TB\_ADDBUTTONS**.</span></span>

<span data-ttu-id="edff6-116">如需如何將點陣圖指派給一或多個影像清單中的工具列按鈕的討論，請參閱 [**TB \_ SETIMAGELIST**](tb-setimagelist.md) 。</span><span class="sxs-lookup"><span data-stu-id="edff6-116">See [**TB\_SETIMAGELIST**](tb-setimagelist.md) for a discussion of how to assign bitmaps to toolbar buttons from one or more image lists.</span></span>

## <a name="examples"></a><span data-ttu-id="edff6-117">範例</span><span class="sxs-lookup"><span data-stu-id="edff6-117">Examples</span></span>

<span data-ttu-id="edff6-118">下列範例程式碼會使用 [視圖] 按鈕的標準系統點陣圖，將三個按鈕加入至工具列。</span><span class="sxs-lookup"><span data-stu-id="edff6-118">The following example code adds three buttons to a toolbar, using the standard system bitmap for view buttons.</span></span> <span data-ttu-id="edff6-119">[**TB \_ ADDBITMAP**](tb-addbitmap.md)訊息會傳回影像清單中第一個按鈕影像的索引。</span><span class="sxs-lookup"><span data-stu-id="edff6-119">The [**TB\_ADDBITMAP**](tb-addbitmap.md) message returns the index of the first button image within the image list.</span></span> <span data-ttu-id="edff6-120">個別的影像是以該值的位移來識別。</span><span class="sxs-lookup"><span data-stu-id="edff6-120">Individual images are identified by their offsets from that value.</span></span>


```C++
TBADDBITMAP tbAddBitmap;
tbAddBitmap.hInst = HINST_COMMCTRL;
tbAddBitmap.nID = IDB_VIEW_SMALL_COLOR;

// There are 12 items in IDB_VIEW_SMALL_COLOR.  However, because this is a standard
// system-defined bitmap, the wParam (nButtons) is ignored.
//
// hWndToolbar is the handle of the toolbar window.
//
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was created
// by using CreateWindowEx.
//
int stdidx = SendMessage(hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tbAddBitmap);

// Define the buttons. 
// IDM_SETLARGEICONVIEW and so on are application-defined command IDs.

const int numButtons = 3;
TBBUTTON tbButtonsAdd[numButtons] = 
{
    {stdidx + VIEW_LARGEICONS, IDM_SETLARGEICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_SMALLICONS, IDM_SETSMALLICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_DETAILS, IDM_SETDETAILSVIEW, TBSTATE_ENABLED, BTNS_BUTTON}
}; 

// Add the view buttons.
SendMessage(hWndToolbar, TB_ADDBUTTONS, numButtons, (LPARAM)tbButtonsAdd);
```



## <a name="requirements"></a><span data-ttu-id="edff6-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="edff6-121">Requirements</span></span>



| <span data-ttu-id="edff6-122">需求</span><span class="sxs-lookup"><span data-stu-id="edff6-122">Requirement</span></span> | <span data-ttu-id="edff6-123">值</span><span class="sxs-lookup"><span data-stu-id="edff6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edff6-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="edff6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="edff6-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="edff6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="edff6-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="edff6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="edff6-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="edff6-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="edff6-128">標頭</span><span class="sxs-lookup"><span data-stu-id="edff6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="edff6-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="edff6-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="edff6-130">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="edff6-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="edff6-131">**TB \_ADDBUTTONSW** (Unicode) 和 **TB \_ ADDBUTTONSA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="edff6-131">**TB\_ADDBUTTONSW** (Unicode) and **TB\_ADDBUTTONSA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="edff6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edff6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edff6-133">**工具列標準按鈕影像索引值**</span><span class="sxs-lookup"><span data-stu-id="edff6-133">**Toolbar Standard Button Image Index Values**</span></span>](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

