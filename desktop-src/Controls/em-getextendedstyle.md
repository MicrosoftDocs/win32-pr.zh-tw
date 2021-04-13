---
title: 'EM_GETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 抓取編輯控制項的延伸樣式。 明確地傳送此訊息，或使用 Edit \_ GetExtendedStyle 宏。
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETEXTENDEDSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 37dc117bccd57b51098a7ca8c19e8b178037bef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466112"
---
# <a name="em_getextendedstyle-message-commctrlh"></a><span data-ttu-id="7fea5-105">EM_GETEXTENDEDSTYLE 訊息 (Commctrl .h) </span><span class="sxs-lookup"><span data-stu-id="7fea5-105">EM_GETEXTENDEDSTYLE message (Commctrl.h)</span></span>

<span data-ttu-id="7fea5-106">抓取樹狀檢視控制項的延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="7fea5-106">Retrieves the extended style for a tree-view control.</span></span> <span data-ttu-id="7fea5-107">明確地傳送此訊息，或使用 [**Edit \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) 宏。</span><span class="sxs-lookup"><span data-stu-id="7fea5-107">Send this message explicitly or by using the [**Edit\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7fea5-108">參數</span><span class="sxs-lookup"><span data-stu-id="7fea5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fea5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7fea5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7fea5-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="7fea5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7fea5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fea5-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7fea5-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="7fea5-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fea5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7fea5-113">Return value</span></span>

<span data-ttu-id="7fea5-114">傳回擴充樣式的值。如需樣式的詳細資訊，請參閱 [編輯控制項延伸樣式](edit-control-window-extended-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="7fea5-114">Returns the value of extended style.For more information on styles, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7fea5-115">備註</span><span class="sxs-lookup"><span data-stu-id="7fea5-115">Remarks</span></span>

<span data-ttu-id="7fea5-116">編輯控制項的擴充樣式與函數 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 或函數 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)所使用的擴充樣式沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="7fea5-116">The extended styles for an edit control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fea5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fea5-117">Requirements</span></span>



| <span data-ttu-id="7fea5-118">需求</span><span class="sxs-lookup"><span data-stu-id="7fea5-118">Requirement</span></span> | <span data-ttu-id="7fea5-119">值</span><span class="sxs-lookup"><span data-stu-id="7fea5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fea5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7fea5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7fea5-121">\[僅 Windows 10 版本1809桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fea5-121">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7fea5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7fea5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7fea5-123">僅限 Windows Server 2019 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fea5-123">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7fea5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="7fea5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fea5-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7fea5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

