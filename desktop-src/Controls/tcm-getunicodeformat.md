---
title: 'TCM_GETUNICODEFORMAT 訊息 (Commctrl .h) '
description: 抓取控制項的 Unicode 字元格式旗標。 您可以明確地傳送此訊息，或使用 TabCtrl \_ GetUnicodeFormat 宏。
ms.assetid: 720e0325-500b-436c-8713-38ed780735bf
keywords:
- TCM_GETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b497f1b2c2b5ac55ee949b498602b50b267fef3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844175"
---
# <a name="tcm_getunicodeformat-message"></a><span data-ttu-id="bcc37-105">TCM \_ GETUNICODEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="bcc37-105">TCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="bcc37-106">抓取控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="bcc37-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="bcc37-107">您可以明確地傳送此訊息，或使用 [**TabCtrl \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) 宏。</span><span class="sxs-lookup"><span data-stu-id="bcc37-107">You can send this message explicitly or use the [**TabCtrl\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bcc37-108">參數</span><span class="sxs-lookup"><span data-stu-id="bcc37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcc37-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bcc37-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bcc37-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="bcc37-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bcc37-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bcc37-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bcc37-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="bcc37-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcc37-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bcc37-113">Return value</span></span>

<span data-ttu-id="bcc37-114">傳回控制項的 Unicode 格式旗標。</span><span class="sxs-lookup"><span data-stu-id="bcc37-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="bcc37-115">如果這個值為非零值，則控制項會使用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="bcc37-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="bcc37-116">如果這個值為零，則控制項會使用 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="bcc37-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcc37-117">備註</span><span class="sxs-lookup"><span data-stu-id="bcc37-117">Remarks</span></span>

<span data-ttu-id="bcc37-118">如需此訊息的討論，請參閱 [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) 的備註。</span><span class="sxs-lookup"><span data-stu-id="bcc37-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcc37-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="bcc37-119">Requirements</span></span>



| <span data-ttu-id="bcc37-120">需求</span><span class="sxs-lookup"><span data-stu-id="bcc37-120">Requirement</span></span> | <span data-ttu-id="bcc37-121">值</span><span class="sxs-lookup"><span data-stu-id="bcc37-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bcc37-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bcc37-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bcc37-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bcc37-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bcc37-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bcc37-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bcc37-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bcc37-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bcc37-126">標頭</span><span class="sxs-lookup"><span data-stu-id="bcc37-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcc37-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="bcc37-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcc37-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bcc37-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcc37-129">**TCM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="bcc37-129">**TCM\_SETUNICODEFORMAT**</span></span>](tcm-setunicodeformat.md)
</dt> </dl>

 

 





