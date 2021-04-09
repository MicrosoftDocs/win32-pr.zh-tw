---
title: 'WM_CAP_DLG_VIDEOCOMPRESSION 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION] 訊息會顯示一個對話方塊，讓使用者可以在此對話方塊中選取要在捕獲進程期間使用的壓縮程式。'
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- WM_CAP_DLG_VIDEOCOMPRESSION message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOCOMPRESSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d851f73df7adbc205585eb7c69ad9d4d969aba66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025065"
---
# <a name="wm_cap_dlg_videocompression-message"></a><span data-ttu-id="a0844-104">WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION 訊息</span><span class="sxs-lookup"><span data-stu-id="a0844-104">WM\_CAP\_DLG\_VIDEOCOMPRESSION message</span></span>

<span data-ttu-id="a0844-105">[ **WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION** ] 訊息會顯示一個對話方塊，讓使用者可以在此對話方塊中選取要在捕獲進程期間使用的壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="a0844-105">The **WM\_CAP\_DLG\_VIDEOCOMPRESSION** message displays a dialog box in which the user can select a compressor to use during the capture process.</span></span> <span data-ttu-id="a0844-106">可用的壓縮機清單會隨著 [捕捉驅動程式的影片格式] 對話方塊中選取的影片格式而有所不同。</span><span class="sxs-lookup"><span data-stu-id="a0844-106">The list of available compressors can vary with the video format selected in the capture driver's Video Format dialog box.</span></span> <span data-ttu-id="a0844-107">您可以使用 [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="a0844-107">You can send this message explicitly or by using the [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="a0844-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="a0844-108">Return Value</span></span>

<span data-ttu-id="a0844-109">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a0844-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0844-110">備註</span><span class="sxs-lookup"><span data-stu-id="a0844-110">Remarks</span></span>

<span data-ttu-id="a0844-111">使用此訊息搭配只提供 BI RGB 格式之框架的捕獲驅動程式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a0844-111">Use this message with capture drivers that provide frames only in the BI\_RGB format.</span></span> <span data-ttu-id="a0844-112">這則訊息最適合用於在單一作業中合併捕捉和壓縮的步驟捕獲作業。</span><span class="sxs-lookup"><span data-stu-id="a0844-112">This message is most useful in the step capture operation to combine capture and compression in a single operation.</span></span> <span data-ttu-id="a0844-113">使用軟體壓縮程式將框架壓縮為即時捕捉作業的一部分，很可能太耗時而無法執行。</span><span class="sxs-lookup"><span data-stu-id="a0844-113">Compressing frames with a software compressor as part of a real-time capture operation is most likely too time-consuming to perform.</span></span>

<span data-ttu-id="a0844-114">壓縮不會影響複製到剪貼簿的畫面。</span><span class="sxs-lookup"><span data-stu-id="a0844-114">Compression does not affect the frames copied to the clipboard.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0844-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0844-115">Requirements</span></span>



| <span data-ttu-id="a0844-116">需求</span><span class="sxs-lookup"><span data-stu-id="a0844-116">Requirement</span></span> | <span data-ttu-id="a0844-117">值</span><span class="sxs-lookup"><span data-stu-id="a0844-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a0844-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0844-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a0844-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0844-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a0844-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0844-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a0844-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0844-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a0844-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a0844-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0844-123"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="a0844-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0844-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0844-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0844-125">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="a0844-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="a0844-126">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="a0844-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





