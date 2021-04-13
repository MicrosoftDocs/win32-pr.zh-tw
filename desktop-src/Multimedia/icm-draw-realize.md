---
title: 'ICM_DRAW_REALIZE 訊息 (Vfw .h) '
description: ICM \_ DRAW 的 \_ 認識訊息會通知轉譯驅動程式，以在繪製時實現其繪圖調色板。 您可以使用 ICDrawRealize 宏明確地傳送此訊息。
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- ICM_DRAW_REALIZE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd054c16caae55cba25c30098337e54b0ec4b681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384486"
---
# <a name="icm_draw_realize-message"></a><span data-ttu-id="eed6a-105">ICM \_ 繪圖 \_ 實現訊息</span><span class="sxs-lookup"><span data-stu-id="eed6a-105">ICM\_DRAW\_REALIZE message</span></span>

<span data-ttu-id="eed6a-106">**ICM \_ DRAW 的 \_ 認識** 訊息會通知轉譯驅動程式，以在繪製時實現其繪圖調色板。</span><span class="sxs-lookup"><span data-stu-id="eed6a-106">The **ICM\_DRAW\_REALIZE** message notifies a rendering driver to realize its drawing palette while drawing.</span></span> <span data-ttu-id="eed6a-107">您可以使用 [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="eed6a-107">You can send this message explicitly or by using the [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) macro.</span></span>


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a><span data-ttu-id="eed6a-108">參數</span><span class="sxs-lookup"><span data-stu-id="eed6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eed6a-109"><span id="hdc"></span><span id="HDC"></span>*hdc*</span><span class="sxs-lookup"><span data-stu-id="eed6a-109"><span id="hdc"></span><span id="HDC"></span>*hdc*</span></span>
</dt> <dd>

<span data-ttu-id="eed6a-110">用來實現調色板的 DC 控點。</span><span class="sxs-lookup"><span data-stu-id="eed6a-110">Handle to the DC used to realize the palette.</span></span>

</dd> <dt>

<span data-ttu-id="eed6a-111"><span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*</span><span class="sxs-lookup"><span data-stu-id="eed6a-111"><span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*</span></span>
</dt> <dd>

<span data-ttu-id="eed6a-112">背景旗標。</span><span class="sxs-lookup"><span data-stu-id="eed6a-112">Background flag.</span></span> <span data-ttu-id="eed6a-113">指定 **TRUE** 以將選擇區視為背景工作，或使用 **FALSE** 來實現前景中的調色板。</span><span class="sxs-lookup"><span data-stu-id="eed6a-113">Specify **TRUE** to realize the palette as a background task or **FALSE** to realize the palette in the foreground.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eed6a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="eed6a-114">Return Value</span></span>

<span data-ttu-id="eed6a-115">如果已實現繪圖選擇區，則會傳回 ICERR \_ OK; \_ 如果已實現與解壓縮資料相關聯的元件，則會 ICERR 不支援此選項。</span><span class="sxs-lookup"><span data-stu-id="eed6a-115">Returns ICERR\_OK if the drawing palette is realized or ICERR\_UNSUPPORTED if the palette associated with the decompressed data is realized.</span></span>

## <a name="remarks"></a><span data-ttu-id="eed6a-116">備註</span><span class="sxs-lookup"><span data-stu-id="eed6a-116">Remarks</span></span>

<span data-ttu-id="eed6a-117">只有當繪圖選擇區與解壓縮的調色板不同時，驅動程式才需要回應此訊息。</span><span class="sxs-lookup"><span data-stu-id="eed6a-117">Drivers need to respond to this message only if the drawing palette is different from the decompressed palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="eed6a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="eed6a-118">Requirements</span></span>



| <span data-ttu-id="eed6a-119">需求</span><span class="sxs-lookup"><span data-stu-id="eed6a-119">Requirement</span></span> | <span data-ttu-id="eed6a-120">值</span><span class="sxs-lookup"><span data-stu-id="eed6a-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eed6a-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eed6a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="eed6a-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eed6a-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="eed6a-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eed6a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="eed6a-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eed6a-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="eed6a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="eed6a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="eed6a-126"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="eed6a-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eed6a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eed6a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed6a-128">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="eed6a-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="eed6a-129">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="eed6a-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





