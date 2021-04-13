---
title: 'PBM_SETSTATE 訊息 (Commctrl .h) '
description: 設定進度列的狀態。
ms.assetid: 4626f334-db74-4618-8fc7-e6f21c88ca19
keywords:
- PBM_SETSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c91e94bcc909957264eff776e56d3580b2c36ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466101"
---
# <a name="pbm_setstate-message"></a><span data-ttu-id="3fdc9-104">PBM \_ SETSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="3fdc9-104">PBM\_SETSTATE message</span></span>

<span data-ttu-id="3fdc9-105">設定進度列的狀態。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-105">Sets the state of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3fdc9-106">參數</span><span class="sxs-lookup"><span data-stu-id="3fdc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fdc9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3fdc9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fdc9-108">所設定進度列的狀態。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-108">State of the progress bar that is being set.</span></span> <span data-ttu-id="3fdc9-109">下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-109">One of the following values.</span></span>



| <span data-ttu-id="3fdc9-110">值</span><span class="sxs-lookup"><span data-stu-id="3fdc9-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="3fdc9-111">意義</span><span class="sxs-lookup"><span data-stu-id="3fdc9-111">Meaning</span></span>                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <span data-ttu-id="3fdc9-112"><dt>**PBST \_ 正常**</dt></span><span class="sxs-lookup"><span data-stu-id="3fdc9-112"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="3fdc9-113">進行中。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-113">In progress.</span></span><br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <span data-ttu-id="3fdc9-114"><dt>**PBST \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="3fdc9-114"><dt>**PBST\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="3fdc9-115">錯誤。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-115">Error.</span></span><br/>       |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <span data-ttu-id="3fdc9-116"><dt>**PBST 已 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="3fdc9-116"><dt>**PBST\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="3fdc9-117">已暫停。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-117">Paused.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="3fdc9-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fdc9-118">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3fdc9-119">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-119">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fdc9-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="3fdc9-120">Return value</span></span>

<span data-ttu-id="3fdc9-121">傳回先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-121">Returns the previous state.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fdc9-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fdc9-122">Requirements</span></span>



| <span data-ttu-id="3fdc9-123">需求</span><span class="sxs-lookup"><span data-stu-id="3fdc9-123">Requirement</span></span> | <span data-ttu-id="3fdc9-124">值</span><span class="sxs-lookup"><span data-stu-id="3fdc9-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fdc9-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3fdc9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3fdc9-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fdc9-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3fdc9-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3fdc9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3fdc9-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fdc9-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3fdc9-129">標頭</span><span class="sxs-lookup"><span data-stu-id="3fdc9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fdc9-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3fdc9-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





