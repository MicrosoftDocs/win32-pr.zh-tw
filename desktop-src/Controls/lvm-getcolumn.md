---
title: 'LVM_GETCOLUMN 訊息 (Commctrl .h) '
description: 取得清單視圖控制項之資料行的屬性。 您可以明確地傳送此訊息，或使用 ListView \_ GetColumn 宏來傳送。
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- LVM_GETCOLUMN message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eebf57138d27c31c5594f271e5d36a052b81673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464280"
---
# <a name="lvm_getcolumn-message"></a><span data-ttu-id="31b13-105">LVM \_ GETCOLUMN 訊息</span><span class="sxs-lookup"><span data-stu-id="31b13-105">LVM\_GETCOLUMN message</span></span>

<span data-ttu-id="31b13-106">取得清單視圖控制項之資料行的屬性。</span><span class="sxs-lookup"><span data-stu-id="31b13-106">Gets the attributes of a list-view control's column.</span></span> <span data-ttu-id="31b13-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="31b13-107">You can send this message explicitly or by using the [**ListView\_GetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="31b13-108">參數</span><span class="sxs-lookup"><span data-stu-id="31b13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31b13-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31b13-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31b13-110">資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="31b13-110">The index of the column.</span></span>

</dd> <dt>

<span data-ttu-id="31b13-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31b13-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31b13-112">[**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna)結構的指標，指定要取出的資訊，並接收資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="31b13-112">A pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that specifies the information to retrieve and receives information about the column.</span></span> <span data-ttu-id="31b13-113">**遮罩** 成員會指定要取出的資料行屬性。</span><span class="sxs-lookup"><span data-stu-id="31b13-113">The **mask** member specifies which column attributes to retrieve.</span></span> <span data-ttu-id="31b13-114">如果 **遮罩** 成員指定 LVCF \_ 文字值， **pszText** 成員就必須包含接收專案文字的緩衝區位址，而且 **cchTextMax** 成員必須指定緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="31b13-114">If the **mask** member specifies the LVCF\_TEXT value, the **pszText** member must contain the address of the buffer that receives the item text and the **cchTextMax** member must specify the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31b13-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="31b13-115">Return value</span></span>

<span data-ttu-id="31b13-116">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="31b13-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="31b13-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="31b13-117">Requirements</span></span>



| <span data-ttu-id="31b13-118">需求</span><span class="sxs-lookup"><span data-stu-id="31b13-118">Requirement</span></span> | <span data-ttu-id="31b13-119">值</span><span class="sxs-lookup"><span data-stu-id="31b13-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31b13-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31b13-120">Minimum supported client</span></span><br/> | <span data-ttu-id="31b13-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31b13-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="31b13-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31b13-122">Minimum supported server</span></span><br/> | <span data-ttu-id="31b13-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31b13-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="31b13-124">標頭</span><span class="sxs-lookup"><span data-stu-id="31b13-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="31b13-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="31b13-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





