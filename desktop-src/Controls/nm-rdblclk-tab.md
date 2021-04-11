---
title: 'NM_RDBLCLK (] 索引標籤) 通知碼 (Commctrl) '
description: 通知索引標籤控制項的父視窗，使用者在控制項內按兩下滑鼠右鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: cdf0df70-e30b-4353-8c2a-26fffa0596c4
keywords:
- NM_RDBLCLK (] 索引標籤) 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4e159e64780f21576aa9e936379c881b32153d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024579"
---
# <a name="nm_rdblclk-tab-notification-code"></a><span data-ttu-id="fd66b-105">NM \_ RDBLCLK (tab) 通知碼</span><span class="sxs-lookup"><span data-stu-id="fd66b-105">NM\_RDBLCLK (tab) notification code</span></span>

<span data-ttu-id="fd66b-106">通知索引標籤控制項的父視窗，使用者在控制項內按兩下滑鼠右鍵。</span><span class="sxs-lookup"><span data-stu-id="fd66b-106">Notifies the parent window of a tab control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="fd66b-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="fd66b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="fd66b-108">參數</span><span class="sxs-lookup"><span data-stu-id="fd66b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd66b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd66b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd66b-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fd66b-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd66b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd66b-111">Return value</span></span>

<span data-ttu-id="fd66b-112">傳回非零以允許預設處理，或零以允許預設處理。</span><span class="sxs-lookup"><span data-stu-id="fd66b-112">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd66b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd66b-113">Requirements</span></span>



| <span data-ttu-id="fd66b-114">需求</span><span class="sxs-lookup"><span data-stu-id="fd66b-114">Requirement</span></span> | <span data-ttu-id="fd66b-115">值</span><span class="sxs-lookup"><span data-stu-id="fd66b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd66b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd66b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fd66b-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd66b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd66b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd66b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fd66b-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd66b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd66b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="fd66b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd66b-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd66b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





