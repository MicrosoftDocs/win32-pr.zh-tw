---
title: 'MCIWNDM_RETURNSTRING 訊息 (Vfw .h) '
description: MCIWNDM \_ RETURNSTRING 訊息會將回復傳給傳送至 MCI 裝置的最新 mci 字串命令。
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- MCIWNDM_RETURNSTRING message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_RETURNSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b99307bd7d61a70db594d0a696cceccd6d246a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025068"
---
# <a name="mciwndm_returnstring-message"></a><span data-ttu-id="6a76d-104">MCIWNDM \_ RETURNSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="6a76d-104">MCIWNDM\_RETURNSTRING message</span></span>

<span data-ttu-id="6a76d-105">**MCIWNDM \_ RETURNSTRING** 訊息會將回復傳給傳送至 MCI 裝置的最新 mci 字串命令。</span><span class="sxs-lookup"><span data-stu-id="6a76d-105">The **MCIWNDM\_RETURNSTRING** message retrieves the reply to the most recent MCI string command sent to an MCI device.</span></span> <span data-ttu-id="6a76d-106">回復中的資訊是以 null 終止字串的形式提供。</span><span class="sxs-lookup"><span data-stu-id="6a76d-106">Information in the reply is supplied as a null-terminated string.</span></span> <span data-ttu-id="6a76d-107">您可以使用 [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="6a76d-107">You can send this message explicitly or by using the [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) macro.</span></span>


```C++
MCIWNDM_RETURNSTRING 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="6a76d-108">參數</span><span class="sxs-lookup"><span data-stu-id="6a76d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a76d-109"><span id="len"></span><span id="LEN"></span>*萊恩*</span><span class="sxs-lookup"><span data-stu-id="6a76d-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="6a76d-110">緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6a76d-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6a76d-111"><span id="lp"></span><span id="LP"></span>*Lp*</span><span class="sxs-lookup"><span data-stu-id="6a76d-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="6a76d-112">應用程式定義的緩衝區指標，包含以 null 終止的字串。</span><span class="sxs-lookup"><span data-stu-id="6a76d-112">Pointer to an application-defined buffer to contain the null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a76d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a76d-113">Return Value</span></span>

<span data-ttu-id="6a76d-114">傳回對應至 MCI 字串的整數。</span><span class="sxs-lookup"><span data-stu-id="6a76d-114">Returns an integer corresponding to the MCI string.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a76d-115">備註</span><span class="sxs-lookup"><span data-stu-id="6a76d-115">Remarks</span></span>

<span data-ttu-id="6a76d-116">如果以 null 終止的字串比緩衝區長，則會截斷字串。</span><span class="sxs-lookup"><span data-stu-id="6a76d-116">If the null-terminated string is longer than the buffer, the string is truncated.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a76d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a76d-117">Requirements</span></span>



| <span data-ttu-id="6a76d-118">需求</span><span class="sxs-lookup"><span data-stu-id="6a76d-118">Requirement</span></span> | <span data-ttu-id="6a76d-119">值</span><span class="sxs-lookup"><span data-stu-id="6a76d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6a76d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a76d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6a76d-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a76d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6a76d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a76d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6a76d-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a76d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6a76d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6a76d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a76d-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a76d-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a76d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a76d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a76d-127">**MCIWndReturnString**</span><span class="sxs-lookup"><span data-stu-id="6a76d-127">**MCIWndReturnString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 





