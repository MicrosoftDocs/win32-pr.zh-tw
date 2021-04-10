---
title: 'TBM_GETPTICS 訊息 (Commctrl .h) '
description: 抓取陣列的位址，這個陣列包含了刻度的刻度位置。
ms.assetid: d15a4b4d-2ced-40a4-9351-ed7ecc5a5751
keywords:
- TBM_GETPTICS message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETPTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5d81e67156c0118310017413b8e73714246b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934409"
---
# <a name="tbm_getptics-message"></a><span data-ttu-id="9f23c-104">TBM \_ GETPTICS 訊息</span><span class="sxs-lookup"><span data-stu-id="9f23c-104">TBM\_GETPTICS message</span></span>

<span data-ttu-id="9f23c-105">抓取陣列的位址，這個陣列包含了刻度的刻度位置。</span><span class="sxs-lookup"><span data-stu-id="9f23c-105">Retrieves the address of an array that contains the positions of the tick marks for a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f23c-106">參數</span><span class="sxs-lookup"><span data-stu-id="9f23c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f23c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f23c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9f23c-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9f23c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9f23c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f23c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9f23c-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9f23c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f23c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f23c-111">Return value</span></span>

<span data-ttu-id="9f23c-112">傳回 **DWORD** 值陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="9f23c-112">Returns the address of an array of **DWORD** values.</span></span> <span data-ttu-id="9f23c-113">陣列的元素會指定這些標頭的刻度的邏輯位置，而不包含由並排標示所建立的第一個和最後一個刻度。</span><span class="sxs-lookup"><span data-stu-id="9f23c-113">The elements of the array specify the logical positions of the trackbar's tick marks, not including the first and last tick marks created by the trackbar.</span></span> <span data-ttu-id="9f23c-114">邏輯位置可以是 [最小值] 和 [最大值] 滑杆位置範圍中的任何整數值。</span><span class="sxs-lookup"><span data-stu-id="9f23c-114">The logical positions can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f23c-115">備註</span><span class="sxs-lookup"><span data-stu-id="9f23c-115">Remarks</span></span>

<span data-ttu-id="9f23c-116">陣列中的元素數目是兩個小於 [**TBM \_ GETNUMTICS**](tbm-getnumtics.md) 訊息所傳回之滴答計數的兩個專案。</span><span class="sxs-lookup"><span data-stu-id="9f23c-116">The number of elements in the array is two less than the tick count returned by the [**TBM\_GETNUMTICS**](tbm-getnumtics.md) message.</span></span> <span data-ttu-id="9f23c-117">請注意，陣列中的值可能包含重複的位置，而且可能不是順序。</span><span class="sxs-lookup"><span data-stu-id="9f23c-117">Note that the values in the array may include duplicate positions and may not be in sequential order.</span></span> <span data-ttu-id="9f23c-118">傳回的指標會一直有效，直到您變更了這些標記的刻度。</span><span class="sxs-lookup"><span data-stu-id="9f23c-118">The returned pointer is valid until you change the trackbar's tick marks.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f23c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f23c-119">Requirements</span></span>



| <span data-ttu-id="9f23c-120">需求</span><span class="sxs-lookup"><span data-stu-id="9f23c-120">Requirement</span></span> | <span data-ttu-id="9f23c-121">值</span><span class="sxs-lookup"><span data-stu-id="9f23c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f23c-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f23c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9f23c-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f23c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f23c-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f23c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9f23c-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f23c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f23c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="9f23c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f23c-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9f23c-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





