---
title: HLSL 磚的資源曝光
description: 需要新的 Microsoft 高階著色器語言 (HLSL) 語法，以支援著色器模型5中的磚資源。
ms.assetid: B6CE51E6-1BA9-4D15-9654-86FE9BAAF585
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b266b98045b38645e1e8d24ed0014a5f448a38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463388"
---
# <a name="hlsl-tiled-resources-exposure"></a>HLSL 磚的資源曝光

需要新的 Microsoft 高階著色器語言 (HLSL) 語法，以支援 [著色器模型 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)中的磚資源。

只有在具有並排資源支援的裝置上，才允許新的 HLSL 語法。 下表中並排顯示資源的每個相關 HLSL 方法，都會接受一個 (的意見反應) 或兩個 (的夾具和依此順序提供的意見反應) 其他選擇性參數。 例如，**Sample** 方法為：

**範例 (取樣器、位置 \[ 、位移 \[ 、夾具 \[ 、意見反應 \] \] \])**

**Sample** 方法的範例為 [**Texture2D.Sample(S,float,int,float,uint)**](/windows/desktop/direct3dhlsl/t2darray-sample-s-float-int-float-uint-)。

offset、clamp 和 feedback 參數為選用。 您必須指定所有選用參數，直到您需要的參數，這與 C++ 對於預設函數引數的規則相同。 例如，如果需要 feedback 狀態，offset 和 clamp 兩個參數就需要明確提供給 **Sample**，即使邏輯上可能不需要它們。

clamp 參數是純量浮點值。 clamp=0.0f 的常值表示 clamp 作業未執行。

feedback 參數是 **uint** 變數，您可以將它提供給記憶體存取查詢內建 [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) 函數。 您不得修改或解譯 feedback 參數值；不過編譯器不會提供任何進階分析和診斷，來偵測您是否修改此值。

以下是 [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) 的語法：

**bool CheckAccessFullyMapped(in uint FeedbackVar);**

[**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) 解譯 *FeedbackVar* 的值，並傳回 true，如果所有存取的資料都在資源中對應；否則 **CheckAccessFullyMapped** 傳回 false。

如果 clamp 或 feedback 參數存在，編譯器會發出基本指令的變化。 例如，磚資源的範例會產生 `sample_cl_s` 指令。 如果 clamp 和 feedback 都未指定，編譯器就會發出基本指令，目前行為也就沒有變更。 clamp 值為 0.0f，表示不會執行 clamp；因此，驅動程式編譯器可進一步依照目標硬體建立指令。 如果 feedback 為指令中的 NULL 暫存器，則 feedback 未使用；因此，驅動程式編譯器可以進一步依照目標架構建立指令。

如果 HLSL 編譯器推斷 clamp 為 0.0f 且 feedback 未使用，則編譯器會發出對應的基本指令 (例如 `sample` 而非 `sample_cl_s`)。

如果並排的資源存取是由數個組成的位元組程式碼指令所組成（例如，針對結構化資源），編譯器會透過或作業匯總個別的意見值，以產生最終的意見反應值。 因此，您會看到這類複雜存取的單一 feedback 值。

這是 HLSL 方法的摘要表，已變更為支援 feedback 和/或 clamp。 這些全都適用于所有維度的並排顯示和非並排的資源。 非並排顯示的資源一律會完全對應。



| [HLSL 物件](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5-objects)                                                                                                                                                                                                                                | 具有回饋選項的內建方法 (\*) -也有夾具選項                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[RW \] Texture2D<br/> \[RW \] Texture2DArray<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                                                                                                                    | Gather<br/> GatherRed<br/> GatherGreen<br/> GatherBlue<br/> GatherAlpha<br/> GatherCmp<br/> GatherCmpRed<br/> GatherCmpGreen<br/> GatherCmpBlue<br/> GatherCmpAlpha<br/> |
| \[RW \] Texture1D<br/> \[RW \] Texture1DArray<br/> \[RW \] Texture2D<br/> \[RW \] Texture2DArray<br/> \[RW \] Texture3D<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                              | 範例\*<br/> SampleBias\*<br/> SampleCmp\*<br/> SampleCmpLevelZero<br/> SampleGrad\*<br/> SampleLevel<br/>                                                                                      |
| \[RW \] Texture1D<br/> \[RW \] Texture1DArray<br/> \[RW \] Texture2D<br/> Texture2DMS<br/> \[RW \] Texture2DArray<br/> Texture2DArrayMS<br/> \[RW \] Texture3D<br/> \[RW \] 緩衝區<br/> \[RW \] ByteAddressBuffer<br/> \[RW \] StructuredBuffer<br/> | 載入                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚資源的管線存取](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

