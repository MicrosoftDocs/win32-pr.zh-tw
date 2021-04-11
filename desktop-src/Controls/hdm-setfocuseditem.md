---
title: 'HDM_SETFOCUSEDITEM 訊息 (Commctrl .h) '
description: 將焦點設定為標題控制項中的指定專案。 明確地傳送此訊息，或使用標頭 \_ SetFocusedItem 宏。
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- HDM_SETFOCUSEDITEM message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_SETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd416744478248760f4e2c9f94a362db5a8d327
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105293"
---
# <a name="hdm_setfocuseditem-message"></a><span data-ttu-id="50b4d-105">HDM \_ SETFOCUSEDITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="50b4d-105">HDM\_SETFOCUSEDITEM message</span></span>

<span data-ttu-id="50b4d-106">將焦點設定為標題控制項中的指定專案。</span><span class="sxs-lookup"><span data-stu-id="50b4d-106">Sets the focus to a specified item in a header control.</span></span> <span data-ttu-id="50b4d-107">明確地傳送此訊息，或使用 [**標頭 \_ SetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) 宏。</span><span class="sxs-lookup"><span data-stu-id="50b4d-107">Send this message explicitly or by using the [**Header\_SetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="50b4d-108">參數</span><span class="sxs-lookup"><span data-stu-id="50b4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50b4d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50b4d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="50b4d-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="50b4d-110">Not used.</span></span> <span data-ttu-id="50b4d-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="50b4d-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="50b4d-112">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="50b4d-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50b4d-113">專案的索引。</span><span class="sxs-lookup"><span data-stu-id="50b4d-113">The index of item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50b4d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="50b4d-114">Return value</span></span>

<span data-ttu-id="50b4d-115">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="50b4d-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="50b4d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="50b4d-116">Requirements</span></span>



| <span data-ttu-id="50b4d-117">需求</span><span class="sxs-lookup"><span data-stu-id="50b4d-117">Requirement</span></span> | <span data-ttu-id="50b4d-118">值</span><span class="sxs-lookup"><span data-stu-id="50b4d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50b4d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50b4d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="50b4d-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50b4d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50b4d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50b4d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="50b4d-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50b4d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50b4d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="50b4d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="50b4d-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="50b4d-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50b4d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50b4d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b4d-126">關於標題控制項</span><span class="sxs-lookup"><span data-stu-id="50b4d-126">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





