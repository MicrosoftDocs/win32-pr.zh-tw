---
title: 'NM_KEYDOWN (Commctrl 的通知碼) '
description: 當控制項具有鍵盤焦點，且使用者按下按鍵時，由控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e3b38096-797d-4948-9595-a252cf33dcdd
keywords:
- NM_KEYDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 222a47733a60590e7d56ca0adba038164c430fab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843071"
---
# <a name="nm_keydown-notification-code"></a><span data-ttu-id="7c941-105">NM \_ KEYDOWN 通知碼</span><span class="sxs-lookup"><span data-stu-id="7c941-105">NM\_KEYDOWN notification code</span></span>

<span data-ttu-id="7c941-106">當控制項具有鍵盤焦點，且使用者按下按鍵時，由控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="7c941-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="7c941-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="7c941-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7c941-108">參數</span><span class="sxs-lookup"><span data-stu-id="7c941-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c941-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c941-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c941-110">[**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey)結構的指標，其中包含造成通知碼之索引鍵的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7c941-110">A pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c941-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c941-111">Return value</span></span>

<span data-ttu-id="7c941-112">傳回非零以防止控制項處理索引鍵，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="7c941-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c941-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c941-113">Requirements</span></span>



| <span data-ttu-id="7c941-114">需求</span><span class="sxs-lookup"><span data-stu-id="7c941-114">Requirement</span></span> | <span data-ttu-id="7c941-115">值</span><span class="sxs-lookup"><span data-stu-id="7c941-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c941-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c941-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7c941-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c941-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c941-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c941-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7c941-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c941-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c941-120">標頭</span><span class="sxs-lookup"><span data-stu-id="7c941-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c941-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7c941-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





