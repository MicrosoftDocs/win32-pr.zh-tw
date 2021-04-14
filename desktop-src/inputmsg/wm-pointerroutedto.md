---
title: WM_POINTERROUTEDTO 訊息
description: 在針對現有指標識別碼進行中的指標輸入時傳送，會在針對跨進程連結設定的內容之間，從一個進程轉換成另一個進程 (AddContentWithCrossProcessChaining) 。
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- WM_POINTERROUTEDTO 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDTO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 7658aeef77a0f7e19f2449213e9332b4e60c9450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384410"
---
# <a name="wm_pointerroutedto-message"></a><span data-ttu-id="d234f-104">WM_POINTERROUTEDTO 訊息</span><span class="sxs-lookup"><span data-stu-id="d234f-104">WM_POINTERROUTEDTO message</span></span>

<span data-ttu-id="d234f-105">在針對現有指標識別碼進行中的指標輸入時傳送，會在針對跨進程連結設定的內容之間，從一個進程轉換成另一個進程 ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)) 。</span><span class="sxs-lookup"><span data-stu-id="d234f-105">Sent when ongoing pointer input, for an existing pointer ID, transitions from one process to another across content configured for cross-process chaining ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span></span>

<span data-ttu-id="d234f-106">這則訊息會傳送至目前未接收指標輸入的進程。</span><span class="sxs-lookup"><span data-stu-id="d234f-106">This message is sent to the process not currently receiving pointer input.</span></span>


```C++
#define WM_POINTERROUTEDTO       0x0251
```



## <a name="parameters"></a><span data-ttu-id="d234f-107">參數</span><span class="sxs-lookup"><span data-stu-id="d234f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d234f-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d234f-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d234f-109">未使用的。</span><span class="sxs-lookup"><span data-stu-id="d234f-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="d234f-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d234f-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d234f-111">未使用的。</span><span class="sxs-lookup"><span data-stu-id="d234f-111">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d234f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d234f-112">Return value</span></span>

<span data-ttu-id="d234f-113">NULL</span><span class="sxs-lookup"><span data-stu-id="d234f-113">NULL</span></span>

## <a name="remarks"></a><span data-ttu-id="d234f-114">備註</span><span class="sxs-lookup"><span data-stu-id="d234f-114">Remarks</span></span>

<span data-ttu-id="d234f-115">當針對不同進程的新指標識別碼張貼 [**WM_POINTERDOWN**](wm-pointerdown.md) 訊息時，不會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="d234f-115">This message is not sent when a [**WM_POINTERDOWN**](wm-pointerdown.md) message is posted for a new pointer ID on a different process.</span></span>

<span data-ttu-id="d234f-116">如果先張貼 **WM_POINTERROUTEDTO** 訊息，則不會傳送 [**WM_POINTERDOWN**](wm-pointerdown.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="d234f-116">A [**WM_POINTERDOWN**](wm-pointerdown.md) message is not sent if a **WM_POINTERROUTEDTO** message is posted first.</span></span>

## <a name="requirements"></a><span data-ttu-id="d234f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d234f-117">Requirements</span></span>



| <span data-ttu-id="d234f-118">需求</span><span class="sxs-lookup"><span data-stu-id="d234f-118">Requirement</span></span> | <span data-ttu-id="d234f-119">值</span><span class="sxs-lookup"><span data-stu-id="d234f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d234f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d234f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d234f-121">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d234f-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d234f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d234f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d234f-123">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d234f-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d234f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d234f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d234f-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d234f-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d234f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d234f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d234f-127">訊息</span><span class="sxs-lookup"><span data-stu-id="d234f-127">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="d234f-128">**WM_POINTERROUTEDAWAY**</span><span class="sxs-lookup"><span data-stu-id="d234f-128">**WM_POINTERROUTEDAWAY**</span></span>](wm-pointerroutedaway.md)
</dt> </dl>

 

