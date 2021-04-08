---
title: 'NM_RELEASEDCAPTURE (monthcal) 通知碼 (Commctrl .h) '
description: 通知 monthcal 控制項的父視窗，控制項正在放開滑鼠捕捉。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: c05d3331-26f3-41f4-8032-36ed38d47917
keywords:
- NM_RELEASEDCAPTURE (monthcal) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: 0b9c743a076c8046aa57ba4306145248ed00f0fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685512"
---
# <a name="nm_releasedcapture-monthcal-notification-code"></a><span data-ttu-id="11215-105">NM \_ RELEASEDCAPTURE (monthcal) 通知碼</span><span class="sxs-lookup"><span data-stu-id="11215-105">NM\_RELEASEDCAPTURE (monthcal) notification code</span></span>

<span data-ttu-id="11215-106">通知 monthcal 控制項的父視窗，控制項正在放開滑鼠捕捉。</span><span class="sxs-lookup"><span data-stu-id="11215-106">Notifies a monthcal control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="11215-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="11215-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="11215-108">參數</span><span class="sxs-lookup"><span data-stu-id="11215-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11215-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11215-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11215-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="11215-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11215-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="11215-111">Return value</span></span>

<span data-ttu-id="11215-112">控制項會忽略此通知碼的傳回值。</span><span class="sxs-lookup"><span data-stu-id="11215-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="11215-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="11215-113">Requirements</span></span>



| <span data-ttu-id="11215-114">需求</span><span class="sxs-lookup"><span data-stu-id="11215-114">Requirement</span></span> | <span data-ttu-id="11215-115">值</span><span class="sxs-lookup"><span data-stu-id="11215-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11215-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11215-116">Minimum supported client</span></span><br/> | <span data-ttu-id="11215-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11215-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="11215-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11215-118">Minimum supported server</span></span><br/> | <span data-ttu-id="11215-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11215-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11215-120">標頭</span><span class="sxs-lookup"><span data-stu-id="11215-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="11215-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="11215-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





