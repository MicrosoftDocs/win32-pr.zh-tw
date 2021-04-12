---
title: 'TB_GETSTRING 訊息 (Commctrl .h) '
description: 從工具列的字串集區抓取字串。
ms.assetid: a5f80c16-bc6d-466d-8ec6-77451432148e
keywords:
- TB_GETSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETSTRING
- TB_GETSTRINGA
- TB_GETSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465ad2546397fa31c33d6a52b4989902c979d91d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024853"
---
# <a name="tb_getstring-message"></a><span data-ttu-id="66cc7-104">TB \_ GETSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="66cc7-104">TB\_GETSTRING message</span></span>

<span data-ttu-id="66cc7-105">從工具列的字串集區抓取字串。</span><span class="sxs-lookup"><span data-stu-id="66cc7-105">Retrieves a string from a toolbar's string pool.</span></span>

## <a name="parameters"></a><span data-ttu-id="66cc7-106">參數</span><span class="sxs-lookup"><span data-stu-id="66cc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66cc7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66cc7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66cc7-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定 *lParam* 緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="66cc7-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the length of the *lParam* buffer, in bytes.</span></span> <span data-ttu-id="66cc7-109">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定字串的索引。</span><span class="sxs-lookup"><span data-stu-id="66cc7-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the index of the string.</span></span>

</dd> <dt>

<span data-ttu-id="66cc7-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66cc7-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66cc7-111">用來傳回字串的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="66cc7-111">Pointer to a buffer used to return the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66cc7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="66cc7-112">Return value</span></span>

<span data-ttu-id="66cc7-113">如果成功，則傳回字串長度，否則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="66cc7-113">Returns the string length if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="66cc7-114">備註</span><span class="sxs-lookup"><span data-stu-id="66cc7-114">Remarks</span></span>

<span data-ttu-id="66cc7-115">此訊息會從工具列的字串集區傳回指定的字串。</span><span class="sxs-lookup"><span data-stu-id="66cc7-115">This message returns the specified string from the toolbar's string pool.</span></span> <span data-ttu-id="66cc7-116">它不一定會對應到目前由按鈕所顯示的文字字串。</span><span class="sxs-lookup"><span data-stu-id="66cc7-116">It does not necessarily correspond to the text string currently being displayed by a button.</span></span> <span data-ttu-id="66cc7-117">若要抓取按鈕的目前文字字串，請將該工具列傳送至 [**TB 的 \_ GETBUTTONTEXT**](tb-getbuttontext.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="66cc7-117">To retrieve a button's current text string, send the toolbar a [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="66cc7-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="66cc7-118">Requirements</span></span>



| <span data-ttu-id="66cc7-119">需求</span><span class="sxs-lookup"><span data-stu-id="66cc7-119">Requirement</span></span> | <span data-ttu-id="66cc7-120">值</span><span class="sxs-lookup"><span data-stu-id="66cc7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66cc7-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66cc7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="66cc7-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66cc7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66cc7-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66cc7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="66cc7-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66cc7-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66cc7-125">標頭</span><span class="sxs-lookup"><span data-stu-id="66cc7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="66cc7-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="66cc7-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="66cc7-127">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="66cc7-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="66cc7-128">**TB \_GETSTRINGW** (Unicode) 和 **TB \_ GETSTRINGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="66cc7-128">**TB\_GETSTRINGW** (Unicode) and **TB\_GETSTRINGA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="66cc7-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66cc7-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="66cc7-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="66cc7-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="66cc7-131">**TB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="66cc7-131">**TB\_ADDSTRING**</span></span>](tb-addstring.md)
</dt> <dt>

[<span data-ttu-id="66cc7-132">**TB \_ ADDBUTTONS**</span><span class="sxs-lookup"><span data-stu-id="66cc7-132">**TB\_ADDBUTTONS**</span></span>](tb-addbuttons.md)
</dt> <dt>

[<span data-ttu-id="66cc7-133">**TB \_ INSERTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="66cc7-133">**TB\_INSERTBUTTON**</span></span>](tb-insertbutton.md)
</dt> </dl>

 

