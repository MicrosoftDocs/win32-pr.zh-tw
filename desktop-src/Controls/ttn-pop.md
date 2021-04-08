---
title: 'TTN_POP (Commctrl 的通知碼) '
description: 通知擁有者視窗即將隱藏工具提示。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 44a38f1a-f1df-4057-bf76-f87eb467f0d7
keywords:
- TTN_POP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TTN_POP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 576aa382f571fb6ded7205d2df3b0abd938c704d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685894"
---
# <a name="ttn_pop-notification-code"></a><span data-ttu-id="ec6cf-105">TTN \_ POP 通知碼</span><span class="sxs-lookup"><span data-stu-id="ec6cf-105">TTN\_POP notification code</span></span>

<span data-ttu-id="ec6cf-106">通知擁有者視窗即將隱藏工具提示。</span><span class="sxs-lookup"><span data-stu-id="ec6cf-106">Notifies the owner window that a tooltip is about to be hidden.</span></span> <span data-ttu-id="ec6cf-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="ec6cf-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_POP

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ec6cf-108">參數</span><span class="sxs-lookup"><span data-stu-id="ec6cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec6cf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec6cf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec6cf-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ec6cf-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec6cf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec6cf-111">Return value</span></span>

<span data-ttu-id="ec6cf-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="ec6cf-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec6cf-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec6cf-113">Requirements</span></span>



| <span data-ttu-id="ec6cf-114">需求</span><span class="sxs-lookup"><span data-stu-id="ec6cf-114">Requirement</span></span> | <span data-ttu-id="ec6cf-115">值</span><span class="sxs-lookup"><span data-stu-id="ec6cf-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec6cf-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec6cf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ec6cf-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec6cf-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec6cf-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec6cf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ec6cf-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec6cf-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec6cf-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ec6cf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec6cf-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec6cf-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





