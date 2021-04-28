---
title: 'TB_GETUNICODEFORMAT 訊息 (Commctrl .h) '
description: TB_GETUNICODEFORMAT 訊息-抓取控制項的 Unicode 字元格式旗標。
ms.assetid: aadce646-daf1-4f1e-9171-2aeac12d3484
keywords:
- TB_GETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4beb5a5ff0b71dd76c85db2788d9dc91aa9f4957
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106786"
---
# <a name="tb_getunicodeformat-message"></a><span data-ttu-id="3cd77-104">TB \_ GETUNICODEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="3cd77-104">TB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="3cd77-105">抓取控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="3cd77-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3cd77-106">參數</span><span class="sxs-lookup"><span data-stu-id="3cd77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cd77-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3cd77-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3cd77-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3cd77-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3cd77-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3cd77-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3cd77-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3cd77-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cd77-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3cd77-111">Return value</span></span>

<span data-ttu-id="3cd77-112">傳回控制項的 Unicode 格式旗標。</span><span class="sxs-lookup"><span data-stu-id="3cd77-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="3cd77-113">如果這個值為非零值，則控制項會使用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="3cd77-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="3cd77-114">如果這個值為零，則控制項會使用 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="3cd77-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cd77-115">備註</span><span class="sxs-lookup"><span data-stu-id="3cd77-115">Remarks</span></span>

<span data-ttu-id="3cd77-116">如需此訊息的討論，請參閱 [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) 的備註。</span><span class="sxs-lookup"><span data-stu-id="3cd77-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cd77-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cd77-117">Requirements</span></span>



| <span data-ttu-id="3cd77-118">需求</span><span class="sxs-lookup"><span data-stu-id="3cd77-118">Requirement</span></span> | <span data-ttu-id="3cd77-119">值</span><span class="sxs-lookup"><span data-stu-id="3cd77-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3cd77-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3cd77-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3cd77-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cd77-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3cd77-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3cd77-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3cd77-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cd77-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3cd77-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3cd77-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cd77-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3cd77-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cd77-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3cd77-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cd77-127">**TB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="3cd77-127">**TB\_SETUNICODEFORMAT**</span></span>](tb-setunicodeformat.md)
</dt> </dl>

 

 





