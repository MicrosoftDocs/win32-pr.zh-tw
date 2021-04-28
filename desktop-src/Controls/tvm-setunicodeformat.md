---
title: 'TVM_SETUNICODEFORMAT 訊息 (Commctrl .h) '
description: TVM_SETUNICODEFORMAT 訊息：設定控制項的 Unicode 字元格式旗標。
ms.assetid: e4b58ae5-6217-4a2e-80e5-3ba9e578859a
keywords:
- TVM_SETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b49fcdd22cff0ac91885ef8f54d49922f9c677e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116546"
---
# <a name="tvm_setunicodeformat-message"></a><span data-ttu-id="febcd-104">TVM \_ SETUNICODEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="febcd-104">TVM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="febcd-105">設定控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="febcd-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="febcd-106">此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。</span><span class="sxs-lookup"><span data-stu-id="febcd-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="febcd-107">您可以明確地傳送此訊息，或使用 [**TreeView \_ SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setunicodeformat) 宏。</span><span class="sxs-lookup"><span data-stu-id="febcd-107">You can send this message explicitly or use the [**TreeView\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="febcd-108">參數</span><span class="sxs-lookup"><span data-stu-id="febcd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="febcd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="febcd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="febcd-110">決定控制項所使用的字元集。</span><span class="sxs-lookup"><span data-stu-id="febcd-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="febcd-111">如果這個值為非零值，控制項將會使用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="febcd-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="febcd-112">如果這個值為零，控制項將會使用 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="febcd-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="febcd-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="febcd-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="febcd-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="febcd-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="febcd-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="febcd-115">Return value</span></span>

<span data-ttu-id="febcd-116">傳回控制項的先前 Unicode 格式旗標。</span><span class="sxs-lookup"><span data-stu-id="febcd-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="febcd-117">備註</span><span class="sxs-lookup"><span data-stu-id="febcd-117">Remarks</span></span>

<span data-ttu-id="febcd-118">如需此訊息的討論，請參閱 [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) 的備註。</span><span class="sxs-lookup"><span data-stu-id="febcd-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="febcd-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="febcd-119">Requirements</span></span>



| <span data-ttu-id="febcd-120">需求</span><span class="sxs-lookup"><span data-stu-id="febcd-120">Requirement</span></span> | <span data-ttu-id="febcd-121">值</span><span class="sxs-lookup"><span data-stu-id="febcd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="febcd-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="febcd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="febcd-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="febcd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="febcd-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="febcd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="febcd-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="febcd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="febcd-126">標頭</span><span class="sxs-lookup"><span data-stu-id="febcd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="febcd-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="febcd-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="febcd-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="febcd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="febcd-129">**TVM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="febcd-129">**TVM\_GETUNICODEFORMAT**</span></span>](tvm-getunicodeformat.md)
</dt> </dl>

 

 





