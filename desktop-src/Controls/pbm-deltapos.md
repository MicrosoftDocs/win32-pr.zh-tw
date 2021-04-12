---
title: 'PBM_DELTAPOS 訊息 (Commctrl .h) '
description: 依指定的遞增量將進度列的目前位置往前移，並重新繪製橫條以反映新的位置。
ms.assetid: 92c89434-d50b-45e7-b686-42e9297518b9
keywords:
- PBM_DELTAPOS message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d0c36bbfdf5a812c8a7ffb2b2cdda6720fb757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025287"
---
# <a name="pbm_deltapos-message"></a><span data-ttu-id="0ba38-104">PBM \_ DELTAPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="0ba38-104">PBM\_DELTAPOS message</span></span>

<span data-ttu-id="0ba38-105">依指定的遞增量將進度列的目前位置往前移，並重新繪製橫條以反映新的位置。</span><span class="sxs-lookup"><span data-stu-id="0ba38-105">Advances the current position of a progress bar by a specified increment and redraws the bar to reflect the new position.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ba38-106">參數</span><span class="sxs-lookup"><span data-stu-id="0ba38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ba38-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ba38-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ba38-108">要預先放置位置的數量。</span><span class="sxs-lookup"><span data-stu-id="0ba38-108">Amount to advance the position.</span></span>

</dd> <dt>

<span data-ttu-id="0ba38-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ba38-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0ba38-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0ba38-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ba38-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ba38-111">Return value</span></span>

<span data-ttu-id="0ba38-112">傳回先前的位置。</span><span class="sxs-lookup"><span data-stu-id="0ba38-112">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ba38-113">備註</span><span class="sxs-lookup"><span data-stu-id="0ba38-113">Remarks</span></span>

<span data-ttu-id="0ba38-114">如果增量產生的值超出控制項範圍，則位置會設定為最接近的界限。</span><span class="sxs-lookup"><span data-stu-id="0ba38-114">If the increment results in a value outside the range of the control, the position is set to the nearest boundary.</span></span>

<span data-ttu-id="0ba38-115">如果傳送給具有 [**PBS \_ 天棚**](progress-bar-control-styles.md) 樣式的控制項，則不會定義此訊息的行為。</span><span class="sxs-lookup"><span data-stu-id="0ba38-115">The behavior of this message is undefined if it is sent to a control that has the [**PBS\_MARQUEE**](progress-bar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ba38-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ba38-116">Requirements</span></span>



| <span data-ttu-id="0ba38-117">需求</span><span class="sxs-lookup"><span data-stu-id="0ba38-117">Requirement</span></span> | <span data-ttu-id="0ba38-118">值</span><span class="sxs-lookup"><span data-stu-id="0ba38-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba38-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ba38-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0ba38-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ba38-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ba38-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ba38-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0ba38-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ba38-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ba38-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0ba38-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ba38-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0ba38-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





