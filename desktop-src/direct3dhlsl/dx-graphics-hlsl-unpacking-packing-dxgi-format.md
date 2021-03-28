---
title: 針對 In-Place 影像編輯解壓縮和封裝 DXGI_FORMAT
description: D3DX \_ DXGIFormatConvert. .inl 檔案包含內嵌格式轉換函式，您可以在 Direct3D 11 硬體上的計算著色器或圖元著色器中使用這些函數。
ms.assetid: 328c4488-9758-4359-a37b-ac50f20e2940
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c613a3f0068537733961b58a8a4c2b4528d21f25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300415"
---
# <a name="unpacking-and-packing-dxgi_format-for-in-place-image-editing"></a>\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式

D3DX \_ DXGIFormatConvert. .inl 檔案包含內嵌格式轉換函式，您可以在 Direct3D 11 硬體上的計算著色器或圖元著色器中使用這些函數。 您可以在應用程式中使用這些函式，同時讀取和寫入材質。 也就是說，您可以執行就地影像編輯。 若要使用這些內嵌格式轉換函式，請將 D3DX \_ DXGIFormatConvert. .inl 檔案包含在您的應用程式中。

Direct3D 11 的未排序存取視圖 (UAV) 的 Texture1D、Texture2D 或 Texture3D 資源支援從計算著色器或圖元著色器隨機存取讀取和寫入記憶體。 不過，Direct3D 11 同時支援讀取和寫入僅限 DXGI \_ 格式的 \_ R32 \_ UINT 材質格式。 例如，Direct3D 11 不支援同時讀取和寫入其他更實用的格式，例如 DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM。 您只能使用 UAV 來隨機寫入這類其他格式，也可以只使用著色器資源檢視 (SRV) 從這類其他格式讀取隨機存取。 格式轉換硬體無法同時從這類其他格式讀取和寫入。

不過，您仍然可以同時讀取和寫入這類其他格式，方法是在建立 UAV 時將材質轉換成 DXGI \_ 格式 \_ R32 \_ UINT 材質格式，只要資源的原始格式支援轉換成 dxgi \_ 格式 \_ R32 \_ UINT 即可。 最多32位的每個元素格式都支援轉換成 DXGI \_ 格式 \_ \_ 的 R32 UINT。 \_ \_ 當您建立 UAV 時，將材質轉換成 DXGI 格式 R32 \_ UINT 材質格式時，只要著色器在讀取和封裝上執行手動格式化解壓縮，就可以同時執行讀取和寫入至材質。

將材質轉換成 DXGI \_ 格式 \_ R32 \_ UINT 材質格式的優點是，您稍後可以使用適當的格式 (例如， \_ [DXGI 格式] \_ R16G16 \_ FLOAT) 與相同材質上的其他視圖，例如轉譯目標視圖 (RTVs) 或 SRVs。 因此，硬體可以執行一般的自動格式化解壓縮和套件、可以執行材質篩選，而不會有硬體限制。

下列案例要求應用程式採取下列動作順序來就地進行影像編輯。

假設您想要設定材質，讓您可以使用圖元著色器或計算著色器來執行就地編輯，而您想要將材質資料儲存為下列其中一種無類型格式的子系格式：

-   DXGI \_ 格式 \_ R10G10B10A2 無別 \_
-   DXGI \_ 格式 \_ R8G8B8A8 無別 \_
-   DXGI \_ 格式 \_ B8G8R8A8 無別 \_
-   DXGI \_ 格式 \_ B8G8R8X8 無別 \_
-   DXGI \_ 格式 \_ R16G16 無別 \_

例如，DXGI \_ format \_ R10G10B10A2 \_ UNORM 格式是 dxgi \_ 格式 R10G10B10A2 無別格式的子 \_ 系 \_ 。 因此，DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM 支援下列順序所述的使用模式。 從 DXGI 格式 R32 不具類型的格式（ \_ \_ \_ 例如 dxgi \_ 格式 \_ R32 \_ FLOAT）支援完整，不需要任何格式轉換說明，如下列順序所述。

**執行就地影像編輯**

1.  使用上一個案例中指定的適當無類型相依格式來建立材質，以及所需的系結旗標，例如 D3D11 系結的未 \_ \_ 排序 \_ 存取 D3D11 系結 \| \_ \_ 著色器 \_ 資源。
2.  針對就地影像編輯，請使用 DXGI \_ 格式 \_ R32 UINT 格式來建立 UAV \_ 。 Direct3D 11 API 通常不允許在不同的格式「系列」之間進行轉換。 不過，Direct3D 11 API 會產生具有 DXGI \_ 格式 \_ R32 UINT 格式的例外狀況 \_ 。
3.  在 [計算著色器] 或 [圖元著色器] 中，使用 D3DX DXGIFormatConvert. .inl 檔案中提供的適當內嵌格式套件和解壓縮函數 \_ 。 例如，假設紋理的 DXGI \_ 格式 \_ R32 \_ UINT UAV 真正持有 DXGI \_ 格式 \_ R10G10B10A2 \_ UNORM 格式的資料。 應用程式從 UAV 將 uint 讀入著色器之後，必須呼叫下列函式來將材質格式解壓縮：

    ```
    XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
    ```

    

    然後，若要在相同的著色器中寫入 UAV，應用程式會呼叫下列函式，將著色器資料封裝成應用程式可寫入至 UAV 的 uint：

    ```
    UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
    ```

    

4.  然後，應用程式可以使用所需的格式來建立其他視圖（例如 SRVs）。 例如， \_ \_ \_ 如果資源是建立為 dxgi \_ 格式的 \_ R10G10B10A2 \_ 無別，則應用程式可以建立具有 dxgi 格式的 SRV R10G10B10A2 UNORM 格式。 當著色器存取該 SRV 時，硬體可以正常執行自動類型轉換。

> [!Note]  
> 如果著色器必須僅寫入至 UAV，或讀取為 SRV，則不需要這項轉換工作，因為您可以使用完整類型的 UAVs 或 SRVs。 D3DX DXGIFormatConvert 中提供的格式轉換函式， \_ 只有在您想要執行同時讀取和寫入材質的 UAV 時，才有可能有用。

 

以下是包含在 D3DX DXGIFormatConvert. .inl 檔案中的格式轉換函式清單 \_ 。 這些函式會根據它們解壓縮和封裝的 DXGI 格式進行分類 \_ 。 每個支援的格式都會從上述案例中所列的其中一種非型別格式進行遞減，並支援轉換成 DXGI \_ 格式的 \_ R32 \_ UINT 作為 UAV。

<dl> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>DXGI \_ 格式 \_ R10G10B10A2 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>DXGI \_ 格式 \_ R10G10B10A2 \_ UINT
</dt> <dd>


```
XMUINT4 D3DX_R10G10B10A2_UINT_to_UINT4(UINT packedInput)
UINT    D3DX_UINT4_to_R10G10B10A2_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM \_ SRGB
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> 不精確的型別函 \_ 式會使用沒有足夠精確度的著色器指令來提供確切的答案。 替代函數會使用儲存在著色器中的查閱資料表，提供確切的 SRGB >浮點數轉換。

 

</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>DXGI \_ 格式 \_ R8G8B8A8 \_ UINT
</dt> <dd>


```
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(UINT packedInput)
XMUINT  D3DX_UINT4_to_R8G8B8A8_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>DXGI \_ 格式 \_ R8G8B8A8 \_ SNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_SNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>DXGI \_ 格式 \_ R8G8B8A8 \_ 聖
</dt> <dd>


```
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(UINT packedInput)
UINT   D3DX_INT4_to_R8G8B8A8_SINT(XMINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_B8G8R8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM \_ SRGB
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> 不精確的型別函 \_ 式會使用沒有足夠精確度的著色器指令來提供確切的答案。 替代函數會使用儲存在著色器中的查閱資料表，提供確切的 SRGB >浮點數轉換。

 

</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM(hlsl_precise XMFLOAT3 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM \_ SRGB
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(UINT packedInput) *
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(hlsl_precise XMFLOAT3 unpackedInput)
```



> [!Note]  
> 不精確的型別函 \_ 式會使用沒有足夠精確度的著色器指令來提供確切的答案。 替代函數會使用儲存在著色器中的查閱資料表，提供確切的 SRGB >浮點數轉換。

 

</dd> <dt>

<span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>DXGI \_ 格式 \_ R16G16 \_ FLOAT
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_FLOAT(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>DXGI \_ 格式 \_ R16G16 \_ UNORM
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_UNORM(hlsl_precise FLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>DXGI \_ 格式 \_ R16G16 \_ UINT
</dt> <dd>


```
XMUINT2 D3DX_R16G16_UINT_to_UINT2(UINT packedInput)
UINT    D3DX_UINT2_to_R16G16_UINT(XMUINT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>DXGI \_ 格式 \_ R16G16 \_ SNORM
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_SNORM(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>DXGI \_ 格式 \_ R16G16 \_ 聖
</dt> <dd>


```
XMINT2 D3DX_R16G16_SINT_to_INT2(UINT packedInput)
UINT   D3DX_INT2_to_R16G16_SINT(XMINT2 unpackedInput)
```



</dd> </dl>

## <a name="related-topics"></a>[相關主題]

[HLSL 的程式設計指南](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>相關主題

<dl> <dt>

[HLSL 的程式設計指南](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




