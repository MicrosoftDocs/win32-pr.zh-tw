---
title: 'RB_MAXIMIZEBAND 訊息 (Commctrl .h) '
description: 將 Rebar 控制項中的寬線大小調整為理想或最大的大小。
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- RB_MAXIMIZEBAND message Windows 控制項
topic_type:
- apiref
api_name:
- RB_MAXIMIZEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708a8fae7c0dd8e72eea8e5acefe43ab50054592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843924"
---
# <a name="rb_maximizeband-message"></a><span data-ttu-id="aec40-104">RB \_ MAXIMIZEBAND 訊息</span><span class="sxs-lookup"><span data-stu-id="aec40-104">RB\_MAXIMIZEBAND message</span></span>

<span data-ttu-id="aec40-105">將 Rebar 控制項中的寬線大小調整為理想或最大的大小。</span><span class="sxs-lookup"><span data-stu-id="aec40-105">Resizes a band in a rebar control to either its ideal or largest size.</span></span>

## <a name="parameters"></a><span data-ttu-id="aec40-106">參數</span><span class="sxs-lookup"><span data-stu-id="aec40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aec40-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aec40-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aec40-108">以零為基底的寬線索引，要最大化。</span><span class="sxs-lookup"><span data-stu-id="aec40-108">Zero-based index of the band to be maximized.</span></span>

</dd> <dt>

<span data-ttu-id="aec40-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aec40-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aec40-110">指出當寬線最大化時，是否應使用寬線的理想寬度。</span><span class="sxs-lookup"><span data-stu-id="aec40-110">Indicates if the ideal width of the band should be used when the band is maximized.</span></span> <span data-ttu-id="aec40-111">如果此值為非零值，則會使用理想的寬度。</span><span class="sxs-lookup"><span data-stu-id="aec40-111">If this value is nonzero, the ideal width will be used.</span></span> <span data-ttu-id="aec40-112">如果此值為零，則會盡可能將此寬線設為最大。</span><span class="sxs-lookup"><span data-stu-id="aec40-112">If this value is zero, the band will be made as large as possible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aec40-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="aec40-113">Return value</span></span>

<span data-ttu-id="aec40-114">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="aec40-114">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="aec40-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="aec40-115">Requirements</span></span>



| <span data-ttu-id="aec40-116">需求</span><span class="sxs-lookup"><span data-stu-id="aec40-116">Requirement</span></span> | <span data-ttu-id="aec40-117">值</span><span class="sxs-lookup"><span data-stu-id="aec40-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aec40-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aec40-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aec40-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aec40-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aec40-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aec40-120">Minimum supported server</span></span><br/> | <span data-ttu-id="aec40-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aec40-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aec40-122">標頭</span><span class="sxs-lookup"><span data-stu-id="aec40-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="aec40-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="aec40-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aec40-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aec40-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="aec40-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="aec40-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aec40-126">**RB \_ SETBANDINFO**</span><span class="sxs-lookup"><span data-stu-id="aec40-126">**RB\_SETBANDINFO**</span></span>](rb-setbandinfo.md)
</dt> </dl>

 

 





