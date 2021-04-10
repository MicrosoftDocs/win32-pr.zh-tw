---
title: 'CB_GETLBTEXTLEN 訊息 (Winuser .h) '
description: 取得下拉式方塊清單中字串的長度（以字元為單位）。
ms.assetid: f0fe0eef-f9db-4d9f-9a42-5bb2aeae30a0
keywords:
- CB_GETLBTEXTLEN message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETLBTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e42dc19b13b22f577fcc21bb32cb8810bab29be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934361"
---
# <a name="cb_getlbtextlen-message"></a><span data-ttu-id="8a940-104">CB \_ GETLBTEXTLEN 訊息</span><span class="sxs-lookup"><span data-stu-id="8a940-104">CB\_GETLBTEXTLEN message</span></span>

<span data-ttu-id="8a940-105">取得下拉式方塊清單中字串的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="8a940-105">Gets the length, in characters, of a string in the list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a940-106">參數</span><span class="sxs-lookup"><span data-stu-id="8a940-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a940-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8a940-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a940-108">字串之以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="8a940-108">The zero-based index of the string.</span></span>

</dd> <dt>

<span data-ttu-id="8a940-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8a940-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a940-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="8a940-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a940-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a940-111">Return value</span></span>

<span data-ttu-id="8a940-112">傳回值是字串的長度（在 **TCHAR** s 中），不包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="8a940-112">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="8a940-113">如果 ANSI 字串是位元組數，而且如果是 Unicode 字串，則這是字元數。</span><span class="sxs-lookup"><span data-stu-id="8a940-113">If an ANSI string this is the number of bytes, and if it is a Unicode string this is the number of characters.</span></span> <span data-ttu-id="8a940-114">在某些情況下，這個值實際上可能大於文字的長度。</span><span class="sxs-lookup"><span data-stu-id="8a940-114">Under certain conditions, this value may actually be greater than the length of the text.</span></span> <span data-ttu-id="8a940-115">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="8a940-115">For more information, see the Remarks section.</span></span>

<span data-ttu-id="8a940-116">如果 *wParam* 參數未指定有效的索引，則傳回值為 CB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="8a940-116">If the *wParam* parameter does not specify a valid index, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a940-117">備註</span><span class="sxs-lookup"><span data-stu-id="8a940-117">Remarks</span></span>

<span data-ttu-id="8a940-118">在某些情況下，傳回值大於文字的實際長度。</span><span class="sxs-lookup"><span data-stu-id="8a940-118">Under certain conditions, the return value is larger than the actual length of the text.</span></span> <span data-ttu-id="8a940-119">這種情況會發生在 ANSI 和 Unicode 的特定混合中，而且是因為作業系統允許在文字內的 (DBCS) 字元中存在雙位元組字元集。</span><span class="sxs-lookup"><span data-stu-id="8a940-119">This occurs with certain mixtures of ANSI and Unicode, and is due to the operating system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="8a940-120">不過，傳回值一律會至少與文字的實際長度一樣大：因此，您隨時都可以使用它來引導緩衝區配置。</span><span class="sxs-lookup"><span data-stu-id="8a940-120">The return value, however, will always be at least as large as the actual length of the text; so you can always use it to guide buffer allocation.</span></span> <span data-ttu-id="8a940-121">當應用程式同時使用 ANSI 函式和使用 Unicode 的通用對話時，就可能會發生這種行為。</span><span class="sxs-lookup"><span data-stu-id="8a940-121">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="8a940-122">若要取得文字的確切長度，請使用 [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)、 [**LB \_ GETTEXT**](lb-gettext.md)或 [**CB \_ GETLBTEXT**](cb-getlbtext.md) 訊息或 [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) 函數。</span><span class="sxs-lookup"><span data-stu-id="8a940-122">To obtain the exact length of the text, use the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext), [**LB\_GETTEXT**](lb-gettext.md), or [**CB\_GETLBTEXT**](cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a940-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a940-123">Requirements</span></span>



| <span data-ttu-id="8a940-124">需求</span><span class="sxs-lookup"><span data-stu-id="8a940-124">Requirement</span></span> | <span data-ttu-id="8a940-125">值</span><span class="sxs-lookup"><span data-stu-id="8a940-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a940-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a940-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8a940-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a940-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8a940-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a940-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8a940-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a940-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8a940-130">標頭</span><span class="sxs-lookup"><span data-stu-id="8a940-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a940-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8a940-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a940-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a940-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="8a940-133">**參考**</span><span class="sxs-lookup"><span data-stu-id="8a940-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8a940-134">**CB \_ GETLBTEXT**</span><span class="sxs-lookup"><span data-stu-id="8a940-134">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="8a940-135">**LB \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="8a940-135">**LB\_GETTEXT**</span></span>](lb-gettext.md)
</dt> <dt>

<span data-ttu-id="8a940-136">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="8a940-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8a940-137">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="8a940-137">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="8a940-138">**WM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="8a940-138">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

