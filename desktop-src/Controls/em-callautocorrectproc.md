---
title: 'EM_CALLAUTOCORRECTPROC 訊息 (Richedit .h) '
description: 呼叫由 EM SETAUTOCORRECTPROC 訊息儲存的自動校正回呼函式 \_ （假設插入點前面的文字是自動校正的候選項）。
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- EM_CALLAUTOCORRECTPROC message Windows 控制項
topic_type:
- apiref
api_name:
- EM_CALLAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73109d2499fc01a1d811066dc6059593c7ed5e0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465913"
---
# <a name="em_callautocorrectproc-message"></a><span data-ttu-id="bf2a1-104">EM \_ CALLAUTOCORRECTPROC 訊息</span><span class="sxs-lookup"><span data-stu-id="bf2a1-104">EM\_CALLAUTOCORRECTPROC message</span></span>

<span data-ttu-id="bf2a1-105">呼叫由 [**EM \_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md) 訊息儲存的自動校正回呼函式（假設插入點前面的文字是自動校正的候選項）。</span><span class="sxs-lookup"><span data-stu-id="bf2a1-105">Calls the autocorrect callback function that is stored by the [**EM\_SETAUTOCORRECTPROC**](em-setautocorrectproc.md) message, provided that the text preceding the insertion point is a candidate for autocorrection.</span></span>


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a><span data-ttu-id="bf2a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="bf2a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf2a1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf2a1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf2a1-108">**WCHAR** 類型的字元。</span><span class="sxs-lookup"><span data-stu-id="bf2a1-108">A character of type **WCHAR**.</span></span> <span data-ttu-id="bf2a1-109">如果此字元是 (U + 0009) 的索引標籤，而插入點前面的字元不是索引標籤，則插入點前面的字元會被視為自動校正候選字串的一部分，而不是字串分隔符號;否則， *wParam* 不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="bf2a1-109">If this character is a tab (U+0009), and the character preceding the insertion point isn t a tab, then the character preceding the insertion point is treated as part of the autocorrect candidate string instead of as a string delimiter; otherwise, *wParam* has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="bf2a1-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf2a1-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf2a1-111">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="bf2a1-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf2a1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf2a1-112">Return value</span></span>

<span data-ttu-id="bf2a1-113">如果訊息成功，則傳回值為零，如果發生錯誤則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="bf2a1-113">The return value is zero if the message succeeds, or nonzero if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf2a1-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf2a1-114">Requirements</span></span>



| <span data-ttu-id="bf2a1-115">需求</span><span class="sxs-lookup"><span data-stu-id="bf2a1-115">Requirement</span></span> | <span data-ttu-id="bf2a1-116">值</span><span class="sxs-lookup"><span data-stu-id="bf2a1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2a1-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf2a1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bf2a1-118">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf2a1-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bf2a1-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf2a1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bf2a1-120">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf2a1-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf2a1-121">標頭</span><span class="sxs-lookup"><span data-stu-id="bf2a1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf2a1-122"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="bf2a1-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf2a1-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf2a1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2a1-124">*AutoCorrectProc*</span><span class="sxs-lookup"><span data-stu-id="bf2a1-124">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="bf2a1-125">**EM \_ GETAUTOCORRECTPROC**</span><span class="sxs-lookup"><span data-stu-id="bf2a1-125">**EM\_GETAUTOCORRECTPROC**</span></span>](em-getautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="bf2a1-126">**EM \_ SETAUTOCORRECTPROC**</span><span class="sxs-lookup"><span data-stu-id="bf2a1-126">**EM\_SETAUTOCORRECTPROC**</span></span>](em-setautocorrectproc.md)
</dt> </dl>

 

 





