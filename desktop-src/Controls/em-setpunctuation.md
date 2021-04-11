---
title: 'EM_SETPUNCTUATION 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的標點符號字元。
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- EM_SETPUNCTUATION message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710392cee7f7a1fb04fce59d6549134255499172
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105569"
---
# <a name="em_setpunctuation-message"></a><span data-ttu-id="c4ee4-104">EM \_ SETPUNCTUATION 訊息</span><span class="sxs-lookup"><span data-stu-id="c4ee4-104">EM\_SETPUNCTUATION message</span></span>

<span data-ttu-id="c4ee4-105">設定 rich edit 控制項的標點符號字元。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-105">Sets the punctuation characters for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="c4ee4-106">只有 Microsoft Rich Edit 1.0 的亞洲語言版本才支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="c4ee4-107">任何較新版本都不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="c4ee4-108">參數</span><span class="sxs-lookup"><span data-stu-id="c4ee4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4ee4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4ee4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4ee4-110">指定標點符號類型，它可以是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-110">Specifies the punctuation type, which can be one of the following values.</span></span>



| <span data-ttu-id="c4ee4-111">值</span><span class="sxs-lookup"><span data-stu-id="c4ee4-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="c4ee4-112">意義</span><span class="sxs-lookup"><span data-stu-id="c4ee4-112">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <span data-ttu-id="c4ee4-113"><dt>**電腦 \_ 領先**</dt></span><span class="sxs-lookup"><span data-stu-id="c4ee4-113"><dt>**PC\_LEADING**</dt></span></span> </dl>       | <span data-ttu-id="c4ee4-114">前置標點符號字元。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-114">Leading punctuation characters.</span></span><br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <span data-ttu-id="c4ee4-115"><dt>**電腦 \_ 遵循**</dt></span><span class="sxs-lookup"><span data-stu-id="c4ee4-115"><dt>**PC\_FOLLOWING**</dt></span></span> </dl> | <span data-ttu-id="c4ee4-116">下列標點符號字元。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-116">Following punctuation characters.</span></span><br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <span data-ttu-id="c4ee4-117"><dt>**電腦 \_ 分隔符號**</dt></span><span class="sxs-lookup"><span data-stu-id="c4ee4-117"><dt>**PC\_DELIMITER**</dt></span></span> </dl> | <span data-ttu-id="c4ee4-118">分隔符號。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-118">Delimiter.</span></span><br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <span data-ttu-id="c4ee4-119"><dt>**電腦 \_溢** 位</dt></span><span class="sxs-lookup"><span data-stu-id="c4ee4-119"><dt>**PC\_OVERFLOW** </dt></span></span> </dl> | <span data-ttu-id="c4ee4-120">不支援。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-120">Not supported.</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="c4ee4-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4ee4-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4ee4-122">包含標點符號字元之 [**標點符號**](/windows/desktop/api/Richedit/ns-richedit-punctuation) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-122">Pointer to a [**PUNCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation) structure that contains the punctuation characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4ee4-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4ee4-123">Return value</span></span>

<span data-ttu-id="c4ee4-124">如果作業成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-124">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c4ee4-125">如果作業失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-125">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4ee4-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4ee4-126">Requirements</span></span>



| <span data-ttu-id="c4ee4-127">需求</span><span class="sxs-lookup"><span data-stu-id="c4ee4-127">Requirement</span></span> | <span data-ttu-id="c4ee4-128">值</span><span class="sxs-lookup"><span data-stu-id="c4ee4-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ee4-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4ee4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c4ee4-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4ee4-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c4ee4-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4ee4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c4ee4-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4ee4-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4ee4-133">標頭</span><span class="sxs-lookup"><span data-stu-id="c4ee4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4ee4-134"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4ee4-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4ee4-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4ee4-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="c4ee4-136">**參考**</span><span class="sxs-lookup"><span data-stu-id="c4ee4-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c4ee4-137">**EM \_ GETPUNCTUATION**</span><span class="sxs-lookup"><span data-stu-id="c4ee4-137">**EM\_GETPUNCTUATION**</span></span>](em-getpunctuation.md)
</dt> <dt>

[<span data-ttu-id="c4ee4-138">**標點符號**</span><span class="sxs-lookup"><span data-stu-id="c4ee4-138">**PUNCTUATION**</span></span>](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





