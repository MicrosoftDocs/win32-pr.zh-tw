---
title: 串流輸出計數器
description: 資料流程輸出是 GPU 將頂點寫入緩衝區的能力。 資料流程輸出計數器會監視進度。
ms.assetid: 7342DA09-25E9-4154-83BA-B03ADBB8B671
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00cc3d78314b5c9130f69c65ebc5fa056d51d7305135025ecf2e4329ecbe6350
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989468"
---
# <a name="stream-output-counters"></a>串流輸出計數器

資料流程輸出是 GPU 將頂點寫入緩衝區的能力。 資料流程輸出計數器會監視進度。

-   [從 Direct3D 11 到 Direct3D 12 的資料流程計數器差異](#differences-in-stream-counters-from-direct3d-11-to-direct3d-12)
-   [BufferFilledSize](#bufferfilledsize)
-   [相關主題](#related-topics)

## <a name="differences-in-stream-counters-from-direct3d-11-to-direct3d-12"></a>從 Direct3D 11 到 Direct3D 12 的資料流程計數器差異

在資料流程輸出流程中，GPU 必須知道其寫入緩衝區中的目前位置。 在 Direct3D 11 中，用來儲存這個位置的記憶體是由驅動程式配置，而應用程式用來操作此值的唯一方法是透過 **SOSetTargets** 方法。 在 Direct3D 12 中，應用程式會配置記憶體來儲存這個目前的位置。 沒有特殊的方法可以操作此值，而且應用程式可以自由地使用 CPU 或 GPU 來讀取/寫入值。

## <a name="bufferfilledsize"></a>BufferFilledSize

應用程式負責配置32位數量的儲存體（稱為 *BufferFilledSize*）。 這包含資料流程輸出緩衝區中的資料位元組數。 此儲存體可放置在與包含資料流程輸出資料的資源相同或不同的資源中。 此值是由資料流程輸出階段中的 GPU 所存取，以決定要在緩衝區中附加新頂點資料的位置。 此外，GPU 會存取此值以判斷何時發生溢位。

請參閱結構 [**D3D12 \_ 資料流程 \_ 輸出 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)。

Debug 層會驗證 [**ID3D12GraphicsCommandList：： SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)中的下列事項：

-   如果指定了非 Null 的資源， *BufferFilledSize* 就會落在 {*OffsetInBytes*， *SizeInBytes*} 所隱含的範圍內。
-   *BufferFilledSizeOffsetInBytes* 是4的倍數。
-   *BufferFilledSizeOffsetInBytes* 在包含資源的範圍內。
-   指定的資源是緩衝區。

執行時間不會驗證與資料流程輸出緩衝區相關聯的堆積型別，因為所有堆積類型都支援資料流程輸出。

根簽章必須使用 [**D3D12 根簽章 \_ \_ \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 標旗標來指定是否要使用資料流程輸出。

D3D12 \_ 根簽章 \_ \_ 旗 \_ \_ 標允許串流 \_ 輸出可針對以 HLSL 撰寫的根簽章指定，其方式類似于指定其他旗標的方式。

[](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)如果幾何著色器包含資料流程輸出，但根簽章沒有 D3D12 的根簽章旗標 \_ \_ \_ \_ 允許 \_ 串流 \_ 輸出旗標，則 CreateGraphicsPipelineState 將會失敗。

當資源當做資料流程輸出目標使用時，使用的資源必須處於 D3D12 \_ 資源 \_ 狀態 \_ 資料流程輸出 \_ 狀態。 這同時適用于頂點資料和 *BufferFilledSize* (，其可位於相同或不同的資源) 。

沒有特殊的 Api 可設定資料流程輸出緩衝區位移，因為應用程式可以直接使用 CPU 或 GPU 寫入 *BufferFilledSize* 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[計數器和查詢](counters-and-queries.md)
</dt> </dl>

 

 




