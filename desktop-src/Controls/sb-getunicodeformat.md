---
title: 'SB_GETUNICODEFORMAT 訊息 (Commctrl .h) '
description: SB_GETUNICODEFORMAT 訊息-抓取控制項的 Unicode 字元格式旗標。
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
ms.openlocfilehash: 857af43911a01ffc58b1a878be6e1875a44c76cb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085896"
---
# <a name="sb_getunicodeformat-message"></a><span data-ttu-id="ce4dc-104">SB \_ GETUNICODEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="ce4dc-104">SB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="ce4dc-105">抓取控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="ce4dc-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce4dc-106">參數</span><span class="sxs-lookup"><span data-stu-id="ce4dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce4dc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce4dc-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ce4dc-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ce4dc-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ce4dc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce4dc-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ce4dc-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ce4dc-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce4dc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce4dc-111">Return value</span></span>

<span data-ttu-id="ce4dc-112">傳回控制項的 Unicode 格式旗標。</span><span class="sxs-lookup"><span data-stu-id="ce4dc-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="ce4dc-113">如果這個值為非零值，則控制項會使用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="ce4dc-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="ce4dc-114">如果這個值為零，則控制項會使用 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="ce4dc-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce4dc-115">備註</span><span class="sxs-lookup"><span data-stu-id="ce4dc-115">Remarks</span></span>

<span data-ttu-id="ce4dc-116">如需此訊息的討論，請參閱 [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) 的備註。</span><span class="sxs-lookup"><span data-stu-id="ce4dc-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce4dc-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce4dc-117">Requirements</span></span>



| <span data-ttu-id="ce4dc-118">需求</span><span class="sxs-lookup"><span data-stu-id="ce4dc-118">Requirement</span></span> | <span data-ttu-id="ce4dc-119">值</span><span class="sxs-lookup"><span data-stu-id="ce4dc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce4dc-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce4dc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ce4dc-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce4dc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce4dc-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce4dc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ce4dc-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce4dc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce4dc-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ce4dc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce4dc-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce4dc-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce4dc-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce4dc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce4dc-127">**SB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="ce4dc-127">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md)
</dt> </dl>

 

 





