---
title: 輸入組合階段
description: Direct3D 10 和更新版本的 API 會將管線的功能區域與階段分開。管線中的第一個階段是輸入組合語言 (IA) 階段。
ms.assetid: 71141a5e-2d79-4b02-8370-c0cbc8618908
keywords:
- " (Direct3D 10) 的輸入組合語言階段"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e16a419dfe57dac5b16562b234a7a60d417c071fcd6214f3defa84bcbe8b4ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408378"
---
# <a name="input-assembler-stage"></a>輸入組合階段

Direct3D 10 和更新版本的 API 會將管線的功能區域與階段分開。管線中的第一個階段是輸入組合語言 (IA) 階段。

輸入組合語言階段的目的是要從使用者填入的緩衝區中讀取基本資料 (點、線條及/或三角形) ，然後將資料組合成其他管線階段將使用的基本專案。 IA 階段可以將頂組合到數個不同的[基本類型](d3d10-graphics-programming-guide-primitive-topologies.md) (例如行清單、三角形連環或相鄰基本類型)。 新的基本類型 (例如具有連續的行清單，或已新增相鄰) 的三角形清單，以支援幾何著色器。

應用程式只能在在幾何著色器中看到相鄰資訊。 如果幾何著色器已叫用包括相鄰關係的三角形，輸入資料將在每個三角形包含 3 個頂點，而每個三角形有 3 個相鄰資料頂點。

當要求輸入組合語言階段輸出相鄰資料時，輸入資料必須包含連續的資料。 這可能需要提供假頂點 (形成變質三角形)，或可能在其中一個頂點屬性標明頂點是否存在。 這也需由幾何著色器偵測和處理，雖然在點陣化階段將會揀選變質幾何。

在組合基本專案時，IA 的次要用途是附加 [系統產生的值](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) ，以協助著色器更有效率。 系統產生的值為也稱為語意的文字字串。 所有三個著色器階段都是從常見的著色器核心來建立，而著色器核心會使用系統產生的值 (例如基本識別碼、實例識別碼或頂點識別碼) ，因此著色器階段可以減少只處理尚未處理的基本、實例或頂點。

如 [管線區塊圖](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)所示，在 IA 階段從記憶體讀取資料之後 (將資料組合成基本專案，並將系統產生的值附加) ，資料就會輸出到 [頂點著色器階段](/previous-versions//bb205146(v=vs.85))。


## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                                   | 描述                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [使用 Input-Assembler 階段開始使用](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)<br/> | 有幾個步驟需要初始化輸入組合語言 (IA) 階段。 例如，您需要使用管線所需的頂點資料來建立緩衝區資源、告知 IA 階段，其中緩衝區是和它們所包含的資料類型，並指定要從資料組合的基本類型。<br/> |
| [基本拓撲](d3d10-graphics-programming-guide-primitive-topologies.md)<br/>                                            | Direct3D 10 和更新版本支援數個基本類型 (或以 [**D3D \_ 基本 \_ 拓撲**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) 列舉類型表示的拓撲) 。 這些類型會定義管線如何轉譯和呈現頂點。<br/>                                                          |
| [使用不含緩衝區的 Input-Assembler 階段](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md)<br/>     | 如果您的著色器不需要緩衝區，則不需要建立和系結緩衝區。 本節包含繪製單一三角形的簡單頂點和圖元著色器範例。<br/>                                                                                                                                  |
| [使用 System-Generated 值](d3d10-graphics-programming-guide-input-assembler-stage-using.md)<br/>                            | 根據使用者提供的輸入 [語義](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) ，IA 階段會產生系統產生的值 (，) 以允許著色器作業中有某些效率。 <br/>                                                                                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖形管線](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[ (Direct3D 10) 的管線階段 ](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

