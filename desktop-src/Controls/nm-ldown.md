---
title: 'NM_LDOWN (Commctrl 的通知碼) '
description: 通知控制項的父視窗，滑鼠左鍵已按下滑鼠左鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 59546fc3-f7c5-4b2d-9fd7-2ff89d72cd9f
keywords:
- NM_LDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d62d1570fc0c10ccb64ae6c1f9af6433025ec79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965276"
---
# <a name="nm_ldown-notification-code"></a><span data-ttu-id="0be92-105">NM \_ LDOWN 通知碼</span><span class="sxs-lookup"><span data-stu-id="0be92-105">NM\_LDOWN notification code</span></span>

<span data-ttu-id="0be92-106">通知控制項的父視窗，滑鼠左鍵已按下滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="0be92-106">Notifies a control's parent window that the left mouse button has been pressed.</span></span> <span data-ttu-id="0be92-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="0be92-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_LDOWN

   lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0be92-108">參數</span><span class="sxs-lookup"><span data-stu-id="0be92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0be92-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0be92-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0be92-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0be92-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0be92-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0be92-111">Return value</span></span>

<span data-ttu-id="0be92-112">控制項會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="0be92-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="0be92-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0be92-113">Requirements</span></span>



| <span data-ttu-id="0be92-114">需求</span><span class="sxs-lookup"><span data-stu-id="0be92-114">Requirement</span></span> | <span data-ttu-id="0be92-115">值</span><span class="sxs-lookup"><span data-stu-id="0be92-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0be92-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0be92-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0be92-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0be92-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0be92-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0be92-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0be92-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0be92-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0be92-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0be92-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0be92-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0be92-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





