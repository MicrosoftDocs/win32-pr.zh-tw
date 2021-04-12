---
title: 'MCM_SETUNICODEFORMAT 訊息 (Commctrl .h) '
description: 設定控制項的 Unicode 字元格式旗標。
ms.assetid: 250789b5-694b-4502-9cc0-3bc260ea06e7
keywords:
- MCM_SETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0aee3318479f4e94b4d85f15fe7c58e4417a1bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465473"
---
# <a name="mcm_setunicodeformat-message"></a><span data-ttu-id="27537-104">MCM \_ SETUNICODEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="27537-104">MCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="27537-105">設定控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="27537-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="27537-106">此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。</span><span class="sxs-lookup"><span data-stu-id="27537-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="27537-107">您可以明確地傳送此訊息，或使用 [**MonthCal \_ SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat) 宏。</span><span class="sxs-lookup"><span data-stu-id="27537-107">You can send this message explicitly or use the [**MonthCal\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="27537-108">參數</span><span class="sxs-lookup"><span data-stu-id="27537-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27537-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27537-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27537-110">決定控制項所使用的字元集。</span><span class="sxs-lookup"><span data-stu-id="27537-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="27537-111">如果這個值為非零值，控制項將會使用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="27537-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="27537-112">如果這個值為零，控制項將會使用 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="27537-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="27537-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27537-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="27537-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="27537-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27537-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="27537-115">Return value</span></span>

<span data-ttu-id="27537-116">傳回控制項的先前 Unicode 格式旗標。</span><span class="sxs-lookup"><span data-stu-id="27537-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="27537-117">備註</span><span class="sxs-lookup"><span data-stu-id="27537-117">Remarks</span></span>

<span data-ttu-id="27537-118">如需此訊息的討論，請參閱 [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) 的備註。</span><span class="sxs-lookup"><span data-stu-id="27537-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="27537-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="27537-119">Requirements</span></span>



| <span data-ttu-id="27537-120">需求</span><span class="sxs-lookup"><span data-stu-id="27537-120">Requirement</span></span> | <span data-ttu-id="27537-121">值</span><span class="sxs-lookup"><span data-stu-id="27537-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27537-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27537-122">Minimum supported client</span></span><br/> | <span data-ttu-id="27537-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27537-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="27537-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27537-124">Minimum supported server</span></span><br/> | <span data-ttu-id="27537-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27537-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27537-126">標頭</span><span class="sxs-lookup"><span data-stu-id="27537-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="27537-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="27537-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27537-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27537-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27537-129">**MCM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="27537-129">**MCM\_GETUNICODEFORMAT**</span></span>](mcm-getunicodeformat.md)
</dt> </dl>

 

 





