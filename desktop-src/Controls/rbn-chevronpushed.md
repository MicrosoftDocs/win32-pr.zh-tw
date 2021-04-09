---
title: 'RBN_CHEVRONPUSHED (Commctrl 的通知碼) '
description: 當推送燕形時由 Rebar 控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 58aa2c9d-8ab6-46ee-b32f-5c04fb7afa84
keywords:
- RBN_CHEVRONPUSHED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- RBN_CHEVRONPUSHED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab28d992b6d4a617b7aa7ee144eb50aef3b0e834
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025076"
---
# <a name="rbn_chevronpushed-notification-code"></a><span data-ttu-id="c1289-105">RBN \_ CHEVRONPUSHED 通知碼</span><span class="sxs-lookup"><span data-stu-id="c1289-105">RBN\_CHEVRONPUSHED notification code</span></span>

<span data-ttu-id="c1289-106">當推送燕形時由 Rebar 控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="c1289-106">Sent by a rebar control when a chevron is pushed.</span></span> <span data-ttu-id="c1289-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="c1289-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_CHEVRONPUSHED

    lpnm = (NMREBARCHEVRON) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c1289-108">參數</span><span class="sxs-lookup"><span data-stu-id="c1289-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1289-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1289-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1289-110">頻外 [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c1289-110">Pointer to the band's [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1289-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1289-111">Return value</span></span>

<span data-ttu-id="c1289-112">未使用此通知的傳回值。</span><span class="sxs-lookup"><span data-stu-id="c1289-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1289-113">備註</span><span class="sxs-lookup"><span data-stu-id="c1289-113">Remarks</span></span>

<span data-ttu-id="c1289-114">當應用程式收到此通知碼時，它會負責顯示快顯功能表，其中包含每個隱藏工具的專案。</span><span class="sxs-lookup"><span data-stu-id="c1289-114">When an application receives this notification code, it is responsible for displaying a popup menu with items for each hidden tool.</span></span> <span data-ttu-id="c1289-115">使用 [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron)結構的 **rc** 成員，找出快顯功能表的正確位置。</span><span class="sxs-lookup"><span data-stu-id="c1289-115">Use the **rc** member of the [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure to find the correct position for the popup menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1289-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1289-116">Requirements</span></span>



| <span data-ttu-id="c1289-117">需求</span><span class="sxs-lookup"><span data-stu-id="c1289-117">Requirement</span></span> | <span data-ttu-id="c1289-118">值</span><span class="sxs-lookup"><span data-stu-id="c1289-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1289-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1289-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c1289-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1289-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c1289-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1289-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c1289-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1289-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1289-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c1289-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1289-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1289-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





