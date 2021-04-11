---
title: 'EM_SETBIDIOPTIONS 訊息 (Richedit .h) '
description: EM \_ SETBIDIOPTIONS 訊息會在 rich edit 控制項中設定雙向選項的目前狀態。
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- EM_SETBIDIOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dc4b92f7a989ab5ef283b36708094a143475de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105593"
---
# <a name="em_setbidioptions-message"></a><span data-ttu-id="8c8ad-104">EM \_ SETBIDIOPTIONS 訊息</span><span class="sxs-lookup"><span data-stu-id="8c8ad-104">EM\_SETBIDIOPTIONS message</span></span>

<span data-ttu-id="8c8ad-105">**EM \_ SETBIDIOPTIONS** 訊息會在 rich edit 控制項中設定雙向選項的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="8c8ad-105">The **EM\_SETBIDIOPTIONS** message sets the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c8ad-106">參數</span><span class="sxs-lookup"><span data-stu-id="8c8ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c8ad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c8ad-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c8ad-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="8c8ad-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8c8ad-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c8ad-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c8ad-110">[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)結構的指標，指出如何在 rich edit 控制項中設定雙向選項的狀態。</span><span class="sxs-lookup"><span data-stu-id="8c8ad-110">Pointer to a [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) structure that indicates how to set the state of the bidirectional options in the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c8ad-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c8ad-111">Return value</span></span>

<span data-ttu-id="8c8ad-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8c8ad-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c8ad-113">備註</span><span class="sxs-lookup"><span data-stu-id="8c8ad-113">Remarks</span></span>

<span data-ttu-id="8c8ad-114">Rich edit 控制項必須是純文字模式，否則 **EM \_ SETBIDIOPTIONS** 將不會進行任何動作。</span><span class="sxs-lookup"><span data-stu-id="8c8ad-114">The rich edit control must be in plain text mode or **EM\_SETBIDIOPTIONS** will not do anything.</span></span>

<span data-ttu-id="8c8ad-115">在純文字控制項中， **EM \_ SETBIDIOPTIONS** 會根據內容規則自動判斷段落方向和（或）對齊。</span><span class="sxs-lookup"><span data-stu-id="8c8ad-115">In plain text controls, **EM\_SETBIDIOPTIONS** automatically determines the paragraph direction and/or alignment based on the context rules.</span></span> <span data-ttu-id="8c8ad-116">這些規則會指出方向和/或對齊衍生自控制項中的第一個強字元。</span><span class="sxs-lookup"><span data-stu-id="8c8ad-116">These rules state that the direction and/or alignment is derived from the first strong character in the control.</span></span> <span data-ttu-id="8c8ad-117">強字元是指可從中判斷文字方向的字元 (請參閱 Unicode 標準2.0 版) 。</span><span class="sxs-lookup"><span data-stu-id="8c8ad-117">A strong character is one from which text direction can be determined (see Unicode Standard version 2.0).</span></span> <span data-ttu-id="8c8ad-118">段落方向和/或對齊會套用至預設格式。</span><span class="sxs-lookup"><span data-stu-id="8c8ad-118">The paragraph direction and/or alignment is applied to the default format.</span></span>

<span data-ttu-id="8c8ad-119">**EM \_SETBIDIOPTIONS** 只會將預設段落格式切換為 rtl (由右至左) 如果找到 RTL 字元，</span><span class="sxs-lookup"><span data-stu-id="8c8ad-119">**EM\_SETBIDIOPTIONS** only switches the default paragraph format to RTL (right to left) if it finds an RTL character,</span></span>

## <a name="requirements"></a><span data-ttu-id="8c8ad-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c8ad-120">Requirements</span></span>



| <span data-ttu-id="8c8ad-121">需求</span><span class="sxs-lookup"><span data-stu-id="8c8ad-121">Requirement</span></span> | <span data-ttu-id="8c8ad-122">值</span><span class="sxs-lookup"><span data-stu-id="8c8ad-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c8ad-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c8ad-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8c8ad-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c8ad-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c8ad-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c8ad-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8c8ad-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c8ad-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c8ad-127">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8c8ad-127">Redistributable</span></span><br/>          | <span data-ttu-id="8c8ad-128">Rich Edit 3。0</span><span class="sxs-lookup"><span data-stu-id="8c8ad-128">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="8c8ad-129">標頭</span><span class="sxs-lookup"><span data-stu-id="8c8ad-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c8ad-130"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c8ad-130"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c8ad-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c8ad-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="8c8ad-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="8c8ad-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8c8ad-133">**BIDIOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="8c8ad-133">**BIDIOPTIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[<span data-ttu-id="8c8ad-134">**EM \_ GETBIDIOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="8c8ad-134">**EM\_GETBIDIOPTIONS**</span></span>](em-getbidioptions.md)
</dt> </dl>

 

 





