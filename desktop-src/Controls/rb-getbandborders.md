---
title: 'RB_GETBANDBORDERS 訊息 (Commctrl .h) '
description: 抓取寬線的框線。 此訊息的結果可以用來計算頻外的可用區域。
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- RB_GETBANDBORDERS message Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521dfecaf5e2573b30f606b7b4d7ecdec9bd896d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934708"
---
# <a name="rb_getbandborders-message"></a><span data-ttu-id="f1db5-105">RB \_ GETBANDBORDERS 訊息</span><span class="sxs-lookup"><span data-stu-id="f1db5-105">RB\_GETBANDBORDERS message</span></span>

<span data-ttu-id="f1db5-106">抓取寬線的框線。</span><span class="sxs-lookup"><span data-stu-id="f1db5-106">Retrieves the borders of a band.</span></span> <span data-ttu-id="f1db5-107">此訊息的結果可以用來計算頻外的可用區域。</span><span class="sxs-lookup"><span data-stu-id="f1db5-107">The result of this message can be used to calculate the usable area in a band.</span></span>

## <a name="parameters"></a><span data-ttu-id="f1db5-108">參數</span><span class="sxs-lookup"><span data-stu-id="f1db5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1db5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f1db5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1db5-110">以零為基底的寬線索引，將會取出框線。</span><span class="sxs-lookup"><span data-stu-id="f1db5-110">Zero-based index of the band for which the borders will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="f1db5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1db5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1db5-112">將會接收帶框線的 [**矩形**](/previous-versions//dd162897(v=vs.85)) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="f1db5-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the band borders.</span></span> <span data-ttu-id="f1db5-113">如果 Rebar 控制項有 [**RBS \_ BANDBORDERS**](rebar-control-styles.md) 樣式，則此結構的每個成員都會收到組成框線之帶狀邊的圖元數。</span><span class="sxs-lookup"><span data-stu-id="f1db5-113">If the rebar control has the [**RBS\_BANDBORDERS**](rebar-control-styles.md) style, each member of this structure will receive the number of pixels, on the corresponding side of the band, that constitute the border.</span></span> <span data-ttu-id="f1db5-114">如果 Rebar 控制項沒有 **RBS \_ BANDBORDERS** 樣式，則只有此結構的 **左側** 成員會收到有效的資訊。</span><span class="sxs-lookup"><span data-stu-id="f1db5-114">If the rebar control does not have the **RBS\_BANDBORDERS** style, only the **left** member of this structure receives valid information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1db5-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1db5-115">Return value</span></span>

<span data-ttu-id="f1db5-116">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="f1db5-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1db5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1db5-117">Requirements</span></span>



| <span data-ttu-id="f1db5-118">需求</span><span class="sxs-lookup"><span data-stu-id="f1db5-118">Requirement</span></span> | <span data-ttu-id="f1db5-119">值</span><span class="sxs-lookup"><span data-stu-id="f1db5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1db5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1db5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f1db5-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1db5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1db5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1db5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f1db5-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1db5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1db5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f1db5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1db5-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1db5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

