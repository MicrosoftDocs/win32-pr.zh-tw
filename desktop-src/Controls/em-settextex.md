---
title: 'EM_SETTEXTEX 訊息 (Richedit .h) '
description: 結合了 WM \_ SETTEXT 和 EM \_ REPLACESEL 訊息的功能，並新增使用字碼頁設定文字的功能，以及使用 rtf 或純文字。
ms.assetid: 1ba9e4c0-7870-4057-8a8b-d0e6577349ac
keywords:
- EM_SETTEXTEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdd7dece965f70fe41d40edf44d365795d44fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465704"
---
# <a name="em_settextex-message"></a><span data-ttu-id="b8c48-104">EM \_ SETTEXTEX 訊息</span><span class="sxs-lookup"><span data-stu-id="b8c48-104">EM\_SETTEXTEX message</span></span>

<span data-ttu-id="b8c48-105">結合了 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 和 [**EM \_ REPLACESEL**](em-replacesel.md) 訊息的功能，並新增使用字碼頁設定文字的功能，以及使用 rtf 或純文字。</span><span class="sxs-lookup"><span data-stu-id="b8c48-105">Combines the functionality of the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) and [**EM\_REPLACESEL**](em-replacesel.md) messages, and adds the ability to set text using a code page and to use either rich text or plain text.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8c48-106">參數</span><span class="sxs-lookup"><span data-stu-id="b8c48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8c48-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8c48-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8c48-108">[**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex)結構的指標，此結構會指定旗標以及要用於翻譯為 Unicode 的選擇性字碼頁。</span><span class="sxs-lookup"><span data-stu-id="b8c48-108">Pointer to a [**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) structure that specifies flags and an optional code page to use in translating to Unicode.</span></span>

</dd> <dt>

<span data-ttu-id="b8c48-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8c48-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8c48-110">要插入之以 null 結束的文字指標。</span><span class="sxs-lookup"><span data-stu-id="b8c48-110">Pointer to the null-terminated text to insert.</span></span> <span data-ttu-id="b8c48-111">除非字碼頁是 1200 (Unicode) ，否則此文字為 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="b8c48-111">This text is an ANSI string, unless the code page is 1200 (Unicode).</span></span> <span data-ttu-id="b8c48-112">如果 *lParam* 以有效的 rtf ASCII 序列（例如 "{ \\ RTF" 或 "{urtf"）開頭，則會使用 RTF 讀取器來讀取文字。</span><span class="sxs-lookup"><span data-stu-id="b8c48-112">If *lParam* starts with a valid RTF ASCII sequence for example, "{\\rtf" or "{urtf" the text is read in using the RTF reader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8c48-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8c48-113">Return value</span></span>

<span data-ttu-id="b8c48-114">如果作業正在設定所有文字且成功，則傳回值為1。</span><span class="sxs-lookup"><span data-stu-id="b8c48-114">If the operation is setting all of the text and succeeds, the return value is 1.</span></span>

<span data-ttu-id="b8c48-115">如果作業正在設定選取範圍，且成功，則傳回值為複製的位元組數或字元數。</span><span class="sxs-lookup"><span data-stu-id="b8c48-115">If the operation is setting the selection and succeeds, the return value is the number of bytes or characters copied.</span></span>

<span data-ttu-id="b8c48-116">如果作業失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="b8c48-116">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8c48-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8c48-117">Requirements</span></span>



| <span data-ttu-id="b8c48-118">需求</span><span class="sxs-lookup"><span data-stu-id="b8c48-118">Requirement</span></span> | <span data-ttu-id="b8c48-119">值</span><span class="sxs-lookup"><span data-stu-id="b8c48-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8c48-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8c48-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b8c48-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8c48-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8c48-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8c48-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b8c48-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8c48-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8c48-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b8c48-124">Redistributable</span></span><br/>          | <span data-ttu-id="b8c48-125">Rich Edit 3。0</span><span class="sxs-lookup"><span data-stu-id="b8c48-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="b8c48-126">標頭</span><span class="sxs-lookup"><span data-stu-id="b8c48-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8c48-127"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b8c48-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8c48-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8c48-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="b8c48-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="b8c48-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b8c48-130">**EM \_ GETTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="b8c48-130">**EM\_GETTEXTEX**</span></span>](em-gettextex.md)
</dt> <dt>

[<span data-ttu-id="b8c48-131">**SETTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="b8c48-131">**SETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-settextex)
</dt> </dl>

 

