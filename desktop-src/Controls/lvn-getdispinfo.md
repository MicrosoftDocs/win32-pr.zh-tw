---
title: 'LVN_GETDISPINFO (Commctrl 的通知碼) '
description: 由清單視圖控制項傳送至其父視窗。 它是父視窗的要求，可提供顯示或排序清單視圖專案所需的資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- LVN_GETDISPINFO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_GETDISPINFO
- LVN_GETDISPINFOA
- LVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1585524dd447c4a1324dc5c7a235490de776fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686679"
---
# <a name="lvn_getdispinfo-notification-code"></a><span data-ttu-id="1e174-106">LVN \_ GETDISPINFO 通知碼</span><span class="sxs-lookup"><span data-stu-id="1e174-106">LVN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="1e174-107">由清單視圖控制項傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="1e174-107">Sent by a list-view control to its parent window.</span></span> <span data-ttu-id="1e174-108">它是父視窗的要求，可提供顯示或排序清單視圖專案所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="1e174-108">It is a request for the parent window to provide information needed to display or sort a list-view item.</span></span> <span data-ttu-id="1e174-109">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="1e174-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a><span data-ttu-id="1e174-110">參數</span><span class="sxs-lookup"><span data-stu-id="1e174-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e174-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e174-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e174-112">[**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1e174-112">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="1e174-113">在輸入時，此結構中所包含的 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構會指定所需的資訊類型，並識別感興趣的專案或子專案。</span><span class="sxs-lookup"><span data-stu-id="1e174-113">On input, the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure contained in this structure specifies the type of information required and identifies the item or subitem of interest.</span></span> <span data-ttu-id="1e174-114">使用 **LVITEM** 結構，將要求的資訊傳回給控制項。</span><span class="sxs-lookup"><span data-stu-id="1e174-114">Use the **LVITEM** structure to return the requested information to the control.</span></span> <span data-ttu-id="1e174-115">如果您的訊息處理常式 \_ \_ 在 **LVITEM** 結構的 **遮罩** 成員中設定 LVIF DI SETITEM 旗標，則清單視圖控制項會儲存要求的資訊，且不會再要求它。</span><span class="sxs-lookup"><span data-stu-id="1e174-115">If your message handler sets the LVIF\_DI\_SETITEM flag in the **mask** member of the **LVITEM** structure, the list-view control stores the requested information and will not ask for it again.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e174-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e174-116">Return value</span></span>

<span data-ttu-id="1e174-117">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="1e174-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e174-118">備註</span><span class="sxs-lookup"><span data-stu-id="1e174-118">Remarks</span></span>

<span data-ttu-id="1e174-119">通知接收者會轉換 *lParam* 來取出 [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) 結構。</span><span class="sxs-lookup"><span data-stu-id="1e174-119">The notification receiver casts *lParam* to retrieve the [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="1e174-120">*WParam* 參數包含通知碼。</span><span class="sxs-lookup"><span data-stu-id="1e174-120">The *wParam* parameter contains the notification code.</span></span>

<span data-ttu-id="1e174-121">清單視圖控制項會傳送 **LVN \_ GETDISPINFO** 通知程式碼，以取得應用程式所儲存的專案資訊，而不是控制項。</span><span class="sxs-lookup"><span data-stu-id="1e174-121">A list-view control sends the **LVN\_GETDISPINFO** notification code to retrieve item information that is stored by the application rather than the control.</span></span> <span data-ttu-id="1e174-122">此資訊可以是專案的文字或圖示資訊。</span><span class="sxs-lookup"><span data-stu-id="1e174-122">The information can be text or icon information for an item.</span></span> <span data-ttu-id="1e174-123">它也可以是專案狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="1e174-123">It can also be item state information.</span></span> <span data-ttu-id="1e174-124">請參閱 [**LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) 訊息，以取得以回呼為基礎執行專案狀態的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1e174-124">See the [**LVM\_SETCALLBACKMASK**](lvm-setcallbackmask.md) message for more information on implementing item state on a callback basis.</span></span>

<span data-ttu-id="1e174-125">如需清單視圖回呼的詳細資訊，請參閱 [回呼專案和回呼遮罩](list-view-controls-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="1e174-125">For more information on list-view callbacks, see [Callback Items and the Callback Mask](list-view-controls-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1e174-126">範例</span><span class="sxs-lookup"><span data-stu-id="1e174-126">Examples</span></span>

<span data-ttu-id="1e174-127">下列範例顯示如何處理此通知程式碼，以在清單視圖的資料行中設定文字。</span><span class="sxs-lookup"><span data-stu-id="1e174-127">The following example shows how this notification code might be handled to set the text in the columns of a list view.</span></span> <span data-ttu-id="1e174-128">每個專案的資料會保存在下列結構中。</span><span class="sxs-lookup"><span data-stu-id="1e174-128">The data for each item is held in the following structure.</span></span>


```C++
 typedef struct tagPETINFO
{
    TCHAR szName[50];
    TCHAR szBreed[50];
    TCHAR szGender[7];
    TCHAR szPrice[20];
    GroupIds iGroup;
} PETINFO;
            
```



<span data-ttu-id="1e174-129">以下是來自于 \_ 對話方塊程式中的 WM 通知處理常式。</span><span class="sxs-lookup"><span data-stu-id="1e174-129">The following is from the WM\_NOTIFY handler in the dialog procedure.</span></span>


```C++
    case WM_NOTIFY:
        switch (((LPNMHDR) lParam)->code)
        {
        case LVN_GETDISPINFO:
            {
                NMLVDISPINFO* plvdi = (NMLVDISPINFO*)lParam;    
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // rgPetInfo is an array of PETINFO structures.
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szName;
                    break;

                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;

                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szGender;
                    break;

                case 3:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;

                default:
                    break;
                }
                return TRUE;
            }
      // More notifications...
      }
```



## <a name="requirements"></a><span data-ttu-id="1e174-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e174-130">Requirements</span></span>



| <span data-ttu-id="1e174-131">需求</span><span class="sxs-lookup"><span data-stu-id="1e174-131">Requirement</span></span> | <span data-ttu-id="1e174-132">值</span><span class="sxs-lookup"><span data-stu-id="1e174-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e174-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e174-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1e174-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e174-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e174-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e174-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1e174-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e174-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e174-137">標頭</span><span class="sxs-lookup"><span data-stu-id="1e174-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e174-138"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1e174-138"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1e174-139">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="1e174-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1e174-140">**LVN \_GETDISPINFOW** (Unicode) 和 **LVN \_ GETDISPINFOA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="1e174-140">**LVN\_GETDISPINFOW** (Unicode) and **LVN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="1e174-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e174-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e174-142">**LVN \_ SETDISPINFO**</span><span class="sxs-lookup"><span data-stu-id="1e174-142">**LVN\_SETDISPINFO**</span></span>](lvn-setdispinfo.md)
</dt> </dl>

 

 





