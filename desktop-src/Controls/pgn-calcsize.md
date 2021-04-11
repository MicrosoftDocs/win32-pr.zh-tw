---
title: 'PGN_CALCSIZE (Commctrl 的通知碼) '
description: 由分頁控制項傳送以取得所包含視窗的可滾動維度。
ms.assetid: a15f4191-2f26-4139-bdaf-bab219449b78
keywords:
- PGN_CALCSIZE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PGN_CALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee6de1c45402f8bdc154f9f10be00140d7c766c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685837"
---
# <a name="pgn_calcsize-notification-code"></a><span data-ttu-id="f09e5-104">PGN \_ CALCSIZE 通知碼</span><span class="sxs-lookup"><span data-stu-id="f09e5-104">PGN\_CALCSIZE notification code</span></span>

<span data-ttu-id="f09e5-105">由分頁控制項傳送以取得所包含視窗的可滾動維度。</span><span class="sxs-lookup"><span data-stu-id="f09e5-105">Sent by a pager control to obtain the scrollable dimensions of the contained window.</span></span> <span data-ttu-id="f09e5-106">這些維度是由分頁控制項用來判斷所包含視窗的可滾動大小。</span><span class="sxs-lookup"><span data-stu-id="f09e5-106">These dimensions are used by the pager control to determine the scrollable size of the contained window.</span></span> <span data-ttu-id="f09e5-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="f09e5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_CALCSIZE

    lpnmcs = (LPNMPGCALCSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f09e5-108">參數</span><span class="sxs-lookup"><span data-stu-id="f09e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f09e5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f09e5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f09e5-110">[**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize)結構的指標，其中包含和接收通知程式碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f09e5-110">Pointer to an [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) structure that contains and receives information about the notification code.</span></span> <span data-ttu-id="f09e5-111">此結構的 **>dwflag** 成員指出正在計算的維度。</span><span class="sxs-lookup"><span data-stu-id="f09e5-111">The **dwFlag** member of this structure indicates which dimension is being calculated.</span></span> <span data-ttu-id="f09e5-112">根據 **>dwflag** 的值，您應該將所需的維度放在此結構的 **iWidth** 或 **iHeight** 成員中。</span><span class="sxs-lookup"><span data-stu-id="f09e5-112">Depending on the value of **dwFlag**, you should place the desired dimension in the **iWidth** or **iHeight** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f09e5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f09e5-113">Return value</span></span>

<span data-ttu-id="f09e5-114">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="f09e5-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="f09e5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f09e5-115">Requirements</span></span>



| <span data-ttu-id="f09e5-116">需求</span><span class="sxs-lookup"><span data-stu-id="f09e5-116">Requirement</span></span> | <span data-ttu-id="f09e5-117">值</span><span class="sxs-lookup"><span data-stu-id="f09e5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f09e5-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f09e5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f09e5-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f09e5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f09e5-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f09e5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f09e5-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f09e5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f09e5-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f09e5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f09e5-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f09e5-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





