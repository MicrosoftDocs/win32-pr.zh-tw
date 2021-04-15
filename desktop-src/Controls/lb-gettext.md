---
title: 'LB_GETTEXT 訊息 (Winuser .h) '
description: 從清單方塊中取得字串。
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- LB_GETTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dd5e2c7a9e6c1c1aa1b847592555a013766134
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466336"
---
# <a name="lb_gettext-message"></a><span data-ttu-id="143b1-104">LB \_ GETTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="143b1-104">LB\_GETTEXT message</span></span>

<span data-ttu-id="143b1-105">從清單方塊中取得字串。</span><span class="sxs-lookup"><span data-stu-id="143b1-105">Gets a string from a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="143b1-106">參數</span><span class="sxs-lookup"><span data-stu-id="143b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="143b1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="143b1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="143b1-108">要抓取之字串的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="143b1-108">The zero-based index of the string to retrieve.</span></span>

<span data-ttu-id="143b1-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="143b1-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="143b1-110">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="143b1-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="143b1-111">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="143b1-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="143b1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="143b1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="143b1-113">將接收字串的緩衝區指標;它是 **LPTSTR** 類型，接著會轉換成 **LPARAM**。</span><span class="sxs-lookup"><span data-stu-id="143b1-113">A pointer to the buffer that will receive the string; it is type **LPTSTR** which is subsequently cast to an **LPARAM**.</span></span> <span data-ttu-id="143b1-114">緩衝區必須有足夠的空間可供字串和終止的 null 字元使用。</span><span class="sxs-lookup"><span data-stu-id="143b1-114">The buffer must have sufficient space for the string and a terminating null character.</span></span> <span data-ttu-id="143b1-115">您可以在 **lb \_ GETTEXT** 訊息之前傳送 [**lb \_ GETTEXTLEN**](lb-gettextlen.md)訊息，以取得字串的長度（以 **TCHAR** s 為限）。</span><span class="sxs-lookup"><span data-stu-id="143b1-115">An [**LB\_GETTEXTLEN**](lb-gettextlen.md) message can be sent before the **LB\_GETTEXT** message to retrieve the length, in **TCHAR** s, of the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="143b1-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="143b1-116">Return value</span></span>

<span data-ttu-id="143b1-117">傳回值是字串的長度（在 **TCHAR** s 中），不包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="143b1-117">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="143b1-118">如果 *wParam* 未指定有效的索引，則傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="143b1-118">If *wParam* does not specify a valid index, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="143b1-119">備註</span><span class="sxs-lookup"><span data-stu-id="143b1-119">Remarks</span></span>

<span data-ttu-id="143b1-120">如果清單方塊有擁有者繪製的樣式，而不是 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式，則 *lParam* 參數所指向的緩衝區會接收與專案資料)  (專案相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="143b1-120">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the buffer pointed to by the *lParam* parameter receives the value associated with the item (the item data).</span></span>

## <a name="requirements"></a><span data-ttu-id="143b1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="143b1-121">Requirements</span></span>



| <span data-ttu-id="143b1-122">需求</span><span class="sxs-lookup"><span data-stu-id="143b1-122">Requirement</span></span> | <span data-ttu-id="143b1-123">值</span><span class="sxs-lookup"><span data-stu-id="143b1-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="143b1-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="143b1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="143b1-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="143b1-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="143b1-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="143b1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="143b1-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="143b1-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="143b1-128">標頭</span><span class="sxs-lookup"><span data-stu-id="143b1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="143b1-129"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="143b1-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="143b1-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="143b1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="143b1-131">**LB \_ GETTEXTLEN**</span><span class="sxs-lookup"><span data-stu-id="143b1-131">**LB\_GETTEXTLEN**</span></span>](lb-gettextlen.md)
</dt> </dl>

 

 





