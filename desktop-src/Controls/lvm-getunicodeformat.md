---
title: 'LVM_GETUNICODEFORMAT 訊息 (Commctrl .h) '
description: 抓取控制項的 UNICODE 字元格式旗標。 您可以明確地傳送此訊息，或使用 ListView \_ GetUnicodeFormat 宏。
ms.assetid: b0598b60-4d0e-4c68-b63a-e614c6268129
keywords:
- LVM_GETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720a65baab8ec9c1ec3b311e49fe3672c97a0fba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844088"
---
# <a name="lvm_getunicodeformat-message"></a><span data-ttu-id="da3d5-105">LVM \_ GETUNICODEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="da3d5-105">LVM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="da3d5-106">抓取控制項的 UNICODE 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="da3d5-106">Retrieves the UNICODE character format flag for the control.</span></span> <span data-ttu-id="da3d5-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat) 宏。</span><span class="sxs-lookup"><span data-stu-id="da3d5-107">You can send this message explicitly or use the [**ListView\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="da3d5-108">參數</span><span class="sxs-lookup"><span data-stu-id="da3d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da3d5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da3d5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="da3d5-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="da3d5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="da3d5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da3d5-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="da3d5-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="da3d5-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da3d5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="da3d5-113">Return value</span></span>

<span data-ttu-id="da3d5-114">傳回控制項的 Unicode 格式旗標。</span><span class="sxs-lookup"><span data-stu-id="da3d5-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="da3d5-115">如果這個值為非零值，則控制項會使用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="da3d5-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="da3d5-116">如果這個值為零，則控制項會使用 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="da3d5-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="da3d5-117">備註</span><span class="sxs-lookup"><span data-stu-id="da3d5-117">Remarks</span></span>

<span data-ttu-id="da3d5-118">如需此訊息的討論，請參閱 [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) 的備註。</span><span class="sxs-lookup"><span data-stu-id="da3d5-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="da3d5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="da3d5-119">Requirements</span></span>



| <span data-ttu-id="da3d5-120">需求</span><span class="sxs-lookup"><span data-stu-id="da3d5-120">Requirement</span></span> | <span data-ttu-id="da3d5-121">值</span><span class="sxs-lookup"><span data-stu-id="da3d5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da3d5-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da3d5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="da3d5-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da3d5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="da3d5-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da3d5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="da3d5-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da3d5-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da3d5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="da3d5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="da3d5-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="da3d5-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da3d5-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da3d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da3d5-129">**LVM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="da3d5-129">**LVM\_SETUNICODEFORMAT**</span></span>](lvm-setunicodeformat.md)
</dt> </dl>

 

 





