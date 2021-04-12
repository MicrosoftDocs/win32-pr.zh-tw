---
title: 'LVM_SETTOOLTIPS 訊息 (Commctrl .h) '
description: 設定 [清單視圖] 控制項將用來顯示工具提示的工具提示控制項。 您可以明確地傳送此訊息，或使用 ListView \_ SetToolTips 宏。
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- LVM_SETTOOLTIPS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff749c24a35cf73de2d75b8a3b516197b57aac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464880"
---
# <a name="lvm_settooltips-message"></a><span data-ttu-id="516f0-105">LVM \_ SETTOOLTIPS 訊息</span><span class="sxs-lookup"><span data-stu-id="516f0-105">LVM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="516f0-106">設定 [清單視圖] 控制項將用來顯示工具提示的工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="516f0-106">Sets the tooltip control that the list-view control will use to display tooltips.</span></span> <span data-ttu-id="516f0-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) 宏。</span><span class="sxs-lookup"><span data-stu-id="516f0-107">You can send this message explicitly or use the [**ListView\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="516f0-108">參數</span><span class="sxs-lookup"><span data-stu-id="516f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="516f0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="516f0-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="516f0-110">要設定之工具提示控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="516f0-110">Handle to the tooltip control to be set.</span></span></dd> <dt>

<span data-ttu-id="516f0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="516f0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="516f0-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="516f0-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="516f0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="516f0-113">Return value</span></span>

<span data-ttu-id="516f0-114">將控制碼傳回至先前的工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="516f0-114">Returns the handle to the previous tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="516f0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="516f0-115">Requirements</span></span>



| <span data-ttu-id="516f0-116">需求</span><span class="sxs-lookup"><span data-stu-id="516f0-116">Requirement</span></span> | <span data-ttu-id="516f0-117">值</span><span class="sxs-lookup"><span data-stu-id="516f0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="516f0-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="516f0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="516f0-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="516f0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="516f0-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="516f0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="516f0-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="516f0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="516f0-122">標頭</span><span class="sxs-lookup"><span data-stu-id="516f0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="516f0-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="516f0-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="516f0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="516f0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="516f0-125">**LVM \_ GETTOOLTIPS**</span><span class="sxs-lookup"><span data-stu-id="516f0-125">**LVM\_GETTOOLTIPS**</span></span>](lvm-gettooltips.md)
</dt> </dl>

 

 





