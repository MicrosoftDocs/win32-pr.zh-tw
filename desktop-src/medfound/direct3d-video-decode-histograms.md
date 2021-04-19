---
description: 本文包含使用 Direct3D 11 或 12 video Api 來解碼影片時產生長條圖的指引。
ms.assetid: ''
title: Direct3D video 解碼長條圖
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 6e25abd39ba95b669c2d76ced5f825ea80c4e3c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999841"
---
# <a name="direct3d-video-decode-histograms"></a>Direct3D video 解碼長條圖

本文包含使用 Direct3D 11 或 12 video Api 來解碼影片時產生長條圖的指引。

## <a name="checking-the-video-device-for-histogram-capabilities"></a>檢查影片裝置的長條圖功能

嘗試產生長條圖之前，您必須先檢查目前的影片裝置是否支援影片解碼長條圖功能。

### <a name="direct3d-12"></a>Direct3D 12

呼叫 [ID3D12VideoDevice：： CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) ，以檢查 Direct3D 12 影片解碼作業的支援詳細資料。 從 [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video)列舉傳遞 **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** 值，以指定您要求支援影片解碼長條圖。

### <a name="direct3d-11"></a>Direct3D 11

呼叫 [ID3D11VideoDevice2：： CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) ，並傳入 [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video)的 **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** 值，以判斷目前裝置是否支援長條圖。

## <a name="enabling-histogram-during-decode"></a>在解碼期間啟用長條圖

提供長條圖資料儲存所在之緩衝區的呼叫端會啟用長條圖資料的集合。  指定元件的 null 長條圖輸出緩衝區表示長條圖集合已停用。

### <a name="direct3d-12"></a>Direct3D 12

為了提供輸出緩衝區以使用 Direct3D 12 接收長條圖資料，您應該使用 [ID3D12VideoDecodeCommandList1：:D ecodeframe1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) 方法來建立解碼命令清單。 這個方法會採用 [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) 結構作為引數。 **D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** 具有 [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram)類型的欄位，可讓您指定要輸出長條圖資料的 [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) 。

### <a name="direct3d-11"></a>Direct3D 11

[ID3D11VideoCoNtext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3)介面提供[DecoderBeginFrame1](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1)方法，可讓您提供一或多個[ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer)介面，以將長條圖資料輸出至其中。 [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component)指定要產生長條圖資料的元件。


## <a name="buffer-format"></a>緩衝區格式

解碼長條圖輸出會寫入緩衝區，作為每個元件的整數計數器。  緩衝區格式為每個 bin 32 位的值。  裝置可使用小於32位的整數計數器位深度，但必須是16、24或32位。  如果是，計數器值會儲存在較低的位，而未使用的位則為零。  當 bin 的計數超過最大值時，裝置會改為設定最大值。 裝置會報告支援的 bin 數目，其值必須是2的乘冪。  支援這項功能的裝置所需的最少 bin 數目是64。 

您必須提供具有256位元組對齊位移的緩衝區，以及支援的 bin 數目乘以 (4 個位元組) 為每個所要求元件所要求的大小。  Bin 放置是由下列各項所決定：

`binIndex = floor(value / [max value of channel + 1] * (countBins))`


當格式定義的元件的有用位小於儲存區的數目時 (例如，P010 會使用16位元件儲存體) 的前10位，只會將 (P010 視為10位值) 。 

影片裝置會報告支援哪些元件。  如果呼叫端不需要指定元件的長條圖，則會指定 nullptr。  如果驅動程式不支援指定元件的長條圖，該元件的長條圖緩衝區必須是 nullptr。

當支援多個元件時，應用程式可能會要求每個畫面格解碼的元件組合。  例如，如果硬體報表支援 Y、U 和 V 元件，則應用程式可能只會要求框架1的 Y 長條圖、第二個畫面格2的 U 長條圖，以及僅針對框架3的 V 長條圖。  它們也可能會要求兩個元件的任意組合，或三個元件的組合。

應用程式會為每個要求的元件提供個別的位移和緩衝區指標/控制碼。  此指標可能會指向與另一個元件或個別資源相同的資源。  位移可將多個元件放在相同的緩衝區中，但是位移和長條圖大小所指定的輸出區域不得與另一個長條圖元件輸出重迭。  長條圖也可以寫入與其他不相關的內容相同的緩衝區，例如在資源子配置策略中使用時。


D3D 執行時間會驗證呼叫端只針對支援的元件啟用長條圖、調整緩衝區位移的對齊，而且緩衝區大小足以滿足所報告的 bin 數量。


## <a name="protected-content"></a>受保護內容

長條圖緩衝區必須與解碼輸出介面具有相同的介面保護。 如果解碼輸出介面不是受保護的資源，則長條圖緩衝區必須不是受保護的資源。 如果解碼輸出介面是受保護的資源，則長條圖必須是受保護的資源。








## <a name="related-topics"></a>相關主題

<dl> <dt>
[Direct3D 12 影片 api](direct3d-12-video-apis.md) 
[媒體基礎程式設計指南](media-foundation-programming-guide.md)
</dt> </dl>

 

 




