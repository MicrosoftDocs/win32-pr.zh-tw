---
title: 'LVM_GETGROUPSTATE 訊息 (Commctrl .h) '
description: 取得指定群組的狀態。 明確地傳送此訊息，或使用 ListView \_ GetGroupState 宏。
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- LVM_GETGROUPSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETGROUPSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17b5bb25fd517816afd04bb700211222e6985f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464413"
---
# <a name="lvm_getgroupstate-message"></a><span data-ttu-id="8cfd4-105">LVM \_ GETGROUPSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="8cfd4-105">LVM\_GETGROUPSTATE message</span></span>

<span data-ttu-id="8cfd4-106">取得指定群組的狀態。</span><span class="sxs-lookup"><span data-stu-id="8cfd4-106">Gets the state for a specified group.</span></span> <span data-ttu-id="8cfd4-107">明確地傳送此訊息，或使用 [**ListView \_ GetGroupState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) 宏。</span><span class="sxs-lookup"><span data-stu-id="8cfd4-107">Send this message explicitly or by using the [**ListView\_GetGroupState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8cfd4-108">參數</span><span class="sxs-lookup"><span data-stu-id="8cfd4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cfd4-109">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8cfd4-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cfd4-110">指定 group by **iGroupId** (參閱 [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) 結構) 。</span><span class="sxs-lookup"><span data-stu-id="8cfd4-110">Specifies the group by **iGroupId** (see [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure).</span></span>

</dd> <dt>

<span data-ttu-id="8cfd4-111">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8cfd4-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cfd4-112">指定要取出的狀態值。</span><span class="sxs-lookup"><span data-stu-id="8cfd4-112">Specifies the state values to retrieve.</span></span> <span data-ttu-id="8cfd4-113">這是 [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)的 **state** 成員所列出的旗標組合。</span><span class="sxs-lookup"><span data-stu-id="8cfd4-113">This is a combination of the flags listed for the **state** member of [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cfd4-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="8cfd4-114">Return value</span></span>

<span data-ttu-id="8cfd4-115">傳回已設定之狀態值的組合。</span><span class="sxs-lookup"><span data-stu-id="8cfd4-115">Returns the combination of state values that are set.</span></span> <span data-ttu-id="8cfd4-116">例如，如果 *lParam* 是 LVGS 折迭 \_ 的，且傳回的值為零，則 \_ 不會設定 LVGS 折迭狀態。</span><span class="sxs-lookup"><span data-stu-id="8cfd4-116">For example, if *lParam* is LVGS\_COLLAPSED and the value returned is zero, the LVGS\_COLLAPSED state is not set.</span></span> <span data-ttu-id="8cfd4-117">如果找不到群組，就會傳回零。</span><span class="sxs-lookup"><span data-stu-id="8cfd4-117">Zero is returned if the group is not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cfd4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="8cfd4-118">Requirements</span></span>



| <span data-ttu-id="8cfd4-119">需求</span><span class="sxs-lookup"><span data-stu-id="8cfd4-119">Requirement</span></span> | <span data-ttu-id="8cfd4-120">值</span><span class="sxs-lookup"><span data-stu-id="8cfd4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8cfd4-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8cfd4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8cfd4-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8cfd4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8cfd4-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8cfd4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8cfd4-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8cfd4-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8cfd4-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8cfd4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cfd4-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8cfd4-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





