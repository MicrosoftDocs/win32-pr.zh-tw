---
title: 'CCM_SETUNICODEFORMAT 訊息 (Commctrl .h) '
description: 設定控制項的 Unicode 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。
ms.assetid: 8028b7d7-30d2-4154-81c7-ba1ed095ef02
keywords:
- CCM_SETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- CCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffbe9f5032c193cb612f68ca8ed6ec6b04ce8094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465916"
---
# <a name="ccm_setunicodeformat-message"></a><span data-ttu-id="d280f-105">CCM \_ SETUNICODEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="d280f-105">CCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="d280f-106">設定控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="d280f-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="d280f-107">此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。</span><span class="sxs-lookup"><span data-stu-id="d280f-107">This message enables you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d280f-108">參數</span><span class="sxs-lookup"><span data-stu-id="d280f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d280f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d280f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d280f-110">值，決定控制項所使用的字元集。</span><span class="sxs-lookup"><span data-stu-id="d280f-110">A value that determines the character set that is used by the control.</span></span> <span data-ttu-id="d280f-111">如果這個值為 **TRUE**，控制項將會使用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="d280f-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="d280f-112">如果這個值為 **FALSE**，控制項將會使用 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="d280f-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="d280f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d280f-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d280f-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="d280f-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d280f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d280f-115">Return value</span></span>

<span data-ttu-id="d280f-116">傳回控制項的先前 Unicode 格式旗標。</span><span class="sxs-lookup"><span data-stu-id="d280f-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d280f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d280f-117">Requirements</span></span>



| <span data-ttu-id="d280f-118">需求</span><span class="sxs-lookup"><span data-stu-id="d280f-118">Requirement</span></span> | <span data-ttu-id="d280f-119">值</span><span class="sxs-lookup"><span data-stu-id="d280f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d280f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d280f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d280f-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d280f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d280f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d280f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d280f-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d280f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d280f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d280f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d280f-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d280f-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d280f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d280f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d280f-127">**CCM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d280f-127">**CCM\_GETUNICODEFORMAT**</span></span>](ccm-getunicodeformat.md)
</dt> </dl>

 

 





