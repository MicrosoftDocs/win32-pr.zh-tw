---
title: 'EM_SETPARAFORMAT 訊息 (Richedit .h) '
description: 設定 rich edit 控制項中目前選取範圍的段落格式。
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- EM_SETPARAFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8780ed79650a90a8d85ee8025dbe97e9af36aa1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465056"
---
# <a name="em_setparaformat-message"></a><span data-ttu-id="3f03d-104">EM \_ SETPARAFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="3f03d-104">EM\_SETPARAFORMAT message</span></span>

<span data-ttu-id="3f03d-105">設定 rich edit 控制項中目前選取範圍的段落格式。</span><span class="sxs-lookup"><span data-stu-id="3f03d-105">Sets the paragraph formatting for the current selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3f03d-106">參數</span><span class="sxs-lookup"><span data-stu-id="3f03d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f03d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3f03d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f03d-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="3f03d-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3f03d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f03d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f03d-110">[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)結構的指標，指定新段落格式化屬性。</span><span class="sxs-lookup"><span data-stu-id="3f03d-110">Pointer to a [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure specifying the new paragraph formatting attributes.</span></span> <span data-ttu-id="3f03d-111">只有 **dwMask** 成員所指定的屬性才會變更。</span><span class="sxs-lookup"><span data-stu-id="3f03d-111">Only the attributes specified by the **dwMask** member are changed.</span></span>

<span data-ttu-id="3f03d-112">Microsoft Rich Edit 2.0 和更新版本：此參數可以是 [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) 結構的指標，也就是 [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) 結構的延伸。</span><span class="sxs-lookup"><span data-stu-id="3f03d-112">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure, which is an extension of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span> <span data-ttu-id="3f03d-113">傳送 **EM \_ SETPARAFORMAT** 訊息之前，請先設定結構的 **cbSize** 成員來指出結構的版本。</span><span class="sxs-lookup"><span data-stu-id="3f03d-113">Before sending the **EM\_SETPARAFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f03d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3f03d-114">Return value</span></span>

<span data-ttu-id="3f03d-115">如果作業成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="3f03d-115">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="3f03d-116">如果作業失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="3f03d-116">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f03d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f03d-117">Requirements</span></span>



| <span data-ttu-id="3f03d-118">需求</span><span class="sxs-lookup"><span data-stu-id="3f03d-118">Requirement</span></span> | <span data-ttu-id="3f03d-119">值</span><span class="sxs-lookup"><span data-stu-id="3f03d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f03d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f03d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3f03d-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f03d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3f03d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f03d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3f03d-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f03d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3f03d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3f03d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f03d-125"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="3f03d-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f03d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f03d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="3f03d-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="3f03d-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3f03d-128">**PARAFORMAT**</span><span class="sxs-lookup"><span data-stu-id="3f03d-128">**PARAFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[<span data-ttu-id="3f03d-129">**PARAFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="3f03d-129">**PARAFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





