---
description: 指定是否將 MPEG-2 檔案接收篩選出 sequence 參數集 (SPS) 和圖片參數集 (PPS) NALUs。
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: 'MF_MPEG4SINK_SPSPPS_PASSTHROUGH 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c02f4f1cdcac17a104b5061c8899c92e0ad824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691815"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a><span data-ttu-id="4dda4-103">MF \_ MPEG4SINK \_ SPSPPS \_ 傳遞屬性</span><span class="sxs-lookup"><span data-stu-id="4dda4-103">MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH attribute</span></span>

<span data-ttu-id="4dda4-104">指定是否將 [**mpeg-2 檔案接收**](mpeg-4-file-sink.md) 篩選出 sequence 參數集 (SPS) 和圖片參數集 (PPS) NALUs。</span><span class="sxs-lookup"><span data-stu-id="4dda4-104">Specifies whether the [**MPEG-4 File Sink**](mpeg-4-file-sink.md) filters out sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

## <a name="data-type"></a><span data-ttu-id="4dda4-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="4dda4-105">Data type</span></span>

<span data-ttu-id="4dda4-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="4dda4-106">**BOOL** stored as **UINT32**</span></span>

## <a name="applies-to"></a><span data-ttu-id="4dda4-107">適用於</span><span class="sxs-lookup"><span data-stu-id="4dda4-107">Applies to</span></span>

[<span data-ttu-id="4dda4-108">**IMFMediaSink**</span><span class="sxs-lookup"><span data-stu-id="4dda4-108">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a><span data-ttu-id="4dda4-109">備註</span><span class="sxs-lookup"><span data-stu-id="4dda4-109">Remarks</span></span>

<span data-ttu-id="4dda4-110">[**Mpeg-2 檔案接收**](mpeg-4-file-sink.md)會將 SP 和 PPS 參數寫入至「數量」檔案的 [範例描述] 方塊中。</span><span class="sxs-lookup"><span data-stu-id="4dda4-110">The [**MPEG-4 File Sink**](mpeg-4-file-sink.md) writes the SPS and PPS parameters into the sample description box of the MP4 file.</span></span> <span data-ttu-id="4dda4-111">根據預設，它會從影片串流篩選出 SPS 和 PPS NALUs。</span><span class="sxs-lookup"><span data-stu-id="4dda4-111">By default, it filters out the SPS and PPS NALUs from the video stream.</span></span> <span data-ttu-id="4dda4-112">若要覆寫此行為，請將 [MF \_ MPEG4SINK \_ SPSPPS \_ 傳遞] 屬性設定為 [ **TRUE**]。</span><span class="sxs-lookup"><span data-stu-id="4dda4-112">To override this behavior, set the MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH attribute to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dda4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4dda4-113">Requirements</span></span>



| <span data-ttu-id="4dda4-114">需求</span><span class="sxs-lookup"><span data-stu-id="4dda4-114">Requirement</span></span> | <span data-ttu-id="4dda4-115">值</span><span class="sxs-lookup"><span data-stu-id="4dda4-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4dda4-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4dda4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4dda4-117">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4dda4-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4dda4-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4dda4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4dda4-119">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4dda4-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4dda4-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4dda4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dda4-121"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4dda4-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dda4-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4dda4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dda4-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="4dda4-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




