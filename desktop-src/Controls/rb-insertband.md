---
title: 'RB_INSERTBAND 訊息 (Commctrl .h) '
description: 在 Rebar 控制項中插入新的波段。
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- RB_INSERTBAND message Windows 控制項
topic_type:
- apiref
api_name:
- RB_INSERTBAND
- RB_INSERTBANDA
- RB_INSERTBANDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39b45eb662fb4c2058b87837352339c84762188
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844456"
---
# <a name="rb_insertband-message"></a><span data-ttu-id="79d54-104">RB \_ INSERTBAND 訊息</span><span class="sxs-lookup"><span data-stu-id="79d54-104">RB\_INSERTBAND message</span></span>

<span data-ttu-id="79d54-105">在 Rebar 控制項中插入新的波段。</span><span class="sxs-lookup"><span data-stu-id="79d54-105">Inserts a new band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="79d54-106">參數</span><span class="sxs-lookup"><span data-stu-id="79d54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79d54-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79d54-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79d54-108">以零為基底的索引，也就是要插入頻外的位置。</span><span class="sxs-lookup"><span data-stu-id="79d54-108">Zero-based index of the location where the band will be inserted.</span></span> <span data-ttu-id="79d54-109">如果您將此參數設定為-1，此控制項將會在最後一個位置新增新的頻外。</span><span class="sxs-lookup"><span data-stu-id="79d54-109">If you set this parameter to -1, the control will add the new band at the last location.</span></span>

</dd> <dt>

<span data-ttu-id="79d54-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79d54-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79d54-111">[**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)結構的指標，該結構定義要插入的帶狀。</span><span class="sxs-lookup"><span data-stu-id="79d54-111">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that defines the band to be inserted.</span></span> <span data-ttu-id="79d54-112">在傳送此訊息之前，您必須將此結構的 **cbSize** 成員設定為 **sizeof** (REBARBANDINFO) 。</span><span class="sxs-lookup"><span data-stu-id="79d54-112">You must set the **cbSize** member of this structure to **sizeof**(REBARBANDINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79d54-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="79d54-113">Return value</span></span>

<span data-ttu-id="79d54-114">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="79d54-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="79d54-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="79d54-115">Requirements</span></span>



| <span data-ttu-id="79d54-116">需求</span><span class="sxs-lookup"><span data-stu-id="79d54-116">Requirement</span></span> | <span data-ttu-id="79d54-117">值</span><span class="sxs-lookup"><span data-stu-id="79d54-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79d54-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79d54-118">Minimum supported client</span></span><br/> | <span data-ttu-id="79d54-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79d54-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79d54-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79d54-120">Minimum supported server</span></span><br/> | <span data-ttu-id="79d54-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79d54-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79d54-122">標頭</span><span class="sxs-lookup"><span data-stu-id="79d54-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="79d54-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="79d54-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="79d54-124">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="79d54-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="79d54-125">**RB \_INSERTBANDW** (Unicode) 和 **RB \_ INSERTBANDA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="79d54-125">**RB\_INSERTBANDW** (Unicode) and **RB\_INSERTBANDA** (ANSI)</span></span><br/>               |



 

 





