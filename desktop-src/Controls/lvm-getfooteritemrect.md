---
title: 'LVM_GETFOOTERITEMRECT 訊息 (Commctrl .h) '
description: 取得清單視圖控制項中指定專案之頁尾的座標。 明確地傳送此訊息，或使用 ListView \_ GetFooterItemRect 宏。
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- LVM_GETFOOTERITEMRECT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142cb92806fa1d58faa0414c10c41bd2815d5b6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187271"
---
# <a name="lvm_getfooteritemrect-message"></a><span data-ttu-id="c2a0c-105">LVM \_ GETFOOTERITEMRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="c2a0c-105">LVM\_GETFOOTERITEMRECT message</span></span>

<span data-ttu-id="c2a0c-106">取得清單視圖控制項中指定專案之頁尾的座標。</span><span class="sxs-lookup"><span data-stu-id="c2a0c-106">Gets the coordinates of a footer for a specified item in a list-view control.</span></span> <span data-ttu-id="c2a0c-107">明確地傳送此訊息，或使用 [**ListView \_ GetFooterItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) 宏。</span><span class="sxs-lookup"><span data-stu-id="c2a0c-107">Send this message explicitly or by using the [**ListView\_GetFooterItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2a0c-108">參數</span><span class="sxs-lookup"><span data-stu-id="c2a0c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2a0c-109">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2a0c-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2a0c-110">清單視圖控制項中專案的索引。</span><span class="sxs-lookup"><span data-stu-id="c2a0c-110">The index of the item in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="c2a0c-111">*lParam* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c2a0c-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2a0c-112">要接收座標的 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="c2a0c-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="c2a0c-113">呼叫應用程式負責配置此結構。</span><span class="sxs-lookup"><span data-stu-id="c2a0c-113">The calling application is responsible for allocating this structure.</span></span> <span data-ttu-id="c2a0c-114">收到的座標會以用戶端座標表示。</span><span class="sxs-lookup"><span data-stu-id="c2a0c-114">The coordinates received are expressed as client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2a0c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2a0c-115">Return value</span></span>

<span data-ttu-id="c2a0c-116">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c2a0c-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2a0c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2a0c-117">Requirements</span></span>



| <span data-ttu-id="c2a0c-118">需求</span><span class="sxs-lookup"><span data-stu-id="c2a0c-118">Requirement</span></span> | <span data-ttu-id="c2a0c-119">值</span><span class="sxs-lookup"><span data-stu-id="c2a0c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a0c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2a0c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a0c-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2a0c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2a0c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2a0c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a0c-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2a0c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2a0c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c2a0c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2a0c-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c2a0c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

