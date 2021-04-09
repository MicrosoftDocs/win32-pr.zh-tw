---
title: 'TCM_SETCURSEL 訊息 (Commctrl .h) '
description: 在索引標籤控制項中選取索引標籤。 您可以使用 TabCtrl SetCurSel 宏明確地傳送此訊息 \_ 。
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- TCM_SETCURSEL message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90033c5a19b0eb7b73f9ed886e8dad8d1ca4c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934404"
---
# <a name="tcm_setcursel-message"></a><span data-ttu-id="33723-105">TCM \_ SETCURSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="33723-105">TCM\_SETCURSEL message</span></span>

<span data-ttu-id="33723-106">在索引標籤控制項中選取索引標籤。</span><span class="sxs-lookup"><span data-stu-id="33723-106">Selects a tab in a tab control.</span></span> <span data-ttu-id="33723-107">您可以使用 [**TabCtrl \_ SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="33723-107">You can send this message explicitly or by using the [**TabCtrl\_SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="33723-108">參數</span><span class="sxs-lookup"><span data-stu-id="33723-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33723-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33723-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33723-110">要選取之索引標籤的索引。</span><span class="sxs-lookup"><span data-stu-id="33723-110">Index of the tab to select.</span></span>

</dd> <dt>

<span data-ttu-id="33723-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33723-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="33723-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="33723-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33723-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="33723-113">Return value</span></span>

<span data-ttu-id="33723-114">如果成功，則傳回先前所選索引標籤的索引，否則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="33723-114">Returns the index of the previously selected tab if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="33723-115">備註</span><span class="sxs-lookup"><span data-stu-id="33723-115">Remarks</span></span>

<span data-ttu-id="33723-116">使用此訊息選取索引標籤時，不會傳送 [TCN \_ SELCHANGING](tcn-selchanging.md) 或 [TCN \_ SELCHANGE](tcn-selchange.md) 通知碼給索引標籤控制項。</span><span class="sxs-lookup"><span data-stu-id="33723-116">A tab control does not send a [TCN\_SELCHANGING](tcn-selchanging.md) or [TCN\_SELCHANGE](tcn-selchange.md) notification code when a tab is selected using this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="33723-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="33723-117">Requirements</span></span>



| <span data-ttu-id="33723-118">需求</span><span class="sxs-lookup"><span data-stu-id="33723-118">Requirement</span></span> | <span data-ttu-id="33723-119">值</span><span class="sxs-lookup"><span data-stu-id="33723-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33723-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33723-120">Minimum supported client</span></span><br/> | <span data-ttu-id="33723-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33723-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33723-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33723-122">Minimum supported server</span></span><br/> | <span data-ttu-id="33723-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33723-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33723-124">標頭</span><span class="sxs-lookup"><span data-stu-id="33723-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="33723-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="33723-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





