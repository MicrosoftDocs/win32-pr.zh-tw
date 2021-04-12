---
title: 'TVM_GETUNICODEFORMAT 訊息 (Commctrl .h) '
description: 抓取控制項的 Unicode 字元格式旗標。 您可以明確地傳送此訊息，或使用 TreeView \_ GetUnicodeFormat 宏。
ms.assetid: d95f61b6-9ec1-4471-b24b-efe141428747
keywords:
- TVM_GETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88478d30e8da98ebf2e2325d6152087a14bc066a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024835"
---
# <a name="tvm_getunicodeformat-message"></a><span data-ttu-id="01d1f-105">TVM \_ GETUNICODEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="01d1f-105">TVM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="01d1f-106">抓取控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="01d1f-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="01d1f-107">您可以明確地傳送此訊息，或使用 [**TreeView \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getunicodeformat) 宏。</span><span class="sxs-lookup"><span data-stu-id="01d1f-107">You can send this message explicitly or use the [**TreeView\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="01d1f-108">參數</span><span class="sxs-lookup"><span data-stu-id="01d1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01d1f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01d1f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="01d1f-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="01d1f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="01d1f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01d1f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="01d1f-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="01d1f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01d1f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="01d1f-113">Return value</span></span>

<span data-ttu-id="01d1f-114">傳回控制項的 Unicode 格式旗標。</span><span class="sxs-lookup"><span data-stu-id="01d1f-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="01d1f-115">如果這個值為非零值，則控制項會使用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="01d1f-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="01d1f-116">如果這個值為零，則控制項會使用 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="01d1f-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="01d1f-117">備註</span><span class="sxs-lookup"><span data-stu-id="01d1f-117">Remarks</span></span>

<span data-ttu-id="01d1f-118">如需此訊息的討論，請參閱 [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) 的備註。</span><span class="sxs-lookup"><span data-stu-id="01d1f-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="01d1f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="01d1f-119">Requirements</span></span>



| <span data-ttu-id="01d1f-120">需求</span><span class="sxs-lookup"><span data-stu-id="01d1f-120">Requirement</span></span> | <span data-ttu-id="01d1f-121">值</span><span class="sxs-lookup"><span data-stu-id="01d1f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01d1f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01d1f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="01d1f-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01d1f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="01d1f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01d1f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="01d1f-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01d1f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="01d1f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="01d1f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="01d1f-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="01d1f-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01d1f-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01d1f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01d1f-129">**TVM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="01d1f-129">**TVM\_SETUNICODEFORMAT**</span></span>](tvm-setunicodeformat.md)
</dt> </dl>

 

 





