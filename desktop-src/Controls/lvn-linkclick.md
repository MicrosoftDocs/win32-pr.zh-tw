---
title: 'LVN_LINKCLICK (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗已按一下連結。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: de8f40d6-b79e-4324-af67-9a3c0915609d
keywords:
- LVN_LINKCLICK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd69fb463e71523fcbd4eeb65a6a718d27847c09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467117"
---
# <a name="lvn_linkclick-notification-code"></a><span data-ttu-id="95e07-105">LVN \_ LINKCLICK 通知碼</span><span class="sxs-lookup"><span data-stu-id="95e07-105">LVN\_LINKCLICK notification code</span></span>

<span data-ttu-id="95e07-106">通知清單視圖控制項的父視窗已按一下連結。</span><span class="sxs-lookup"><span data-stu-id="95e07-106">Notifies a list-view control's parent window that a link has been clicked on.</span></span> <span data-ttu-id="95e07-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="95e07-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_LINKCLICK
        
    pLinkInfo = (NMLVLINK*) lParam;         
```



## <a name="parameters"></a><span data-ttu-id="95e07-108">參數</span><span class="sxs-lookup"><span data-stu-id="95e07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95e07-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95e07-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95e07-110">[**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="95e07-110">Pointer to an [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) structure.</span></span> <span data-ttu-id="95e07-111">包含連結的群組識別碼位於 **iSubItem** 成員中。</span><span class="sxs-lookup"><span data-stu-id="95e07-111">The identifier of the group containing the link is in the **iSubItem** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95e07-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="95e07-112">Return value</span></span>

<span data-ttu-id="95e07-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="95e07-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95e07-114">備註</span><span class="sxs-lookup"><span data-stu-id="95e07-114">Remarks</span></span>

<span data-ttu-id="95e07-115">下列範例顯示應用程式如何在其 [**WM \_ 通知**](wm-notify.md) 訊息處理常式中回應此通知碼。</span><span class="sxs-lookup"><span data-stu-id="95e07-115">The following example shows how an application might respond to this notification code in its [**WM\_NOTIFY**](wm-notify.md) message handler.</span></span> <span data-ttu-id="95e07-116">此範例會切換群組的折迭狀態，並設定適當的連結文字。</span><span class="sxs-lookup"><span data-stu-id="95e07-116">The example toggles the collapsed state of the group and sets the appropriate link text.</span></span>

``` syntax
case LVN_LINKCLICK:
{
    NMLVLINK* pLinkInfo = (NMLVLINK*)lParam;
    HWND hList = pLinkInfo->hdr.hwndFrom;
    LVGROUP groupInfo;
    groupInfo.cbSize = sizeof(groupInfo);
    groupInfo.mask = LVGF_TASK;
    int groupIndex = pLinkInfo->iSubItem;
    if (ListView_GetGroupState(hList, groupIndex, LVGS_COLLAPSED))
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, 0);
        groupInfo.pszTask = L"Hide";
    }
    else
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, LVGS_COLLAPSED);
        groupInfo.pszTask = L"Show";
     }
      ListView_SetGroupInfo(hList, groupIndex, &groupInfo);
      break;
}
```

## <a name="requirements"></a><span data-ttu-id="95e07-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="95e07-117">Requirements</span></span>



| <span data-ttu-id="95e07-118">需求</span><span class="sxs-lookup"><span data-stu-id="95e07-118">Requirement</span></span> | <span data-ttu-id="95e07-119">值</span><span class="sxs-lookup"><span data-stu-id="95e07-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95e07-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95e07-120">Minimum supported client</span></span><br/> | <span data-ttu-id="95e07-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95e07-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95e07-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95e07-122">Minimum supported server</span></span><br/> | <span data-ttu-id="95e07-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95e07-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95e07-124">標頭</span><span class="sxs-lookup"><span data-stu-id="95e07-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="95e07-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="95e07-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





