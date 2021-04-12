---
title: 'NM_KEYDOWN (工具列) 通知碼 (Commctrl) '
description: 當控制項具有鍵盤焦點，且使用者按下按鍵時，由控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: bdfcf9da-118b-4fe6-9a0a-6329eb9196ef
keywords:
- NM_KEYDOWN (工具列) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: e7326946a8234122c81b2fd057dab0ad313d49a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024582"
---
# <a name="nm_keydown-toolbar-notification-code"></a><span data-ttu-id="4c472-105">NM \_ KEYDOWN (工具列) 通知碼</span><span class="sxs-lookup"><span data-stu-id="4c472-105">NM\_KEYDOWN (toolbar) notification code</span></span>

<span data-ttu-id="4c472-106">當控制項具有鍵盤焦點，且使用者按下按鍵時，由控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="4c472-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="4c472-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="4c472-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="4c472-108">參數</span><span class="sxs-lookup"><span data-stu-id="4c472-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c472-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c472-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c472-110">[**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey)結構的指標，其中包含造成通知碼之索引鍵的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4c472-110">Pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c472-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c472-111">Return value</span></span>

<span data-ttu-id="4c472-112">傳回非零以防止控制項處理索引鍵，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="4c472-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c472-113">備註</span><span class="sxs-lookup"><span data-stu-id="4c472-113">Remarks</span></span>

<span data-ttu-id="4c472-114">目前，只有 toolbar 控制項會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="4c472-114">Currently, only the toolbar control sends this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c472-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c472-115">Requirements</span></span>



| <span data-ttu-id="4c472-116">需求</span><span class="sxs-lookup"><span data-stu-id="4c472-116">Requirement</span></span> | <span data-ttu-id="4c472-117">值</span><span class="sxs-lookup"><span data-stu-id="4c472-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c472-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c472-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4c472-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c472-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4c472-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c472-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4c472-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c472-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c472-122">標頭</span><span class="sxs-lookup"><span data-stu-id="4c472-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c472-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c472-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





