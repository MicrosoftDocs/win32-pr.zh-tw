---
title: 'LVM_GETCOLUMNORDERARRAY 訊息 (Commctrl .h) '
description: 取得清單視圖控制項中資料行的目前由左到右的順序。 您可以明確地傳送此訊息，或使用 ListView \_ GetColumnOrderArray 宏。
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- LVM_GETCOLUMNORDERARRAY message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee387f65abd3f30826e361778d5acac02dfab7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024595"
---
# <a name="lvm_getcolumnorderarray-message"></a><span data-ttu-id="c072b-105">LVM \_ GETCOLUMNORDERARRAY 訊息</span><span class="sxs-lookup"><span data-stu-id="c072b-105">LVM\_GETCOLUMNORDERARRAY message</span></span>

<span data-ttu-id="c072b-106">取得清單視圖控制項中資料行的目前由左到右的順序。</span><span class="sxs-lookup"><span data-stu-id="c072b-106">Gets the current left-to-right order of columns in a list-view control.</span></span> <span data-ttu-id="c072b-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) 宏。</span><span class="sxs-lookup"><span data-stu-id="c072b-107">You can send this message explicitly or use the [**ListView\_GetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c072b-108">參數</span><span class="sxs-lookup"><span data-stu-id="c072b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c072b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c072b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c072b-110">清單視圖控制項中的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="c072b-110">The number of columns in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="c072b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c072b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c072b-112">整數陣列的指標，這個陣列會接收清單視圖控制項中資料行的索引值。</span><span class="sxs-lookup"><span data-stu-id="c072b-112">A pointer to an array of integers that receives the index values of the columns in the list-view control.</span></span> <span data-ttu-id="c072b-113">陣列必須夠大，才能容納 *wParam* 元素。</span><span class="sxs-lookup"><span data-stu-id="c072b-113">The array must be large enough to hold *wParam* elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c072b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c072b-114">Return value</span></span>

<span data-ttu-id="c072b-115">如果成功，會傳回非零，而 *lParam* 的緩衝區會接收控制項中每個資料行的資料行索引（依其出現的順序，由左至右排列）。</span><span class="sxs-lookup"><span data-stu-id="c072b-115">If successful, returns nonzero, and the buffer at *lParam* receives the column index of each column in the control in the order they appear from left to right.</span></span> <span data-ttu-id="c072b-116">否則，傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="c072b-116">Otherwise, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c072b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c072b-117">Requirements</span></span>



| <span data-ttu-id="c072b-118">需求</span><span class="sxs-lookup"><span data-stu-id="c072b-118">Requirement</span></span> | <span data-ttu-id="c072b-119">值</span><span class="sxs-lookup"><span data-stu-id="c072b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c072b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c072b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c072b-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c072b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c072b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c072b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c072b-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c072b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c072b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c072b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c072b-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c072b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





