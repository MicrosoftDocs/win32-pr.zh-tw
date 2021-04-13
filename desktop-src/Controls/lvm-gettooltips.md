---
title: 'LVM_GETTOOLTIPS 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項用來顯示工具提示的工具提示控制項。 您可以明確地傳送此訊息，或使用 ListView \_ GetToolTips 宏。
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- LVM_GETTOOLTIPS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f409c85ed6157e8cfc837e5efa3a68488aec504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466504"
---
# <a name="lvm_gettooltips-message"></a><span data-ttu-id="22328-105">LVM \_ GETTOOLTIPS 訊息</span><span class="sxs-lookup"><span data-stu-id="22328-105">LVM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="22328-106">抓取清單視圖控制項用來顯示工具提示的工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="22328-106">Retrieves the tooltip control that the list-view control uses to display tooltips.</span></span> <span data-ttu-id="22328-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) 宏。</span><span class="sxs-lookup"><span data-stu-id="22328-107">You can send this message explicitly or use the [**ListView\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="22328-108">參數</span><span class="sxs-lookup"><span data-stu-id="22328-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22328-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22328-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="22328-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="22328-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="22328-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22328-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="22328-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="22328-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22328-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="22328-113">Return value</span></span>

<span data-ttu-id="22328-114">傳回工具提示控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="22328-114">Returns the handle of the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="22328-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="22328-115">Requirements</span></span>



| <span data-ttu-id="22328-116">需求</span><span class="sxs-lookup"><span data-stu-id="22328-116">Requirement</span></span> | <span data-ttu-id="22328-117">值</span><span class="sxs-lookup"><span data-stu-id="22328-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22328-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22328-118">Minimum supported client</span></span><br/> | <span data-ttu-id="22328-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22328-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="22328-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="22328-120">Minimum supported server</span></span><br/> | <span data-ttu-id="22328-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22328-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="22328-122">標頭</span><span class="sxs-lookup"><span data-stu-id="22328-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="22328-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="22328-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22328-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22328-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22328-125">**LVM \_ SETTOOLTIPS**</span><span class="sxs-lookup"><span data-stu-id="22328-125">**LVM\_SETTOOLTIPS**</span></span>](lvm-settooltips.md)
</dt> </dl>

 

 





