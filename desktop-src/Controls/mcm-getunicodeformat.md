---
title: 'MCM_GETUNICODEFORMAT 訊息 (Commctrl .h) '
description: 抓取控制項的 Unicode 字元格式旗標。 您可以明確地傳送此訊息，或使用 MonthCal \_ GetUnicodeFormat 宏。
ms.assetid: 28261e11-0fd0-407e-9f62-446536d62460
keywords:
- MCM_GETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4be573923f154958e1defd0be2adb02068076950
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686464"
---
# <a name="mcm_getunicodeformat-message"></a><span data-ttu-id="e2527-105">MCM \_ GETUNICODEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="e2527-105">MCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="e2527-106">抓取控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="e2527-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="e2527-107">您可以明確地傳送此訊息，或使用 [**MonthCal \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getunicodeformat) 宏。</span><span class="sxs-lookup"><span data-stu-id="e2527-107">You can send this message explicitly or use the [**MonthCal\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2527-108">參數</span><span class="sxs-lookup"><span data-stu-id="e2527-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2527-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2527-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e2527-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="e2527-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e2527-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2527-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e2527-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="e2527-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2527-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2527-113">Return value</span></span>

<span data-ttu-id="e2527-114">傳回控制項的 Unicode 格式旗標。</span><span class="sxs-lookup"><span data-stu-id="e2527-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="e2527-115">如果這個值為非零值，則控制項會使用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="e2527-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="e2527-116">如果這個值為零，則控制項會使用 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="e2527-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2527-117">備註</span><span class="sxs-lookup"><span data-stu-id="e2527-117">Remarks</span></span>

<span data-ttu-id="e2527-118">如需此訊息的討論，請參閱 [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) 的備註。</span><span class="sxs-lookup"><span data-stu-id="e2527-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2527-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2527-119">Requirements</span></span>



| <span data-ttu-id="e2527-120">需求</span><span class="sxs-lookup"><span data-stu-id="e2527-120">Requirement</span></span> | <span data-ttu-id="e2527-121">值</span><span class="sxs-lookup"><span data-stu-id="e2527-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2527-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2527-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e2527-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2527-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2527-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2527-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e2527-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2527-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2527-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e2527-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2527-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e2527-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2527-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2527-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2527-129">**MCM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="e2527-129">**MCM\_SETUNICODEFORMAT**</span></span>](mcm-setunicodeformat.md)
</dt> </dl>

 

 





