---
title: 'TCM_GETCURFOCUS 訊息 (Commctrl .h) '
description: 傳回在索引標籤控制項中具有焦點之專案的索引。 您可以使用 TabCtrl GetCurFocus 宏明確地傳送此訊息 \_ 。
ms.assetid: ae6ee159-c769-41d6-b0bb-2a9ade4c0e71
keywords:
- TCM_GETCURFOCUS message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0d0f3d2bbd4a7cf0ab2a63c5a988f60768eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934948"
---
# <a name="tcm_getcurfocus-message"></a><span data-ttu-id="3634c-105">TCM \_ GETCURFOCUS 訊息</span><span class="sxs-lookup"><span data-stu-id="3634c-105">TCM\_GETCURFOCUS message</span></span>

<span data-ttu-id="3634c-106">傳回在索引標籤控制項中具有焦點之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="3634c-106">Returns the index of the item that has the focus in a tab control.</span></span> <span data-ttu-id="3634c-107">您可以使用 [**TabCtrl \_ GetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="3634c-107">You can send this message explicitly or by using the [**TabCtrl\_GetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3634c-108">參數</span><span class="sxs-lookup"><span data-stu-id="3634c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3634c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3634c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3634c-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3634c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3634c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3634c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3634c-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3634c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3634c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3634c-113">Return value</span></span>

<span data-ttu-id="3634c-114">傳回具有焦點之索引標籤專案的索引。</span><span class="sxs-lookup"><span data-stu-id="3634c-114">Returns the index of the tab item that has the focus.</span></span>

## <a name="remarks"></a><span data-ttu-id="3634c-115">備註</span><span class="sxs-lookup"><span data-stu-id="3634c-115">Remarks</span></span>

<span data-ttu-id="3634c-116">具有焦點的專案可能會與選取的專案不同。</span><span class="sxs-lookup"><span data-stu-id="3634c-116">The item that has the focus may be different than the selected item.</span></span>

## <a name="requirements"></a><span data-ttu-id="3634c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3634c-117">Requirements</span></span>



| <span data-ttu-id="3634c-118">需求</span><span class="sxs-lookup"><span data-stu-id="3634c-118">Requirement</span></span> | <span data-ttu-id="3634c-119">值</span><span class="sxs-lookup"><span data-stu-id="3634c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3634c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3634c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3634c-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3634c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3634c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3634c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3634c-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3634c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3634c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3634c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3634c-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3634c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





