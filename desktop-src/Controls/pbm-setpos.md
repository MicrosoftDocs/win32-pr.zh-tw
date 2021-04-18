---
title: 'PBM_SETPOS 訊息 (Commctrl .h) '
description: 設定進度列的目前位置，並重新繪製橫條以反映新的位置。
ms.assetid: 9ebeaa19-0f42-4af7-85d8-aae22498fd6f
keywords:
- PBM_SETPOS message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a157f6a220f4932d39d13f08df79afa99d7348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968576"
---
# <a name="pbm_setpos-message"></a><span data-ttu-id="2a73c-104">PBM \_ SETPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="2a73c-104">PBM\_SETPOS message</span></span>

<span data-ttu-id="2a73c-105">設定進度列的目前位置，並重新繪製橫條以反映新的位置。</span><span class="sxs-lookup"><span data-stu-id="2a73c-105">Sets the current position for a progress bar and redraws the bar to reflect the new position.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a73c-106">參數</span><span class="sxs-lookup"><span data-stu-id="2a73c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a73c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a73c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a73c-108">成為新位置的帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="2a73c-108">Signed integer that becomes the new position.</span></span>

</dd> <dt>

<span data-ttu-id="2a73c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a73c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2a73c-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2a73c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a73c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a73c-111">Return value</span></span>

<span data-ttu-id="2a73c-112">傳回先前的位置。</span><span class="sxs-lookup"><span data-stu-id="2a73c-112">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a73c-113">備註</span><span class="sxs-lookup"><span data-stu-id="2a73c-113">Remarks</span></span>

<span data-ttu-id="2a73c-114">如果 *wParam* 超出控制項的範圍，則位置會設定為最接近的界限。</span><span class="sxs-lookup"><span data-stu-id="2a73c-114">If *wParam* is outside the range of the control, the position is set to the closest boundary.</span></span>

<span data-ttu-id="2a73c-115">請勿將此訊息傳送至具有 [**PBS \_ 字幕**](progress-bar-control-styles.md) 樣式的控制項。</span><span class="sxs-lookup"><span data-stu-id="2a73c-115">Do not send this message to a control that has the [**PBS\_MARQUEE**](progress-bar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a73c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a73c-116">Requirements</span></span>



| <span data-ttu-id="2a73c-117">需求</span><span class="sxs-lookup"><span data-stu-id="2a73c-117">Requirement</span></span> | <span data-ttu-id="2a73c-118">值</span><span class="sxs-lookup"><span data-stu-id="2a73c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a73c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a73c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2a73c-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a73c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a73c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a73c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2a73c-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a73c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a73c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="2a73c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a73c-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2a73c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





