---
title: 'TTM_TRACKPOSITION 訊息 (Commctrl .h) '
description: 設定追蹤工具提示的位置。
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- TTM_TRACKPOSITION message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_TRACKPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6eab8184049d8bf876a7e782b9adc2091d5fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025247"
---
# <a name="ttm_trackposition-message"></a><span data-ttu-id="cc550-104">TTM \_ TRACKPOSITION 訊息</span><span class="sxs-lookup"><span data-stu-id="cc550-104">TTM\_TRACKPOSITION message</span></span>

<span data-ttu-id="cc550-105">設定追蹤工具提示的位置。</span><span class="sxs-lookup"><span data-stu-id="cc550-105">Sets the position of a tracking tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="cc550-106">參數</span><span class="sxs-lookup"><span data-stu-id="cc550-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc550-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc550-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc550-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="cc550-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cc550-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc550-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc550-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定要顯示追蹤工具提示之點的 x 座標（以螢幕座標表示）。</span><span class="sxs-lookup"><span data-stu-id="cc550-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the x-coordinate of the point at which the tracking tooltip will be displayed, in screen coordinates.</span></span> <span data-ttu-id="cc550-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定顯示追蹤工具提示的點 y 座標（以螢幕座標表示）。</span><span class="sxs-lookup"><span data-stu-id="cc550-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the y-coordinate of the point at which the tracking tooltip will be displayed, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc550-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="cc550-112">Return value</span></span>

<span data-ttu-id="cc550-113">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="cc550-113">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc550-114">備註</span><span class="sxs-lookup"><span data-stu-id="cc550-114">Remarks</span></span>

<span data-ttu-id="cc550-115">工具提示控制項會根據您在此訊息中提供的座標，選擇要顯示工具提示視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="cc550-115">The tooltip control chooses where to display the tooltip window based on the coordinates you provide with this message.</span></span> <span data-ttu-id="cc550-116">這會導致工具提示視窗顯示在其所對應的工具旁邊。</span><span class="sxs-lookup"><span data-stu-id="cc550-116">This causes the tooltip window to appear beside the tool to which it corresponds.</span></span> <span data-ttu-id="cc550-117">若要在特定座標顯示工具提示視窗，加入 \_ 工具時，請在 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **UFLAGS** 成員中包含 TTF 絕對旗標。</span><span class="sxs-lookup"><span data-stu-id="cc550-117">To have tooltip windows displayed at specific coordinates, include the TTF\_ABSOLUTE flag in the **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure when adding the tool.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc550-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc550-118">Requirements</span></span>



| <span data-ttu-id="cc550-119">需求</span><span class="sxs-lookup"><span data-stu-id="cc550-119">Requirement</span></span> | <span data-ttu-id="cc550-120">值</span><span class="sxs-lookup"><span data-stu-id="cc550-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc550-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc550-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cc550-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc550-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc550-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc550-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cc550-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc550-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc550-125">標頭</span><span class="sxs-lookup"><span data-stu-id="cc550-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc550-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cc550-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc550-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc550-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="cc550-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="cc550-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cc550-129">**TTM \_ TRACKACTI加值稅E**</span><span class="sxs-lookup"><span data-stu-id="cc550-129">**TTM\_TRACKACTIVATE**</span></span>](ttm-trackactivate.md)
</dt> <dt>

<span data-ttu-id="cc550-130">**概念**</span><span class="sxs-lookup"><span data-stu-id="cc550-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cc550-131">使用工具提示控制項</span><span class="sxs-lookup"><span data-stu-id="cc550-131">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

