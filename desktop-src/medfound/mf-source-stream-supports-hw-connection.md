---
description: 指出媒體來源是否支援硬體資料流程。
ms.assetid: 32FEBC99-0AE0-4FE9-90AB-5FB204BD4C83
title: 'MF_SOURCE_STREAM_SUPPORTS_HW_CONNECTION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751d672e664ab1849376d839285393075ddf6af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979302"
---
# <a name="mf_source_stream_supports_hw_connection-attribute"></a><span data-ttu-id="4d208-103">MF \_ 來源 \_ 資料流程 \_ 支援 \_ HW \_ 連接屬性</span><span class="sxs-lookup"><span data-stu-id="4d208-103">MF\_SOURCE\_STREAM\_SUPPORTS\_HW\_CONNECTION attribute</span></span>

<span data-ttu-id="4d208-104">指出媒體來源是否支援硬體資料流程。</span><span class="sxs-lookup"><span data-stu-id="4d208-104">Indicates whether a media source supports hardware data flow.</span></span>

## <a name="data-type"></a><span data-ttu-id="4d208-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="4d208-105">Data type</span></span>

<span data-ttu-id="4d208-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="4d208-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4d208-107">備註</span><span class="sxs-lookup"><span data-stu-id="4d208-107">Remarks</span></span>

<span data-ttu-id="4d208-108">當媒體來源 proxy 硬體裝置，而且能夠透過硬體匯流排傳輸下游資料，而不需要將資料傳送到 CPU 時，就會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="4d208-108">This attribute is used when a media source proxies a hardware device and is able to transfer data downstream over a hardware bus, without sending data up to the CPU.</span></span> <span data-ttu-id="4d208-109">例如，網路攝影機可能會將 h.264 編碼的影片直接傳遞至整合式硬體解碼器。</span><span class="sxs-lookup"><span data-stu-id="4d208-109">For example, a webcam might deliver H.264-encoded video directly to an integrated hardware decoder.</span></span>

<span data-ttu-id="4d208-110">在此案例中，來源和解碼器仍會以 [媒體來源](media-sources.md) 物件的 Microsoft 媒體基礎來表示，而 [媒體基礎轉換](media-foundation-transforms.md) (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="4d208-110">In this scenario, the source and decoder are still represented in the Microsoft Media Foundation by a [media source](media-sources.md) object and a [Media Foundation transform](media-foundation-transforms.md) (MFT).</span></span> <span data-ttu-id="4d208-111">不過，在管線層的這兩個物件之間不會有資料流程，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="4d208-111">However, no data flows between these two objects at the pipeline layer, only at the hardware layer, as shown in the following diagram.</span></span>

![顯示硬體 proxy 來源的圖表。](images/proxy-mft3.png)

<span data-ttu-id="4d208-113">媒體來源和 MFT 之間的連接會以下面方式協商。</span><span class="sxs-lookup"><span data-stu-id="4d208-113">The connection between the media source and the MFT is negotiated as follows.</span></span>

1.  <span data-ttu-id="4d208-114">管線會查詢 [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) 介面的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="4d208-114">The pipeline queries the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span> <span data-ttu-id="4d208-115"> (此介面為支援媒體來源的選擇性。 ) </span><span class="sxs-lookup"><span data-stu-id="4d208-115">(This interface is optional for media sources to support.)</span></span>
2.  <span data-ttu-id="4d208-116">管線會呼叫 [**IMFMediaSourceEx：： GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) 來取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。</span><span class="sxs-lookup"><span data-stu-id="4d208-116">The pipeline calls [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
3.  <span data-ttu-id="4d208-117">適用于 MF \_ 來來源資料流的管線 \_ 查詢 \_ 支援 \_ HW \_ 連接屬性。</span><span class="sxs-lookup"><span data-stu-id="4d208-117">The pipeline queries for the MF\_SOURCE\_STREAM\_SUPPORTS\_HW\_CONNECTION attribute.</span></span> <span data-ttu-id="4d208-118">如果屬性存在且等於 **TRUE**，則媒體來源支援硬體連接。</span><span class="sxs-lookup"><span data-stu-id="4d208-118">If the attribute is present and equal to **TRUE**, the media source supports hardware connections.</span></span>
4.  <span data-ttu-id="4d208-119">此管線會檢查 mft 上的 [mft \_ 列舉 \_ 硬體 \_ URL \_ 屬性](mft-enum-hardware-url-attribute.md) 屬性，以檢查 mft 是否也是硬體 proxy。</span><span class="sxs-lookup"><span data-stu-id="4d208-119">The pipeline checks if the MFT is also a hardware proxy, by checking for the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="4d208-120">如需詳細資訊，請參閱 [硬體 MFTs](hardware-mfts.md)。</span><span class="sxs-lookup"><span data-stu-id="4d208-120">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>
5.  <span data-ttu-id="4d208-121">管線會在 MFT 上設定 [mft \_ 連線 \_ 資料流程 \_ 屬性](mft-connected-stream-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4d208-121">The pipeline sets the [MFT\_CONNECTED\_STREAM\_ATTRIBUTE](mft-connected-stream-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="4d208-122">這個屬性的值是從步驟2中的媒體來源取得的 [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。</span><span class="sxs-lookup"><span data-stu-id="4d208-122">The value of this attribute is the [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer obtained from the media source in step 2.</span></span>
6.  <span data-ttu-id="4d208-123">管線會在媒體來源和 MFT 上將 [ \_ 連接 \_ 至 \_ HW \_ STREAM](mft-connected-to-hw-stream.md) 屬性的 MFT 設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="4d208-123">The pipeline sets the [MFT\_CONNECTED\_TO\_HW\_STREAM](mft-connected-to-hw-stream.md) attribute to **TRUE** on both the media source and the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d208-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d208-124">Requirements</span></span>



| <span data-ttu-id="4d208-125">需求</span><span class="sxs-lookup"><span data-stu-id="4d208-125">Requirement</span></span> | <span data-ttu-id="4d208-126">值</span><span class="sxs-lookup"><span data-stu-id="4d208-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4d208-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d208-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4d208-128">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d208-128">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4d208-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d208-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4d208-130">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d208-130">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4d208-131">標頭</span><span class="sxs-lookup"><span data-stu-id="4d208-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d208-132"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4d208-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d208-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d208-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d208-134">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="4d208-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4d208-135">硬體 MFTs</span><span class="sxs-lookup"><span data-stu-id="4d208-135">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> </dl>

 

 




