---
title: 'LB_GETTEXTLEN 訊息 (Winuser .h) '
description: 取得清單方塊中字串的長度。
ms.assetid: 866730bc-ffd4-42fd-9cea-5d326e129189
keywords:
- LB_GETTEXTLEN message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1f76bf3574b09b76d5f1010dcb59c8245555dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094432"
---
# <a name="lb_gettextlen-message"></a><span data-ttu-id="b5cfe-104">LB \_ GETTEXTLEN 訊息</span><span class="sxs-lookup"><span data-stu-id="b5cfe-104">LB\_GETTEXTLEN message</span></span>

<span data-ttu-id="b5cfe-105">取得清單方塊中字串的長度。</span><span class="sxs-lookup"><span data-stu-id="b5cfe-105">Gets the length of a string in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5cfe-106">參數</span><span class="sxs-lookup"><span data-stu-id="b5cfe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5cfe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5cfe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5cfe-108">字串之以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="b5cfe-108">The zero-based index of the string.</span></span>

<span data-ttu-id="b5cfe-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="b5cfe-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="b5cfe-110">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="b5cfe-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="b5cfe-111">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b5cfe-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="b5cfe-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5cfe-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5cfe-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="b5cfe-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5cfe-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b5cfe-114">Return value</span></span>

<span data-ttu-id="b5cfe-115">傳回值是字串的長度（在 **TCHAR** s 中），不包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="b5cfe-115">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="b5cfe-116">在某些情況下，這個值實際上可能大於文字的長度。</span><span class="sxs-lookup"><span data-stu-id="b5cfe-116">Under certain conditions, this value may actually be greater than the length of the text.</span></span> <span data-ttu-id="b5cfe-117">如需詳細資訊，請參閱接下來的＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="b5cfe-117">For more information, see the following Remarks section.</span></span>

<span data-ttu-id="b5cfe-118">如果 *wParam* 參數未指定有效的索引，則傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="b5cfe-118">If the *wParam* parameter does not specify a valid index, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5cfe-119">備註</span><span class="sxs-lookup"><span data-stu-id="b5cfe-119">Remarks</span></span>

<span data-ttu-id="b5cfe-120">在某些情況下，傳回值大於文字的實際長度。</span><span class="sxs-lookup"><span data-stu-id="b5cfe-120">Under certain conditions, the return value is larger than the actual length of the text.</span></span> <span data-ttu-id="b5cfe-121">這種情況會發生在 ANSI 和 Unicode 的特定混合中，而且是因為作業系統允許在文字內的 (DBCS) 字元中存在雙位元組字元集。</span><span class="sxs-lookup"><span data-stu-id="b5cfe-121">This occurs with certain mixtures of ANSI and Unicode, and is due to the operating system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="b5cfe-122">不過，傳回值一律會至少與文字的實際長度一樣大：因此，您可以一律使用它來引導緩衝區配置。</span><span class="sxs-lookup"><span data-stu-id="b5cfe-122">The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation.</span></span> <span data-ttu-id="b5cfe-123">當應用程式同時使用 ANSI 函式和使用 Unicode 的通用對話時，就可能會發生這種行為。</span><span class="sxs-lookup"><span data-stu-id="b5cfe-123">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="b5cfe-124">若要取得文字的確切長度，請使用 [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)、 [**LB \_ GETTEXT**](lb-gettext.md)或 [**CB \_ GETLBTEXT**](cb-getlbtext.md) 訊息或 [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) 函數。</span><span class="sxs-lookup"><span data-stu-id="b5cfe-124">To obtain the exact length of the text, use the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext), [**LB\_GETTEXT**](lb-gettext.md), or [**CB\_GETLBTEXT**](cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

<span data-ttu-id="b5cfe-125">如果清單方塊有擁有者繪製的樣式，而不是 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式，則傳回值一律為 **DWORD** 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b5cfe-125">If the list box has an owner-drawn style, but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the return value is always the size, in bytes, of a **DWORD**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5cfe-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5cfe-126">Requirements</span></span>



| <span data-ttu-id="b5cfe-127">需求</span><span class="sxs-lookup"><span data-stu-id="b5cfe-127">Requirement</span></span> | <span data-ttu-id="b5cfe-128">值</span><span class="sxs-lookup"><span data-stu-id="b5cfe-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5cfe-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5cfe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b5cfe-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5cfe-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b5cfe-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5cfe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b5cfe-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5cfe-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b5cfe-133">標頭</span><span class="sxs-lookup"><span data-stu-id="b5cfe-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5cfe-134"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b5cfe-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5cfe-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5cfe-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="b5cfe-136">**參考**</span><span class="sxs-lookup"><span data-stu-id="b5cfe-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b5cfe-137">**CB \_ GETLBTEXT**</span><span class="sxs-lookup"><span data-stu-id="b5cfe-137">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="b5cfe-138">**LB \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="b5cfe-138">**LB\_GETTEXT**</span></span>](lb-gettext.md)
</dt> <dt>

<span data-ttu-id="b5cfe-139">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="b5cfe-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b5cfe-140">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="b5cfe-140">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="b5cfe-141">**WM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="b5cfe-141">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

