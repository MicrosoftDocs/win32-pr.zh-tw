---
description: 資源是 3D 管線使用的一組資料。
ms.assetid: 802400fa-a606-4d3d-a61d-1cdb5a9f0437
title: 選擇 (Direct3D 10) 的資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be887fb94f04783b01f8873fb61812bca20faa5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689160"
---
# <a name="choosing-a-resource-direct3d-10"></a>選擇 (Direct3D 10) 的資源

資源是 3D 管線使用的一組資料。 建立資源及定義其行為，是應用程式的程式設計首項步驟。 本指引涵蓋基本主題，內容為選擇應用程式所需的資源。

-   [識別需要資源的管線階段](#identify-pipeline-stages-that-need-resources)
-   [識別每個資源的使用方式](#identify-how-each-resource-will-be-used)
-   [將資源系結至管線階段](#binding-resources-to-pipeline-stages)
-   [相關主題](#related-topics)

## <a name="identify-pipeline-stages-that-need-resources"></a>識別需要資源的管線階段

第一個步驟是選擇將使用資源 (或階段) 的 [管線階段](d3d10-graphics-programming-guide-pipeline-stages.md) 。 意即，找出會從資源讀取資料以及將資料寫入資源的階段。 了解資源使用所在的管線階段，可決定要呼叫用來將資源繫結至階段的 API。

此表列出可繫結至各管線階段的資源類型， 它包含資源是否可系結為輸入或輸出，以及系結 API。



| 管線階段  | 輸入/輸出 | 資源               | 資源類型                           | 系結 API                                                                                                                                                                                                |
|-----------------|--------|------------------------|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 輸入組合器 | 位於     | 頂點緩衝區          | Buffer                                  | [**IASetVertexBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers)                                                                                                                                           |
| 輸入組合器 | 位於     | 索引緩衝區           | Buffer                                  | [**IASetIndexBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer)                                                                                                                                               |
| 著色器階段   | 位於     | Shader-ResourceView    | 緩衝區, Texture1D, Texture2D, Texture3D | [**VSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshaderresources)、 [**GSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshaderresources)、 [**PSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshaderresources) |
| 著色器階段   | 位於     | Shader-Constant Buffer | Buffer                                  | [**VSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers)、 [**GSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers)、 [**PSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers) |
| 資料流輸出   | 外    | Buffer                 | Buffer                                  | [**SOSetTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-sosettargets)                                                                                                                                                       |
| 輸出合併   | 外    | 轉譯目標檢視     | 緩衝區, Texture1D, Texture2D, Texture3D | [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)                                                                                                                                           |
| 輸出合併   | 外    | 深度/樣板檢視     | Texture1D, Texture2D                    | [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)                                                                                                                                           |



 

## <a name="identify-how-each-resource-will-be-used"></a>識別每個資源的使用方式

選擇應用程式要使用的管線階段 (以及各階段需要的資源) 後，下一個步驟為決定各個資源的使用方式，意即 CPU 或 GPU 是否可存取資源。

應用程式執行所在的硬體上至少會有一個 CPU 和一個 GPU。 若要挑選使用值，請考慮哪種類型的處理器需要從下列選項讀取或寫入資源 (請參閱 [**D3D10 \_ 使用量**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) 。



| 資源使用狀況 | 可透過下項更新                    | 更新的頻率 |
|----------------|--------------------------------------|---------------------|
| 預設        | GPU                                  | 不常        |
| 動態        | CPU                                  | 頻繁          |
| 預備        | GPU                                  | n/a                 |
| 固定      | CPU (只能在資源建立的時間) | n/a                 |



 

預設使用方式應用於預期不常由 CPU 更新的資源 (少於每畫面一次)。 理想的狀況是，CPU 永遠不會使用預設使用方式直接寫入資源，以避免潛在的效能降低。

動態使用方式應用於相對而言較常由 CPU 更新的資源 (等於或多於每畫面一次)。 動態資源的常見案例為建立動態頂點和索引緩衝區，其會在執行階段由每個畫面使用者視角可見的幾何資料填滿。 這些緩衝區僅會用來轉譯該畫面使用者可見的幾何。

暫存使用方式應用於自其他資源複製資料，以及將資料複製到其中。 常見案例是將使用預設使用方式 (CPU 不能加以存取) 之資源的資料複製到使用暫存使用方式 (CPU 可以加以存取) 的資源。

資源中的資料永遠不會變更時，應使用固定資源。

另一種看待相同想法的方式是，試想應用程式與資源的搭配方式。



| 應用程式使用資源的方式     | 資源使用狀況       |
|---------------------------------------|----------------------|
| 載入一次且永不更新            | 固定或預設 |
| 應用程式重複填滿資源 | 動態              |
| 轉譯至紋理                     | 預設              |
| CPU 的 GPU 資料存取權                | 預備              |



 

如果您不確定要選擇哪個使用方式，請先使用預設使用方式，因其是最常見的情形。 著色器常數緩衝區這項資源類型應一律使用預設使用方式。

## <a name="binding-resources-to-pipeline-stages"></a>將資源系結至管線階段

資源可以同時系結至一個以上的管線階段，只要在建立資源時所指定的限制 ([**使用旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)標、系結 [**旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)標、 [**cpu 存取旗標**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)) 符合。 更明確地說，資源可同時繫結為輸入與輸出，只要不同時發生資源的讀取和寫入部分即可。

繫結資源時，請思考 GPU 和 CPU 存取資源的方式。 為單一目的所設計的資源 (不使用多個使用方式、繫結及 CPU 存取旗標) 效能很有可能更好。

例如，請考量轉譯目標多次作為紋理的案例。 若有兩個資源可能會更快速︰轉譯目標和紋理作為著色器資源。 每個資源只會使用一個系結旗標 ([**D3D10 \_ bind 轉譯 \_ \_ 目標**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) 或 D3D10 系結 **\_ \_ 著色器 \_ 資源**) 。 您可以使用 [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) 或 [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)，將資料從呈現目標材質複製到著色器材質。 這可以藉由隔離轉譯器材質讀取的轉譯目標寫入，來改善效能。 當然，要確定的唯一方法是同時執行這兩種方法，並測量特定應用程式中的效能差異。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的資源 ](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



