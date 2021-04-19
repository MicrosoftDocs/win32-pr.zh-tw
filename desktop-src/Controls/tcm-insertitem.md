---
title: 'TCM_INSERTITEM 訊息 (Commctrl .h) '
description: 在索引標籤控制項中插入新的索引標籤。 您可以使用 TabCtrl InsertItem 宏明確地傳送此訊息 \_ 。
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- TCM_INSERTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_INSERTITEM
- TCM_INSERTITEMA
- TCM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58002006944a221571e37c37d25259d0aaa74fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968375"
---
# <a name="tcm_insertitem-message"></a><span data-ttu-id="c6bcd-105">TCM \_ INSERTITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="c6bcd-105">TCM\_INSERTITEM message</span></span>

<span data-ttu-id="c6bcd-106">在索引標籤控制項中插入新的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="c6bcd-106">Inserts a new tab in a tab control.</span></span> <span data-ttu-id="c6bcd-107">您可以使用 [**TabCtrl \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c6bcd-107">You can send this message explicitly or by using the [**TabCtrl\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c6bcd-108">參數</span><span class="sxs-lookup"><span data-stu-id="c6bcd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6bcd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6bcd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6bcd-110">新索引標籤的索引。</span><span class="sxs-lookup"><span data-stu-id="c6bcd-110">Index of the new tab.</span></span>

</dd> <dt>

<span data-ttu-id="c6bcd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6bcd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6bcd-112">[**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema)結構的指標，指定索引標籤的屬性。此訊息會忽略此結構的 **dwState** 和 **dwStateMask** 成員。</span><span class="sxs-lookup"><span data-stu-id="c6bcd-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that specifies the attributes of the tab. The **dwState** and **dwStateMask** members of this structure are ignored by this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6bcd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6bcd-113">Return value</span></span>

<span data-ttu-id="c6bcd-114">如果成功，則傳回新索引標籤的索引，否則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="c6bcd-114">Returns the index of the new tab if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6bcd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6bcd-115">Requirements</span></span>



| <span data-ttu-id="c6bcd-116">需求</span><span class="sxs-lookup"><span data-stu-id="c6bcd-116">Requirement</span></span> | <span data-ttu-id="c6bcd-117">值</span><span class="sxs-lookup"><span data-stu-id="c6bcd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6bcd-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6bcd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c6bcd-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6bcd-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6bcd-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6bcd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c6bcd-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6bcd-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c6bcd-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c6bcd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6bcd-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6bcd-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c6bcd-124">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="c6bcd-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c6bcd-125">**TCM \_INSERTITEMW** (Unicode) 和 **TCM \_ INSERTITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="c6bcd-125">**TCM\_INSERTITEMW** (Unicode) and **TCM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





