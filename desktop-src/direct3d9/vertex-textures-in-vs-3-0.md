---
description: 頂點著色器3.0 模型支援使用 texldl-vs 材質 load 語句，在頂點著色器中進行紋理查閱。
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Vs_3_0 (DirectX HLSL) 中的頂點紋理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4cbd4aa1e1830d29656fea2bc7b028191bee158eede119c9a47ae2457d10e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519445"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a>Vs \_ 3 \_ 0 (DirectX HLSL) 的頂點紋理

頂點著色器3.0 模型支援使用 [texldl-vs](../direct3dhlsl/texldl---vs.md) 材質 load 語句，在頂點著色器中進行紋理查閱。 頂點引擎包含四個紋理取樣器階段，名稱為 [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md)、D3DVERTEXTEXTURESAMPLER1、D3DVERTEXTEXTURESAMPLER2 和 D3DVERTEXTEXTURESAMPLER3。 這些與圖元引擎中的置換地圖取樣器和紋理取樣器不同。

若要在這四個階段設定範例紋理，您可以使用頂點引擎並使用 [**CheckDeviceFormat**](/windows/desktop/api) 方法來程式設計階段。 使用 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)在階段索引 [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) 到 D3DVERTEXTEXTURESAMPLER3 的階段設定紋理。 端點著色器中引進了新的暫存器，取樣器註冊 (如 ps \_ 2 0) 中所示 \_ ，這代表頂點紋理取樣器。 在使用之前，必須先在著色器中定義這個暫存器。

應用程式可以藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api) with [D3DUSAGE \_ query \_ VERTEXTEXTURE](d3dusage-query.md)，查詢是否支援將格式作為頂點紋理。

> [!Note]  
> 這是查詢旗標，因此不接受任何 Createxxx 函數。 在預設集區中建立的頂點紋理可以設定為圖元材質，反之亦然。 不過，若要使用軟體頂點處理，您必須在暫存集區中建立頂點材質 (無論是混合模式裝置或軟體頂點處理裝置) 。

 

這項功能與圖元材質相同，不同之處如下：

-   不支援非等向材質篩選，因此 \_ 會忽略 D3DSAMP MAXANISOTROPY，而且無法針對 [ \_ 放大] 或 [縮短] 設定這些階段的 D3DTEXF。
-   無法使用變更資訊的速率，因此應用程式必須計算詳細資料層級，並將該資訊以參數的形式提供給 [texldl-vs](../direct3dhlsl/texldl---vs.md)。

限制包含：

-   如同圖元著色器，如果支援 multielement 紋理， \_ 則會使用 D3DSAMP ELEMENTINDEX 來找出要取樣的元素。
-   \_這些階段會忽略狀態 D3DSAMP DMAPOFFSET。
-   使用 [**CheckDeviceFormat**](/windows/desktop/api) 搭配 [D3DUSAGE \_ query \_ VERTEXTEXTURE "](d3dusage-query.md) 來查詢材質，以查看是否可將其當做頂點材質使用。
-   VertexTextureFilterCaps 指出頂點紋理取樣器允許何種篩選。 [D3DPTFILTERCAPS \_](d3dptfiltercaps.md)不允許 MINFANISOTROPIC 和 D3DPTFILTERCAPS \_ MAGFANISOTROPIC。

## <a name="sampling-stage-registers"></a>取樣階段暫存器

取樣階段暫存器會識別可在材質載入語句中使用的取樣單位。 取樣單位會對應至材質取樣階段，封裝 [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)中提供的取樣特定狀態。

每個取樣器都會使用 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)來唯一識別設定為對應取樣器的單一材質介面。 不過，您可以在多個取樣器設定相同的材質介面。

在繪圖時，紋理不能同時設定為轉譯目標和某個階段的材質。

由於 vs \_ 3 \_ 0 支援四個取樣器，因此在單一著色器階段中最多可以讀取四個材質表面。 取樣器暫存器可能只會顯示為材質 load 語句中的引數： [texldl-vs](../direct3dhlsl/texldl---vs.md)。

在 vs \_ 3 \_ 0 中，如果您使用取樣器，則必須在著色器程式的開頭宣告它，並使用 [ (samplerType] 的 [ [ \_ sm3-vs asm]) ](../direct3dhlsl/dcl-samplertype---vs.md) (和 ps \_ 2 0) 中的相同 \_ 。

## <a name="software-processing"></a>軟體處理

軟體頂點處理將支援這項功能。 您可以藉由呼叫 [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) 和檢查 VertexTextureFilterCaps，檢查支援的特定篩選類型。 所有已發佈的材質格式在軟體頂點處理中都支援做為頂點紋理。

應用程式可以藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api) 並提供 (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md)) 為使用方式，檢查軟體頂點處理模式中是否支援特定的材質格式。 所有格式都支援軟體頂點處理。 臨時集區是軟體頂點處理的必要項。

## <a name="api-changes"></a>API 變更


```
   
// New define
#define D3DVERTEXTEXTURESAMPLER0 (D3DDMAPSAMPLER+1)
#define D3DVERTEXTEXTURESAMPLER1 (D3DDMAPSAMPLER+2)
#define D3DVERTEXTEXTURESAMPLER2 (D3DDMAPSAMPLER+3)
#define D3DVERTEXTEXTURESAMPLER3 (D3DDMAPSAMPLER+4)
    

#define D3DVERTEXTEXTURESAMPLER  (0x00100000L)

// New caps field in D3DCAPS9
DWORD VertexTextureFilterCaps;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點管線](vertex-pipeline.md)
</dt> </dl>

 

 
