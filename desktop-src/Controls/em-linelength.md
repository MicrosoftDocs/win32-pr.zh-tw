---
title: 'EM_LINELENGTH 訊息 (Winuser .h) '
description: 抓取編輯控制項中的行長度（以字元為單位）。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_LINELENGTH message Windows 控制項
topic_type:
- apiref
api_name:
- EM_LINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cbf59cbe31886e55c34bce9f7c2421e431012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844044"
---
# <a name="em_linelength-message"></a><span data-ttu-id="284d3-105">EM \_ LINELENGTH 訊息</span><span class="sxs-lookup"><span data-stu-id="284d3-105">EM\_LINELENGTH message</span></span>

<span data-ttu-id="284d3-106">抓取編輯控制項中的行長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="284d3-106">Retrieves the length, in characters, of a line in an edit control.</span></span> <span data-ttu-id="284d3-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="284d3-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="284d3-108">參數</span><span class="sxs-lookup"><span data-stu-id="284d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="284d3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="284d3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="284d3-110">要取出其長度的行字元字元索引。</span><span class="sxs-lookup"><span data-stu-id="284d3-110">The character index of a character in the line whose length is to be retrieved.</span></span> <span data-ttu-id="284d3-111">如果此參數大於控制項中的字元數，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="284d3-111">If this parameter is greater than the number of characters in the control, the return value is zero.</span></span>

<span data-ttu-id="284d3-112">此參數可以是-1。</span><span class="sxs-lookup"><span data-stu-id="284d3-112">This parameter can be -1.</span></span> <span data-ttu-id="284d3-113">在此情況下，訊息會傳回包含所選字元的行上未選取的字元數。</span><span class="sxs-lookup"><span data-stu-id="284d3-113">In this case, the message returns the number of unselected characters on lines containing selected characters.</span></span> <span data-ttu-id="284d3-114">例如，如果選取範圍是從下一行結尾的第四個字元到第四個字元，則傳回值會是第一行的 10 (三個字元，而在下一個) 則是七個字元。</span><span class="sxs-lookup"><span data-stu-id="284d3-114">For example, if the selection extended from the fourth character of one line through the eighth character from the end of the next line, the return value would be 10 (three characters on the first line and seven on the next).</span></span>

</dd> <dt>

<span data-ttu-id="284d3-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="284d3-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="284d3-116">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="284d3-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="284d3-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="284d3-117">Return value</span></span>

<span data-ttu-id="284d3-118">若為多行編輯控制項，傳回值是 *wParam* 參數所指定之行的長度（以 **TCHAR** s）。</span><span class="sxs-lookup"><span data-stu-id="284d3-118">For multiline edit controls, the return value is the length, in **TCHAR** s, of the line specified by the *wParam* parameter.</span></span> <span data-ttu-id="284d3-119">若為 ANSI 文字，此為位元組數;若為 Unicode 文字，此為字元數。</span><span class="sxs-lookup"><span data-stu-id="284d3-119">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="284d3-120">它不會在行尾包含換行字元。</span><span class="sxs-lookup"><span data-stu-id="284d3-120">It does not include the carriage-return character at the end of the line.</span></span>

<span data-ttu-id="284d3-121">針對單行編輯控制項，傳回值是編輯控制項中文字的長度（以 **TCHAR** s）。</span><span class="sxs-lookup"><span data-stu-id="284d3-121">For single-line edit controls, the return value is the length, in **TCHAR** s, of the text in the edit control.</span></span>

<span data-ttu-id="284d3-122">如果 *wParam* 大於控制項中的字元數，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="284d3-122">If *wParam* is greater than the number of characters in the control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="284d3-123">備註</span><span class="sxs-lookup"><span data-stu-id="284d3-123">Remarks</span></span>

<span data-ttu-id="284d3-124">使用 [**EM \_ LINEINDEX**](em-lineindex.md) 訊息，在多行編輯控制項內取出指定行號的字元索引。</span><span class="sxs-lookup"><span data-stu-id="284d3-124">Use the [**EM\_LINEINDEX**](em-lineindex.md) message to retrieve a character index for a given line number within a multiline edit control.</span></span>

<span data-ttu-id="284d3-125">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="284d3-125">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="284d3-126">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="284d3-126">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="284d3-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="284d3-127">Requirements</span></span>



| <span data-ttu-id="284d3-128">需求</span><span class="sxs-lookup"><span data-stu-id="284d3-128">Requirement</span></span> | <span data-ttu-id="284d3-129">值</span><span class="sxs-lookup"><span data-stu-id="284d3-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="284d3-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="284d3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="284d3-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="284d3-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="284d3-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="284d3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="284d3-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="284d3-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="284d3-134">標頭</span><span class="sxs-lookup"><span data-stu-id="284d3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="284d3-135"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="284d3-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="284d3-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="284d3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="284d3-137">**EM \_ LINEINDEX**</span><span class="sxs-lookup"><span data-stu-id="284d3-137">**EM\_LINEINDEX**</span></span>](em-lineindex.md)
</dt> </dl>

 

 





