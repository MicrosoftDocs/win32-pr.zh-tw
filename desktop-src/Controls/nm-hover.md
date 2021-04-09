---
title: 'NM_HOVER (Commctrl 的通知碼) '
description: 當滑鼠停留在專案上時，由控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0eef3e88-c1f0-4f9c-9ccf-580d8e464157
keywords:
- NM_HOVER 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69344b1aae78ebee99b86c78f4442df20f66187a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685514"
---
# <a name="nm_hover-notification-code"></a><span data-ttu-id="e25a2-105">NM \_ 停留通知碼</span><span class="sxs-lookup"><span data-stu-id="e25a2-105">NM\_HOVER notification code</span></span>

<span data-ttu-id="e25a2-106">當滑鼠停留在專案上時，由控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="e25a2-106">Sent by a control when the mouse hovers over an item.</span></span> <span data-ttu-id="e25a2-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="e25a2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e25a2-108">參數</span><span class="sxs-lookup"><span data-stu-id="e25a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e25a2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e25a2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e25a2-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e25a2-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e25a2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e25a2-111">Return value</span></span>

<span data-ttu-id="e25a2-112">除非另有指定，否則會傳回零以允許控制項正常地處理暫留，或非零，以防止暫止處理。</span><span class="sxs-lookup"><span data-stu-id="e25a2-112">Unless otherwise specified, return zero to allow the control to process the hover normally, or nonzero to prevent the hover from being processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e25a2-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e25a2-113">Requirements</span></span>



| <span data-ttu-id="e25a2-114">需求</span><span class="sxs-lookup"><span data-stu-id="e25a2-114">Requirement</span></span> | <span data-ttu-id="e25a2-115">值</span><span class="sxs-lookup"><span data-stu-id="e25a2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e25a2-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e25a2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e25a2-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e25a2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e25a2-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e25a2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e25a2-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e25a2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e25a2-120">標頭</span><span class="sxs-lookup"><span data-stu-id="e25a2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e25a2-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e25a2-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





