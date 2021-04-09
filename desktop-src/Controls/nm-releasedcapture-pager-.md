---
title: 'NM_RELEASEDCAPTURE (呼機) 通知碼 (Commctrl) '
description: 通知頁面控制項的父視窗，控制項已放開滑鼠捕捉。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 5ce9c38a-5d37-4ac7-8510-30bc59d85cca
keywords:
- NM_RELEASEDCAPTURE (呼機) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb1d258d9baa0952e1707e36884a492ff65f99b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843703"
---
# <a name="nm_releasedcapture-pager-notification-code"></a><span data-ttu-id="69242-105">NM \_ RELEASEDCAPTURE (的呼叫器) 通知碼</span><span class="sxs-lookup"><span data-stu-id="69242-105">NM\_RELEASEDCAPTURE (pager) notification code</span></span>

<span data-ttu-id="69242-106">通知頁面控制項的父視窗，控制項已放開滑鼠捕捉。</span><span class="sxs-lookup"><span data-stu-id="69242-106">Notifies a pager control's parent window that the control has released the mouse capture.</span></span> <span data-ttu-id="69242-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="69242-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="69242-108">參數</span><span class="sxs-lookup"><span data-stu-id="69242-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69242-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69242-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69242-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="69242-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69242-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="69242-111">Return value</span></span>

<span data-ttu-id="69242-112">呼機控制項會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="69242-112">The return value is ignored by the pager control.</span></span>

## <a name="requirements"></a><span data-ttu-id="69242-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="69242-113">Requirements</span></span>



| <span data-ttu-id="69242-114">需求</span><span class="sxs-lookup"><span data-stu-id="69242-114">Requirement</span></span> | <span data-ttu-id="69242-115">值</span><span class="sxs-lookup"><span data-stu-id="69242-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69242-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69242-116">Minimum supported client</span></span><br/> | <span data-ttu-id="69242-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69242-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="69242-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69242-118">Minimum supported server</span></span><br/> | <span data-ttu-id="69242-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69242-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69242-120">標頭</span><span class="sxs-lookup"><span data-stu-id="69242-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="69242-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="69242-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





