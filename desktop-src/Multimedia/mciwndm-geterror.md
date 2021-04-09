---
title: 'MCIWNDM_GETERROR 訊息 (Vfw .h) '
description: MCIWNDM \_ GETERROR 訊息會捕獲最後發生的 MCI 錯誤。 您可以使用 MCIWndGetError 宏明確地傳送此訊息。
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- MCIWNDM_GETERROR message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2977bb079351824b48da21f4ba3cc2dc5afe7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843195"
---
# <a name="mciwndm_geterror-message"></a><span data-ttu-id="3bee8-105">MCIWNDM \_ GETERROR 訊息</span><span class="sxs-lookup"><span data-stu-id="3bee8-105">MCIWNDM\_GETERROR message</span></span>

<span data-ttu-id="3bee8-106">**MCIWNDM \_ GETERROR** 訊息會捕獲最後發生的 MCI 錯誤。</span><span class="sxs-lookup"><span data-stu-id="3bee8-106">The **MCIWNDM\_GETERROR** message retrieves the last MCI error encountered.</span></span> <span data-ttu-id="3bee8-107">您可以使用 [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="3bee8-107">You can send this message explicitly or by using the [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) macro.</span></span>


```C++
MCIWNDM_GETERROR 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="3bee8-108">參數</span><span class="sxs-lookup"><span data-stu-id="3bee8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bee8-109"><span id="len"></span><span id="LEN"></span>*萊恩*</span><span class="sxs-lookup"><span data-stu-id="3bee8-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="3bee8-110">錯誤緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3bee8-110">Size, in bytes, of the error buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3bee8-111"><span id="lp"></span><span id="LP"></span>*Lp*</span><span class="sxs-lookup"><span data-stu-id="3bee8-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="3bee8-112">用來傳回錯誤字串之應用程式定義緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="3bee8-112">Pointer to an application-defined buffer used to return the error string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bee8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3bee8-113">Return Value</span></span>

<span data-ttu-id="3bee8-114">如果成功，則傳回整數誤差值。</span><span class="sxs-lookup"><span data-stu-id="3bee8-114">Returns the integer error value if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bee8-115">備註</span><span class="sxs-lookup"><span data-stu-id="3bee8-115">Remarks</span></span>

<span data-ttu-id="3bee8-116">如果 *lp* 是有效的指標，則會在緩衝區中傳回對應至錯誤的以 null 終止的字串。</span><span class="sxs-lookup"><span data-stu-id="3bee8-116">If *lp* is a valid pointer, a null-terminated string corresponding to the error is returned in its buffer.</span></span> <span data-ttu-id="3bee8-117">如果錯誤字串的長度超過緩衝區，MCIWnd 會將它截斷。</span><span class="sxs-lookup"><span data-stu-id="3bee8-117">If the error string is longer than the buffer, MCIWnd truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bee8-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bee8-118">Requirements</span></span>



| <span data-ttu-id="3bee8-119">需求</span><span class="sxs-lookup"><span data-stu-id="3bee8-119">Requirement</span></span> | <span data-ttu-id="3bee8-120">值</span><span class="sxs-lookup"><span data-stu-id="3bee8-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3bee8-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3bee8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3bee8-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3bee8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3bee8-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3bee8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3bee8-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3bee8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3bee8-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3bee8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bee8-126"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="3bee8-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bee8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bee8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bee8-128">**MCIWndGetError**</span><span class="sxs-lookup"><span data-stu-id="3bee8-128">**MCIWndGetError**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





