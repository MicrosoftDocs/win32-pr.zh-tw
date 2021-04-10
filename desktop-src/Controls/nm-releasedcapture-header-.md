---
title: 'NM_RELEASEDCAPTURE (標頭) 通知碼 (Commctrl) '
description: 通知標題控制項的父視窗，控制項正在放開滑鼠捕捉。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: fca57009-dc96-4575-8c64-c753884b05fe
keywords:
- NM_RELEASEDCAPTURE (標頭) 通知碼 Windows 控制項
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
ms.openlocfilehash: 88334b9eb9791ee20be4b9defd6e979f788c5067
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686201"
---
# <a name="nm_releasedcapture-header-notification-code"></a><span data-ttu-id="38f69-105">NM \_ RELEASEDCAPTURE (標頭) 通知碼</span><span class="sxs-lookup"><span data-stu-id="38f69-105">NM\_RELEASEDCAPTURE (header) notification code</span></span>

<span data-ttu-id="38f69-106">通知標題控制項的父視窗，控制項正在放開滑鼠捕捉。</span><span class="sxs-lookup"><span data-stu-id="38f69-106">Notifies a header control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="38f69-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="38f69-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="38f69-108">參數</span><span class="sxs-lookup"><span data-stu-id="38f69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38f69-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38f69-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38f69-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="38f69-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38f69-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="38f69-111">Return value</span></span>

<span data-ttu-id="38f69-112">控制項會忽略此通知碼的傳回值。</span><span class="sxs-lookup"><span data-stu-id="38f69-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="38f69-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="38f69-113">Requirements</span></span>



| <span data-ttu-id="38f69-114">需求</span><span class="sxs-lookup"><span data-stu-id="38f69-114">Requirement</span></span> | <span data-ttu-id="38f69-115">值</span><span class="sxs-lookup"><span data-stu-id="38f69-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38f69-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38f69-116">Minimum supported client</span></span><br/> | <span data-ttu-id="38f69-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38f69-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="38f69-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38f69-118">Minimum supported server</span></span><br/> | <span data-ttu-id="38f69-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38f69-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="38f69-120">標頭</span><span class="sxs-lookup"><span data-stu-id="38f69-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="38f69-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="38f69-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





