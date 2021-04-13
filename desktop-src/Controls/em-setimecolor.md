---
title: 'EM_SETIMECOLOR 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的輸入法) 組合色彩 (IME。
ms.assetid: ea5449c9-7d0f-4340-8e3e-1e0b77d443f6
keywords:
- EM_SETIMECOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c020bb3af2b1197afc005bd0b6efec82b609b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465712"
---
# <a name="em_setimecolor-message"></a><span data-ttu-id="bb40e-104">EM \_ SETIMECOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="bb40e-104">EM\_SETIMECOLOR message</span></span>

<span data-ttu-id="bb40e-105">設定 rich edit 控制項的輸入法) 組合色彩 (IME。</span><span class="sxs-lookup"><span data-stu-id="bb40e-105">Sets the Input Method Editor (IME) composition color for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="bb40e-106">只有 Microsoft Rich Edit 1.0 的亞洲語言版本才支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="bb40e-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="bb40e-107">任何較新版本都不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="bb40e-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="bb40e-108">參數</span><span class="sxs-lookup"><span data-stu-id="bb40e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb40e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb40e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb40e-110">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="bb40e-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bb40e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb40e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb40e-112">[**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor)結構的指標，其中包含要設定的組合色彩。</span><span class="sxs-lookup"><span data-stu-id="bb40e-112">Pointer to a [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) structure that contains the composition color to be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb40e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb40e-113">Return value</span></span>

<span data-ttu-id="bb40e-114">如果作業成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="bb40e-114">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="bb40e-115">如果作業失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="bb40e-115">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb40e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb40e-116">Requirements</span></span>



| <span data-ttu-id="bb40e-117">需求</span><span class="sxs-lookup"><span data-stu-id="bb40e-117">Requirement</span></span> | <span data-ttu-id="bb40e-118">值</span><span class="sxs-lookup"><span data-stu-id="bb40e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb40e-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb40e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bb40e-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb40e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb40e-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb40e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bb40e-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb40e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb40e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="bb40e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb40e-124"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb40e-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb40e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb40e-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb40e-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="bb40e-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bb40e-127">**EM \_ GETIMECOLOR**</span><span class="sxs-lookup"><span data-stu-id="bb40e-127">**EM\_GETIMECOLOR**</span></span>](em-getimecolor.md)
</dt> <dt>

[<span data-ttu-id="bb40e-128">**COMPCOLOR**</span><span class="sxs-lookup"><span data-stu-id="bb40e-128">**COMPCOLOR**</span></span>](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





