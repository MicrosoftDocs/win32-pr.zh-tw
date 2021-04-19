---
title: 'TVM_SETSCROLLTIME 訊息 (Commctrl .h) '
description: 設定樹狀檢視控制項的最大滾動時間。 您可以使用 TreeView SetScrollTime 宏明確地傳送此訊息 \_ 。
ms.assetid: b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a
keywords:
- TVM_SETSCROLLTIME message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b49fab2f662b5ec641d9ffc6cc276f2196d2613e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106984525"
---
# <a name="tvm_setscrolltime-message"></a><span data-ttu-id="ef549-105">TVM \_ SETSCROLLTIME 訊息</span><span class="sxs-lookup"><span data-stu-id="ef549-105">TVM\_SETSCROLLTIME message</span></span>

<span data-ttu-id="ef549-106">設定樹狀檢視控制項的最大滾動時間。</span><span class="sxs-lookup"><span data-stu-id="ef549-106">Sets the maximum scroll time for the tree-view control.</span></span> <span data-ttu-id="ef549-107">您可以使用 [**TreeView \_ SetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ef549-107">You can send this message explicitly or by using the [**TreeView\_SetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ef549-108">參數</span><span class="sxs-lookup"><span data-stu-id="ef549-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef549-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ef549-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef549-110">新的最大滾動時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ef549-110">New maximum scroll time, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="ef549-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef549-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ef549-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ef549-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef549-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef549-113">Return value</span></span>

<span data-ttu-id="ef549-114">傳回之前的最大滾動時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ef549-114">Returns the previous maximum scroll time, in milliseconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef549-115">備註</span><span class="sxs-lookup"><span data-stu-id="ef549-115">Remarks</span></span>

<span data-ttu-id="ef549-116">最長的滾動時間是捲軸操作可花費的最長時間量。</span><span class="sxs-lookup"><span data-stu-id="ef549-116">The maximum scroll time is the longest amount of time that a scroll operation can take.</span></span> <span data-ttu-id="ef549-117">將會調整滾動，讓捲軸在最大滾動時間內進行。</span><span class="sxs-lookup"><span data-stu-id="ef549-117">Scrolling will be adjusted so that the scroll will take place within the maximum scroll time.</span></span> <span data-ttu-id="ef549-118">捲軸操作的時間可能會比最大值少。</span><span class="sxs-lookup"><span data-stu-id="ef549-118">A scroll operation may take less time than the maximum.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef549-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef549-119">Requirements</span></span>



| <span data-ttu-id="ef549-120">需求</span><span class="sxs-lookup"><span data-stu-id="ef549-120">Requirement</span></span> | <span data-ttu-id="ef549-121">值</span><span class="sxs-lookup"><span data-stu-id="ef549-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef549-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef549-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ef549-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef549-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef549-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef549-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ef549-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef549-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef549-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ef549-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef549-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ef549-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef549-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef549-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef549-129">**TVM \_ GETSCROLLTIME**</span><span class="sxs-lookup"><span data-stu-id="ef549-129">**TVM\_GETSCROLLTIME**</span></span>](tvm-getscrolltime.md)
</dt> </dl>

 

 





