---
title: 'TBN_RESTORE (Commctrl 的通知碼) '
description: 通知工具列的父視窗正在還原工具列。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: b1f0c801-d56b-4e93-b9ba-b572aaa38647
keywords:
- TBN_RESTORE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_RESTORE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 374ed0fb68accbb65515d39ea01f237707eb16c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466220"
---
# <a name="tbn_restore-notification-code"></a><span data-ttu-id="c1644-105">TBN \_ 還原通知碼</span><span class="sxs-lookup"><span data-stu-id="c1644-105">TBN\_RESTORE notification code</span></span>

<span data-ttu-id="c1644-106">通知工具列的父視窗正在還原工具列。</span><span class="sxs-lookup"><span data-stu-id="c1644-106">Notifies a toolbar's parent window that a toolbar is in the process of being restored.</span></span> <span data-ttu-id="c1644-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="c1644-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_RESTORE 

    lpnmtb = (LPNMTBRESTORE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c1644-108">參數</span><span class="sxs-lookup"><span data-stu-id="c1644-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1644-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1644-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1644-110">[**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c1644-110">Pointer to an [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1644-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1644-111">Return value</span></span>

<span data-ttu-id="c1644-112">應用程式應該會傳回零以回應還原程式開始時所收到的第一個 **TBN \_ 還原** 通知程式碼，以繼續還原按鈕資訊。</span><span class="sxs-lookup"><span data-stu-id="c1644-112">The application should return zero in response to the first **TBN\_RESTORE** notification code received at the start of the restore process to continue restoring the button information.</span></span> <span data-ttu-id="c1644-113">如果應用程式傳回非零值，則還原進程會取消。</span><span class="sxs-lookup"><span data-stu-id="c1644-113">If the application returns a nonzero value, the restore process is canceled.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1644-114">備註</span><span class="sxs-lookup"><span data-stu-id="c1644-114">Remarks</span></span>

<span data-ttu-id="c1644-115">應用程式會在一開始還原程式時，每個按鈕一次收到此通知碼。</span><span class="sxs-lookup"><span data-stu-id="c1644-115">The application will receive this notification code once at the start of the restore process and once for each button.</span></span> <span data-ttu-id="c1644-116">此通知碼讓您有機會從先前儲存的資料流程中解壓縮資訊。</span><span class="sxs-lookup"><span data-stu-id="c1644-116">This notification code gives you an opportunity to extract the information from the data stream that you saved previously.</span></span> <span data-ttu-id="c1644-117">如果您尚未儲存任何資訊，請忽略通知碼。</span><span class="sxs-lookup"><span data-stu-id="c1644-117">If you haven't saved any information, ignore the notification code.</span></span> <span data-ttu-id="c1644-118">如需如何處理 **TBN \_ 還原** 的詳細討論，請參閱 [工具列自訂](toolbar-controls-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="c1644-118">See [Toolbar Customization](toolbar-controls-overview.md) for a more detailed discussion of how to handle **TBN\_RESTORE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1644-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1644-119">Requirements</span></span>



| <span data-ttu-id="c1644-120">需求</span><span class="sxs-lookup"><span data-stu-id="c1644-120">Requirement</span></span> | <span data-ttu-id="c1644-121">值</span><span class="sxs-lookup"><span data-stu-id="c1644-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1644-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1644-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c1644-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1644-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c1644-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1644-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c1644-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1644-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1644-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c1644-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1644-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1644-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





