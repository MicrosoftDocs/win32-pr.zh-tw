---
title: 'NM_CUSTOMTEXT (Commctrl 的通知碼) '
description: 通知控制項的父視窗有關自訂文字作業的相關資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: b4bde648-3479-4fac-ad32-b34c7272c1fc
keywords:
- NM_CUSTOMTEXT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_CUSTOMTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eebc4033a76d137e28a0c4170c5c613c7933562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383862"
---
# <a name="nm_customtext-notification-code"></a><span data-ttu-id="dc2cc-105">NM \_ CUSTOMTEXT 通知碼</span><span class="sxs-lookup"><span data-stu-id="dc2cc-105">NM\_CUSTOMTEXT notification code</span></span>

<span data-ttu-id="dc2cc-106">通知控制項的父視窗有關自訂文字作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dc2cc-106">Notifies a control's parent window about custom text operations.</span></span> <span data-ttu-id="dc2cc-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="dc2cc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMTEXT

    lpnmct = (NMCUSTOMTEXT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="dc2cc-108">參數</span><span class="sxs-lookup"><span data-stu-id="dc2cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc2cc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc2cc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc2cc-110">[**NMCUSTOMTEXT**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dc2cc-110">A pointer to an [**NMCUSTOMTEXT**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc2cc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc2cc-111">Return value</span></span>

<span data-ttu-id="dc2cc-112">控制項會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="dc2cc-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc2cc-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc2cc-113">Requirements</span></span>



| <span data-ttu-id="dc2cc-114">需求</span><span class="sxs-lookup"><span data-stu-id="dc2cc-114">Requirement</span></span> | <span data-ttu-id="dc2cc-115">值</span><span class="sxs-lookup"><span data-stu-id="dc2cc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2cc-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc2cc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dc2cc-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc2cc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc2cc-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc2cc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dc2cc-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc2cc-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc2cc-120">標頭</span><span class="sxs-lookup"><span data-stu-id="dc2cc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc2cc-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc2cc-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





