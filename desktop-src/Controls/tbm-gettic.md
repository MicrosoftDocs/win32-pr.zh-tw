---
title: 'TBM_GETTIC 訊息 (Commctrl .h) '
description: 捕獲刻度中刻度標記的邏輯位置。 邏輯位置可以是 [最小值] 和 [最大值] 滑杆位置範圍中的任何整數值。
ms.assetid: 9d70c860-de97-4579-bb10-e9e9db7f1784
keywords:
- TBM_GETTIC message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d534d5100e20cc544c31fca2fc9e49cda3bd976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465361"
---
# <a name="tbm_gettic-message"></a><span data-ttu-id="c51f6-105">TBM \_ GETTIC 訊息</span><span class="sxs-lookup"><span data-stu-id="c51f6-105">TBM\_GETTIC message</span></span>

<span data-ttu-id="c51f6-106">捕獲刻度中刻度標記的邏輯位置。</span><span class="sxs-lookup"><span data-stu-id="c51f6-106">Retrieves the logical position of a tick mark in a trackbar.</span></span> <span data-ttu-id="c51f6-107">邏輯位置可以是 [最小值] 和 [最大值] 滑杆位置範圍中的任何整數值。</span><span class="sxs-lookup"><span data-stu-id="c51f6-107">The logical position can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="c51f6-108">參數</span><span class="sxs-lookup"><span data-stu-id="c51f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c51f6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c51f6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c51f6-110">以零為基底的索引，識別刻度。</span><span class="sxs-lookup"><span data-stu-id="c51f6-110">Zero-based index identifying a tick mark.</span></span> <span data-ttu-id="c51f6-111">有效索引的範圍介於0到2之間，小於 [**TBM \_ GETNUMTICS**](tbm-getnumtics.md) 訊息所傳回的滴答計數。</span><span class="sxs-lookup"><span data-stu-id="c51f6-111">Valid indexes are in the range from zero to two less than the tick count returned by the [**TBM\_GETNUMTICS**](tbm-getnumtics.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="c51f6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c51f6-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c51f6-113">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c51f6-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c51f6-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c51f6-114">Return value</span></span>

<span data-ttu-id="c51f6-115">傳回指定刻度的邏輯位置; 如果 *wParam* 未指定有效的索引，則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="c51f6-115">Returns the logical position of the specified tick mark, or -1 if *wParam* does not specify a valid index.</span></span>

## <a name="requirements"></a><span data-ttu-id="c51f6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c51f6-116">Requirements</span></span>



| <span data-ttu-id="c51f6-117">需求</span><span class="sxs-lookup"><span data-stu-id="c51f6-117">Requirement</span></span> | <span data-ttu-id="c51f6-118">值</span><span class="sxs-lookup"><span data-stu-id="c51f6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c51f6-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c51f6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c51f6-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c51f6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c51f6-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c51f6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c51f6-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c51f6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c51f6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c51f6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c51f6-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c51f6-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





