---
title: 'TBM_CLEARTICS 訊息 (Commctrl .h) '
description: 從跟蹤條中移除目前的刻度標記。 此訊息不會移除第一個和最後一個刻度，這些刻度會由 [並排顯示] 自動建立。
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- TBM_CLEARTICS message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_CLEARTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1ecb4f9f931c976b2542a1f263fc069f1eca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464777"
---
# <a name="tbm_cleartics-message"></a><span data-ttu-id="33760-105">TBM \_ CLEARTICS 訊息</span><span class="sxs-lookup"><span data-stu-id="33760-105">TBM\_CLEARTICS message</span></span>

<span data-ttu-id="33760-106">從跟蹤條中移除目前的刻度標記。</span><span class="sxs-lookup"><span data-stu-id="33760-106">Removes the current tick marks from a trackbar.</span></span> <span data-ttu-id="33760-107">此訊息不會移除第一個和最後一個刻度，這些刻度會由 [並排顯示] 自動建立。</span><span class="sxs-lookup"><span data-stu-id="33760-107">This message does not remove the first and last tick marks, which are created automatically by the trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="33760-108">參數</span><span class="sxs-lookup"><span data-stu-id="33760-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33760-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33760-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33760-110">重繪旗標。</span><span class="sxs-lookup"><span data-stu-id="33760-110">Redraw flag.</span></span> <span data-ttu-id="33760-111">如果此參數為 **TRUE**，則在清除刻度之後，會重新繪製這些標記。</span><span class="sxs-lookup"><span data-stu-id="33760-111">If this parameter is **TRUE**, the trackbar is redrawn after the tick marks are cleared.</span></span> <span data-ttu-id="33760-112">如果此參數為 **FALSE**，則訊息會清除刻度，但不會重新繪製這些標記。</span><span class="sxs-lookup"><span data-stu-id="33760-112">If this parameter is **FALSE**, the message clears the tick marks but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="33760-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33760-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="33760-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="33760-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33760-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="33760-115">Return value</span></span>

<span data-ttu-id="33760-116">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="33760-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="33760-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="33760-117">Requirements</span></span>



| <span data-ttu-id="33760-118">需求</span><span class="sxs-lookup"><span data-stu-id="33760-118">Requirement</span></span> | <span data-ttu-id="33760-119">值</span><span class="sxs-lookup"><span data-stu-id="33760-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33760-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33760-120">Minimum supported client</span></span><br/> | <span data-ttu-id="33760-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33760-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33760-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33760-122">Minimum supported server</span></span><br/> | <span data-ttu-id="33760-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33760-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33760-124">標頭</span><span class="sxs-lookup"><span data-stu-id="33760-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="33760-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="33760-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





