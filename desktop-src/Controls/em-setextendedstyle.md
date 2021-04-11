---
title: 'EM_SETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 通知編輯控制項設定擴充樣式。 傳送此訊息或使用巨集編輯 \_ SetExtendedStyle。
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- EM_SETEXTENDEDSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 560b675927b4497810b8d492fd89b5765aa5a2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105570"
---
# <a name="em_setextendedstyle-message"></a><span data-ttu-id="88bb4-105">EM \_ SETEXTENDEDSTYLE 訊息</span><span class="sxs-lookup"><span data-stu-id="88bb4-105">EM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="88bb4-106">通知編輯控制項設定擴充樣式。</span><span class="sxs-lookup"><span data-stu-id="88bb4-106">Informs the edit control to set extended styles.</span></span> <span data-ttu-id="88bb4-107">傳送此訊息或使用宏 [**編輯 \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle)。</span><span class="sxs-lookup"><span data-stu-id="88bb4-107">Send this message or use the macro [**Edit\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).</span></span>

## <a name="parameters"></a><span data-ttu-id="88bb4-108">參數</span><span class="sxs-lookup"><span data-stu-id="88bb4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88bb4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="88bb4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88bb4-110">用來選取要設定之樣式的遮罩。</span><span class="sxs-lookup"><span data-stu-id="88bb4-110">Mask used to select the styles to be set.</span></span>

</dd> <dt>

<span data-ttu-id="88bb4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88bb4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88bb4-112">指出擴充樣式的值。</span><span class="sxs-lookup"><span data-stu-id="88bb4-112">Value that indicates the extended style.</span></span> <span data-ttu-id="88bb4-113">如需樣式的詳細資訊，請參閱 [編輯控制項延伸樣式](edit-control-window-extended-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="88bb4-113">For more information on styles, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88bb4-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="88bb4-114">Return value</span></span>

<span data-ttu-id="88bb4-115">如果此訊息成功，則會 **傳回 \_ [確定]**。</span><span class="sxs-lookup"><span data-stu-id="88bb4-115">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88bb4-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="88bb4-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="88bb4-117">備註</span><span class="sxs-lookup"><span data-stu-id="88bb4-117">Remarks</span></span>

<span data-ttu-id="88bb4-118">編輯控制項的擴充樣式與函數 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 或函數 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)所使用的擴充樣式沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="88bb4-118">The extended styles for an edit control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="88bb4-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="88bb4-119">Requirements</span></span>



| <span data-ttu-id="88bb4-120">需求</span><span class="sxs-lookup"><span data-stu-id="88bb4-120">Requirement</span></span> | <span data-ttu-id="88bb4-121">值</span><span class="sxs-lookup"><span data-stu-id="88bb4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88bb4-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88bb4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="88bb4-123">\[僅 Windows 10 版本1809桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88bb4-123">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="88bb4-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88bb4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="88bb4-125">僅限 Windows Server 2019 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88bb4-125">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="88bb4-126">標頭</span><span class="sxs-lookup"><span data-stu-id="88bb4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="88bb4-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="88bb4-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

