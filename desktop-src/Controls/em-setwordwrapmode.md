---
title: 'EM_SETWORDWRAPMODE 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的自動換行和斷字選項。
ms.assetid: 43703ac8-6ae5-470b-9156-e60330ef97c4
keywords:
- EM_SETWORDWRAPMODE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1dc6f064f52bf2a5f58c71db099f38b9350e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025209"
---
# <a name="em_setwordwrapmode-message"></a><span data-ttu-id="f0e2a-104">EM \_ SETWORDWRAPMODE 訊息</span><span class="sxs-lookup"><span data-stu-id="f0e2a-104">EM\_SETWORDWRAPMODE message</span></span>

<span data-ttu-id="f0e2a-105">設定 rich edit 控制項的自動換行和斷字選項。</span><span class="sxs-lookup"><span data-stu-id="f0e2a-105">Sets the word-wrapping and word-breaking options for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="f0e2a-106">只有 Microsoft Rich Edit 1.0 的亞洲語言版本才支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="f0e2a-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="f0e2a-107">任何較新版本都不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="f0e2a-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="f0e2a-108">參數</span><span class="sxs-lookup"><span data-stu-id="f0e2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0e2a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0e2a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0e2a-110">指定下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="f0e2a-110">Specifies one or more of the following values.</span></span>



| <span data-ttu-id="f0e2a-111">值</span><span class="sxs-lookup"><span data-stu-id="f0e2a-111">Value</span></span>                                                                                                                                                         | <span data-ttu-id="f0e2a-112">意義</span><span class="sxs-lookup"><span data-stu-id="f0e2a-112">Meaning</span></span>                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="WBF_WORDWRAP"></span><span id="wbf_wordwrap"></span><dl> <span data-ttu-id="f0e2a-113"><dt>**WBF \_ WORDWRAP**</dt></span><span class="sxs-lookup"><span data-stu-id="f0e2a-113"><dt>**WBF\_WORDWRAP**</dt></span></span> </dl>    | <span data-ttu-id="f0e2a-114">啟用亞洲特定的文字換行作業，例如日文的避避。</span><span class="sxs-lookup"><span data-stu-id="f0e2a-114">Enables Asian-specific word wrap operations, such as kinsoku in Japanese.</span></span> <br/>                                 |
| <span id="WBF_WORDBREAK"></span><span id="wbf_wordbreak"></span><dl> <span data-ttu-id="f0e2a-115"><dt>**WBF \_ WORDBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="f0e2a-115"><dt>**WBF\_WORDBREAK**</dt></span></span> </dl> | <span data-ttu-id="f0e2a-116">啟用日文和中文的英文斷字作業。</span><span class="sxs-lookup"><span data-stu-id="f0e2a-116">Enables English word-breaking operations in Japanese and Chinese.</span></span> <span data-ttu-id="f0e2a-117">啟用 Hangeul 斷詞操作。</span><span class="sxs-lookup"><span data-stu-id="f0e2a-117">Enables Hangeul word-breaking operation.</span></span><br/> |
| <span id="WBF_OVERFLOW"></span><span id="wbf_overflow"></span><dl> <span data-ttu-id="f0e2a-118"><dt>**WBF \_ 溢位**</dt></span><span class="sxs-lookup"><span data-stu-id="f0e2a-118"><dt>**WBF\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="f0e2a-119">辨識溢位標點符號。</span><span class="sxs-lookup"><span data-stu-id="f0e2a-119">Recognizes overflow punctuation.</span></span> <span data-ttu-id="f0e2a-120">目前不支援 (。 ) </span><span class="sxs-lookup"><span data-stu-id="f0e2a-120">(Not currently supported.)</span></span><br/>                                                |
| <span id="WBF_LEVEL1"></span><span id="wbf_level1"></span><dl> <span data-ttu-id="f0e2a-121"><dt>**WBF \_ 級1**</dt></span><span class="sxs-lookup"><span data-stu-id="f0e2a-121"><dt>**WBF\_LEVEL1**</dt></span></span> </dl>          | <span data-ttu-id="f0e2a-122">將 [層級 1] 標點符號資料表設定為預設值。</span><span class="sxs-lookup"><span data-stu-id="f0e2a-122">Sets the Level 1 punctuation table as the default.</span></span><br/>                                                         |
| <span id="WBF_LEVEL2"></span><span id="wbf_level2"></span><dl> <span data-ttu-id="f0e2a-123"><dt>**WBF 的 \_ 級別2**</dt></span><span class="sxs-lookup"><span data-stu-id="f0e2a-123"><dt>**WBF\_LEVEL2**</dt></span></span> </dl>          | <span data-ttu-id="f0e2a-124">將層級2標點符號資料表設定為預設值。</span><span class="sxs-lookup"><span data-stu-id="f0e2a-124">Sets the Level 2 punctuation table as the default.</span></span><br/>                                                         |
| <span id="WBF_CUSTOM"></span><span id="wbf_custom"></span><dl> <span data-ttu-id="f0e2a-125"><dt>**WBF \_ 自訂**</dt></span><span class="sxs-lookup"><span data-stu-id="f0e2a-125"><dt>**WBF\_CUSTOM**</dt></span></span> </dl>          | <span data-ttu-id="f0e2a-126">設定應用程式定義的標點符號資料表。</span><span class="sxs-lookup"><span data-stu-id="f0e2a-126">Sets the application-defined punctuation table.</span></span><br/>                                                            |



 

</dd> <dt>

<span data-ttu-id="f0e2a-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0e2a-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0e2a-128">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="f0e2a-128">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0e2a-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0e2a-129">Return value</span></span>

<span data-ttu-id="f0e2a-130">這則訊息會傳回目前的自動換行和斷詞選項。</span><span class="sxs-lookup"><span data-stu-id="f0e2a-130">This message returns the current word-wrapping and word-breaking options.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0e2a-131">備註</span><span class="sxs-lookup"><span data-stu-id="f0e2a-131">Remarks</span></span>

<span data-ttu-id="f0e2a-132">此訊息不得由應用程式定義的斷詞程式傳送。</span><span class="sxs-lookup"><span data-stu-id="f0e2a-132">This message must not be sent by the application defined word breaking procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0e2a-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0e2a-133">Requirements</span></span>



| <span data-ttu-id="f0e2a-134">需求</span><span class="sxs-lookup"><span data-stu-id="f0e2a-134">Requirement</span></span> | <span data-ttu-id="f0e2a-135">值</span><span class="sxs-lookup"><span data-stu-id="f0e2a-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e2a-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0e2a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f0e2a-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0e2a-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0e2a-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0e2a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f0e2a-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0e2a-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0e2a-140">標頭</span><span class="sxs-lookup"><span data-stu-id="f0e2a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0e2a-141"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0e2a-141"><dt>Richedit.h</dt></span></span> </dl> |



 

 





