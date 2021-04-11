---
title: 'EM_GETPUNCTUATION 訊息 (Richedit .h) '
description: 取得 rich edit 控制項的目前標點符號字元。
ms.assetid: 1c04967b-d75e-4f54-b35b-cd50bac9cdfa
keywords:
- EM_GETPUNCTUATION message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158c26deca3328d9cdbed7ffe7cf885b0582d1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105299"
---
# <a name="em_getpunctuation-message"></a><span data-ttu-id="5b704-104">EM \_ GETPUNCTUATION 訊息</span><span class="sxs-lookup"><span data-stu-id="5b704-104">EM\_GETPUNCTUATION message</span></span>

<span data-ttu-id="5b704-105">取得 rich edit 控制項的目前標點符號字元。</span><span class="sxs-lookup"><span data-stu-id="5b704-105">Gets the current punctuation characters for the rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="5b704-106">只有 Microsoft Rich Edit 1.0 的亞洲語言版本才支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="5b704-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="5b704-107">任何較新版本的 Rich Edit 都不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="5b704-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="5b704-108">參數</span><span class="sxs-lookup"><span data-stu-id="5b704-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b704-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b704-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b704-110">標點符號類型可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5b704-110">The punctuation type can be one of the following values.</span></span>



| <span data-ttu-id="5b704-111">值</span><span class="sxs-lookup"><span data-stu-id="5b704-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="5b704-112">意義</span><span class="sxs-lookup"><span data-stu-id="5b704-112">Meaning</span></span>                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <span data-ttu-id="5b704-113"><dt>**電腦 \_ 領先**</dt></span><span class="sxs-lookup"><span data-stu-id="5b704-113"><dt>**PC\_LEADING**</dt></span></span> </dl>       | <span data-ttu-id="5b704-114">前置標點符號字元</span><span class="sxs-lookup"><span data-stu-id="5b704-114">Leading punctuation characters</span></span><br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <span data-ttu-id="5b704-115"><dt>**電腦 \_ 遵循**</dt></span><span class="sxs-lookup"><span data-stu-id="5b704-115"><dt>**PC\_FOLLOWING**</dt></span></span> </dl> | <span data-ttu-id="5b704-116">下列標點符號字元</span><span class="sxs-lookup"><span data-stu-id="5b704-116">Following punctuation characters</span></span><br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <span data-ttu-id="5b704-117"><dt>**電腦 \_ 分隔符號**</dt></span><span class="sxs-lookup"><span data-stu-id="5b704-117"><dt>**PC\_DELIMITER**</dt></span></span> </dl> | <span data-ttu-id="5b704-118">分隔符號</span><span class="sxs-lookup"><span data-stu-id="5b704-118">Delimiter</span></span><br/>                        |
| <span id="PC_OVERFLOW"></span><span id="pc_overflow"></span><dl> <span data-ttu-id="5b704-119"><dt>**電腦 \_ 溢位**</dt></span><span class="sxs-lookup"><span data-stu-id="5b704-119"><dt>**PC\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="5b704-120">不支援</span><span class="sxs-lookup"><span data-stu-id="5b704-120">Not supported</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="5b704-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b704-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b704-122">接收標點符號字元之 [**標點符號**](/windows/desktop/api/Richedit/ns-richedit-punctuation) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5b704-122">Pointer to a [**PUNCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation) structure that receives the punctuation characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b704-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b704-123">Return value</span></span>

<span data-ttu-id="5b704-124">如果作業成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="5b704-124">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="5b704-125">如果作業失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="5b704-125">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b704-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b704-126">Requirements</span></span>



| <span data-ttu-id="5b704-127">需求</span><span class="sxs-lookup"><span data-stu-id="5b704-127">Requirement</span></span> | <span data-ttu-id="5b704-128">值</span><span class="sxs-lookup"><span data-stu-id="5b704-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b704-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b704-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5b704-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b704-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b704-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b704-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5b704-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b704-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b704-133">標頭</span><span class="sxs-lookup"><span data-stu-id="5b704-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b704-134"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5b704-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b704-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b704-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="5b704-136">**參考**</span><span class="sxs-lookup"><span data-stu-id="5b704-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5b704-137">**EM \_ SETPUNCTUATION**</span><span class="sxs-lookup"><span data-stu-id="5b704-137">**EM\_SETPUNCTUATION**</span></span>](em-setpunctuation.md)
</dt> <dt>

[<span data-ttu-id="5b704-138">**標點符號**</span><span class="sxs-lookup"><span data-stu-id="5b704-138">**PUNCTUATION**</span></span>](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





