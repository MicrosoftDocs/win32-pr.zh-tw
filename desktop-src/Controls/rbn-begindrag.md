---
title: 'RBN_BEGINDRAG (Commctrl 的通知碼) '
description: 當使用者開始拖曳寬線時，由 Rebar 控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e1565b31-7694-43cc-87ee-c9294a0612cd
keywords:
- RBN_BEGINDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- RBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c797e026484b32e68408cf720a1d4681d066c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464389"
---
# <a name="rbn_begindrag-notification-code"></a><span data-ttu-id="27749-105">RBN \_ BEGINDRAG 通知碼</span><span class="sxs-lookup"><span data-stu-id="27749-105">RBN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="27749-106">當使用者開始拖曳寬線時，由 Rebar 控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="27749-106">Sent by a rebar control when the user begins dragging a band.</span></span> <span data-ttu-id="27749-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="27749-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_BEGINDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="27749-108">參數</span><span class="sxs-lookup"><span data-stu-id="27749-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27749-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27749-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27749-110">[**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="27749-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27749-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="27749-111">Return value</span></span>

<span data-ttu-id="27749-112">傳回零以允許 Rebar 繼續拖曳作業，或非零值以中止拖曳作業。</span><span class="sxs-lookup"><span data-stu-id="27749-112">Return zero to allow the rebar to continue the drag operation, or nonzero to abort the drag operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="27749-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="27749-113">Requirements</span></span>



| <span data-ttu-id="27749-114">需求</span><span class="sxs-lookup"><span data-stu-id="27749-114">Requirement</span></span> | <span data-ttu-id="27749-115">值</span><span class="sxs-lookup"><span data-stu-id="27749-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27749-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27749-116">Minimum supported client</span></span><br/> | <span data-ttu-id="27749-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27749-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="27749-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27749-118">Minimum supported server</span></span><br/> | <span data-ttu-id="27749-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27749-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27749-120">標頭</span><span class="sxs-lookup"><span data-stu-id="27749-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="27749-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="27749-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





