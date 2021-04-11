---
title: 'EM_GETFILELINECOUNT 訊息 (CommCtrl .h) '
description: 取得多行編輯控制項中的行數，與螢幕上的線條顯示方式無關。
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETFILELINECOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETFILELINECOUNT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: bf48b3abeb10b98bf0c22a7dd2ef93c73a2a59c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104832"
---
# <a name="em_getfilelinecount-message-commctrlh"></a><span data-ttu-id="2ff47-104">EM_GETFILELINECOUNT 訊息 (CommCtrl .h) </span><span class="sxs-lookup"><span data-stu-id="2ff47-104">EM_GETFILELINECOUNT message (CommCtrl.h)</span></span>

<span data-ttu-id="2ff47-105">取得多行編輯控制項中的行數，與螢幕上的線條顯示方式無關。</span><span class="sxs-lookup"><span data-stu-id="2ff47-105">Gets the number of lines in a multiline edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ff47-106">參數</span><span class="sxs-lookup"><span data-stu-id="2ff47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ff47-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ff47-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ff47-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="2ff47-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2ff47-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ff47-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ff47-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="2ff47-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ff47-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ff47-111">Return value</span></span>

<span data-ttu-id="2ff47-112">傳回值是一個整數，它會指定多行編輯控制項中的文字行總數，而不會與螢幕上顯示的行數分開。</span><span class="sxs-lookup"><span data-stu-id="2ff47-112">The return value is an integer specifying the total number of text lines in the multiline edit control, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="2ff47-113">如果控制項沒有任何文字，則傳回值為1。</span><span class="sxs-lookup"><span data-stu-id="2ff47-113">If the control has no text, the return value is 1.</span></span> <span data-ttu-id="2ff47-114">傳回值永遠不會小於1。</span><span class="sxs-lookup"><span data-stu-id="2ff47-114">The return value will never be less than 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ff47-115">備註</span><span class="sxs-lookup"><span data-stu-id="2ff47-115">Remarks</span></span>

<span data-ttu-id="2ff47-116">**EM \_ GETFILELINECOUNT** 訊息會抓取文字行總數，與螢幕上顯示的行數無關，而不只是目前可見的行數。</span><span class="sxs-lookup"><span data-stu-id="2ff47-116">The **EM\_GETFILELINECOUNT** message retrieves the total number of text lines, independently of how lines are displayed on the screen, not just the number of lines that are currently visible.</span></span>

<span data-ttu-id="2ff47-117">自動換行並不會變更此訊息傳回的行數，因為此訊息與螢幕上的行顯示方式無關。</span><span class="sxs-lookup"><span data-stu-id="2ff47-117">Word-wrap does not change the number of lines this message returns, as this message works independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ff47-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ff47-118">Requirements</span></span>



| <span data-ttu-id="2ff47-119">需求</span><span class="sxs-lookup"><span data-stu-id="2ff47-119">Requirement</span></span> | <span data-ttu-id="2ff47-120">值</span><span class="sxs-lookup"><span data-stu-id="2ff47-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff47-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ff47-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2ff47-122">Windows 10， \[ 僅限 1809 desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ff47-122">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2ff47-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ff47-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2ff47-124">僅限 Windows Server 2019 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ff47-124">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2ff47-125">標頭</span><span class="sxs-lookup"><span data-stu-id="2ff47-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ff47-126"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ff47-126"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ff47-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ff47-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="2ff47-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="2ff47-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2ff47-129">**EM \_ GETFILELINE**</span><span class="sxs-lookup"><span data-stu-id="2ff47-129">**EM\_GETFILELINE**</span></span>](em-getfileline.md)
</dt> <dt>

[<span data-ttu-id="2ff47-130">**EM \_ FILELINELENGTH**</span><span class="sxs-lookup"><span data-stu-id="2ff47-130">**EM\_FILELINELENGTH**</span></span>](em-filelinelength.md)
</dt> <dt>

[<span data-ttu-id="2ff47-131">**編輯 \_ GetFileLineCount**</span><span class="sxs-lookup"><span data-stu-id="2ff47-131">**Edit\_GetFileLineCount**</span></span>](/windows/win32/api/commctrl/nf-commctrl-edit_getfilelinecount)
</dt> </dl>

 

 





