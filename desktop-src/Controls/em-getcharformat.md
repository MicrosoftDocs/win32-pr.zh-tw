---
title: 'EM_GETCHARFORMAT 訊息 (Richedit .h) '
description: 判斷 rich edit 控制項中的字元格式。
ms.assetid: 210b8719-5ed7-49f2-bd93-8a4e1efab1e8
keywords:
- EM_GETCHARFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd71db4d3a13f2acfe33c2843b0d9aad46c6f9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025180"
---
# <a name="em_getcharformat-message"></a><span data-ttu-id="da5d5-104">EM \_ GETCHARFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="da5d5-104">EM\_GETCHARFORMAT message</span></span>

<span data-ttu-id="da5d5-105">判斷 rich edit 控制項中的字元格式。</span><span class="sxs-lookup"><span data-stu-id="da5d5-105">Determines the character formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="da5d5-106">參數</span><span class="sxs-lookup"><span data-stu-id="da5d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da5d5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da5d5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da5d5-108">指定要從其中抓取格式的文字範圍。</span><span class="sxs-lookup"><span data-stu-id="da5d5-108">Specifies the range of text from which to retrieve formatting.</span></span> <span data-ttu-id="da5d5-109">它可以是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="da5d5-109">It can be one of the following values.</span></span>



| <span data-ttu-id="da5d5-110">值</span><span class="sxs-lookup"><span data-stu-id="da5d5-110">Value</span></span>                                                                                                                                                         | <span data-ttu-id="da5d5-111">意義</span><span class="sxs-lookup"><span data-stu-id="da5d5-111">Meaning</span></span>                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <span data-ttu-id="da5d5-112"><dt>**SCF \_ 預設值**</dt></span><span class="sxs-lookup"><span data-stu-id="da5d5-112"><dt>**SCF\_DEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="da5d5-113">預設的字元格式。</span><span class="sxs-lookup"><span data-stu-id="da5d5-113">The default character formatting.</span></span><br/>             |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <span data-ttu-id="da5d5-114"><dt>**SCF \_ 選取專案**</dt></span><span class="sxs-lookup"><span data-stu-id="da5d5-114"><dt>**SCF\_SELECTION**</dt></span></span> </dl> | <span data-ttu-id="da5d5-115">目前選取範圍的字元格式。</span><span class="sxs-lookup"><span data-stu-id="da5d5-115">The current selection's character formatting.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="da5d5-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da5d5-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da5d5-117">[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)結構，此結構會接收第一個字元的屬性。</span><span class="sxs-lookup"><span data-stu-id="da5d5-117">A [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure that receives the attributes of the first character.</span></span> <span data-ttu-id="da5d5-118">**DwMask** 成員會指定整個選取範圍中的屬性是一致的。</span><span class="sxs-lookup"><span data-stu-id="da5d5-118">The **dwMask** member specifies which attributes are consistent throughout the entire selection.</span></span> <span data-ttu-id="da5d5-119">例如，如果整個選取範圍是斜體或不是斜體，則 \_ 會設定 CFM 斜體; 如果選取範圍部分為斜體，則 \_ 不會設定 CFM 斜體。</span><span class="sxs-lookup"><span data-stu-id="da5d5-119">For example, if the entire selection is either in italics or not in italics, CFM\_ITALIC is set; if the selection is partly in italics and partly not, CFM\_ITALIC is not set.</span></span>

<span data-ttu-id="da5d5-120">Microsoft Rich Edit 2.0 和更新版本：此參數可以是 [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) 結構的指標，也就是 [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) 結構的延伸。</span><span class="sxs-lookup"><span data-stu-id="da5d5-120">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure, which is an extension of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span> <span data-ttu-id="da5d5-121">傳送 **EM \_ GETCHARFORMAT** 訊息之前，請先設定結構的 **cbSize** 成員來指出結構的版本。</span><span class="sxs-lookup"><span data-stu-id="da5d5-121">Before sending the **EM\_GETCHARFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da5d5-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="da5d5-122">Return value</span></span>

<span data-ttu-id="da5d5-123">此訊息會傳回 [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)結構之 **dwMask** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="da5d5-123">This message returns the value of the **dwMask** member of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="da5d5-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="da5d5-124">Requirements</span></span>



| <span data-ttu-id="da5d5-125">需求</span><span class="sxs-lookup"><span data-stu-id="da5d5-125">Requirement</span></span> | <span data-ttu-id="da5d5-126">值</span><span class="sxs-lookup"><span data-stu-id="da5d5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da5d5-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da5d5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="da5d5-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da5d5-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="da5d5-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da5d5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="da5d5-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da5d5-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da5d5-131">標頭</span><span class="sxs-lookup"><span data-stu-id="da5d5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="da5d5-132"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="da5d5-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da5d5-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da5d5-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="da5d5-134">**參考**</span><span class="sxs-lookup"><span data-stu-id="da5d5-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="da5d5-135">**CHARFORMAT**</span><span class="sxs-lookup"><span data-stu-id="da5d5-135">**CHARFORMAT**</span></span>](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[<span data-ttu-id="da5d5-136">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="da5d5-136">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





