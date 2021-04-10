---
title: 'LVN_ITEMACTI加值稅E (Commctrl 的通知碼) '
description: 由清單視圖控制項在使用者啟用專案時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- LVN_ITEMACTI加值稅E 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_ITEMACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9f139559b03fd82ac655381972803a288f00db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106667"
---
# <a name="lvn_itemactivate-notification-code"></a><span data-ttu-id="e4a26-105">LVN \_ ITEMACTI加值稅E 通知碼</span><span class="sxs-lookup"><span data-stu-id="e4a26-105">LVN\_ITEMACTIVATE notification code</span></span>

<span data-ttu-id="e4a26-106">由清單視圖控制項在使用者啟用專案時傳送。</span><span class="sxs-lookup"><span data-stu-id="e4a26-106">Sent by a list-view control when the user activates an item.</span></span> <span data-ttu-id="e4a26-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="e4a26-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMACTIVATE

#if (_WIN32_IE >= 0x0400)
    lpnmia = (LPNMITEMACTIVATE)lParam;
#else
    lpnm = (LPNMHDR)lParam;
#endif
```



## <a name="parameters"></a><span data-ttu-id="e4a26-108">參數</span><span class="sxs-lookup"><span data-stu-id="e4a26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4a26-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4a26-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4a26-110">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="e4a26-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="e4a26-111">[**NMITEMACTI加值稅E**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate)結構的指標，其中包含此通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e4a26-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains information about this notification code.</span></span>

<span data-ttu-id="e4a26-112">[4.70 版](common-control-versions.md) 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="e4a26-112">[Version 4.70](common-control-versions.md) and earlier.</span></span> <span data-ttu-id="e4a26-113">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e4a26-113">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4a26-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4a26-114">Return value</span></span>

<span data-ttu-id="e4a26-115">接收此通知碼的應用程式必須傳回零。</span><span class="sxs-lookup"><span data-stu-id="e4a26-115">The application receiving this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4a26-116">備註</span><span class="sxs-lookup"><span data-stu-id="e4a26-116">Remarks</span></span>

<span data-ttu-id="e4a26-117">若要取得正在啟用的專案，接收應用程式應該使用 [**LVM \_ GETSELECTEDCOUNT**](lvm-getselectedcount.md)訊息來取出所選的專案數目，然後將已 **\_ 選取 LVNI** 的 [**lvm \_ GETNEXTITEM**](lvm-getnextitem.md)訊息傳送到所有的專案都已抓取為止。</span><span class="sxs-lookup"><span data-stu-id="e4a26-117">To obtain the items being activated, the receiving application should use the [**LVM\_GETSELECTEDCOUNT**](lvm-getselectedcount.md) message to retrieve the number of items that are selected and then send the [**LVM\_GETNEXTITEM**](lvm-getnextitem.md) message with **LVNI\_SELECTED** until all of the items have been retrieved.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4a26-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4a26-118">Requirements</span></span>



| <span data-ttu-id="e4a26-119">需求</span><span class="sxs-lookup"><span data-stu-id="e4a26-119">Requirement</span></span> | <span data-ttu-id="e4a26-120">值</span><span class="sxs-lookup"><span data-stu-id="e4a26-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a26-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4a26-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e4a26-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4a26-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4a26-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4a26-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e4a26-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4a26-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4a26-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e4a26-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4a26-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e4a26-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





