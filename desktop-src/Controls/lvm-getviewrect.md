---
title: 'LVM_GETVIEWRECT 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項中所有專案的周框。 清單視圖必須在圖示或小型圖示視圖中。 您可以明確地傳送此訊息，或使用 ListView \_ GetViewRect 宏來傳送。
ms.assetid: 69b96f86-8b7e-42c1-ad73-f9b2732ab9f9
keywords:
- LVM_GETVIEWRECT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d4c4fdf0e8466d3fb0b2ad164241c3f6a541570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025374"
---
# <a name="lvm_getviewrect-message"></a><span data-ttu-id="2b488-106">LVM \_ GETVIEWRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="2b488-106">LVM\_GETVIEWRECT message</span></span>

<span data-ttu-id="2b488-107">抓取清單視圖控制項中所有專案的周框。</span><span class="sxs-lookup"><span data-stu-id="2b488-107">Retrieves the bounding rectangle of all items in the list-view control.</span></span> <span data-ttu-id="2b488-108">清單視圖必須在圖示或小型圖示視圖中。</span><span class="sxs-lookup"><span data-stu-id="2b488-108">The list view must be in icon or small icon view.</span></span> <span data-ttu-id="2b488-109">您可以明確地傳送此訊息，或使用 [**ListView \_ GetViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="2b488-109">You can send this message explicitly or by using the [**ListView\_GetViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b488-110">參數</span><span class="sxs-lookup"><span data-stu-id="2b488-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b488-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b488-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2b488-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2b488-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2b488-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b488-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b488-114">接收周框 [**的矩形結構指標**](/previous-versions//dd162897(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="2b488-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span> <span data-ttu-id="2b488-115">所有座標都是相對於清單視圖控制項的可見區域。</span><span class="sxs-lookup"><span data-stu-id="2b488-115">All coordinates are relative to the visible area of the list-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b488-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b488-116">Return value</span></span>

<span data-ttu-id="2b488-117">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="2b488-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b488-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b488-118">Requirements</span></span>



| <span data-ttu-id="2b488-119">需求</span><span class="sxs-lookup"><span data-stu-id="2b488-119">Requirement</span></span> | <span data-ttu-id="2b488-120">值</span><span class="sxs-lookup"><span data-stu-id="2b488-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b488-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b488-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2b488-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b488-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2b488-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b488-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2b488-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b488-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b488-125">標頭</span><span class="sxs-lookup"><span data-stu-id="2b488-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b488-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b488-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

