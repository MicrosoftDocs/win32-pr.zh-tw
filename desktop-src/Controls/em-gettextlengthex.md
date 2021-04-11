---
title: 'EM_GETTEXTLENGTHEX 訊息 (Richedit .h) '
description: 以各種方式計算文字長度。 通常會在建立緩衝區之前呼叫，以接收控制項的文字。
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- EM_GETTEXTLENGTHEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2d91674e07ef60c2ce95535983a31cf380f9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843480"
---
# <a name="em_gettextlengthex-message"></a><span data-ttu-id="4dd0f-105">EM \_ GETTEXTLENGTHEX 訊息</span><span class="sxs-lookup"><span data-stu-id="4dd0f-105">EM\_GETTEXTLENGTHEX message</span></span>

<span data-ttu-id="4dd0f-106">以各種方式計算文字長度。</span><span class="sxs-lookup"><span data-stu-id="4dd0f-106">Calculates text length in various ways.</span></span> <span data-ttu-id="4dd0f-107">通常會在建立緩衝區之前呼叫，以接收控制項的文字。</span><span class="sxs-lookup"><span data-stu-id="4dd0f-107">It is usually called before creating a buffer to receive the text from the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4dd0f-108">參數</span><span class="sxs-lookup"><span data-stu-id="4dd0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dd0f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4dd0f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4dd0f-110">[**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)結構的指標，此結構會接收文字長度資訊。</span><span class="sxs-lookup"><span data-stu-id="4dd0f-110">Pointer to a [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) structure that receives the text length information.</span></span>

</dd> <dt>

<span data-ttu-id="4dd0f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4dd0f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4dd0f-112">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="4dd0f-112">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dd0f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4dd0f-113">Return value</span></span>

<span data-ttu-id="4dd0f-114">訊息會根據 [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)結構中的旗標設定，傳回編輯控制項中的 **TCHAR** 數目。</span><span class="sxs-lookup"><span data-stu-id="4dd0f-114">The message returns the number of **TCHAR** s in the edit control, depending on the setting of the flags in the [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) structure.</span></span> <span data-ttu-id="4dd0f-115">如果 **旗** 標成員中設定了不相容的旗標，訊息會傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="4dd0f-115">If incompatible flags were set in the **flags** member, the message returns E\_INVALIDARG .</span></span>

## <a name="remarks"></a><span data-ttu-id="4dd0f-116">備註</span><span class="sxs-lookup"><span data-stu-id="4dd0f-116">Remarks</span></span>

<span data-ttu-id="4dd0f-117">這則訊息是一種快速且簡單的方式，可判斷 rich edit 控制項的 Unicode 版本中的字元數。</span><span class="sxs-lookup"><span data-stu-id="4dd0f-117">This message is a fast and easy way to determine the number of characters in the Unicode version of the rich edit control.</span></span> <span data-ttu-id="4dd0f-118">不過，對於非 Unicode 目標字碼頁，您可能會轉換成單一位元組和雙位元組字元的組合。</span><span class="sxs-lookup"><span data-stu-id="4dd0f-118">However, for a non-Unicode target code page you will potentially be converting to a combination of single-byte and double-byte characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dd0f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4dd0f-119">Requirements</span></span>



| <span data-ttu-id="4dd0f-120">需求</span><span class="sxs-lookup"><span data-stu-id="4dd0f-120">Requirement</span></span> | <span data-ttu-id="4dd0f-121">值</span><span class="sxs-lookup"><span data-stu-id="4dd0f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd0f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4dd0f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4dd0f-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4dd0f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4dd0f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4dd0f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4dd0f-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4dd0f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4dd0f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="4dd0f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dd0f-127"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="4dd0f-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dd0f-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4dd0f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dd0f-129">**GETTEXTLENGTHEX**</span><span class="sxs-lookup"><span data-stu-id="4dd0f-129">**GETTEXTLENGTHEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





