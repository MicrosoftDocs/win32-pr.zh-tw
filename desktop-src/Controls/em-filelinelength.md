---
title: 'EM_FILELINELENGTH 訊息 (CommCtrl .h) '
description: 抓取編輯控制項中某一行的長度（以字元為單位），與螢幕上的線條顯示方式無關。
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_FILELINELENGTH message Windows 控制項
topic_type:
- apiref
api_name:
- EM_FILELINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa50f4d9b49253a558095be78e0e781d7d4c7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508712"
---
# <a name="em_filelinelength-message"></a><span data-ttu-id="78af2-104">EM \_ FILELINELENGTH 訊息</span><span class="sxs-lookup"><span data-stu-id="78af2-104">EM\_FILELINELENGTH message</span></span>

<span data-ttu-id="78af2-105">抓取編輯控制項中某一行的長度（以字元為單位），與螢幕上的線條顯示方式無關。</span><span class="sxs-lookup"><span data-stu-id="78af2-105">Retrieves the length, in characters, of a line in an edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="parameters"></a><span data-ttu-id="78af2-106">參數</span><span class="sxs-lookup"><span data-stu-id="78af2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78af2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78af2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78af2-108">要取出其長度的行字元字元索引。</span><span class="sxs-lookup"><span data-stu-id="78af2-108">The character index of a character in the line whose length is to be retrieved.</span></span> <span data-ttu-id="78af2-109">如果此參數大於控制項中的字元數，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="78af2-109">If this parameter is greater than the number of characters in the control, the return value is zero.</span></span>

<span data-ttu-id="78af2-110">此參數可以是-1。</span><span class="sxs-lookup"><span data-stu-id="78af2-110">This parameter can be -1.</span></span> <span data-ttu-id="78af2-111">在此情況下，訊息會傳回包含所選字元的行上未選取的字元數。</span><span class="sxs-lookup"><span data-stu-id="78af2-111">In this case, the message returns the number of unselected characters on lines containing selected characters.</span></span> <span data-ttu-id="78af2-112">例如，如果選取範圍是從下一行結尾的第四個字元到第四個字元，則傳回值會是第一行的 10 (三個字元，而在下一個) 則是七個字元。</span><span class="sxs-lookup"><span data-stu-id="78af2-112">For example, if the selection extended from the fourth character of one line through the eighth character from the end of the next line, the return value would be 10 (three characters on the first line and seven on the next).</span></span>

</dd> <dt>

<span data-ttu-id="78af2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78af2-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78af2-114">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="78af2-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78af2-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="78af2-115">Return value</span></span>

<span data-ttu-id="78af2-116">若為多行編輯控制項，傳回值是 *wParam* 參數所指定之線條的長度（以 **TCHAR** s），與螢幕上的線條顯示方式無關。</span><span class="sxs-lookup"><span data-stu-id="78af2-116">For multiline edit controls, the return value is the length, in **TCHAR** s, of the line specified by the *wParam* parameter, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="78af2-117">它不會在行尾包含回車或換行字元。</span><span class="sxs-lookup"><span data-stu-id="78af2-117">It does not include the carriage-return or linefeed character at the end of the line.</span></span>

<span data-ttu-id="78af2-118">針對單行編輯控制項，傳回值是編輯控制項中文字的長度（以 **TCHAR** s）。</span><span class="sxs-lookup"><span data-stu-id="78af2-118">For single-line edit controls, the return value is the length, in **TCHAR** s, of the text in the edit control.</span></span>

<span data-ttu-id="78af2-119">如果 *wParam* 大於控制項中的字元數，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="78af2-119">If *wParam* is greater than the number of characters in the control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="78af2-120">備註</span><span class="sxs-lookup"><span data-stu-id="78af2-120">Remarks</span></span>

<span data-ttu-id="78af2-121">使用 [**EM \_ FILELINEINDEX**](em-lineindex.md) 訊息來抓取多行編輯控制項內指定行號的字元索引，與螢幕上的線條顯示方式無關。</span><span class="sxs-lookup"><span data-stu-id="78af2-121">Use the [**EM\_FILELINEINDEX**](em-lineindex.md) message to retrieve a character index for a given line number within a multiline edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="78af2-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="78af2-122">Requirements</span></span>



| <span data-ttu-id="78af2-123">需求</span><span class="sxs-lookup"><span data-stu-id="78af2-123">Requirement</span></span> | <span data-ttu-id="78af2-124">值</span><span class="sxs-lookup"><span data-stu-id="78af2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78af2-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78af2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="78af2-126">Windows 10， \[ 僅限 1809 desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78af2-126">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="78af2-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78af2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="78af2-128">僅限 Windows Server 2019 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78af2-128">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="78af2-129">標頭</span><span class="sxs-lookup"><span data-stu-id="78af2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="78af2-130"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="78af2-130"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78af2-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78af2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78af2-132">**EM \_ FILELINEINDEX**</span><span class="sxs-lookup"><span data-stu-id="78af2-132">**EM\_FILELINEINDEX**</span></span>](em-filelineindex.md)
</dt> </dl>

 

 





