---
title: 'HDM_GETFOCUSEDITEM 訊息 (Commctrl .h) '
description: 取得標題控制項中具有焦點的專案。 明確地傳送此訊息，或使用標頭 \_ GetFocusedItem 宏。
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- HDM_GETFOCUSEDITEM message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c21fcb29f5f431e32ca3f07265b7e96620d5a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465888"
---
# <a name="hdm_getfocuseditem-message"></a><span data-ttu-id="243b0-105">HDM \_ GETFOCUSEDITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="243b0-105">HDM\_GETFOCUSEDITEM message</span></span>

<span data-ttu-id="243b0-106">取得標題控制項中具有焦點的專案。</span><span class="sxs-lookup"><span data-stu-id="243b0-106">Gets the item in a header control that has the focus.</span></span> <span data-ttu-id="243b0-107">明確地傳送此訊息，或使用 [**標頭 \_ GetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) 宏。</span><span class="sxs-lookup"><span data-stu-id="243b0-107">Send this message explicitly or by using the [**Header\_GetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="243b0-108">參數</span><span class="sxs-lookup"><span data-stu-id="243b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="243b0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="243b0-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="243b0-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="243b0-110">Not used.</span></span> <span data-ttu-id="243b0-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="243b0-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="243b0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="243b0-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="243b0-113">未使用。</span><span class="sxs-lookup"><span data-stu-id="243b0-113">Not used.</span></span> <span data-ttu-id="243b0-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="243b0-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="243b0-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="243b0-115">Return value</span></span>

<span data-ttu-id="243b0-116">傳回焦點專案的索引。</span><span class="sxs-lookup"><span data-stu-id="243b0-116">Returns the index of the item in focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="243b0-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="243b0-117">Requirements</span></span>



| <span data-ttu-id="243b0-118">需求</span><span class="sxs-lookup"><span data-stu-id="243b0-118">Requirement</span></span> | <span data-ttu-id="243b0-119">值</span><span class="sxs-lookup"><span data-stu-id="243b0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="243b0-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="243b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="243b0-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="243b0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="243b0-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="243b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="243b0-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="243b0-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="243b0-124">標頭</span><span class="sxs-lookup"><span data-stu-id="243b0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="243b0-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="243b0-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="243b0-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="243b0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="243b0-127">關於標題控制項</span><span class="sxs-lookup"><span data-stu-id="243b0-127">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





