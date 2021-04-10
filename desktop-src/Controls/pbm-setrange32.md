---
title: 'PBM_SETRANGE32 訊息 (Commctrl .h) '
description: 將進度列的最小值和最大值設定為32位值，並重新繪製橫條以反映新的範圍。
ms.assetid: 7958ea14-17b4-4c0e-97ec-b09fa0d36e8b
keywords:
- PBM_SETRANGE32 message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_SETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55fcf91c794ec9ae3880d67f8df947f87fec413d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686165"
---
# <a name="pbm_setrange32-message"></a><span data-ttu-id="9762f-104">PBM \_ SETRANGE32 訊息</span><span class="sxs-lookup"><span data-stu-id="9762f-104">PBM\_SETRANGE32 message</span></span>

<span data-ttu-id="9762f-105">將進度列的最小值和最大值設定為32位值，並重新繪製橫條以反映新的範圍。</span><span class="sxs-lookup"><span data-stu-id="9762f-105">Sets the minimum and maximum values for a progress bar to 32-bit values, and redraws the bar to reflect the new range.</span></span>

## <a name="parameters"></a><span data-ttu-id="9762f-106">參數</span><span class="sxs-lookup"><span data-stu-id="9762f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9762f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9762f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9762f-108">最小範圍值。</span><span class="sxs-lookup"><span data-stu-id="9762f-108">Minimum range value.</span></span> <span data-ttu-id="9762f-109">根據預設，最小值為零。</span><span class="sxs-lookup"><span data-stu-id="9762f-109">By default, the minimum value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="9762f-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9762f-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9762f-111">最大範圍值。</span><span class="sxs-lookup"><span data-stu-id="9762f-111">Maximum range value.</span></span> <span data-ttu-id="9762f-112">此值必須大於 *wParam*。</span><span class="sxs-lookup"><span data-stu-id="9762f-112">This value must be greater than *wParam*.</span></span> <span data-ttu-id="9762f-113">根據預設，最大值為100。</span><span class="sxs-lookup"><span data-stu-id="9762f-113">By default, the maximum value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9762f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9762f-114">Return value</span></span>

<span data-ttu-id="9762f-115">傳回 **DWORD** 值，此值會在其 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 中保留先前的16位低限制，並在其 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))中保留先前的16位高限制。</span><span class="sxs-lookup"><span data-stu-id="9762f-115">Returns a **DWORD** value that holds the previous 16-bit low limit in its [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the previous 16-bit high limit in its [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="9762f-116">如果先前的範圍是32位的值，則傳回值是由兩個32位限制的 **LOWORD** 所組成。</span><span class="sxs-lookup"><span data-stu-id="9762f-116">If the previous ranges were 32-bit values, the return value consists of the **LOWORD** s of both 32-bit limits.</span></span>

## <a name="remarks"></a><span data-ttu-id="9762f-117">備註</span><span class="sxs-lookup"><span data-stu-id="9762f-117">Remarks</span></span>

<span data-ttu-id="9762f-118">若要取出整個最高和最低的32位值，請使用 [**PBM \_ GETRANGE**](pbm-getrange.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="9762f-118">To retrieve the entire high and low 32-bit values, use the [**PBM\_GETRANGE**](pbm-getrange.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9762f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9762f-119">Requirements</span></span>



| <span data-ttu-id="9762f-120">需求</span><span class="sxs-lookup"><span data-stu-id="9762f-120">Requirement</span></span> | <span data-ttu-id="9762f-121">值</span><span class="sxs-lookup"><span data-stu-id="9762f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9762f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9762f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9762f-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9762f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9762f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9762f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9762f-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9762f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9762f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="9762f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9762f-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9762f-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

