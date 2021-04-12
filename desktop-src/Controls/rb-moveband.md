---
title: 'RB_MOVEBAND 訊息 (Commctrl .h) '
description: 將一個索引區從一個索引移至另一個索引。
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- RB_MOVEBAND message Windows 控制項
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146103c4c3d70fc0514729a00eac152c4847b85c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464392"
---
# <a name="rb_moveband-message"></a><span data-ttu-id="a31f1-104">RB \_ MOVEBAND 訊息</span><span class="sxs-lookup"><span data-stu-id="a31f1-104">RB\_MOVEBAND message</span></span>

<span data-ttu-id="a31f1-105">將一個索引區從一個索引移至另一個索引。</span><span class="sxs-lookup"><span data-stu-id="a31f1-105">Moves a band from one index to another.</span></span>

## <a name="parameters"></a><span data-ttu-id="a31f1-106">參數</span><span class="sxs-lookup"><span data-stu-id="a31f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a31f1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a31f1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a31f1-108">要移動之帶狀線的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="a31f1-108">Zero-based index of the band to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="a31f1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a31f1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a31f1-110">新的寬線位置之以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="a31f1-110">Zero-based index of the new band position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a31f1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a31f1-111">Return value</span></span>

<span data-ttu-id="a31f1-112">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="a31f1-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a31f1-113">備註</span><span class="sxs-lookup"><span data-stu-id="a31f1-113">Remarks</span></span>

<span data-ttu-id="a31f1-114">這則訊息很有可能會變更 Rebar 控制項中其他等區的索引。</span><span class="sxs-lookup"><span data-stu-id="a31f1-114">This message will most likely change the index of other bands in the rebar control.</span></span> <span data-ttu-id="a31f1-115">如果將範圍從索引6移至索引0，則介於兩者之間的所有波段都會以1遞增其索引。</span><span class="sxs-lookup"><span data-stu-id="a31f1-115">If a band is moved from index 6 to index 0, all of the bands in between will have their index incremented by one.</span></span>

<span data-ttu-id="a31f1-116">*lParam* 絕不能大於區段數減一。</span><span class="sxs-lookup"><span data-stu-id="a31f1-116">*lParam* must never be greater than the number of bands minus one.</span></span> <span data-ttu-id="a31f1-117">您可以使用 [**RB \_ GETBANDCOUNT**](rb-getbandcount.md) 訊息來取得群組數。</span><span class="sxs-lookup"><span data-stu-id="a31f1-117">The number of bands can be obtained with the [**RB\_GETBANDCOUNT**](rb-getbandcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a31f1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a31f1-118">Requirements</span></span>



| <span data-ttu-id="a31f1-119">需求</span><span class="sxs-lookup"><span data-stu-id="a31f1-119">Requirement</span></span> | <span data-ttu-id="a31f1-120">值</span><span class="sxs-lookup"><span data-stu-id="a31f1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a31f1-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a31f1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a31f1-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a31f1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a31f1-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a31f1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a31f1-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a31f1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a31f1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a31f1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a31f1-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a31f1-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





