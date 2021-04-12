---
title: 'SB_GETPARTS 訊息 (Commctrl .h) '
description: 捕獲狀態視窗中的部分計數。 此訊息也會抓取指定之部分數目的右邊緣座標。
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- SB_GETPARTS message Windows 控制項
topic_type:
- apiref
api_name:
- SB_GETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee0f33331c579490cf66a38b9ce6655215ae673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509020"
---
# <a name="sb_getparts-message"></a><span data-ttu-id="60005-105">SB \_ GETPARTS 訊息</span><span class="sxs-lookup"><span data-stu-id="60005-105">SB\_GETPARTS message</span></span>

<span data-ttu-id="60005-106">捕獲狀態視窗中的部分計數。</span><span class="sxs-lookup"><span data-stu-id="60005-106">Retrieves a count of the parts in a status window.</span></span> <span data-ttu-id="60005-107">此訊息也會抓取指定之部分數目的右邊緣座標。</span><span class="sxs-lookup"><span data-stu-id="60005-107">The message also retrieves the coordinate of the right edge of the specified number of parts.</span></span>

## <a name="parameters"></a><span data-ttu-id="60005-108">參數</span><span class="sxs-lookup"><span data-stu-id="60005-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60005-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="60005-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60005-110">要抓取座標的部分數目。</span><span class="sxs-lookup"><span data-stu-id="60005-110">Number of parts for which to retrieve coordinates.</span></span> <span data-ttu-id="60005-111">如果此參數大於視窗中的部分數目，則訊息只會抓取現有元件的座標。</span><span class="sxs-lookup"><span data-stu-id="60005-111">If this parameter is greater than the number of parts in the window, the message retrieves coordinates for existing parts only.</span></span>

</dd> <dt>

<span data-ttu-id="60005-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60005-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60005-113">整數陣列的指標，該陣列與 *wParam* 所指定的元件具有相同的專案數。</span><span class="sxs-lookup"><span data-stu-id="60005-113">Pointer to an integer array that has the same number of elements as parts specified by *wParam*.</span></span> <span data-ttu-id="60005-114">陣列中的每個元素都會接收相對應元件右邊緣的用戶端座標。</span><span class="sxs-lookup"><span data-stu-id="60005-114">Each element in the array receives the client coordinate of the right edge of the corresponding part.</span></span> <span data-ttu-id="60005-115">如果元素設定為-1，則該部分的右邊緣位置會延伸至視窗的右邊緣。</span><span class="sxs-lookup"><span data-stu-id="60005-115">If an element is set to -1, the position of the right edge for that part extends to the right edge of the window.</span></span> <span data-ttu-id="60005-116">若要取出目前的部分數目，請將此參數設定為零。</span><span class="sxs-lookup"><span data-stu-id="60005-116">To retrieve the current number of parts, set this parameter to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60005-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="60005-117">Return value</span></span>

<span data-ttu-id="60005-118">傳回視窗中的部分數目。</span><span class="sxs-lookup"><span data-stu-id="60005-118">Returns the number of parts in the window.</span></span>

## <a name="remarks"></a><span data-ttu-id="60005-119">備註</span><span class="sxs-lookup"><span data-stu-id="60005-119">Remarks</span></span>

<span data-ttu-id="60005-120">此訊息一律會傳回狀態列中的部分數目。</span><span class="sxs-lookup"><span data-stu-id="60005-120">This message always returns the number of parts in the status bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="60005-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="60005-121">Requirements</span></span>



| <span data-ttu-id="60005-122">需求</span><span class="sxs-lookup"><span data-stu-id="60005-122">Requirement</span></span> | <span data-ttu-id="60005-123">值</span><span class="sxs-lookup"><span data-stu-id="60005-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60005-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60005-124">Minimum supported client</span></span><br/> | <span data-ttu-id="60005-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60005-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="60005-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60005-126">Minimum supported server</span></span><br/> | <span data-ttu-id="60005-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60005-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="60005-128">標頭</span><span class="sxs-lookup"><span data-stu-id="60005-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="60005-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="60005-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





