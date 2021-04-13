---
title: 'EM_GETENDOFLINE 訊息 (Commctrl .h) '
description: 抓取插入 linebreak 時所使用的行尾字元。 明確地傳送此訊息，或使用 Edit \_ GetEndOfLine 宏。
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETENDOFLINE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETENDOFLINE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 98d537d2ea4239ab3f511666aeba46be93a2b881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464545"
---
# <a name="em_getendofline-message"></a><span data-ttu-id="58a4c-105">EM \_ GETENDOFLINE 訊息</span><span class="sxs-lookup"><span data-stu-id="58a4c-105">EM\_GETENDOFLINE message</span></span>

<span data-ttu-id="58a4c-106">抓取編輯控制項的行尾字元。</span><span class="sxs-lookup"><span data-stu-id="58a4c-106">Retrieves the end-of-line character for an edit control.</span></span> <span data-ttu-id="58a4c-107">明確地傳送此訊息，或使用 [**Edit \_ GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) 宏。</span><span class="sxs-lookup"><span data-stu-id="58a4c-107">Send this message explicitly or by using the [**Edit\_GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="58a4c-108">參數</span><span class="sxs-lookup"><span data-stu-id="58a4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58a4c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58a4c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="58a4c-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="58a4c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="58a4c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58a4c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="58a4c-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="58a4c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58a4c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="58a4c-113">Return value</span></span>

<span data-ttu-id="58a4c-114">傳回編輯控制項使用的行尾字元。</span><span class="sxs-lookup"><span data-stu-id="58a4c-114">Returns the end-of-line character used by the edit control.</span></span> <span data-ttu-id="58a4c-115">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="58a4c-115">This can be one of the following values.</span></span>

| <span data-ttu-id="58a4c-116">值</span><span class="sxs-lookup"><span data-stu-id="58a4c-116">Value</span></span>                                                                                                                                                   | <span data-ttu-id="58a4c-117">意義</span><span class="sxs-lookup"><span data-stu-id="58a4c-117">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <span data-ttu-id="58a4c-118"><dt>**EC \_ ENDOFLINE \_ CRLF**</dt></span><span class="sxs-lookup"><span data-stu-id="58a4c-118"><dt>**EC\_ENDOFLINE\_CRLF**</dt></span></span> </dl> | <span data-ttu-id="58a4c-119">用於新分行符號的行尾字元是換行字元，後面接著換行字元 (CRLF) 。</span><span class="sxs-lookup"><span data-stu-id="58a4c-119">The end-of-line character used for new linebreaks is carriage return followed by linefeed (CRLF).</span></span><br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <span data-ttu-id="58a4c-120"><dt>**EC \_ ENDOFLINE \_ CR**</dt></span><span class="sxs-lookup"><span data-stu-id="58a4c-120"><dt>**EC\_ENDOFLINE\_CR**</dt></span></span> </dl>       | <span data-ttu-id="58a4c-121">用於新分行符號的行尾字元是 (CR) 的回車。</span><span class="sxs-lookup"><span data-stu-id="58a4c-121">The end-of-line character used for new linebreaks is carriage return (CR).</span></span><br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <span data-ttu-id="58a4c-122"><dt>**EC \_ ENDOFLINE \_ LF**</dt></span><span class="sxs-lookup"><span data-stu-id="58a4c-122"><dt>**EC\_ENDOFLINE\_LF**</dt></span></span> </dl>       | <span data-ttu-id="58a4c-123">用於新分行符號的行尾字元是換行字元 (LF) 。</span><span class="sxs-lookup"><span data-stu-id="58a4c-123">The end-of-line character used for new linebreaks is linefeed (LF).</span></span><br/>                               |

## <a name="remarks"></a><span data-ttu-id="58a4c-124">備註</span><span class="sxs-lookup"><span data-stu-id="58a4c-124">Remarks</span></span>

<span data-ttu-id="58a4c-125">使用 [[**編輯 \_ SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline)] 將使用的行尾字元設定為 [ **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** ] 時，此訊息會傳回偵測到的行尾字元。</span><span class="sxs-lookup"><span data-stu-id="58a4c-125">When the end-of-line character used is set to **EC\_ENDOFLINE\_DETECTFROMCONTENT** using [**Edit\_SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), this message will return the detected end-of-line character.</span></span>

## <a name="requirements"></a><span data-ttu-id="58a4c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="58a4c-126">Requirements</span></span>



| <span data-ttu-id="58a4c-127">需求</span><span class="sxs-lookup"><span data-stu-id="58a4c-127">Requirement</span></span> | <span data-ttu-id="58a4c-128">值</span><span class="sxs-lookup"><span data-stu-id="58a4c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58a4c-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58a4c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="58a4c-130">\[僅 Windows 10 版本1809桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58a4c-130">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="58a4c-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58a4c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="58a4c-132">僅限 Windows Server 2019 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58a4c-132">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="58a4c-133">標頭</span><span class="sxs-lookup"><span data-stu-id="58a4c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="58a4c-134"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="58a4c-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58a4c-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58a4c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58a4c-136">\**EM \_ SETENDOFLINE*</span><span class="sxs-lookup"><span data-stu-id="58a4c-136">\**EM\_SETENDOFLINE*</span></span>](em-setendofline.md)
</dt> </dl>
 

 





