---
title: 'TBN_SAVE (Commctrl 的通知碼) '
description: 通知工具列的父視窗，工具列正在儲存中。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- TBN_SAVE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_SAVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cd28cb9d5fa1804caa3fe0ca89823305725ddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686579"
---
# <a name="tbn_save-notification-code"></a><span data-ttu-id="f1eb3-105">TBN \_ 儲存通知碼</span><span class="sxs-lookup"><span data-stu-id="f1eb3-105">TBN\_SAVE notification code</span></span>

<span data-ttu-id="f1eb3-106">通知工具列的父視窗，工具列正在儲存中。</span><span class="sxs-lookup"><span data-stu-id="f1eb3-106">Notifies a toolbar's parent window that a toolbar is in the process of being saved.</span></span> <span data-ttu-id="f1eb3-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="f1eb3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f1eb3-108">參數</span><span class="sxs-lookup"><span data-stu-id="f1eb3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1eb3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1eb3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1eb3-110">[**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f1eb3-110">Pointer to an [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1eb3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1eb3-111">Return value</span></span>

<span data-ttu-id="f1eb3-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="f1eb3-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1eb3-113">備註</span><span class="sxs-lookup"><span data-stu-id="f1eb3-113">Remarks</span></span>

<span data-ttu-id="f1eb3-114">應用程式會在儲存程式開始時接收此通知碼一次，並在每個按鈕上接收一次。</span><span class="sxs-lookup"><span data-stu-id="f1eb3-114">The application will receive this notification code once at the start of the save process and once for each button.</span></span> <span data-ttu-id="f1eb3-115">此通知碼可讓您有機會將自己的資訊新增至 Shell 所儲存的資訊。</span><span class="sxs-lookup"><span data-stu-id="f1eb3-115">This notification code gives you an opportunity to add your own information to that saved by the Shell.</span></span> <span data-ttu-id="f1eb3-116">如果您不想要新增資訊，請忽略通知碼。</span><span class="sxs-lookup"><span data-stu-id="f1eb3-116">If you do not wish to add information, ignore the notification code.</span></span> <span data-ttu-id="f1eb3-117">如需如何處理 TBN 儲存的詳細討論，請參閱 [工具列自訂](toolbar-controls-overview.md) \_ 。</span><span class="sxs-lookup"><span data-stu-id="f1eb3-117">See [Toolbar Customization](toolbar-controls-overview.md) for a more detailed discussion of how to handle TBN\_SAVE.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1eb3-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1eb3-118">Requirements</span></span>



| <span data-ttu-id="f1eb3-119">需求</span><span class="sxs-lookup"><span data-stu-id="f1eb3-119">Requirement</span></span> | <span data-ttu-id="f1eb3-120">值</span><span class="sxs-lookup"><span data-stu-id="f1eb3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1eb3-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1eb3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f1eb3-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1eb3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1eb3-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1eb3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f1eb3-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1eb3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1eb3-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f1eb3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1eb3-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1eb3-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1eb3-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1eb3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1eb3-128">TBN \_ 還原</span><span class="sxs-lookup"><span data-stu-id="f1eb3-128">TBN\_RESTORE</span></span>](tbn-restore.md)
</dt> </dl>

 

 





