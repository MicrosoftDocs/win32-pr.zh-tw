---
title: 'EM_GETPARAFORMAT 訊息 (Richedit .h) '
description: 抓取 rich edit 控制項中目前選取範圍的段落格式。
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- EM_GETPARAFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49060861a955e85d153fc9041c9b364db109f83a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934913"
---
# <a name="em_getparaformat-message"></a><span data-ttu-id="fa734-104">EM \_ GETPARAFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="fa734-104">EM\_GETPARAFORMAT message</span></span>

<span data-ttu-id="fa734-105">抓取 rich edit 控制項中目前選取範圍的段落格式。</span><span class="sxs-lookup"><span data-stu-id="fa734-105">Retrieves the paragraph formatting of the current selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa734-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa734-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa734-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa734-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa734-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="fa734-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fa734-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa734-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa734-110">[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)結構的指標，此結構會接收目前選取範圍的段落格式化屬性。</span><span class="sxs-lookup"><span data-stu-id="fa734-110">Pointer to a [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure that receives the paragraph formatting attributes of the current selection.</span></span>

<span data-ttu-id="fa734-111">如果選取了一個以上的段落，結構會接收第一個段落的屬性，而 **dwMask** 成員會指定整個選取範圍中的屬性是一致的。</span><span class="sxs-lookup"><span data-stu-id="fa734-111">If more than one paragraph is selected, the structure receives the attributes of the first paragraph, and the **dwMask** member specifies which attributes are consistent throughout the entire selection.</span></span>

<span data-ttu-id="fa734-112">Microsoft Rich Edit 2.0 和更新版本：此參數可以是 [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) 結構的指標，也就是 [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) 結構的延伸。</span><span class="sxs-lookup"><span data-stu-id="fa734-112">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure, which is an extension of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span> <span data-ttu-id="fa734-113">傳送 **EM \_ GETPARAFORMAT** 訊息之前，請先設定結構的 **cbSize** 成員來指出結構的版本。</span><span class="sxs-lookup"><span data-stu-id="fa734-113">Before sending the **EM\_GETPARAFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa734-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa734-114">Return value</span></span>

<span data-ttu-id="fa734-115">此訊息會傳回 [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)結構之 **dwMask** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="fa734-115">This message returns the value of the **dwMask** member of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa734-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa734-116">Requirements</span></span>



| <span data-ttu-id="fa734-117">需求</span><span class="sxs-lookup"><span data-stu-id="fa734-117">Requirement</span></span> | <span data-ttu-id="fa734-118">值</span><span class="sxs-lookup"><span data-stu-id="fa734-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa734-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa734-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fa734-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa734-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa734-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa734-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fa734-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa734-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa734-123">標頭</span><span class="sxs-lookup"><span data-stu-id="fa734-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa734-124"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa734-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa734-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa734-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="fa734-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="fa734-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fa734-127">**PARAFORMAT**</span><span class="sxs-lookup"><span data-stu-id="fa734-127">**PARAFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[<span data-ttu-id="fa734-128">**PARAFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="fa734-128">**PARAFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





