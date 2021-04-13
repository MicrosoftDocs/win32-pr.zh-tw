---
title: 'ICM_DRAW_QUERY 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ 查詢訊息會查詢轉譯驅動程式，以判斷它是否可以轉譯特定格式的資料。 您可以使用 ICDrawQuery 宏明確地傳送此訊息。
ms.assetid: b829a04b-c1be-47c6-96e9-a6dc6f802811
keywords:
- ICM_DRAW_QUERY message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27266484cffa503583df32b60c6e8a0c04f344f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465668"
---
# <a name="icm_draw_query-message"></a><span data-ttu-id="945a8-105">ICM \_ 繪製 \_ 查詢訊息</span><span class="sxs-lookup"><span data-stu-id="945a8-105">ICM\_DRAW\_QUERY message</span></span>

<span data-ttu-id="945a8-106">**ICM \_ DRAW \_ 查詢** 訊息會查詢轉譯驅動程式，以判斷它是否可以轉譯特定格式的資料。</span><span class="sxs-lookup"><span data-stu-id="945a8-106">The **ICM\_DRAW\_QUERY** message queries a rendering driver to determine if it can render data in a specific format.</span></span> <span data-ttu-id="945a8-107">您可以使用 [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="945a8-107">You can send this message explicitly or by using the [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) macro.</span></span>


```C++
ICM_DRAW_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="945a8-108">參數</span><span class="sxs-lookup"><span data-stu-id="945a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="945a8-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="945a8-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="945a8-110">[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸入格式。</span><span class="sxs-lookup"><span data-stu-id="945a8-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="945a8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="945a8-111">Return Value</span></span>

<span data-ttu-id="945a8-112">\_如果驅動程式能以指定的格式或 ICERR BADFORMAT 轉譯資料，則會傳回 ICERR OK （否則為） \_ 。</span><span class="sxs-lookup"><span data-stu-id="945a8-112">Returns ICERR\_OK if the driver can render data in the specified format or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="945a8-113">備註</span><span class="sxs-lookup"><span data-stu-id="945a8-113">Remarks</span></span>

<span data-ttu-id="945a8-114">這則訊息與 [**ICM \_ DRAW \_ 開始**](icm-draw-begin.md) 訊息不同之處在于，它會查詢驅動程式的一般意義。</span><span class="sxs-lookup"><span data-stu-id="945a8-114">This message differs from the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message in that it queries the driver in a general sense.</span></span> <span data-ttu-id="945a8-115">**ICM \_DRAW \_ BEGIN** 會決定驅動程式是否可以在特定情況下使用指定的格式來繪製資料，例如延展影像。</span><span class="sxs-lookup"><span data-stu-id="945a8-115">**ICM\_DRAW\_BEGIN** determines if the driver can draw the data using the specified format under specific conditions, such as stretching the image.</span></span>

## <a name="requirements"></a><span data-ttu-id="945a8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="945a8-116">Requirements</span></span>



| <span data-ttu-id="945a8-117">需求</span><span class="sxs-lookup"><span data-stu-id="945a8-117">Requirement</span></span> | <span data-ttu-id="945a8-118">值</span><span class="sxs-lookup"><span data-stu-id="945a8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="945a8-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="945a8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="945a8-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="945a8-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="945a8-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="945a8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="945a8-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="945a8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="945a8-123">標頭</span><span class="sxs-lookup"><span data-stu-id="945a8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="945a8-124"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="945a8-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="945a8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="945a8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="945a8-126">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="945a8-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="945a8-127">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="945a8-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

