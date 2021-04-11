---
title: 'LVN_KEYDOWN (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，表示已按下按鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 3aa3d165-7227-41c4-8bc2-3e51a0f52ee3
keywords:
- LVN_KEYDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 516c64e9050a6946d3a135ecc0d00d7e384e9844
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935167"
---
# <a name="lvn_keydown-notification-code"></a><span data-ttu-id="13bdd-105">LVN \_ KEYDOWN 通知碼</span><span class="sxs-lookup"><span data-stu-id="13bdd-105">LVN\_KEYDOWN notification code</span></span>

<span data-ttu-id="13bdd-106">通知清單視圖控制項的父視窗，表示已按下按鍵。</span><span class="sxs-lookup"><span data-stu-id="13bdd-106">Notifies a list-view control's parent window that a key has been pressed.</span></span> <span data-ttu-id="13bdd-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="13bdd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_KEYDOWN

    pnkd = (LPNMLVKEYDOWN) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="13bdd-108">參數</span><span class="sxs-lookup"><span data-stu-id="13bdd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13bdd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13bdd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13bdd-110">[**NMLVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="13bdd-110">Pointer to an [**NMLVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13bdd-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="13bdd-111">Return value</span></span>

<span data-ttu-id="13bdd-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="13bdd-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="13bdd-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="13bdd-113">Requirements</span></span>



| <span data-ttu-id="13bdd-114">需求</span><span class="sxs-lookup"><span data-stu-id="13bdd-114">Requirement</span></span> | <span data-ttu-id="13bdd-115">值</span><span class="sxs-lookup"><span data-stu-id="13bdd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13bdd-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13bdd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="13bdd-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13bdd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="13bdd-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13bdd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="13bdd-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13bdd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="13bdd-120">標頭</span><span class="sxs-lookup"><span data-stu-id="13bdd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="13bdd-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="13bdd-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





