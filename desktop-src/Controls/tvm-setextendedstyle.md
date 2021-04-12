---
title: 'TVM_SETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 通知樹狀檢視控制項設定擴充樣式。 傳送此訊息或使用宏 TreeView \_ SetExtendedStyle。
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- TVM_SETEXTENDEDSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c450f72f85e40514c35f08284428feec4f7caf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508695"
---
# <a name="tvm_setextendedstyle-message"></a><span data-ttu-id="203ba-105">TVM \_ SETEXTENDEDSTYLE 訊息</span><span class="sxs-lookup"><span data-stu-id="203ba-105">TVM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="203ba-106">通知樹狀檢視控制項設定擴充樣式。</span><span class="sxs-lookup"><span data-stu-id="203ba-106">Informs the tree-view control to set extended styles.</span></span> <span data-ttu-id="203ba-107">傳送此訊息或使用宏 [**TreeView \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle)。</span><span class="sxs-lookup"><span data-stu-id="203ba-107">Send this message or use the macro [**TreeView\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).</span></span>

## <a name="parameters"></a><span data-ttu-id="203ba-108">參數</span><span class="sxs-lookup"><span data-stu-id="203ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="203ba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="203ba-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="203ba-110">用來選取要設定之樣式的遮罩。</span><span class="sxs-lookup"><span data-stu-id="203ba-110">Mask used to select the styles to be set.</span></span>

</dd> <dt>

<span data-ttu-id="203ba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="203ba-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="203ba-112">指出擴充樣式的值。</span><span class="sxs-lookup"><span data-stu-id="203ba-112">Value that indicates the extended style.</span></span> <span data-ttu-id="203ba-113">如需樣式的詳細資訊，請參閱 [樹狀檢視控制項擴充樣式](tree-view-control-window-extended-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="203ba-113">For more information on styles, see [Tree-View Control Extended Styles](tree-view-control-window-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="203ba-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="203ba-114">Return value</span></span>

<span data-ttu-id="203ba-115">如果此訊息成功，則會 **傳回 \_ [確定]**。</span><span class="sxs-lookup"><span data-stu-id="203ba-115">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="203ba-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="203ba-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="203ba-117">備註</span><span class="sxs-lookup"><span data-stu-id="203ba-117">Remarks</span></span>

<span data-ttu-id="203ba-118">樹狀檢視控制項的擴充樣式與函數 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 或函數 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)所使用的擴充樣式沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="203ba-118">The extended styles for a tree-view control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="203ba-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="203ba-119">Requirements</span></span>



| <span data-ttu-id="203ba-120">需求</span><span class="sxs-lookup"><span data-stu-id="203ba-120">Requirement</span></span> | <span data-ttu-id="203ba-121">值</span><span class="sxs-lookup"><span data-stu-id="203ba-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="203ba-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="203ba-122">Minimum supported client</span></span><br/> | <span data-ttu-id="203ba-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="203ba-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="203ba-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="203ba-124">Minimum supported server</span></span><br/> | <span data-ttu-id="203ba-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="203ba-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="203ba-126">標頭</span><span class="sxs-lookup"><span data-stu-id="203ba-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="203ba-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="203ba-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

