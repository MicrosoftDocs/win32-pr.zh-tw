---
title: 'TCM_HIGHLIGHTITEM 訊息 (Commctrl .h) '
description: 設定索引標籤專案的醒目提示狀態。 您可以使用 TabCtrl HighlightItem 宏明確地傳送此訊息 \_ 。
ms.assetid: b0d0850a-62d9-46a1-8846-81f67a886ea8
keywords:
- TCM_HIGHLIGHTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_HIGHLIGHTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55664aeeeefadfcb5205b9a5bde4fee1aafdfef3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844172"
---
# <a name="tcm_highlightitem-message"></a><span data-ttu-id="64053-105">TCM \_ HIGHLIGHTITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="64053-105">TCM\_HIGHLIGHTITEM message</span></span>

<span data-ttu-id="64053-106">設定索引標籤專案的醒目提示狀態。</span><span class="sxs-lookup"><span data-stu-id="64053-106">Sets the highlight state of a tab item.</span></span> <span data-ttu-id="64053-107">您可以使用 [**TabCtrl \_ HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="64053-107">You can send this message explicitly or by using the [**TabCtrl\_HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="64053-108">參數</span><span class="sxs-lookup"><span data-stu-id="64053-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64053-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64053-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64053-110">**INT** 值，指定索引標籤控制項專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="64053-110">An **INT** value that specifies the zero-based index of a tab control item.</span></span>

</dd> <dt>

<span data-ttu-id="64053-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64053-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64053-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 **布林** 值，指定要設定的醒目提示狀態。</span><span class="sxs-lookup"><span data-stu-id="64053-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** specifying the highlight state to be set.</span></span> <span data-ttu-id="64053-113">如果這個值為 **TRUE**，則會反白顯示索引標籤;如果 **為 FALSE**，則索引標籤會設定為其預設狀態。</span><span class="sxs-lookup"><span data-stu-id="64053-113">If this value is **TRUE**, the tab is highlighted; if **FALSE**, the tab is set to its default state.</span></span> <span data-ttu-id="64053-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))必須為零。</span><span class="sxs-lookup"><span data-stu-id="64053-114">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64053-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="64053-115">Return value</span></span>

<span data-ttu-id="64053-116">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="64053-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="64053-117">備註</span><span class="sxs-lookup"><span data-stu-id="64053-117">Remarks</span></span>

<span data-ttu-id="64053-118">在 Comctl32.dll 6.0 版中，當主題為作用中時，此訊息沒有任何可見效果。</span><span class="sxs-lookup"><span data-stu-id="64053-118">In Comctl32.dll version 6.0, this message has no visible effect when a theme is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="64053-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="64053-119">Requirements</span></span>



| <span data-ttu-id="64053-120">需求</span><span class="sxs-lookup"><span data-stu-id="64053-120">Requirement</span></span> | <span data-ttu-id="64053-121">值</span><span class="sxs-lookup"><span data-stu-id="64053-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64053-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64053-122">Minimum supported client</span></span><br/> | <span data-ttu-id="64053-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64053-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="64053-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64053-124">Minimum supported server</span></span><br/> | <span data-ttu-id="64053-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64053-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="64053-126">標頭</span><span class="sxs-lookup"><span data-stu-id="64053-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="64053-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="64053-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

