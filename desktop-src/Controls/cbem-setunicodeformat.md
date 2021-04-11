---
title: 'CBEM_SETUNICODEFORMAT 訊息 (Commctrl .h) '
description: 設定控制項的 UNICODE 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。
ms.assetid: 4811709b-1639-4468-8598-97d9dc8d9057
keywords:
- CBEM_SETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89540d4e942b8b705685c13addeeb17adf0b4f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105762"
---
# <a name="cbem_setunicodeformat-message"></a><span data-ttu-id="87dc7-105">CBEM \_ SETUNICODEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="87dc7-105">CBEM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="87dc7-106">設定控制項的 UNICODE 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="87dc7-106">Sets the UNICODE character format flag for the control.</span></span> <span data-ttu-id="87dc7-107">此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。</span><span class="sxs-lookup"><span data-stu-id="87dc7-107">This message enables you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="87dc7-108">參數</span><span class="sxs-lookup"><span data-stu-id="87dc7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87dc7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87dc7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87dc7-110">決定控制項所使用的字元集。</span><span class="sxs-lookup"><span data-stu-id="87dc7-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="87dc7-111">如果這個值為非零值，控制項將會使用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="87dc7-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="87dc7-112">如果這個值為零，控制項將會使用 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="87dc7-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="87dc7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87dc7-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="87dc7-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="87dc7-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87dc7-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="87dc7-115">Return value</span></span>

<span data-ttu-id="87dc7-116">傳回控制項的先前 Unicode 格式旗標。</span><span class="sxs-lookup"><span data-stu-id="87dc7-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="87dc7-117">備註</span><span class="sxs-lookup"><span data-stu-id="87dc7-117">Remarks</span></span>

<span data-ttu-id="87dc7-118">如需此訊息的討論，請參閱 [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) 的備註。</span><span class="sxs-lookup"><span data-stu-id="87dc7-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="87dc7-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="87dc7-119">Requirements</span></span>



| <span data-ttu-id="87dc7-120">需求</span><span class="sxs-lookup"><span data-stu-id="87dc7-120">Requirement</span></span> | <span data-ttu-id="87dc7-121">值</span><span class="sxs-lookup"><span data-stu-id="87dc7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87dc7-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87dc7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="87dc7-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87dc7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87dc7-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87dc7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="87dc7-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87dc7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87dc7-126">標頭</span><span class="sxs-lookup"><span data-stu-id="87dc7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="87dc7-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="87dc7-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87dc7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87dc7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87dc7-129">**CBEM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="87dc7-129">**CBEM\_GETUNICODEFORMAT**</span></span>](cbem-getunicodeformat.md)
</dt> </dl>

 

 





