---
title: 'CB_GETLBTEXT 訊息 (Winuser .h) '
description: 從下拉式方塊的清單中取得字串。
ms.assetid: f84e302a-65bb-45c8-958b-1cb438fb5a7a
keywords:
- CB_GETLBTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETLBTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d26a964b463daedab1ad5d9f50888b3e0c1e0db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025089"
---
# <a name="cb_getlbtext-message"></a><span data-ttu-id="1be1d-104">CB \_ GETLBTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="1be1d-104">CB\_GETLBTEXT message</span></span>

<span data-ttu-id="1be1d-105">從下拉式方塊的清單中取得字串。</span><span class="sxs-lookup"><span data-stu-id="1be1d-105">Gets a string from the list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="1be1d-106">參數</span><span class="sxs-lookup"><span data-stu-id="1be1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1be1d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1be1d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1be1d-108">要抓取之字串的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="1be1d-108">The zero-based index of the string to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="1be1d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1be1d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1be1d-110">接收字串的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="1be1d-110">A pointer to the buffer that receives the string.</span></span> <span data-ttu-id="1be1d-111">緩衝區必須有足夠的空間可供字串和終止的 null 字元使用。</span><span class="sxs-lookup"><span data-stu-id="1be1d-111">The buffer must have sufficient space for the string and a terminating null character.</span></span> <span data-ttu-id="1be1d-112">您可以在 **cb \_ GETLBTEXT** 訊息之前傳送 [**cb \_ GETLBTEXTLEN**](cb-getlbtextlen.md)訊息，以取得字串的長度（以 **TCHAR** s 為限）。</span><span class="sxs-lookup"><span data-stu-id="1be1d-112">You can send a [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) message prior to the **CB\_GETLBTEXT** message to retrieve the length, in **TCHAR** s, of the string.</span></span> <span data-ttu-id="1be1d-113">如果是 ANSI 字串，則這是位元組的數目，但如果它是 Unicode 字串，則這是字元數。</span><span class="sxs-lookup"><span data-stu-id="1be1d-113">If it is an ANSI string this is the number of bytes, but if it is a Unicode string this is the number of characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1be1d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="1be1d-114">Return value</span></span>

<span data-ttu-id="1be1d-115">傳回值是字串的長度（在 **TCHAR** s 中），不包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="1be1d-115">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="1be1d-116">如果 *wParam* 未指定有效的索引，則傳回值為 CB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="1be1d-116">If *wParam* does not specify a valid index, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="1be1d-117">備註</span><span class="sxs-lookup"><span data-stu-id="1be1d-117">Remarks</span></span>

<span data-ttu-id="1be1d-118">**安全性警告：** 不當使用此訊息可能會危及程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="1be1d-118">**Security Warning:** Using this message incorrectly can compromise the security of your program.</span></span> <span data-ttu-id="1be1d-119">此訊息不會提供您知道緩衝區大小的方法。</span><span class="sxs-lookup"><span data-stu-id="1be1d-119">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="1be1d-120">如果您使用此訊息，請先呼叫 [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) 來取得所需的字元數，然後呼叫訊息以取得字串。</span><span class="sxs-lookup"><span data-stu-id="1be1d-120">If you use this message, first call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) to get the number of characters that are required and then call the message to retrieve the string.</span></span> <span data-ttu-id="1be1d-121">您應該先複習 [安全性考慮： Microsoft Windows 控制項](sec-comctls.md) ，再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="1be1d-121">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="1be1d-122">如果您建立具有主控描繪樣式的下拉式方塊，但沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式，則 *lParam* 所指向的緩衝區會接收與該專案相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="1be1d-122">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the buffer pointed to by *lParam* receives the data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="1be1d-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="1be1d-123">Requirements</span></span>



| <span data-ttu-id="1be1d-124">需求</span><span class="sxs-lookup"><span data-stu-id="1be1d-124">Requirement</span></span> | <span data-ttu-id="1be1d-125">值</span><span class="sxs-lookup"><span data-stu-id="1be1d-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1be1d-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1be1d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1be1d-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1be1d-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1be1d-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1be1d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1be1d-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1be1d-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1be1d-130">標頭</span><span class="sxs-lookup"><span data-stu-id="1be1d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1be1d-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1be1d-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1be1d-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1be1d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1be1d-133">**CB \_ GETLBTEXTLEN**</span><span class="sxs-lookup"><span data-stu-id="1be1d-133">**CB\_GETLBTEXTLEN**</span></span>](cb-getlbtextlen.md)
</dt> </dl>

 

 





