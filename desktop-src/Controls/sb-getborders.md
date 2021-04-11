---
title: 'SB_GETBORDERS 訊息 (Commctrl .h) '
description: 抓取狀態視窗水準和垂直框線的目前寬度。
ms.assetid: 120c1e0d-6f42-424e-94e0-a080d216d39d
keywords:
- SB_GETBORDERS message Windows 控制項
topic_type:
- apiref
api_name:
- SB_GETBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854df2cd367a852a2e6a0e638b470187efabe58c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105083"
---
# <a name="sb_getborders-message"></a><span data-ttu-id="0e928-104">SB \_ GETBORDERS 訊息</span><span class="sxs-lookup"><span data-stu-id="0e928-104">SB\_GETBORDERS message</span></span>

<span data-ttu-id="0e928-105">抓取狀態視窗水準和垂直框線的目前寬度。</span><span class="sxs-lookup"><span data-stu-id="0e928-105">Retrieves the current widths of the horizontal and vertical borders of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e928-106">參數</span><span class="sxs-lookup"><span data-stu-id="0e928-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e928-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e928-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0e928-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0e928-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0e928-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e928-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e928-110">具有三個元素之整數陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="0e928-110">Pointer to an integer array that has three elements.</span></span> <span data-ttu-id="0e928-111">第一個元素會接收水準框線的寬度，第二個會接收垂直框線的寬度，而第三個專案會接收矩形之間的框線寬度。</span><span class="sxs-lookup"><span data-stu-id="0e928-111">The first element receives the width of the horizontal border, the second receives the width of the vertical border, and the third receives the width of the border between rectangles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e928-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e928-112">Return value</span></span>

<span data-ttu-id="0e928-113">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="0e928-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e928-114">備註</span><span class="sxs-lookup"><span data-stu-id="0e928-114">Remarks</span></span>

<span data-ttu-id="0e928-115">框線會決定視窗外緣和包含文字之視窗內的矩形之間的間距。</span><span class="sxs-lookup"><span data-stu-id="0e928-115">The borders determine the spacing between the outside edge of the window and the rectangles within the window that contain text.</span></span> <span data-ttu-id="0e928-116">框線也會決定矩形之間的間距。</span><span class="sxs-lookup"><span data-stu-id="0e928-116">The borders also determine the spacing between rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e928-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e928-117">Requirements</span></span>



| <span data-ttu-id="0e928-118">需求</span><span class="sxs-lookup"><span data-stu-id="0e928-118">Requirement</span></span> | <span data-ttu-id="0e928-119">值</span><span class="sxs-lookup"><span data-stu-id="0e928-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e928-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e928-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0e928-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e928-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e928-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e928-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0e928-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e928-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e928-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0e928-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e928-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0e928-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





