---
title: 'HDM_GETUNICODEFORMAT 訊息 (Commctrl .h) '
description: 取得控制項的 Unicode 字元格式旗標。 您可以明確地傳送此訊息，或使用標頭 \_ GetUnicodeFormat 宏。
ms.assetid: 2b36265a-023c-4083-a755-769461f3804b
keywords:
- HDM_GETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce625cc9d4c0ede0c4ce9b54dc852025b22d4870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103769"
---
# <a name="hdm_getunicodeformat-message"></a><span data-ttu-id="af5dd-105">HDM \_ GETUNICODEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="af5dd-105">HDM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="af5dd-106">取得控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="af5dd-106">Gets the Unicode character format flag for the control.</span></span> <span data-ttu-id="af5dd-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat) 宏。</span><span class="sxs-lookup"><span data-stu-id="af5dd-107">You can send this message explicitly or use the [**Header\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="af5dd-108">參數</span><span class="sxs-lookup"><span data-stu-id="af5dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af5dd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af5dd-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="af5dd-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="af5dd-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="af5dd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af5dd-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="af5dd-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="af5dd-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af5dd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="af5dd-113">Return value</span></span>

<span data-ttu-id="af5dd-114">傳回控制項的 Unicode 格式旗標。</span><span class="sxs-lookup"><span data-stu-id="af5dd-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="af5dd-115">如果這個值為非零值，則控制項會使用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="af5dd-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="af5dd-116">如果這個值為零，則控制項會使用 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="af5dd-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="af5dd-117">備註</span><span class="sxs-lookup"><span data-stu-id="af5dd-117">Remarks</span></span>

<span data-ttu-id="af5dd-118">如需此訊息的討論，請參閱 [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) 的備註。</span><span class="sxs-lookup"><span data-stu-id="af5dd-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="af5dd-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="af5dd-119">Requirements</span></span>



| <span data-ttu-id="af5dd-120">需求</span><span class="sxs-lookup"><span data-stu-id="af5dd-120">Requirement</span></span> | <span data-ttu-id="af5dd-121">值</span><span class="sxs-lookup"><span data-stu-id="af5dd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af5dd-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af5dd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="af5dd-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af5dd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af5dd-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af5dd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="af5dd-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af5dd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af5dd-126">標頭</span><span class="sxs-lookup"><span data-stu-id="af5dd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="af5dd-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="af5dd-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af5dd-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af5dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af5dd-129">**HDM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="af5dd-129">**HDM\_SETUNICODEFORMAT**</span></span>](hdm-setunicodeformat.md)
</dt> </dl>

 

 





