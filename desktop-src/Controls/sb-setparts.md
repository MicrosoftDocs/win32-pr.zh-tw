---
title: 'SB_SETPARTS 訊息 (Commctrl .h) '
description: 設定狀態視窗中的部分數目，以及每個元件右邊緣的座標。
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- SB_SETPARTS message Windows 控制項
topic_type:
- apiref
api_name:
- SB_SETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 062058fa3778cd0394cadd9d76b363a0353ffb2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509015"
---
# <a name="sb_setparts-message"></a><span data-ttu-id="39c65-104">SB \_ SETPARTS 訊息</span><span class="sxs-lookup"><span data-stu-id="39c65-104">SB\_SETPARTS message</span></span>

<span data-ttu-id="39c65-105">設定狀態視窗中的部分數目，以及每個元件右邊緣的座標。</span><span class="sxs-lookup"><span data-stu-id="39c65-105">Sets the number of parts in a status window and the coordinate of the right edge of each part.</span></span>

## <a name="parameters"></a><span data-ttu-id="39c65-106">參數</span><span class="sxs-lookup"><span data-stu-id="39c65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39c65-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39c65-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39c65-108">要設定的部分數目 (不能大於 256) 。</span><span class="sxs-lookup"><span data-stu-id="39c65-108">Number of parts to set (cannot be greater than 256).</span></span>

</dd> <dt>

<span data-ttu-id="39c65-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39c65-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39c65-110">整數陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="39c65-110">Pointer to an integer array.</span></span> <span data-ttu-id="39c65-111">在 *wParam* 中指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="39c65-111">The number of elements is specified in *wParam*.</span></span> <span data-ttu-id="39c65-112">每個元素會指定相對應元件右邊緣的位置（以客戶座標為單位）。</span><span class="sxs-lookup"><span data-stu-id="39c65-112">Each element specifies the position, in client coordinates, of the right edge of the corresponding part.</span></span> <span data-ttu-id="39c65-113">如果元素為-1，對應元件的右邊緣會延伸至視窗的框線。</span><span class="sxs-lookup"><span data-stu-id="39c65-113">If an element is -1, the right edge of the corresponding part extends to the border of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39c65-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="39c65-114">Return value</span></span>

<span data-ttu-id="39c65-115">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="39c65-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="39c65-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="39c65-116">Requirements</span></span>



| <span data-ttu-id="39c65-117">需求</span><span class="sxs-lookup"><span data-stu-id="39c65-117">Requirement</span></span> | <span data-ttu-id="39c65-118">值</span><span class="sxs-lookup"><span data-stu-id="39c65-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39c65-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39c65-119">Minimum supported client</span></span><br/> | <span data-ttu-id="39c65-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39c65-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39c65-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39c65-121">Minimum supported server</span></span><br/> | <span data-ttu-id="39c65-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39c65-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39c65-123">標頭</span><span class="sxs-lookup"><span data-stu-id="39c65-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="39c65-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="39c65-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





