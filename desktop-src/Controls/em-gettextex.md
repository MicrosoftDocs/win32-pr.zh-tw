---
title: 'EM_GETTEXTEX 訊息 (Richedit .h) '
description: 取得 rich edit 控制項中的文字。
ms.assetid: 46431563-fde1-4407-ab7a-b2248c0e12b8
keywords:
- EM_GETTEXTEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357cfe37d3432b396183b500c945ad89397c0294
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465149"
---
# <a name="em_gettextex-message"></a><span data-ttu-id="5c34b-104">EM \_ GETTEXTEX 訊息</span><span class="sxs-lookup"><span data-stu-id="5c34b-104">EM\_GETTEXTEX message</span></span>

<span data-ttu-id="5c34b-105">取得 rich edit 控制項中的文字。</span><span class="sxs-lookup"><span data-stu-id="5c34b-105">Gets the text from a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5c34b-106">參數</span><span class="sxs-lookup"><span data-stu-id="5c34b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c34b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c34b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c34b-108">[**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex)結構的指標，此結構表示如何在將文字放入輸出緩衝區之前將文字轉譯。</span><span class="sxs-lookup"><span data-stu-id="5c34b-108">Pointer to a [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure, which indicates how to translate the text before putting it into the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5c34b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c34b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c34b-110">要接收文字之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="5c34b-110">Pointer to the buffer to receive the text.</span></span> <span data-ttu-id="5c34b-111">這個緩衝區的大小（以位元組為單位）是由 [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex)結構的 **cb** 成員所指定。</span><span class="sxs-lookup"><span data-stu-id="5c34b-111">The size of this buffer, in bytes, is specified by the **cb** member of the [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure.</span></span> <span data-ttu-id="5c34b-112">使用 [**EM \_ GETTEXTLENGTHEX**](em-gettextlengthex.md) 訊息來取得所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="5c34b-112">Use the [**EM\_GETTEXTLENGTHEX**](em-gettextlengthex.md) message to get the required size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c34b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c34b-113">Return value</span></span>

<span data-ttu-id="5c34b-114">傳回值是複製到輸出緩衝區的 **TCHAR** 數，包括 null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="5c34b-114">The return value is the number of **TCHAR** s copied into the output buffer, including the null terminator.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c34b-115">備註</span><span class="sxs-lookup"><span data-stu-id="5c34b-115">Remarks</span></span>

<span data-ttu-id="5c34b-116">如果輸出緩衝區的大小小於控制項中文字的大小，則編輯控制項會從開頭複製文字，並將它放在緩衝區中，直到緩衝區已滿為止。</span><span class="sxs-lookup"><span data-stu-id="5c34b-116">If the size of the output buffer is less than the size of the text in the control, the edit control will copy text from its beginning and place it in the buffer until the buffer is full.</span></span> <span data-ttu-id="5c34b-117">終止的 null 字元仍會放置在緩衝區的結尾。</span><span class="sxs-lookup"><span data-stu-id="5c34b-117">A terminating null character will still be placed at the end of the buffer.</span></span>

<span data-ttu-id="5c34b-118">如果要求 ANSI 文字， **EM \_ GETTEXTEX** 會使用 [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) 函數將 Unicode 字元轉譯為 ansi。</span><span class="sxs-lookup"><span data-stu-id="5c34b-118">If ANSI text is requested, **EM\_GETTEXTEX** uses the [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) function to translate the Unicode characters to ANSI.</span></span> <span data-ttu-id="5c34b-119">它可讓您使用特定字碼頁，從 Unicode 移至 ANSI。</span><span class="sxs-lookup"><span data-stu-id="5c34b-119">It allows you to go from Unicode to ANSI using a particular code page.</span></span> <span data-ttu-id="5c34b-120">[**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex)結構包含 (**lpDefaultChar** 和 **lpUsedDefChar**) 的成員，這些成員會用於從 Unicode 翻譯為 ANSI。</span><span class="sxs-lookup"><span data-stu-id="5c34b-120">The [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure contains members (**lpDefaultChar** and **lpUsedDefChar**) that are used in the translation from Unicode to ANSI.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c34b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c34b-121">Requirements</span></span>



| <span data-ttu-id="5c34b-122">需求</span><span class="sxs-lookup"><span data-stu-id="5c34b-122">Requirement</span></span> | <span data-ttu-id="5c34b-123">值</span><span class="sxs-lookup"><span data-stu-id="5c34b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c34b-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c34b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5c34b-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c34b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5c34b-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c34b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5c34b-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c34b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c34b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="5c34b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c34b-129"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c34b-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c34b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c34b-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="5c34b-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="5c34b-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5c34b-132">**EM \_ SETTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="5c34b-132">**EM\_SETTEXTEX**</span></span>](em-settextex.md)
</dt> <dt>

[<span data-ttu-id="5c34b-133">**GETTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="5c34b-133">**GETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextex)
</dt> <dt>

<span data-ttu-id="5c34b-134">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="5c34b-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5c34b-135">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="5c34b-135">**WideCharToMultiByte**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
</dt> <dt>

[<span data-ttu-id="5c34b-136">**WM \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="5c34b-136">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

