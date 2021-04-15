---
description: 指出媒體接收器是否支援硬體資料流程。
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: 'MF_STREAM_SINK_SUPPORTS_HW_CONNECTION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95bfecba4cf53b6ef7c8863ec0456e310d8bcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469189"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a><span data-ttu-id="75ac1-103">MF \_ 資料流程 \_ 接收 \_ 支援 \_ HW \_ 連接屬性</span><span class="sxs-lookup"><span data-stu-id="75ac1-103">MF\_STREAM\_SINK\_SUPPORTS\_HW\_CONNECTION attribute</span></span>

<span data-ttu-id="75ac1-104">指出媒體接收器是否支援硬體資料流程。</span><span class="sxs-lookup"><span data-stu-id="75ac1-104">Indicates whether a media sink supports hardware data flow.</span></span>

## <a name="data-type"></a><span data-ttu-id="75ac1-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="75ac1-105">Data type</span></span>

<span data-ttu-id="75ac1-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="75ac1-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="75ac1-107">備註</span><span class="sxs-lookup"><span data-stu-id="75ac1-107">Remarks</span></span>

<span data-ttu-id="75ac1-108">當媒體接收器 proxy 硬體裝置，而且能夠透過硬體匯流排接收資料時，就會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="75ac1-108">This attribute is used when a media sink proxies a hardware device and is able to receive data over a hardware bus.</span></span> <span data-ttu-id="75ac1-109">例如，硬體音訊解碼器可能會直接將音訊資料傳送到音訊轉譯硬體。</span><span class="sxs-lookup"><span data-stu-id="75ac1-109">For example, a hardware audio decoder might send audio data directly to the audio rendering hardware.</span></span>

<span data-ttu-id="75ac1-110">在此案例中， [媒體基礎轉換](media-foundation-transforms.md) (MFT) 和媒體接收器仍會在 Microsoft 媒體基礎中表示解碼器和接收器。</span><span class="sxs-lookup"><span data-stu-id="75ac1-110">In this scenario, the decoder and the sink are still represented in the Microsoft Media Foundation by a [Media Foundation transform](media-foundation-transforms.md) (MFT) and a media sink.</span></span> <span data-ttu-id="75ac1-111">不過，在管線層的這兩個物件之間不會有資料流程，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="75ac1-111">However, no data flows between these two objects at the pipeline layer, only at the hardware layer, as shown in the following diagram.</span></span>

![顯示硬體 proxy 來源的圖表。](images/proxy-mft4.png)

<span data-ttu-id="75ac1-113">MFT 和媒體接收器之間的連接會以下面方式進行協商。</span><span class="sxs-lookup"><span data-stu-id="75ac1-113">The connection between the MFT and the media sink is negotiated as follows.</span></span>

1.  <span data-ttu-id="75ac1-114">此管線會檢查 mft 上的 [mft \_ 列舉 \_ 硬體 \_ URL \_ 屬性](mft-enum-hardware-url-attribute.md) 屬性，以檢查 mft 是否為硬體 proxy。</span><span class="sxs-lookup"><span data-stu-id="75ac1-114">The pipeline checks if the MFT is a hardware proxy, by checking for the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="75ac1-115">如需詳細資訊，請參閱 [硬體 MFTs](hardware-mfts.md)。</span><span class="sxs-lookup"><span data-stu-id="75ac1-115">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>
2.  <span data-ttu-id="75ac1-116">管線會取得媒體接收器上資料流程接收之 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="75ac1-116">The pipeline gets a pointer to the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface of the stream sink on the media sink.</span></span>
3.  <span data-ttu-id="75ac1-117">此管線會使用 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 指標來查詢 MF \_ 資料流程接收， \_ 以 \_ 支援 \_ HW \_ 連接屬性。</span><span class="sxs-lookup"><span data-stu-id="75ac1-117">The pipeline uses the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer to query for the MF\_STREAM\_SINK\_SUPPORTS\_HW\_CONNECTION attribute.</span></span> <span data-ttu-id="75ac1-118">如果此屬性存在且等於 **TRUE**，則媒體來源支援硬體連接。</span><span class="sxs-lookup"><span data-stu-id="75ac1-118">If this attribute is present and equal to **TRUE**, the media source supports hardware connections.</span></span>
4.  <span data-ttu-id="75ac1-119">管線會在資料流程接收上設定 [MFT \_ 連接的 \_ 資料流程 \_ 屬性](mft-connected-stream-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="75ac1-119">The pipeline sets the [MFT\_CONNECTED\_STREAM\_ATTRIBUTE](mft-connected-stream-attribute.md) attribute on the stream sink.</span></span> <span data-ttu-id="75ac1-120">這個屬性的值是從 MFT [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 的指標。</span><span class="sxs-lookup"><span data-stu-id="75ac1-120">The value of this attribute is the [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer from the MFT.</span></span>
5.  <span data-ttu-id="75ac1-121">此管線會在串流接收和 MFT 上將 [ \_ 連接 \_ 至 \_ HW \_ 串流](mft-connected-to-hw-stream.md) 屬性的 MFT 設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="75ac1-121">The pipeline sets the [MFT\_CONNECTED\_TO\_HW\_STREAM](mft-connected-to-hw-stream.md) attribute to **TRUE** on both the stream sink and the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="75ac1-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="75ac1-122">Requirements</span></span>



| <span data-ttu-id="75ac1-123">需求</span><span class="sxs-lookup"><span data-stu-id="75ac1-123">Requirement</span></span> | <span data-ttu-id="75ac1-124">值</span><span class="sxs-lookup"><span data-stu-id="75ac1-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="75ac1-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75ac1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="75ac1-126">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75ac1-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="75ac1-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75ac1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="75ac1-128">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75ac1-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="75ac1-129">標頭</span><span class="sxs-lookup"><span data-stu-id="75ac1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="75ac1-130"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="75ac1-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75ac1-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75ac1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ac1-132">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="75ac1-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




