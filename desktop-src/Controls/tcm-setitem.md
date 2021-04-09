---
title: 'TCM_SETITEM 訊息 (Commctrl .h) '
description: 設定部分或全部索引標籤的屬性。 您可以使用 TabCtrl SetItem 宏明確地傳送此訊息 \_ 。
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- TCM_SETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETITEM
- TCM_SETITEMA
- TCM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee86cd0737c3c50c89a97d3881e2cdfd3850f481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685504"
---
# <a name="tcm_setitem-message"></a><span data-ttu-id="0ddca-105">TCM \_ SETITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="0ddca-105">TCM\_SETITEM message</span></span>

<span data-ttu-id="0ddca-106">設定部分或全部索引標籤的屬性。</span><span class="sxs-lookup"><span data-stu-id="0ddca-106">Sets some or all of a tab's attributes.</span></span> <span data-ttu-id="0ddca-107">您可以使用 [**TabCtrl \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="0ddca-107">You can send this message explicitly or by using the [**TabCtrl\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ddca-108">參數</span><span class="sxs-lookup"><span data-stu-id="0ddca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ddca-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ddca-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ddca-110">專案的索引。</span><span class="sxs-lookup"><span data-stu-id="0ddca-110">Index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="0ddca-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ddca-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ddca-112">[**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema)結構的指標，其中包含新的專案屬性。</span><span class="sxs-lookup"><span data-stu-id="0ddca-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="0ddca-113">**遮罩** 成員會指定要設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="0ddca-113">The **mask** member specifies which attributes to set.</span></span> <span data-ttu-id="0ddca-114">如果 **遮罩** 成員指定 TCIF \_ 文字值，則 **pszText** 成員是以 null 結束之字串的位址，而且會忽略 **cchTextMax** 成員。</span><span class="sxs-lookup"><span data-stu-id="0ddca-114">If the **mask** member specifies the TCIF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ddca-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ddca-115">Return value</span></span>

<span data-ttu-id="0ddca-116">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="0ddca-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ddca-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ddca-117">Requirements</span></span>



| <span data-ttu-id="0ddca-118">需求</span><span class="sxs-lookup"><span data-stu-id="0ddca-118">Requirement</span></span> | <span data-ttu-id="0ddca-119">值</span><span class="sxs-lookup"><span data-stu-id="0ddca-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ddca-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ddca-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0ddca-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ddca-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ddca-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ddca-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0ddca-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ddca-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ddca-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0ddca-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ddca-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0ddca-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0ddca-126">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="0ddca-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0ddca-127">**TCM \_SETITEMW** (Unicode) 和 **TCM \_ SETITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="0ddca-127">**TCM\_SETITEMW** (Unicode) and **TCM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





