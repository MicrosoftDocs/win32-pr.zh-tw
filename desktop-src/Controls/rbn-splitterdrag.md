---
title: 'RBN_SPLITTERDRAG (Commctrl 的通知碼) '
description: 由 Rebar 控制項在使用者拖曳分隔器時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 7827c971-6a92-452f-b961-1abe6ae66d2a
keywords:
- RBN_SPLITTERDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- RBN_SPLITTERDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b2d3fc00433be9cd3011f2f2b24d515b8cbd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508903"
---
# <a name="rbn_splitterdrag-notification-code"></a><span data-ttu-id="a5835-105">RBN \_ SPLITTERDRAG 通知碼</span><span class="sxs-lookup"><span data-stu-id="a5835-105">RBN\_SPLITTERDRAG notification code</span></span>

<span data-ttu-id="a5835-106">由 Rebar 控制項在使用者拖曳分隔器時傳送。</span><span class="sxs-lookup"><span data-stu-id="a5835-106">Sent by a rebar control when the user drags a splitter.</span></span> <span data-ttu-id="a5835-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="a5835-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_SPLITTERDRAG

    lpnmrbspltr = (LPNMREBARSPLITTER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a5835-108">參數</span><span class="sxs-lookup"><span data-stu-id="a5835-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5835-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a5835-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5835-110">[**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5835-110">Pointer to an [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5835-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5835-111">Return value</span></span>

<span data-ttu-id="a5835-112">未使用此通知的傳回值。</span><span class="sxs-lookup"><span data-stu-id="a5835-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5835-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5835-113">Requirements</span></span>



| <span data-ttu-id="a5835-114">需求</span><span class="sxs-lookup"><span data-stu-id="a5835-114">Requirement</span></span> | <span data-ttu-id="a5835-115">值</span><span class="sxs-lookup"><span data-stu-id="a5835-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5835-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5835-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a5835-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5835-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a5835-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5835-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a5835-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5835-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a5835-120">標頭</span><span class="sxs-lookup"><span data-stu-id="a5835-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5835-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a5835-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





