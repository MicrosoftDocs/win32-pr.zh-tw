---
title: 'SB_GETUNICODEFORMAT 訊息 (Commctrl .h) '
description: 抓取控制項的 Unicode 字元格式旗標。
ms.assetid: 0b2b543a-b1ef-452c-9b34-c5fbbac4aaa9
keywords:
- SB_GETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- SB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dbb639a04f0a40d9d5e11b938aaadbcc8b4c730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509019"
---
# <a name="sb_getunicodeformat-message"></a><span data-ttu-id="7141b-104">SB \_ GETUNICODEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="7141b-104">SB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="7141b-105">抓取控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="7141b-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7141b-106">參數</span><span class="sxs-lookup"><span data-stu-id="7141b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7141b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7141b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7141b-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="7141b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7141b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7141b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7141b-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="7141b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7141b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7141b-111">Return value</span></span>

<span data-ttu-id="7141b-112">傳回控制項的 Unicode 格式旗標。</span><span class="sxs-lookup"><span data-stu-id="7141b-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="7141b-113">如果這個值為非零值，則控制項會使用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="7141b-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="7141b-114">如果這個值為零，則控制項會使用 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="7141b-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="7141b-115">備註</span><span class="sxs-lookup"><span data-stu-id="7141b-115">Remarks</span></span>

<span data-ttu-id="7141b-116">如需此訊息的討論，請參閱 [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) 的備註。</span><span class="sxs-lookup"><span data-stu-id="7141b-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7141b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="7141b-117">Requirements</span></span>



| <span data-ttu-id="7141b-118">需求</span><span class="sxs-lookup"><span data-stu-id="7141b-118">Requirement</span></span> | <span data-ttu-id="7141b-119">值</span><span class="sxs-lookup"><span data-stu-id="7141b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7141b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7141b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7141b-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7141b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7141b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7141b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7141b-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7141b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7141b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="7141b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7141b-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7141b-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7141b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7141b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7141b-127">**SB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="7141b-127">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md)
</dt> </dl>

 

 





