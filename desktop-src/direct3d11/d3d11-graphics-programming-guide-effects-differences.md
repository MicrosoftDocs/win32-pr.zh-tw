---
title: 效果的差異10和效果11
description: 本主題顯示效果10和效果11之間的差異。
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29af1b9e7aec72f96a62e0f62668b81a6eec8367
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682590"
---
# <a name="differences-between-effects-10-and-effects-11"></a>效果的差異10和效果11

本主題顯示效果10和效果11之間的差異。

## <a name="device-contexts-threading-and-cloning"></a>裝置內容、執行緒和複製

ID3D10Device 介面已在 Direct3D 11： ID3D11Device 和 >id3d11devicecoNtext 中分割成兩個介面。 您可以建立多個 ID3D11DeviceCoNtexts，以協助在多個執行緒上同時執行。 效果11將此概念延伸至效果架構。

效果11的執行時間為單一執行緒。 基於這個理由，您不應該同時使用具有多個執行緒的單一 ID3DX11Effect 實例。

若要在多個實例上使用效果11執行時間，您必須建立個別的 ID3DX11Effect 實例。 由於 >id3d11devicecoNtext 也是單一執行緒，因此您應該在套用時將不同的 >id3d11devicecoNtext 實例傳遞至每個效果實例。 您可以使用這些不同的裝置內容來建立命令清單，讓轉譯執行緒可以將它們套用至立即裝置內容。

若要建立多個封裝相同功能的效果，以在多個執行緒上使用，最簡單的方式就是建立一個效果，然後製作複製的複本。 相較于從頭開始建立多個複本，複製的優點如下：

1.  複製常式比建立常式更快。
2.  複製的效果會共用已建立的著色器、狀態欄塊和類別實例 (因此不需要重新建立) 。
3.  複製的效果可以共用常數緩衝區。
4.  複製的效果會從符合目前效果的狀態開始 (變數值，不論它是否已優化) 。

如需詳細資訊，請參閱 [複製效果](d3d11-graphics-programming-guide-effects-cloning.md) 。

## <a name="effect-pools-and-groups"></a>效果集區和群組

到目前為止，Direct3D 10 中效果集區最普遍的使用是用於群組材質。 效果集區已從效果11移除，而新增了群組，這是更有效率的分組材質方法。

效果群組只是一組技術。 如需詳細資訊，請參閱 [效果群組語法 (Direct3D 11) ](d3d11-effect-group-syntax.md) 。

請考慮下列具有四個子效果和一個效果集區的效果階層：


```
// Effect Pool
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

// Effect Child 1
#include "EffectPool.fx"
technique10 GrassMaterialLowSpec { ... }

// Effect Child 2
#include "EffectPool.fx"
technique10 GrassMaterialHighSpec { ... }

// Effect Child 3
#include "EffectPool.fx"
technique10 WaterMaterialLowSpec { ... }

// Effect Child 4
#include "EffectPool.fx"
technique10 WaterMaterialHighSpec { ... }
```



您可以使用群組在效果11中達成相同的功能：


```
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

fxgroup GrassMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}

fxgroup WaterMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}
```



## <a name="new-shader-stages"></a>新的著色器階段

Direct3D 11 中有三個新的著色器階段：輪廓著色器、網域著色器和計算著色器。 效果11以類似頂點著色器、幾何著色器和圖元著色器的方式來處理這些結果。

有三個新的變數類型已新增到效果11：

-   HullShader
-   DomainShader
-   ComputeShader

如果您在技術中使用這些著色器，則必須將該技術標示為「technique11」，而不是「technique10」。 計算著色器不能與任何其他圖形狀態設定相同的傳遞 (其他著色器、狀態欄塊或轉譯目標) 。

## <a name="new-texture-types"></a>新的材質類型

Direct3D 11 支援下列材質類型：

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a>未排序的存取權視圖

效果11支援取得和設定新的未排序存取檢視類型。 其運作方式與紋理類似。

請考慮此效果 HLSL 範例：


```
  
RWTexture1D<float> myUAV;
```



您可以在 c + + 中設定此變數，如下所示：


```
  
ID3D11UnorderedAccessView* pUAVTexture1D = NULL;
ID3DX11EffectUnorderedAccessViewVariable* pUAVVar;
pUAVVar = pEffect->GetVariableByName("myUAV")->AsUnorderedAccessView();
pUAVVar->SetUnorderedAccessView( pUAVTexture1D );
```



Direct3D 11 支援下列未排序的存取檢視類型：

-   RWBuffer
-   RWByteAddressBuffer
-   RWStructuredBuffer
-   RWTexture1D
-   RWTexture1DArray
-   RWTexture2D
-   RWTexture2DArray
-   RWTexture3D

## <a name="interfaces-and-class-instances"></a>介面和類別實例

如需介面和類別語法，請參閱 [介面和類別](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class)。

如需使用介面和類別的效果，請參閱 [效果中的介面和類別](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md)。

## <a name="addressable-stream-out"></a>可定址的資料流程輸出

在 Direct3D 10 中，幾何著色器可以將一個資料流程輸出到資料流程輸出單位和轉譯器單位。 在 Direct3D11 中，幾何著色器最多可以將四個數據流輸出到資料流程輸出單位，而且大部分的串流都是轉譯器單位。 已更新 **ConstructGSWithSO** 內建，以反映這種新功能。

如需詳細資訊，請參閱 [資料流程輸出語法](d3d11-graphics-reference-effect-streamout.md) 。

## <a name="setting-and-unsetting-device-state"></a>設定和取消裝置狀態

在效果10中，您可以使用 [**ID3D10EffectConstantBuffer：： SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) 和 [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) 函式，讓使用者管理常數緩衝區和材質緩衝區。 在您呼叫這些函式之後，10個執行時間的效果就不再管理常數緩衝區或紋理緩衝區，而使用者必須使用 ID3D10Device 介面填滿資料。

在效果11中，您也可以使用下列呼叫，讓狀態欄塊 (blend 狀態、轉譯器狀態、深度樣板狀態和取樣器狀態) 使用者管理：

-   [**ID3DX11EffectBlendVariable::SetBlendState**](id3dx11effectblendvariable-setblendstate.md)
-   [**ID3DX11EffectRasterizerVariable::SetRasterizerState**](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable::SetSampler**](id3dx11effectsamplervariable-setsampler.md)

在您呼叫這些函式之後，效果11的執行時間就不會再管理狀態欄塊變數，且值會維持不變。 請注意，因為狀態欄塊是不可變的，所以使用者必須設定新的狀態欄塊來變更值。

您也可以將常數緩衝區、材質緩衝區和狀態欄塊還原為非使用者管理的狀態。 如果您取消設定這些變數，則在必要時，11執行時間會繼續更新這些變數。 您可以使用下列呼叫來取消設定使用者管理的變數：

-   [**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [**ID3DX11EffectBlendVariable::UndoSetBlendState**](id3dx11effectblendvariable-undosetblendstate.md)
-   [**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable::UndoSetSampler**](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a>效果虛擬機器

已移除在函式之外評估複雜運算式的效果虛擬機器。

下列複雜運算式範例不受支援：

1.  SetPixelShader ( myPSArray ( i \* 3 + j ) ) ;
2.  SetPixelShader ( myPSArray ( (float) i ) ;
3.  篩選 = i + 2;

以下是支援的非複雜運算式範例：

1.  SetPixelShader ( myPS ) ;
2.  SetPixelShader ( myPS \[ \] ) ;
3.  SetPixelShader ( myPS \[ uIndex \] ) ;//uIndex 是 uint 變數
4.  篩選 = i;
5.  FILTER = 各向異性;

這些運算式可能會出現在狀態欄塊運算式 (例如篩選) 和傳遞運算式 (例如 SetPixelShader) 。

## <a name="source-availability-and-location"></a>來源可用性和位置

在 D3D10.dll 中散佈了10個效果。 效果11會以來源的形式散發，並以對應的 Visual Studio 解決方案來進行編譯。 當您建立效果類型的應用程式時，建議您直接在這些應用程式中包含效果11來源。

您可以從 [Direct3D 11 Update 的效果](https://github.com/Microsoft/FX11)得到11個效果。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 11) 的效果 ](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 