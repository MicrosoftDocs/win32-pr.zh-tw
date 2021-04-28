---
title: 'TBM_GETUNICODEFORMAT 訊息 (Commctrl .h) '
description: TBM_GETUNICODEFORMAT 訊息-抓取控制項的 Unicode 字元格式旗標。
ms.assetid: cecd7e55-f482-4381-bde8-a60b8c5173eb
keywords:
- TBM_GETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82e7424a4e561ee8f8be79135309089fe4bb0bf9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104086"
---
# <a name="tbm_getunicodeformat-message"></a><span data-ttu-id="9e272-104">TBM \_ GETUNICODEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="9e272-104">TBM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="9e272-105">抓取控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="9e272-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e272-106">參數</span><span class="sxs-lookup"><span data-stu-id="9e272-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e272-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e272-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9e272-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9e272-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9e272-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e272-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9e272-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9e272-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e272-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e272-111">Return value</span></span>

<span data-ttu-id="9e272-112">傳回控制項的 Unicode 格式旗標。</span><span class="sxs-lookup"><span data-stu-id="9e272-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="9e272-113">如果這個值為非零值，則控制項會使用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="9e272-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="9e272-114">如果這個值為零，則控制項會使用 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="9e272-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e272-115">備註</span><span class="sxs-lookup"><span data-stu-id="9e272-115">Remarks</span></span>

<span data-ttu-id="9e272-116">如需此訊息的討論，請參閱 [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) 的備註。</span><span class="sxs-lookup"><span data-stu-id="9e272-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e272-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e272-117">Requirements</span></span>



| <span data-ttu-id="9e272-118">需求</span><span class="sxs-lookup"><span data-stu-id="9e272-118">Requirement</span></span> | <span data-ttu-id="9e272-119">值</span><span class="sxs-lookup"><span data-stu-id="9e272-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e272-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e272-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9e272-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e272-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e272-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e272-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9e272-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e272-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e272-124">標頭</span><span class="sxs-lookup"><span data-stu-id="9e272-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e272-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9e272-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e272-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e272-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e272-127">**TBM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="9e272-127">**TBM\_SETUNICODEFORMAT**</span></span>](tbm-setunicodeformat.md)
</dt> </dl>

 

 





