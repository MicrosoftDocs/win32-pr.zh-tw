---
title: 'TVM_GETSCROLLTIME 訊息 (Commctrl .h) '
description: 抓取樹狀檢視控制項的最大滾動時間。 您可以使用 TreeView GetScrollTime 宏明確地傳送此訊息 \_ 。
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- TVM_GETSCROLLTIME message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f0bacc6c12dd7f54f20d882faf738c11848d59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094159"
---
# <a name="tvm_getscrolltime-message"></a><span data-ttu-id="387d8-105">TVM \_ GETSCROLLTIME 訊息</span><span class="sxs-lookup"><span data-stu-id="387d8-105">TVM\_GETSCROLLTIME message</span></span>

<span data-ttu-id="387d8-106">抓取樹狀檢視控制項的最大滾動時間。</span><span class="sxs-lookup"><span data-stu-id="387d8-106">Retrieves the maximum scroll time for the tree-view control.</span></span> <span data-ttu-id="387d8-107">您可以使用 [**TreeView \_ GetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="387d8-107">You can send this message explicitly or by using the [**TreeView\_GetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="387d8-108">參數</span><span class="sxs-lookup"><span data-stu-id="387d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="387d8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="387d8-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="387d8-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="387d8-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="387d8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="387d8-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="387d8-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="387d8-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="387d8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="387d8-113">Return value</span></span>

<span data-ttu-id="387d8-114">傳回最大滾動時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="387d8-114">Returns the maximum scroll time, in milliseconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="387d8-115">備註</span><span class="sxs-lookup"><span data-stu-id="387d8-115">Remarks</span></span>

<span data-ttu-id="387d8-116">最長的滾動時間是捲軸操作可花費的最長時間量。</span><span class="sxs-lookup"><span data-stu-id="387d8-116">The maximum scroll time is the longest amount of time that a scroll operation can take.</span></span> <span data-ttu-id="387d8-117">將會調整滾動，讓捲軸在最大滾動時間內進行。</span><span class="sxs-lookup"><span data-stu-id="387d8-117">The scrolling will be adjusted so that the scroll will take place within the maximum scroll time.</span></span> <span data-ttu-id="387d8-118">捲軸操作的時間可能會比最大值少。</span><span class="sxs-lookup"><span data-stu-id="387d8-118">A scroll operation may take less time than the maximum.</span></span>

## <a name="requirements"></a><span data-ttu-id="387d8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="387d8-119">Requirements</span></span>



| <span data-ttu-id="387d8-120">需求</span><span class="sxs-lookup"><span data-stu-id="387d8-120">Requirement</span></span> | <span data-ttu-id="387d8-121">值</span><span class="sxs-lookup"><span data-stu-id="387d8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="387d8-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="387d8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="387d8-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="387d8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="387d8-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="387d8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="387d8-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="387d8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="387d8-126">標頭</span><span class="sxs-lookup"><span data-stu-id="387d8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="387d8-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="387d8-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="387d8-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="387d8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="387d8-129">**TVM \_ SETSCROLLTIME**</span><span class="sxs-lookup"><span data-stu-id="387d8-129">**TVM\_SETSCROLLTIME**</span></span>](tvm-setscrolltime.md)
</dt> </dl>

 

 





