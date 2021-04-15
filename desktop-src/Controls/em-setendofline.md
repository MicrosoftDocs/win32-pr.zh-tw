---
title: 'EM_SETENDOFLINE 訊息 (CommCtrl .h) '
description: 設定插入 linebreak 時所使用的行尾字元。
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETENDOFLINE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETENDOFLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 5ee7c500ba3818cad0f5ee74e9994ed8af049ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466544"
---
# <a name="em_setendofline-message"></a><span data-ttu-id="d9ae2-104">EM \_ SETENDOFLINE 訊息</span><span class="sxs-lookup"><span data-stu-id="d9ae2-104">EM\_SETENDOFLINE message</span></span>

<span data-ttu-id="d9ae2-105">設定插入 linebreak 時所使用的行尾字元。</span><span class="sxs-lookup"><span data-stu-id="d9ae2-105">Sets the end-of-line character used when a linebreak is inserted.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9ae2-106">參數</span><span class="sxs-lookup"><span data-stu-id="d9ae2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9ae2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9ae2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9ae2-108">指定插入 linebreak 時所使用的行尾字元。</span><span class="sxs-lookup"><span data-stu-id="d9ae2-108">Specifies the end-of-line character used when a linebreak is inserted.</span></span> <span data-ttu-id="d9ae2-109">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d9ae2-109">This can be one of the following values.</span></span>


| <span data-ttu-id="d9ae2-110">值</span><span class="sxs-lookup"><span data-stu-id="d9ae2-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="d9ae2-111">意義</span><span class="sxs-lookup"><span data-stu-id="d9ae2-111">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_DETECTFROMCONTENT"></span><span id="ec_endofline_detectfromcontent"></span><dl> <span data-ttu-id="d9ae2-112"><dt>**EC \_ ENDOFLINE \_ DETECTFROMCONTENT**</dt></span><span class="sxs-lookup"><span data-stu-id="d9ae2-112"><dt>**EC\_ENDOFLINE\_DETECTFROMCONTENT**</dt></span></span> </dl> | <span data-ttu-id="d9ae2-113">將用於新分行符號的行尾字元設定為目前檔所使用的字元。</span><span class="sxs-lookup"><span data-stu-id="d9ae2-113">Sets the end-of-line character used for new linebreaks to the character used by the current document.</span></span><br/>  |
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <span data-ttu-id="d9ae2-114"><dt>**EC \_ ENDOFLINE \_ CRLF**</dt></span><span class="sxs-lookup"><span data-stu-id="d9ae2-114"><dt>**EC\_ENDOFLINE\_CRLF**</dt></span></span> </dl>                                        | <span data-ttu-id="d9ae2-115">將新分行符號的行尾字元設定為分行符號，後面接著換行字元 (CRLF) 。</span><span class="sxs-lookup"><span data-stu-id="d9ae2-115">Sets the end-of-line character used for new linebreaks to carriage return followed by linefeed (CRLF).</span></span><br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <span data-ttu-id="d9ae2-116"><dt>**EC \_ ENDOFLINE \_ CR**</dt></span><span class="sxs-lookup"><span data-stu-id="d9ae2-116"><dt>**EC\_ENDOFLINE\_CR**</dt></span></span> </dl>                                              | <span data-ttu-id="d9ae2-117">將新分行符號的行尾字元設定為換行字元， (CR) 。</span><span class="sxs-lookup"><span data-stu-id="d9ae2-117">Sets the end-of-line character used for new linebreaks to carriage return (CR).</span></span><br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <span data-ttu-id="d9ae2-118"><dt>**EC \_ ENDOFLINE \_ LF**</dt></span><span class="sxs-lookup"><span data-stu-id="d9ae2-118"><dt>**EC\_ENDOFLINE\_LF**</dt></span></span> </dl>                                              | <span data-ttu-id="d9ae2-119">將用於新分行符號的行尾字元設定為換行 (LF) 。</span><span class="sxs-lookup"><span data-stu-id="d9ae2-119">Sets the end-of-line character used for new linebreaks to linefeed (LF).</span></span><br/>                               |

</dd> <dt>

<span data-ttu-id="d9ae2-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9ae2-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9ae2-121">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="d9ae2-121">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9ae2-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9ae2-122">Return value</span></span>

<span data-ttu-id="d9ae2-123">如果作業成功，則傳回值為非零。</span><span class="sxs-lookup"><span data-stu-id="d9ae2-123">If the operation succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="d9ae2-124">如果作業失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="d9ae2-124">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9ae2-125">備註</span><span class="sxs-lookup"><span data-stu-id="d9ae2-125">Remarks</span></span>

<span data-ttu-id="d9ae2-126">當行尾字元集為 **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** 時，編輯控制項只會偵測根據其擴充視窗樣式所支援的行尾字元，請參閱 [編輯控制項延伸樣式](edit-control-window-extended-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="d9ae2-126">When the end-of-line character set is **EC\_ENDOFLINE\_DETECTFROMCONTENT**, the edit control will only detect end-of-line characters supported according to its extended window style, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9ae2-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9ae2-127">Requirements</span></span>



| <span data-ttu-id="d9ae2-128">需求</span><span class="sxs-lookup"><span data-stu-id="d9ae2-128">Requirement</span></span> | <span data-ttu-id="d9ae2-129">值</span><span class="sxs-lookup"><span data-stu-id="d9ae2-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9ae2-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d9ae2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d9ae2-131">Windows 10， \[ 僅限 1809 desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9ae2-131">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d9ae2-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d9ae2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d9ae2-133">僅限 Windows Server 2019 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9ae2-133">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d9ae2-134">標頭</span><span class="sxs-lookup"><span data-stu-id="d9ae2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9ae2-135"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d9ae2-135"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9ae2-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9ae2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9ae2-137">\**EM \_ GETENDOFLINE*</span><span class="sxs-lookup"><span data-stu-id="d9ae2-137">\**EM\_GETENDOFLINE*</span></span>](em-getendofline.md)
</dt> </dl>

 

 





