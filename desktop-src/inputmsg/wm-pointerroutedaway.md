---
title: WM_POINTERROUTEDAWAY 訊息
description: 當指標輸入路由傳送至另一個進程時，在接收輸入的進程上發生。AddContentWithCrossProcessChaining) 。
ms.assetid: 06F8152C-0DA0-4820-835E-07AD35B24310
keywords:
- WM_POINTERROUTEDAWAY 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDAWAY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3c099c02338aa70817d75717064e0b99ac13c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025263"
---
# <a name="wm_pointerroutedaway-message"></a><span data-ttu-id="4885d-104">WM_POINTERROUTEDAWAY 訊息</span><span class="sxs-lookup"><span data-stu-id="4885d-104">WM_POINTERROUTEDAWAY message</span></span>

<span data-ttu-id="4885d-105">當指標輸入路由傳送至另一個進程時，在接收輸入的進程上發生。</span><span class="sxs-lookup"><span data-stu-id="4885d-105">Occurs on the process receiving input when the pointer input is routed to another process.</span></span>

<span data-ttu-id="4885d-106">當指標輸入在設定為跨進程連結 ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)) 的內容之間轉換時，會傳送到另一個進程。</span><span class="sxs-lookup"><span data-stu-id="4885d-106">Sent when pointer input transitions from one process to another across content configured for cross-process chaining ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span></span>

<span data-ttu-id="4885d-107">這則訊息會傳送至目前正在接收指標輸入的進程。</span><span class="sxs-lookup"><span data-stu-id="4885d-107">This message is sent to the process currently receiving pointer input.</span></span>


```C++
#define WM_POINTERROUTEDAWAY       0x0252
```



## <a name="parameters"></a><span data-ttu-id="4885d-108">參數</span><span class="sxs-lookup"><span data-stu-id="4885d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4885d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4885d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4885d-110">未使用的。</span><span class="sxs-lookup"><span data-stu-id="4885d-110">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="4885d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4885d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4885d-112">未使用的。</span><span class="sxs-lookup"><span data-stu-id="4885d-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4885d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4885d-113">Return value</span></span>

<span data-ttu-id="4885d-114">NULL</span><span class="sxs-lookup"><span data-stu-id="4885d-114">NULL</span></span>

## <a name="remarks"></a><span data-ttu-id="4885d-115">備註</span><span class="sxs-lookup"><span data-stu-id="4885d-115">Remarks</span></span>

<span data-ttu-id="4885d-116">此訊息不會隨 [**WM_POINTERUP**](wm-pointerup.md) 訊息或 [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) 訊息傳送。</span><span class="sxs-lookup"><span data-stu-id="4885d-116">This message is not sent with either a [**WM_POINTERUP**](wm-pointerup.md) message or a [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4885d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4885d-117">Requirements</span></span>



| <span data-ttu-id="4885d-118">需求</span><span class="sxs-lookup"><span data-stu-id="4885d-118">Requirement</span></span> | <span data-ttu-id="4885d-119">值</span><span class="sxs-lookup"><span data-stu-id="4885d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4885d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4885d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4885d-121">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4885d-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4885d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4885d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4885d-123">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4885d-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4885d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="4885d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4885d-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4885d-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4885d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4885d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4885d-127">訊息</span><span class="sxs-lookup"><span data-stu-id="4885d-127">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="4885d-128">**WM_POINTERROUTEDTO**</span><span class="sxs-lookup"><span data-stu-id="4885d-128">**WM_POINTERROUTEDTO**</span></span>](wm-pointerroutedto.md)
</dt> </dl>

 

