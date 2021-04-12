---
title: 'ICM_DRAW_BEGIN 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ 開始訊息會通知轉譯驅動程式，以準備繪製資料。
ms.assetid: e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8
keywords:
- ICM_DRAW_BEGIN message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db7b9e20a0b0621038e1c7e092a871a6727566cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934879"
---
# <a name="icm_draw_begin-message"></a><span data-ttu-id="ac6b0-104">ICM \_ 繪圖 \_ 開始訊息</span><span class="sxs-lookup"><span data-stu-id="ac6b0-104">ICM\_DRAW\_BEGIN message</span></span>

<span data-ttu-id="ac6b0-105">**ICM \_ DRAW \_ 開始** 訊息會通知轉譯驅動程式，以準備繪製資料。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-105">The **ICM\_DRAW\_BEGIN** message notifies a rendering driver to prepare to draw data.</span></span>


```C++
ICM_DRAW_BEGIN 
wParam = (DWORD) (LPVOID) &icdrwBgn; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a><span data-ttu-id="ac6b0-106">參數</span><span class="sxs-lookup"><span data-stu-id="ac6b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac6b0-107"><span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*</span><span class="sxs-lookup"><span data-stu-id="ac6b0-107"><span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*</span></span>
</dt> <dd>

<span data-ttu-id="ac6b0-108">[**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)結構的指標，其中包含輸入格式。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-108">Pointer to an [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="ac6b0-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac6b0-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="ac6b0-110">**ICDRAWBEGIN** 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-110">Size, in bytes, of **ICDRAWBEGIN**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac6b0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac6b0-111">Return Value</span></span>

<span data-ttu-id="ac6b0-112">\_如果驅動程式支援以指定的方式和格式將資料繪製到螢幕，則會傳回 ICERR OK，否則會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-112">Returns ICERR\_OK if the driver supports drawing the data to the screen in the specified manner and format, or an error code otherwise.</span></span> <span data-ttu-id="ac6b0-113">可能的錯誤值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-113">Possible error values include the following.</span></span>



| <span data-ttu-id="ac6b0-114">值</span><span class="sxs-lookup"><span data-stu-id="ac6b0-114">Value</span></span>               | <span data-ttu-id="ac6b0-115">意義</span><span class="sxs-lookup"><span data-stu-id="ac6b0-115">Meaning</span></span>                                                                       |
|---------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="ac6b0-116">ICERR \_ BADFORMAT</span><span class="sxs-lookup"><span data-stu-id="ac6b0-116">ICERR\_BADFORMAT</span></span>    | <span data-ttu-id="ac6b0-117">不支援輸入或輸出格式。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-117">Input or output format is not supported.</span></span>                                      |
| <span data-ttu-id="ac6b0-118">ICERR \_ NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="ac6b0-118">ICERR\_NOTSUPPORTED</span></span> | <span data-ttu-id="ac6b0-119">驅動程式不會直接繪製到螢幕上，或不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-119">Driver does not draw directly to the screen or does not support this message.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ac6b0-120">備註</span><span class="sxs-lookup"><span data-stu-id="ac6b0-120">Remarks</span></span>

<span data-ttu-id="ac6b0-121">如果您想要驅動程式將資料解壓縮到緩衝區中，請傳送 [**ICM \_ 解壓縮 \_ 開始**](icm-decompress-begin.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-121">If you want the driver to decompress data into a buffer, send the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="ac6b0-122">**Icm \_ draw \_ BEGIN** 和 [**icm \_ draw \_ END**](icm-draw-end.md)訊息不會被嵌套。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-122">The **ICM\_DRAW\_BEGIN** and [**ICM\_DRAW\_END**](icm-draw-end.md) messages do not nest.</span></span> <span data-ttu-id="ac6b0-123">如果您的驅動程式會在使用 **icm \_ draw \_ END** 停止解壓縮之前 **\_ \_ 開始進行 icm 繪製**，則應該以新的參數重新開機解壓縮。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-123">If your driver receives **ICM\_DRAW\_BEGIN** before decompression is stopped with **ICM\_DRAW\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac6b0-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac6b0-124">Requirements</span></span>



| <span data-ttu-id="ac6b0-125">需求</span><span class="sxs-lookup"><span data-stu-id="ac6b0-125">Requirement</span></span> | <span data-ttu-id="ac6b0-126">值</span><span class="sxs-lookup"><span data-stu-id="ac6b0-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ac6b0-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac6b0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ac6b0-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac6b0-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ac6b0-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac6b0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ac6b0-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac6b0-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ac6b0-131">標頭</span><span class="sxs-lookup"><span data-stu-id="ac6b0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac6b0-132"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="ac6b0-132"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac6b0-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac6b0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac6b0-134">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="ac6b0-134">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="ac6b0-135">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="ac6b0-135">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





