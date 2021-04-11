---
title: 'NM_GETCUSTOMSPLITRECT (Commctrl 的通知碼) '
description: 由按鈕控制項傳送至其父系，以取得分割按鈕的兩個矩形的度量。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ce72778d-3cca-46a4-9d05-40954a18681d
keywords:
- NM_GETCUSTOMSPLITRECT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_GETCUSTOMSPLITRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b839540da7e07069fdf56ed656ed8772d029eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093828"
---
# <a name="nm_getcustomsplitrect-notification-code"></a><span data-ttu-id="89531-105">NM \_ GETCUSTOMSPLITRECT 通知碼</span><span class="sxs-lookup"><span data-stu-id="89531-105">NM\_GETCUSTOMSPLITRECT notification code</span></span>

<span data-ttu-id="89531-106">由按鈕控制項傳送至其父系，以取得分割按鈕的兩個矩形的度量。</span><span class="sxs-lookup"><span data-stu-id="89531-106">Sent by a button control to its parent to get measurements for the two rectangles of the split button.</span></span> <span data-ttu-id="89531-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="89531-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_GETCUSTOMSPLITRECT
        
    nmCustomSplit = (NMCUSTOMSPLITRECTINFO *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="89531-108">參數</span><span class="sxs-lookup"><span data-stu-id="89531-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89531-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89531-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89531-110">[**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo)的指標，用來接收周框矩形的資訊。</span><span class="sxs-lookup"><span data-stu-id="89531-110">A pointer to an [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) to receive bounding rectangles information.</span></span> <span data-ttu-id="89531-111">**NMCUSTOMSPLITRECTINFO** 結構會隨著通知程式碼傳送，作為父代的要求，以針對分割按鈕的矩形提供度量。</span><span class="sxs-lookup"><span data-stu-id="89531-111">The **NMCUSTOMSPLITRECTINFO** structure is sent with the notification code as a request for the parent to provide measurements for the rectangles of the split button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89531-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="89531-112">Return value</span></span>

<span data-ttu-id="89531-113">傳回 [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md) ，告知按鈕控制項使用 [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) 結構中傳回的值，否則傳回 [**CDRF \_ DODEFAULT**](cdrf-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="89531-113">Return [**CDRF\_SKIPDEFAULT**](cdrf-constants.md) to tell the button control to use the values returned in the [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) structure; otherwise, return [**CDRF\_DODEFAULT**](cdrf-constants.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="89531-114">備註</span><span class="sxs-lookup"><span data-stu-id="89531-114">Remarks</span></span>

<span data-ttu-id="89531-115">此通知碼是由按鈕控制項在繪製前傳送。</span><span class="sxs-lookup"><span data-stu-id="89531-115">This notification code is sent by a button control before it is drawn.</span></span> <span data-ttu-id="89531-116">此按鈕的樣式必須是 [**BS \_ SPLITBUTTON**](button-styles.md) 或 [**BS \_ DEFSPLITBUTTON**](button-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="89531-116">The button must be of style [**BS\_SPLITBUTTON**](button-styles.md) or [**BS\_DEFSPLITBUTTON**](button-styles.md).</span></span> <span data-ttu-id="89531-117">如果在 *lParam* 中傳回給控制項的矩形無效，則會忽略它們。</span><span class="sxs-lookup"><span data-stu-id="89531-117">If the rectangles returned to the control in *lParam* are not valid, they are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="89531-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="89531-118">Requirements</span></span>



| <span data-ttu-id="89531-119">需求</span><span class="sxs-lookup"><span data-stu-id="89531-119">Requirement</span></span> | <span data-ttu-id="89531-120">值</span><span class="sxs-lookup"><span data-stu-id="89531-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89531-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89531-121">Minimum supported client</span></span><br/> | <span data-ttu-id="89531-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89531-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89531-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89531-123">Minimum supported server</span></span><br/> | <span data-ttu-id="89531-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89531-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89531-125">標頭</span><span class="sxs-lookup"><span data-stu-id="89531-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="89531-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="89531-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





