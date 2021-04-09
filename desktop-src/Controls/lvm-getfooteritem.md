---
title: 'LVM_GETFOOTERITEM 訊息 (Commctrl .h) '
description: 取得清單視圖控制項中頁尾專案的資訊。 明確地傳送此訊息，或使用 ListView \_ GetFooterItem 宏。
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- LVM_GETFOOTERITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e642c9d853ae11edcd9199e48de61592de4883c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024588"
---
# <a name="lvm_getfooteritem-message"></a><span data-ttu-id="049f9-105">LVM \_ GETFOOTERITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="049f9-105">LVM\_GETFOOTERITEM message</span></span>

<span data-ttu-id="049f9-106">取得清單視圖控制項中頁尾專案的資訊。</span><span class="sxs-lookup"><span data-stu-id="049f9-106">Gets information on a footer item in a list-view control.</span></span> <span data-ttu-id="049f9-107">明確地傳送此訊息，或使用 [**ListView \_ GetFooterItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) 宏。</span><span class="sxs-lookup"><span data-stu-id="049f9-107">Send this message explicitly or by using the [**ListView\_GetFooterItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="049f9-108">參數</span><span class="sxs-lookup"><span data-stu-id="049f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="049f9-109">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="049f9-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="049f9-110">項目的索引。</span><span class="sxs-lookup"><span data-stu-id="049f9-110">The index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="049f9-111">*lParam* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="049f9-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="049f9-112">[**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem)結構的指標，可根據 **mask** 成員的值接收 **狀態** 和/或 **pszText** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="049f9-112">A pointer to a [**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) structure to receive a value for the **state** and/or **pszText** members according to the value of the **mask** member.</span></span> <span data-ttu-id="049f9-113">呼叫進程負責配置此結構並設定其成員，向接收者指出要傳回的資訊。</span><span class="sxs-lookup"><span data-stu-id="049f9-113">The calling process is responsible for allocating this structure and setting its members to indicate to the receiver what information to return.</span></span> <span data-ttu-id="049f9-114">如需詳細資訊，請參閱 **LVFOOTERITEM**。</span><span class="sxs-lookup"><span data-stu-id="049f9-114">For more information, see **LVFOOTERITEM**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="049f9-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="049f9-115">Return value</span></span>

<span data-ttu-id="049f9-116">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="049f9-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="049f9-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="049f9-117">Requirements</span></span>



| <span data-ttu-id="049f9-118">需求</span><span class="sxs-lookup"><span data-stu-id="049f9-118">Requirement</span></span> | <span data-ttu-id="049f9-119">值</span><span class="sxs-lookup"><span data-stu-id="049f9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="049f9-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="049f9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="049f9-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="049f9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="049f9-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="049f9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="049f9-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="049f9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="049f9-124">標頭</span><span class="sxs-lookup"><span data-stu-id="049f9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="049f9-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="049f9-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





