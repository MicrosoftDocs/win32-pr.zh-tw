---
title: 建立根簽章
description: 根簽章是包含嵌套結構的複雜資料結構。
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3705f4e1a0a88841560d67d5904e0f1b5dabd3f8
ms.sourcegitcommit: a0cb986d5694b69d4a65b7d42a22694d02a6e83a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/30/2021
ms.locfileid: "108296333"
---
# <a name="creating-a-root-signature"></a>建立根簽章

根簽章是包含嵌套結構的複雜資料結構。 您可以使用下列資料結構定義，以程式設計的方式定義這些方法 (其中包含有助於初始化成員) 的方法。 或者，您也可以使用高階的陰影語言來撰寫 (HLSL) –提供編譯器將會及早驗證配置與著色器相容的優點。

用來建立根簽章的 API 會採用序列化的 (自我自主、指標 free) 版本的版面配置描述，如下所述。 提供的方法是用來從 c + + 資料結構產生這個序列化版本，但是取得序列化的根簽章定義的另一種方法，就是從已經使用根簽章編譯的著色器中取出。

如果您想要利用根簽章描述元和資料的驅動程式優化，請參閱根簽章 [版本 1.1](root-signature-version-1-1.md)

-   [描述項資料表系結類型](#descriptor-table-bind-types)
-   [描述項範圍](#descriptor-range)
-   [描述項資料表版面配置](#descriptor-table-layout)
-   [根常數](#root-constants)
-   [根描述元](#root-descriptor)
-   [著色器可見度](#shader-visibility)
-   [根簽章定義](#root-signature-definition)
-   [根簽章資料結構序列化/還原序列化](/windows)
-   [建立根簽章 API](#root-signature-creation-api)
-   [管線狀態物件中的根簽章](#root-signature-in-pipeline-state-objects)
-   [定義版本1.1 根簽章的程式碼](#code-for-defining-a-version-11-root-signature)
-   [相關主題](#related-topics)

## <a name="descriptor-table-bind-types"></a>描述項資料表系結類型

列舉 [**D3D12 \_ 描述項 \_ 範圍 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) 會定義描述項的類型，這些描述元可以參考為描述項資料表配置定義的一部分。

它是一個範圍，例如，如果部分描述中繼資料表有 100 SRVs，則可以在一個專案中宣告該範圍，而不是100。 因此描述項資料表定義是範圍的集合。

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a>描述項範圍

[**D3D12 \_ 描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)結構會定義指定類型的描述項範圍 (例如在描述中繼資料表內的 SRVs) 。

`D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND`宏通常可以用於 `OffsetInDescriptorsFromTableStart` [**D3D12 \_ 描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)的參數。 這表示會將描述項範圍附加在描述中繼資料表中的上一個描述項之後，再加以定義。 如果應用程式想要別名描述項，或基於某些原因想要略過位置，它可以設定 `OffsetInDescriptorsFromTableStart` 為所需的任何位移。 定義不同類型的重迭範圍無效。

由、、和組合所指定的著色器集合 `RangeType` ，在 `NumDescriptors` `BaseShaderRegister` `RegisterSpace` 具有通用 [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 的根簽章中的任何宣告之間，不能互相衝突或重迭 (請參閱下方的著色器可見度區段) 。

## <a name="descriptor-table-layout"></a>描述項資料表版面配置

[**D3D12 \_ 根描述 \_ 元 \_ 資料表**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)結構會將描述項資料表的配置宣告為描述項範圍的集合，而這些描述項範圍會在描述元堆積中的另一個後面出現。 在 CBV/UAV/SRVs 的相同描述項資料表中，不允許取樣器。

當根簽章位置類型設定為時，就會使用這個結構 `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` 。

若要設定圖形 (CBV、SRV、UAV、取樣器) 描述中繼資料表，請使用 [**ID3D12GraphicsCommandList：： SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable)。

若要設定計算描述中繼資料表，請使用 [**ID3D12GraphicsCommandList：： SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)。

## <a name="root-constants"></a>根常數

[**D3D12 \_ 根 \_ 常數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)結構會在以著色器形式出現的根簽章中宣告內嵌常數，作為一個常數緩衝區。

當根簽章位置類型設定為時，就會使用這個結構 `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` 。

## <a name="root-descriptor"></a>根描述元

[**D3D12 的 \_ 根 \_ 描述**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)元結構會宣告出現在根簽章中，) 內嵌于著色器中的描述元 (。

當根簽章位置類型設定為或時，會使用此結構 `D3D12_ROOT_PARAMETER_TYPE_CBV` `D3D12_ROOT_PARAMETER_TYPE_SRV` `D3D12_ROOT_PARAMETER_TYPE_UAV` 。

## <a name="shader-visibility"></a>著色器可見度

[**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)列舉集合中的成員會設定為 [**D3D12 \_ 根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)的著色器可見度參數，以決定哪一種著色器會查看指定之根簽章位置的內容。 計算一律 \_ 會使用所有 (，因為只有一個使用中階段) 。 圖形可以選擇，但如果它使用 \_ all，所有著色器階段都會看到任何系結于根簽章位置。

著色器可見度的其中一種用法是協助使用重迭的命名空間，針對每個著色器階段所撰寫的著色器提供不同的系結。 例如，頂點著色器可能會宣告：

```hlsl
Texture2D foo : register(t0);
```

此外，圖元著色器也可以宣告：

```hlsl
Texture2D bar : register(t0);
```

如果應用程式將根簽章系結至 t0 可見度 \_ ，則這兩種著色器會看到相同的材質。 如果著色器定義真的希望每個著色器都能看到不同的材質，則可以使用可見度 \_ 頂點和圖元來定義2個根簽章位置 \_ 。 無論根簽章位置上的可見度為何，它一律會具有相同的成本 (成本，而這取決於將 SlotType) 至一個固定的根簽章大小上限。

在低終端 D3D11 硬體上，在 \_ 根配置中驗證描述項資料表的大小時，也會將著色器可見度納入考慮，因為某些 D3D11 硬體只支援每一階段的系結數量上限。 只有在低層級硬體上執行時才會強制執行這些限制，而且完全不會限制更新式的硬體。

如果根簽章有定義在命名空間中彼此重迭的多個描述中繼資料表 (將) 的暫存器系結，而且其中任何一個都指定 \_ 為可見度，則配置無效 (建立將會失敗) 。

## <a name="root-signature-definition"></a>根簽章定義

[**D3D12 根簽章 \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)結構可以包含描述項資料表和內嵌常數，以及 [**D3D12 \_ 根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)結構和 enum [**D3D12 \_ 根 \_ 參數 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type)所定義的每個位置類型。

若要起始根簽章位置，請參閱 [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)的 **SetComputeRoot \* \* \*** 和 **SetGraphicsRoot \* \* \*** 方法。

靜態取樣器會使用 [**D3D12 \_ 靜態 \_ 取樣**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) 器結構，在根簽章中描述。

許多旗標會限制某些著色器存取根簽章的許可權，請參閱 [**D3D12 \_ 根簽章 \_ \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)。

## <a name="root-signature-data-structure-serialization--deserialization"></a>根簽章資料結構序列化/還原序列化

本節中所述的方法是由 D3D12Core.dll 匯出，並且提供序列化和還原序列化根簽章資料結構的方法。

序列化形式是在建立根簽章時傳遞至 API 的表單。 如果著色器在其中以根簽章撰寫 (當) 新增該功能時，已編譯的著色器會在其中包含已序列化的根簽章。

如果應用程式 cti 產生 D3D12 的根簽章 [**\_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) 資料結構，它必須使用 [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)來建立序列化的表單。 可以傳遞至 [**ID3D12Device：： CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)的輸出。

如果應用程式已經有序列化的根簽章，或具有已編譯的著色器，其中包含根簽章，而且想要以程式設計的方式探索配置定義 (稱為「反映」 ) ，則可以呼叫 [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) 。 這會產生 [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) 介面，其中包含傳回已還原序列化之 [**D3D12 根簽章 \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) 資料結構的方法。 介面擁有還原序列化之資料結構的存留期。

## <a name="root-signature-creation-api"></a>建立根簽章 API

[**ID3D12Device：： CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) API 會採用根簽章的序列化版本。

## <a name="root-signature-in-pipeline-state-objects"></a>管線狀態物件中的根簽章

建立管線狀態 ([**ID3D12Device：： CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) 和 [**ID3D12Device：： ) CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) 的方法會採用選擇性的 [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) 介面做為輸入參數 (儲存在 [**D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) 結構) 中。 這將會覆寫已在著色器中的任何根簽章。

如果將根簽章傳遞給其中一個「建立管線」狀態方法，此根簽章會針對 PSO 中的所有著色器進行驗證，以提供相容性，並提供給驅動程式以搭配所有著色器使用。 如果任何著色器中有不同的根簽章，它就會被傳入 API 的根簽章取代。 如果未傳入根簽章，則所有傳入的著色器都必須有根簽章，而且必須相符–這會提供給驅動程式。 設定命令清單或配套上的 PSO 並不會變更根簽章。 這是透過 [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) 和 [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)方法來完成。 隨著時間繪製 (graphics) /dispatch (計算) 叫用，應用程式必須確定目前的 PSO 符合目前的根簽章;否則，行為會是未定義的。

## <a name="code-for-defining-a-version-11-root-signature"></a>定義版本1.1 根簽章的程式碼

下列範例顯示如何建立具有下列格式的根簽章：



|                        |                                                |                                              |
|------------------------|------------------------------------------------|----------------------------------------------|
| **RootParameterIndex** | **Contents**                                   |                                              |
| \[0\]                  | 根常數： {b2}                         |  (1 CBV)                                       |
| \[1\]                  | 描述項資料表： {t2-t7，u0-u3}             |  (6 SRVs + 4 UAVs)                             |
| \[2\]                  | 根 CBV： {b0}                               |  (1 CBV、靜態資料)                          |
| \[3\]                  | 描述項資料表： {s0-s1}                    |  (2 取樣器)                                  |
| \[4\]                  | 描述項資料表： {t8-未系結}           |  (未系結 \# 的 SRVs、volatile 描述項)  |
| \[5\]                  | 描述項資料表： { (t0，space1) -未系結} |  (未系結 \# 的 SRVs、volatile 描述項)  |
| \[6\]                  | 描述項資料表： {b1}                       |  (1 CBV、靜態資料)                          |



 

如果根本簽章大部分的部分都是在大部分的時間內使用，則可能比太頻繁地切換根簽章更好。 應用程式應該將根簽章中的專案排序為最常變更為最少。 當應用程式將系結變更為根簽章的任何部分時，驅動程式可能必須複製部分或全部的根簽章狀態，而這可能會在乘以許多狀態變更時成為重要成本。

此外，根簽章會定義在著色器註冊 s3 執行非等向材質篩選的靜態取樣器。

系結這個根簽章之後，可以將描述中繼資料表、根 CBV 和常數指派給 \[ 0.. 6 \] 參數空間。 例如，描述元堆積中 (範圍的描述項資料表) 可以在每個根參數 \[ 1 \] 和 \[ 3. 6 上 \] 系結。

``` syntax
CD3DX12_DESCRIPTOR_RANGE1 DescRange[6];

DescRange[0].Init(D3D12_DESCRIPTOR_RANGE_SRV,6,2); // t2-t7
DescRange[1].Init(D3D12_DESCRIPTOR_RANGE_UAV,4,0); // u0-u3
DescRange[2].Init(D3D12_DESCRIPTOR_RANGE_SAMPLER,2,0); // s0-s1
DescRange[3].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,8, 0,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); // t8-unbounded
DescRange[4].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,0,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); 
                                                            // (t0,space1)-unbounded
DescRange[5].Init(D3D12_DESCRIPTOR_RANGE_CBV,1,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC); // b1

CD3DX12_ROOT_PARAMETER1 RP[7];

RP[0].InitAsConstants(3,2); // 3 constants at b2
RP[1].InitAsDescriptorTable(2,&DescRange[0]); // 2 ranges t2-t7 and u0-u3
RP[2].InitAsConstantBufferView(0, 0, 
                               D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC); // b0
RP[3].InitAsDescriptorTable(1,&DescRange[2]); // s0-s1
RP[4].InitAsDescriptorTable(1,&DescRange[3]); // t8-unbounded
RP[5].InitAsDescriptorTable(1,&DescRange[4]); // (t0,space1)-unbounded
RP[6].InitAsDescriptorTable(1,&DescRange[5]); // b1

CD3DX12_STATIC_SAMPLER StaticSamplers[1];
StaticSamplers[0].Init(3, D3D12_FILTER_ANISOTROPIC); // s3
CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC RootSig(7,RP,1,StaticSamplers);
ID3DBlob* pSerializedRootSig;
CheckHR(D3D12SerializeVersionedRootSignature(&RootSig,pSerializedRootSig)); 

ID3D12RootSignature* pRootSignature;
hr = CheckHR(pDevice->CreateRootSignature(
    pSerializedRootSig->GetBufferPointer(),pSerializedRootSig->GetBufferSize(),
    __uuidof(ID3D12RootSignature),
    &pRootSignature));
```

下列程式碼說明如何在圖形命令清單上使用上述的根簽章。

``` syntax
InitializeMyDescriptorHeapContentsAheadOfTime(); // for simplicity of the 
                                                 // example
CreatePipelineStatesAhreadOfTime(pRootSignature); // The root signature is passed into 
                                     // shader / pipeline state creation
...

ID3D12DescriptorHeap* pHeaps[2] = {pCommonHeap, pSamplerHeap};
pGraphicsCommandList->SetDescriptorHeaps(pHeaps,2);
pGraphicsCommandList->SetGraphicsRootSignature(pRootSignature);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        6,heapOffsetForMoreData,DescRange[5].NumDescriptors);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(5,heapOffsetForMisc,5000); 
pGraphicsCommandList->SetGraphicsRootDescriptorTable(4,heapOffsetForTerrain,20000);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        3,heapOffsetForSamplers,DescRange[2].NumDescriptors);
pGraphicsCommandList->SetComputeRootConstantBufferView(2,pDynamicCBHeap,&CBVDesc);

MY_PER_DRAW_STUFF stuff;
InitMyPerDrawStuff(&stuff);
pGraphicsCommandList->SetSetGraphicsRoot32BitConstants(
                        0,&stuff,0,RTSlot[0].Constants.Num32BitValues);

SetMyRTVAndOtherMiscBindings();

for(UINT i = 0; i < numObjects; i++)
{
    pGraphicsCommandList->SetPipelineState(PSO[i]);
    pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                    1,heapOffsetForFooAndBar[i],DescRange[1].NumDescriptors);
    pGraphicsCommandList->SetGraphicsRoot32BitConstant(0,&i,1,drawIDOffset);
    SetMyIndexBuffers(i);
    pGraphicsCommandList->DrawIndexedInstanced(...);
}
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[根簽章](root-signatures.md)
</dt> <dt>

[在 HLSL 中指定根簽章](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[使用根簽章](using-a-root-signature.md)
</dt> </dl>

 

 
