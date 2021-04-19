---
title: 'CBEM_DELETEITEM 訊息 (Commctrl .h) '
description: 從 ComboBoxEx 控制項中移除專案。
ms.assetid: 688cf388-54ba-4b45-88d7-628da49d8615
keywords:
- CBEM_DELETEITEM message Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3034f79dffabcd7d7aa780582646e17d30b62f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996587"
---
# <a name="cbem_deleteitem-message"></a><span data-ttu-id="ab04d-104">CBEM \_ DELETEITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="ab04d-104">CBEM\_DELETEITEM message</span></span>

<span data-ttu-id="ab04d-105">從 ComboBoxEx 控制項中移除專案。</span><span class="sxs-lookup"><span data-stu-id="ab04d-105">Removes an item from a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ab04d-106">參數</span><span class="sxs-lookup"><span data-stu-id="ab04d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab04d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ab04d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab04d-108">要移除之專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="ab04d-108">The zero-based index of the item to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="ab04d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ab04d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ab04d-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ab04d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab04d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab04d-111">Return value</span></span>

<span data-ttu-id="ab04d-112">傳回 INT 值，表示控制項中剩餘的專案數目。</span><span class="sxs-lookup"><span data-stu-id="ab04d-112">Returns an INT value that represents the number of items remaining in the control.</span></span> <span data-ttu-id="ab04d-113">如果 *iIndex* 無效，訊息會傳回 CB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="ab04d-113">If *iIndex* is invalid, the message returns CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab04d-114">備註</span><span class="sxs-lookup"><span data-stu-id="ab04d-114">Remarks</span></span>

<span data-ttu-id="ab04d-115">這則訊息會對應至下拉式方塊控制項訊息 [**CB \_ DELETESTRING**](cb-deletestring.md)。</span><span class="sxs-lookup"><span data-stu-id="ab04d-115">This message maps to the combo box control message [**CB\_DELETESTRING**](cb-deletestring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab04d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab04d-116">Requirements</span></span>



| <span data-ttu-id="ab04d-117">需求</span><span class="sxs-lookup"><span data-stu-id="ab04d-117">Requirement</span></span> | <span data-ttu-id="ab04d-118">值</span><span class="sxs-lookup"><span data-stu-id="ab04d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab04d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab04d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ab04d-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab04d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ab04d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab04d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ab04d-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab04d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ab04d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ab04d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab04d-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab04d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





