---
title: 'RB_SIZETORECT 訊息 (Commctrl .h) '
description: 嘗試找出指定矩形之區段的最佳版面配置。
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- RB_SIZETORECT message Windows 控制項
topic_type:
- apiref
api_name:
- RB_SIZETORECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3db5727ee8c94d2473b503c9a81b7669bb829a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106253"
---
# <a name="rb_sizetorect-message"></a><span data-ttu-id="9fd9f-104">RB \_ SIZETORECT 訊息</span><span class="sxs-lookup"><span data-stu-id="9fd9f-104">RB\_SIZETORECT message</span></span>

<span data-ttu-id="9fd9f-105">嘗試找出指定矩形之區段的最佳版面配置。</span><span class="sxs-lookup"><span data-stu-id="9fd9f-105">Attempts to find the best layout of the bands for the given rectangle.</span></span>

## <a name="parameters"></a><span data-ttu-id="9fd9f-106">參數</span><span class="sxs-lookup"><span data-stu-id="9fd9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fd9f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9fd9f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9fd9f-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9fd9f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9fd9f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9fd9f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9fd9f-110">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會指定 Rebar 控制項應調整大小的矩形。</span><span class="sxs-lookup"><span data-stu-id="9fd9f-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the rectangle to which the rebar control should be sized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fd9f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9fd9f-111">Return value</span></span>

<span data-ttu-id="9fd9f-112">如果發生版面配置變更，則傳回非零值，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="9fd9f-112">Returns nonzero if a layout change occurred, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fd9f-113">備註</span><span class="sxs-lookup"><span data-stu-id="9fd9f-113">Remarks</span></span>

<span data-ttu-id="9fd9f-114">將會視需要排列和包裝 Rebar 群組，以配合矩形。</span><span class="sxs-lookup"><span data-stu-id="9fd9f-114">The rebar bands will be arranged and wrapped as necessary to fit the rectangle.</span></span> <span data-ttu-id="9fd9f-115">具有 RBBS \_ VARIABLEHEIGHT 樣式的波段會盡可能平均調整大小以符合矩形。</span><span class="sxs-lookup"><span data-stu-id="9fd9f-115">Bands that have the RBBS\_VARIABLEHEIGHT style will be resized as evenly as possible to fit the rectangle.</span></span> <span data-ttu-id="9fd9f-116">水準 Rebar 或垂直 Rebar 寬度的高度可能會變更，視新的版面配置而定。</span><span class="sxs-lookup"><span data-stu-id="9fd9f-116">The height of a horizontal rebar or the width of a vertical rebar may change, depending on the new layout.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fd9f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fd9f-117">Requirements</span></span>



| <span data-ttu-id="9fd9f-118">需求</span><span class="sxs-lookup"><span data-stu-id="9fd9f-118">Requirement</span></span> | <span data-ttu-id="9fd9f-119">值</span><span class="sxs-lookup"><span data-stu-id="9fd9f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd9f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9fd9f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9fd9f-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9fd9f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9fd9f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9fd9f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9fd9f-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9fd9f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9fd9f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="9fd9f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fd9f-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9fd9f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

