---
title: 'UDM_GETUNICODEFORMAT 訊息 (Commctrl .h) '
description: UDM_GETUNICODEFORMAT 訊息-抓取控制項的 Unicode 字元格式旗標。
ms.assetid: 8c09d37b-95a2-49cd-b578-919f9c39fa8b
keywords:
- UDM_GETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 273164df7f7021f39ec26a22eb637e8b9969fc24
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113587"
---
# <a name="udm_getunicodeformat-message"></a><span data-ttu-id="18325-104">UDM \_ GETUNICODEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="18325-104">UDM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="18325-105">抓取控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="18325-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="18325-106">參數</span><span class="sxs-lookup"><span data-stu-id="18325-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18325-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="18325-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="18325-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="18325-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="18325-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="18325-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="18325-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="18325-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18325-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="18325-111">Return value</span></span>

<span data-ttu-id="18325-112">傳回控制項的 Unicode 格式旗標。</span><span class="sxs-lookup"><span data-stu-id="18325-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="18325-113">如果這個值為非零值，則控制項會使用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="18325-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="18325-114">如果這個值為零，則控制項會使用 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="18325-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="18325-115">備註</span><span class="sxs-lookup"><span data-stu-id="18325-115">Remarks</span></span>

<span data-ttu-id="18325-116">如需此訊息的討論，請參閱 [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) 的備註。</span><span class="sxs-lookup"><span data-stu-id="18325-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="18325-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="18325-117">Requirements</span></span>



| <span data-ttu-id="18325-118">需求</span><span class="sxs-lookup"><span data-stu-id="18325-118">Requirement</span></span> | <span data-ttu-id="18325-119">值</span><span class="sxs-lookup"><span data-stu-id="18325-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18325-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18325-120">Minimum supported client</span></span><br/> | <span data-ttu-id="18325-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18325-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="18325-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18325-122">Minimum supported server</span></span><br/> | <span data-ttu-id="18325-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18325-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="18325-124">標頭</span><span class="sxs-lookup"><span data-stu-id="18325-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="18325-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="18325-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18325-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18325-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18325-127">**UDM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="18325-127">**UDM\_SETUNICODEFORMAT**</span></span>](udm-setunicodeformat.md)
</dt> </dl>

 

 





