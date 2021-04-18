---
title: WM_POINTERROUTEDRELEASED 訊息
description: 傳送至所有進程 (透過 AddContentWithCrossProcessChaining 設定跨進程的連結，而且目前在目前的進程上收到 WM_POINTERUP 訊息時，目前未處理指標輸入) 與特定指標識別碼相關聯。
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- WM_POINTERROUTEDRELEASED 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDRELEASED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 8e24a0df1a2bbdf2b0a9df97057686aa6045eff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384685"
---
# <a name="wm_pointerroutedreleased-message"></a><span data-ttu-id="bd5ab-104">WM_POINTERROUTEDRELEASED 訊息</span><span class="sxs-lookup"><span data-stu-id="bd5ab-104">WM_POINTERROUTEDRELEASED message</span></span>

<span data-ttu-id="bd5ab-105">傳送至所有進程 (透過 [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) 設定跨進程的連結，而且目前在目前的進程上收到 [**WM_POINTERUP**](wm-pointerup.md) 訊息時，目前未處理指標輸入) 與特定指標識別碼相關聯。</span><span class="sxs-lookup"><span data-stu-id="bd5ab-105">Sent to all processes (configured for cross-process chaining through [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) and not currently handling pointer input) ever associated with a specific pointer ID, when a [**WM_POINTERUP**](wm-pointerup.md) message is received on the current process.</span></span>


```C++
#define WM_POINTERROUTEDRELEASED       0x0253
```



## <a name="parameters"></a><span data-ttu-id="bd5ab-106">參數</span><span class="sxs-lookup"><span data-stu-id="bd5ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd5ab-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd5ab-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd5ab-108">未使用的。</span><span class="sxs-lookup"><span data-stu-id="bd5ab-108">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="bd5ab-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd5ab-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd5ab-110">未使用的。</span><span class="sxs-lookup"><span data-stu-id="bd5ab-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd5ab-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd5ab-111">Return value</span></span>

<span data-ttu-id="bd5ab-112">NULL</span><span class="sxs-lookup"><span data-stu-id="bd5ab-112">NULL</span></span>

## <a name="requirements"></a><span data-ttu-id="bd5ab-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd5ab-113">Requirements</span></span>



| <span data-ttu-id="bd5ab-114">需求</span><span class="sxs-lookup"><span data-stu-id="bd5ab-114">Requirement</span></span> | <span data-ttu-id="bd5ab-115">值</span><span class="sxs-lookup"><span data-stu-id="bd5ab-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd5ab-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd5ab-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bd5ab-117">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd5ab-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bd5ab-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd5ab-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bd5ab-119">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd5ab-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bd5ab-120">標頭</span><span class="sxs-lookup"><span data-stu-id="bd5ab-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd5ab-121"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="bd5ab-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd5ab-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd5ab-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd5ab-123">訊息</span><span class="sxs-lookup"><span data-stu-id="bd5ab-123">Messages</span></span>](messages.md)
</dt> </dl>

 

