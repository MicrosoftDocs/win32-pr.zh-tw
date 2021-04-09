---
title: 'LVN_GETEMPTYMARKUP (Commctrl 的通知碼) '
description: 當控制項沒有專案時，由清單視圖控制項傳送至其父視窗。 LVN \_ GETEMPTYMARKUP 通知碼是要求父視窗提供標記文字。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- LVN_GETEMPTYMARKUP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_GETEMPTYMARKUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea693475ca42f962be07936f980cd3f5d52479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844476"
---
# <a name="lvn_getemptymarkup-notification-code"></a><span data-ttu-id="f02e1-106">LVN \_ GETEMPTYMARKUP 通知碼</span><span class="sxs-lookup"><span data-stu-id="f02e1-106">LVN\_GETEMPTYMARKUP notification code</span></span>

<span data-ttu-id="f02e1-107">當控制項沒有專案時，由清單視圖控制項傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="f02e1-107">Sent by list-view control to its parent window when the control has no items.</span></span> <span data-ttu-id="f02e1-108">LVN \_ GETEMPTYMARKUP 通知碼是要求父視窗提供標記文字。</span><span class="sxs-lookup"><span data-stu-id="f02e1-108">The LVN\_GETEMPTYMARKUP notification code is a request for the parent window to provide markup text.</span></span> <span data-ttu-id="f02e1-109">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="f02e1-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETEMPTYMARKUP
        
    pnmMarkup = (NMLVEMPTYMARKUP*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f02e1-110">參數</span><span class="sxs-lookup"><span data-stu-id="f02e1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f02e1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f02e1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f02e1-112">[**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f02e1-112">Pointer to a [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) structure.</span></span> <span data-ttu-id="f02e1-113">設定此結構的成員，以提供清單視圖控制項的標記文字。</span><span class="sxs-lookup"><span data-stu-id="f02e1-113">Set the members of this structure to provide markup text for the list-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f02e1-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f02e1-114">Return value</span></span>

<span data-ttu-id="f02e1-115">傳回 **TRUE** 表示在清單視圖控制項中設定標記文字，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f02e1-115">Return **TRUE** to set the markup text in the list-view control, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f02e1-116">備註</span><span class="sxs-lookup"><span data-stu-id="f02e1-116">Remarks</span></span>

<span data-ttu-id="f02e1-117">通知接收者會轉換 *lParam* 來取出 [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) 結構。</span><span class="sxs-lookup"><span data-stu-id="f02e1-117">The notification receiver casts *lParam* to retrieve the [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) structure.</span></span> <span data-ttu-id="f02e1-118">*WParam* 參數包含傳送此訊息之控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f02e1-118">The *wParam* parameter contains the ID of the control that sends this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f02e1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f02e1-119">Requirements</span></span>



| <span data-ttu-id="f02e1-120">需求</span><span class="sxs-lookup"><span data-stu-id="f02e1-120">Requirement</span></span> | <span data-ttu-id="f02e1-121">值</span><span class="sxs-lookup"><span data-stu-id="f02e1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f02e1-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f02e1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f02e1-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f02e1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f02e1-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f02e1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f02e1-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f02e1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f02e1-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f02e1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f02e1-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f02e1-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





