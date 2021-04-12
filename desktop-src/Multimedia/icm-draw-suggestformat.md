---
title: 'ICM_DRAW_SUGGESTFORMAT 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ SUGGESTFORMAT 訊息會查詢轉譯驅動程式，以建議可繪製的解壓縮格式。
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- ICM_DRAW_SUGGESTFORMAT message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_SUGGESTFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97c8782b16336427b3832f36b5a06987399df1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464632"
---
# <a name="icm_draw_suggestformat-message"></a><span data-ttu-id="284cd-104">ICM \_ 繪圖 \_ SUGGESTFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="284cd-104">ICM\_DRAW\_SUGGESTFORMAT message</span></span>

<span data-ttu-id="284cd-105">**ICM \_ DRAW \_ SUGGESTFORMAT** 訊息會查詢轉譯驅動程式，以建議可繪製的解壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="284cd-105">The **ICM\_DRAW\_SUGGESTFORMAT** message queries a rendering driver to suggest a decompressed format that it can draw.</span></span>


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a><span data-ttu-id="284cd-106">參數</span><span class="sxs-lookup"><span data-stu-id="284cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="284cd-107"><span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*</span><span class="sxs-lookup"><span data-stu-id="284cd-107"><span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*</span></span>
</dt> <dd>

<span data-ttu-id="284cd-108">[**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="284cd-108">Pointer to an [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure.</span></span>

</dd> <dt>

<span data-ttu-id="284cd-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="284cd-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="284cd-110">[**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="284cd-110">Size, in bytes, of [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="284cd-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="284cd-111">Return Value</span></span>

<span data-ttu-id="284cd-112">\_如果成功，則會傳回 ICERR OK。</span><span class="sxs-lookup"><span data-stu-id="284cd-112">Returns ICERR\_OK if successful.</span></span> <span data-ttu-id="284cd-113">如果 [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)結構的 **LpbiSuggest** 成員是 **Null**，則此訊息會傳回包含建議格式所需的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="284cd-113">If the **lpbiSuggest** member of the [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure is **NULL**, this message returns the amount of memory required to contain the suggested format.</span></span>

## <a name="remarks"></a><span data-ttu-id="284cd-114">備註</span><span class="sxs-lookup"><span data-stu-id="284cd-114">Remarks</span></span>

<span data-ttu-id="284cd-115">驅動程式應該檢查 [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)結構的 **lpbiIn** 成員中指定的格式，並使用 **lpbiSuggest** 成員傳回可繪製的格式。</span><span class="sxs-lookup"><span data-stu-id="284cd-115">The driver should examine the format specified in the **lpbiIn** member of the [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure and use the **lpbiSuggest** member to return a format it can draw.</span></span> <span data-ttu-id="284cd-116">輸出格式應盡可能保留輸入格式的最多資料。</span><span class="sxs-lookup"><span data-stu-id="284cd-116">The output format should preserve as much data as possible from the input format.</span></span>

<span data-ttu-id="284cd-117">（選擇性）驅動程式可以使用在 [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)的 **hicDecompressor** 成員中傳遞的可安裝的壓縮程式控制碼，以進行更複雜的選取。</span><span class="sxs-lookup"><span data-stu-id="284cd-117">Optionally, the driver can use the installable compressor handle passed in the **hicDecompressor** member of [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) to make more complex selections.</span></span> <span data-ttu-id="284cd-118">例如，如果輸入格式是24位 JPEG 資料，轉譯器可以查詢解壓縮程式以找出是否可以解壓縮至 YUV 格式 (在選取要建議的格式之前，) 可能會更有效率地繪製。</span><span class="sxs-lookup"><span data-stu-id="284cd-118">For example, if the input format is 24-bit JPEG data, a renderer could query the decompressor to find out if it can decompress to a YUV format (which might be drawn more efficiently) before selecting the format to suggest.</span></span>

## <a name="requirements"></a><span data-ttu-id="284cd-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="284cd-119">Requirements</span></span>



| <span data-ttu-id="284cd-120">需求</span><span class="sxs-lookup"><span data-stu-id="284cd-120">Requirement</span></span> | <span data-ttu-id="284cd-121">值</span><span class="sxs-lookup"><span data-stu-id="284cd-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="284cd-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="284cd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="284cd-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="284cd-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="284cd-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="284cd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="284cd-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="284cd-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="284cd-126">標頭</span><span class="sxs-lookup"><span data-stu-id="284cd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="284cd-127"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="284cd-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="284cd-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="284cd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="284cd-129">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="284cd-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="284cd-130">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="284cd-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





