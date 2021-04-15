---
title: 'HDM_SETITEM 訊息 (Commctrl .h) '
description: 在標題控制項中設定指定專案的屬性。 您可以明確地傳送此訊息，或使用標頭 \_ SetItem 宏。
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- HDM_SETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_SETITEM
- HDM_SETITEMA
- HDM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b03a05b909cf8c7887edd2031f5346c419f1cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466341"
---
# <a name="hdm_setitem-message"></a><span data-ttu-id="cefcb-105">HDM \_ SETITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="cefcb-105">HDM\_SETITEM message</span></span>

<span data-ttu-id="cefcb-106">在標題控制項中設定指定專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="cefcb-106">Sets the attributes of the specified item in a header control.</span></span> <span data-ttu-id="cefcb-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) 宏。</span><span class="sxs-lookup"><span data-stu-id="cefcb-107">You can send this message explicitly or use the [**Header\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cefcb-108">參數</span><span class="sxs-lookup"><span data-stu-id="cefcb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cefcb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cefcb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cefcb-110">要變更其屬性之專案的目前索引。</span><span class="sxs-lookup"><span data-stu-id="cefcb-110">The current index of the item whose attributes are to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="cefcb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cefcb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cefcb-112">包含專案資訊之 [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="cefcb-112">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that contains item information.</span></span> <span data-ttu-id="cefcb-113">傳送此訊息時，必須設定結構的 **遮罩** 成員，以指出要設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="cefcb-113">When this message is sent, the **mask** member of the structure must be set to indicate which attributes are being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cefcb-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="cefcb-114">Return value</span></span>

<span data-ttu-id="cefcb-115">在成功時傳回非零值，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="cefcb-115">Returns nonzero upon success, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cefcb-116">備註</span><span class="sxs-lookup"><span data-stu-id="cefcb-116">Remarks</span></span>

<span data-ttu-id="cefcb-117">支援此訊息的 [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) 結構支援專案順序和影像清單資訊。</span><span class="sxs-lookup"><span data-stu-id="cefcb-117">The [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that supports this message supports item order and image list information.</span></span> <span data-ttu-id="cefcb-118">藉由使用這些成員，您可以控制顯示專案的順序，並指定要與專案一起顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="cefcb-118">By using these members, you can control the order in which items are displayed and specify images to appear with items.</span></span>

## <a name="requirements"></a><span data-ttu-id="cefcb-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="cefcb-119">Requirements</span></span>



| <span data-ttu-id="cefcb-120">需求</span><span class="sxs-lookup"><span data-stu-id="cefcb-120">Requirement</span></span> | <span data-ttu-id="cefcb-121">值</span><span class="sxs-lookup"><span data-stu-id="cefcb-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cefcb-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cefcb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cefcb-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cefcb-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cefcb-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cefcb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cefcb-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cefcb-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cefcb-126">標頭</span><span class="sxs-lookup"><span data-stu-id="cefcb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cefcb-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cefcb-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="cefcb-128">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="cefcb-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cefcb-129">**HDM \_SETITEMW** (Unicode) 和 **HDM \_ SETITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="cefcb-129">**HDM\_SETITEMW** (Unicode) and **HDM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





