---
title: Stream-Output 階段
description: 資料流程輸出階段的目的是要持續輸出 (或串流) 頂點資料從幾何著色器階段 (或頂點著色器階段（如果幾何著色器階段非使用中) 至記憶體中的一或多個緩衝區） (請參閱開始使用階段 Stream-Output。
ms.assetid: f902dc93-9612-481b-a6bd-073e924a4c79
keywords:
- " (Direct3D 10) 的資料流程輸出階段"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f630208b60b107b211f8bb6f6ee0f1efac3ed736c96756dbe1e95e24032b02f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538572"
---
# <a name="stream-output-stage"></a>Stream-Output 階段

資料流程輸出階段的目的是要持續輸出 (或串流) 頂點資料從幾何著色器階段 (或頂點著色器階段（如果幾何著色器階段非使用中) 至記憶體中的一或多個緩衝區） (請參閱開始使用 [階段](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md) Stream-Output。

資料流程輸出階段 (所以) 位於幾何著色器階段之後，緊接在點陣化階段之前的管線中，如下圖所示。

![在管線中資料流輸出階段的位置圖](images/d3d10-pipeline-stages-so.png)

串流輸出到記憶體的資料可在後續轉譯行程中讀回到管線，或者可以複製到預備環境資源（讓它可供 CPU 讀取）。 資料流程處理的資料量可能不同; [**>id3d11devicecoNtext：:D rawauto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) API 是設計用來處理資料，而不需要對寫入的資料量 (的 GPU) 進行查詢。

當三角形或行帶系結至輸入組合語言階段時，每個區域會先轉換成清單，再進行資料流程處理。頂點一律會寫出做為完整的基本專案 (例如，一次有3個頂點用於三角形) ;未完成的基本專案永遠不會串流處理。具有相鄰性的基本型別會捨棄相鄰資料，然後再將資料串流。

有兩種方式可將資料流輸出資料饋送至管線：

-   資料流程-輸出資料可以回送至輸入組合語言階段。
-   您可以使用載入函數 (（例如 [load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)) ），利用可程式化的著色器來讀取資料流程輸出資料。

若要使用緩衝區作為資料流程輸出資源，請使用 D3D11 系結 [**\_ \_ 資料流程 \_ 輸出**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) 旗標建立緩衝區。 資料流輸出階段同時支援最多 4 個緩衝區。

-   如果您要串流資料到多個緩衝區，每個緩衝區只可以擷取每個頂點資料的單一元素（最多 4 個元件），隱含的資料分散等於每個緩衝區中的元素寬度（相容於單一元素可繫結以供輸入到著色器階段的方式）。 此外，如果緩衝區有不同的大小，其中一個緩衝區已滿時寫入會立即停止。
-   如果您要串流資料到單一緩衝區，緩衝區可以擷取每個頂點資料最多 64 個純量元件 (256 位元組或更少)，或者頂點分散可能是 2048 位元組。


## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                               | 描述                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [使用 Stream-Output 階段開始使用](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)<br/> | 本節說明如何搭配資料流程輸出階段使用幾何著色器。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖形管線](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[ (Direct3D 10) 的管線階段 ](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

