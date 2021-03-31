---
title: BC7 格式
description: BC7 格式是用於高品質 RGB 和 RGBA 資料壓縮的紋理壓縮格式。
ms.assetid: DF333106-293E-4B3E-A1EB-B0BF0ADBAC72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9b64c3d4a8b5e960077a9f33de82ff08cd4bbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382458"
---
# <a name="bc7-format"></a>BC7 格式

BC7 格式是用於高品質 RGB 和 RGBA 資料壓縮的紋理壓縮格式。

-   [關於 BC7/DXGI \_ 格式 \_ BC7](/windows)
-   [BC7 執行](#bc7-implementation)
-   [解碼 BC7 格式](#decoding-the-bc7-format)
-   [相關主題](#related-topics)

如需 BC7 格式的區塊模式資訊，請參閱 [BC7 格式模式參考](bc7-format-mode-reference.md) (英文)。

## <a name="about-bc7dxgi_format_bc7"></a>關於 BC7/DXGI \_ 格式 \_ BC7

BC7 是由下列 DXGI \_ 格式列舉值所指定：

-   **DXGI \_格式化 \_ BC7 \_** 無別。
-   **DXGI \_FORMAT \_ BC7 \_ UNORM**。
-   **DXGI \_FORMAT \_ BC7 \_ UNORM \_ SRGB**。

BC7 格式可用於 [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (包括陣列)、Texture3D，或 TextureCube (包括陣列) 紋理資源。 同樣地，此格式適用於任何與這些資源建立關聯的 Mipmap 表面。

BC7 使用固定的 16 位元組 (128 位元) 區塊大小，以及固定之 4x4 材質的磚大小。 與之前的 BC 格式一樣，大於支援之磚大小 (4x4) 的紋理影像，程式會使用多重區塊對其進行壓縮。 此位址身分識別也適用於 3D 圖片和 Mipmap、立方體貼圖，以及紋理陣列。 所有影像磚都必須格式相同。

BC7 壓縮三通道 (RGB) 和四通道 (RGBA) 定點資料影像。 一般而言，來源資料的每個色彩元件 (通道) 為 8 位元，但此格式可將來源資料的每個色彩元件編碼為較高位元。 所有影像磚都必須格式相同。

BC7 解碼器在套用紋理篩選之前，會先執行解壓縮。

BC7 解壓縮硬體必須為位元精確。也就是硬體傳回的結果，必須和本文中所述解碼器傳回的結果相同。

## <a name="bc7-implementation"></a>BC7 實作

BC7 實作可以指定 8 種模式中的一種，並具有在 16 位元組 (128 位元) 區塊之最低有效位元中指定的模式。 該模式的編碼，是由 0 或更多具有 0 值的位元，最後再加上一個 1 而成。

BC7 區塊可能包含多個端點配對。 基於本檔的目的，對應至端點配對的一組索引可能稱為「子集」。 此外，在某些區塊模式中，端點標記法的編碼方式，也就是此檔的用途，也就是所謂的「RBGP」，其中「P」位代表端點之色彩元件的共用最少位。 例如，如果格式的端點表示法為 "RGB 5.5.5.1"，則端點會解譯為 RGB 6.6.6 值，其中 P 位元的狀態定義了每個元件的最低有效位元。 同樣地，對於具有 Alpha 色板的來源資料，如果格式的表示為 "RGBAP 5.5.5.5.1"，則端點會 interepreted 為 RGBA 6.6.6.6。 依區塊模式而定，您能為子集的兩個端點 (每一子集 2 個 P 位元) 個別指定共用最低有效位元，或讓子集的兩個端點 (每一子集 1 個 P 位元) 共用。

對於沒有明確編碼 Alpha 元件的 BC7 區塊，BC7 區塊包含模式位元、分割位元、壓縮端點、壓縮索引，和一個選擇性的 P 位元。 在這些區塊中，端點具有僅限 RGB 的表示法，且 Alpha 元件為來源資料中的所有材質都解碼為 1.0。

對於具有合併色彩和 Alpha 元件的 BC7 區塊，一個區塊包含模式位元、壓縮端點、壓縮索引，以及選用的分割位元和一個 P 位元。 在這些區塊中，端點色彩以 RGBA 格式表示，而且會插入 Alpha 元件值和色彩元件值。

對於具有不同色彩與 Alpha 元件的 BC7 區塊，一個區塊包含模式位元、旋轉位元、壓縮端點、壓縮索引，和一個選擇性的索引選取器位元。 這些區塊具有有效的 RGB 向量 \[ R、G、B \] 和純量 Alpha 通道，而且會 \[ 另外進行 \] 編碼。

下表列出每個區塊類型的元件。



| BC7 區塊包含...     | 模式位元 | 旋轉位元 | 索引選取器位元 | 分割位元 | 壓縮端點 | P 位元    | 壓縮索引 |
|---------------------------|-----------|---------------|--------------------|----------------|----------------------|----------|--------------------|
| 僅限色彩元件     | 必要  | N/A           | N/A                | 必要       | 必要             | 選用 | 必要           |
| 色彩 + Alpha 合併    | 必要  | N/A           | N/A                | 選用       | 必要             | 選用 | 必要           |
| 色彩和 Alpha 分隔 | 必要  | 必要      | 選用           | N/A            | 必要             | N/A      | 必要           |



 

BC7 在兩個端點之間的大約行定義調色盤。 模式值判斷每個區塊的端點配對插入數量。 BC7 在每個材質上儲存一個調色盤索引。

對於每個對應至一組端點的索引子集，編碼器修正了該子集壓縮索引資料中一個位元的狀態。 它藉由選擇一個端點順序來完成此項工作，該端點順序可讓指定的「修正」索引之索引將其最高有效位元設為 0，之後便能捨棄該位元，為每個子集節省一個位元。 對於僅具有一個單一子集的區塊模式，修正索引一律為索引 0。

## <a name="decoding-the-bc7-format"></a>解碼 BC7 格式

下列虛擬程式碼概述了於 16 位元組 BC7 區塊中，解壓縮位於 (x,y) 之像素的步驟。

``` syntax
decompress_bc7(x, y, block)
{
    mode = extract_mode(block);
    
    //decode partition data from explicit partition bits
    subset_index = 0;
    num_subsets = 1;
    
    if (mode.type == 0 OR == 1 OR == 2 OR == 3 OR == 7)
    {
        num_subsets = get_num_subsets(mode.type);
        partition_set_id = extract_partition_set_id(mode, block);
        subset_index = get_partition_index(num_subsets, partition_set_id, x, y);
    }
    
    //extract raw, compressed endpoint bits
    UINT8 endpoint_array[num_subsets][4] = extract_endpoints(mode, block);
    
    //decode endpoint color and alpha for each subset
    fully_decode_endpoints(endpoint_array, mode, block);
    
    //endpoints are now complete.
    UINT8 endpoint_start[4] = endpoint_array[2 * subset_index];
    UINT8 endpoint_end[4]   = endpoint_array[2 * subset_index + 1];
        
    //Determine the palette index for this pixel
    alpha_index     = get_alpha_index(block, mode, x, y);
    alpha_bitcount  = get_alpha_bitcount(block, mode);
    color_index     = get_color_index(block, mode, x, y);
    color_bitcount  = get_color_bitcount(block, mode);

    //determine output
    UINT8 output[4];
    output.rgb = interpolate(endpoint_start.rgb, endpoint_end.rgb, color_index, color_bitcount);
    output.a   = interpolate(endpoint_start.a,   endpoint_end.a,   alpha_index, alpha_bitcount);
    
    if (mode.type == 4 OR == 5)
    {
        //Decode the 2 color rotation bits as follows:
        // 00 – Block format is Scalar(A) Vector(RGB) - no swapping
        // 01 – Block format is Scalar(R) Vector(AGB) - swap A and R
        // 10 – Block format is Scalar(G) Vector(RAB) - swap A and G
        // 11 - Block format is Scalar(B) Vector(RGA) - swap A and B
        rotation = extract_rot_bits(mode, block);
        output = swap_channels(output, rotation);
    }
    
}
```

下列虛擬程式碼概述了於 16 位元組 BC7 區塊中，為每個子集完整解碼端點色彩和 Alpha 元件的步驟。

``` syntax
fully_decode_endpoints(endpoint_array, mode, block)
{
    //first handle modes that have P-bits
    if (mode.type == 0 OR == 1 OR == 3 OR == 6 OR == 7)
    {
        for each endpoint i
        {
            //component-wise left-shift
            endpoint_array[i].rgba = endpoint_array[i].rgba << 1;
        }
        
        //if P-bit is shared
        if (mode.type == 1) 
        {
            pbit_zero = extract_pbit_zero(mode, block);
            pbit_one = extract_pbit_one(mode, block);
            
            //rgb component-wise insert pbits
            endpoint_array[0].rgb |= pbit_zero;
            endpoint_array[1].rgb |= pbit_zero;
            endpoint_array[2].rgb |= pbit_one;
            endpoint_array[3].rgb |= pbit_one;  
        }
        else //unique P-bit per endpoint
        {  
            pbit_array = extract_pbit_array(mode, block);
            for each endpoint i
            {
                endpoint_array[i].rgba |= pbit_array[i];
            }
        }
    }

    for each endpoint i
    {
        // Color_component_precision & alpha_component_precision includes pbit
        // left shift endpoint components so that their MSB lies in bit 7
        endpoint_array[i].rgb = endpoint_array[i].rgb << (8 - color_component_precision(mode));
        endpoint_array[i].a = endpoint_array[i].a << (8 - alpha_component_precision(mode));

        // Replicate each component's MSB into the LSBs revealed by the left-shift operation above
        endpoint_array[i].rgb = endpoint_array[i].rgb | (endpoint_array[i].rgb >> color_component_precision(mode));
        endpoint_array[i].a = endpoint_array[i].a | (endpoint_array[i].a >> alpha_component_precision(mode));
    }
        
    //If this mode does not explicitly define the alpha component
    //set alpha equal to 1.0
    if (mode.type == 0 OR == 1 OR == 2 OR == 3)
    {
        for each endpoint i
        {
            endpoint_array[i].a = 255; //i.e. alpha = 1.0f
        }
    }
}
```

若要為每個子集產生每個插入的元件，請使用下列演算法︰讓 "c" 成為產生的元件、讓 "e0" 成為該子集端點 0 的元件，並讓 "e1" 成為該子集端點 1 的元件。

``` syntax
UINT16 aWeight2[] = {0, 21, 43, 64};
UINT16 aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
UINT16 aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

UINT8 interpolate(UINT8 e0, UINT8 e1, UINT8 index, UINT8 indexprecision)
{
    if(indexprecision == 2)
        return (UINT8) (((64 - aWeights2[index])*UINT16(e0) + aWeights2[index]*UINT16(e1) + 32) >> 6);
    else if(indexprecision == 3)
        return (UINT8) (((64 - aWeights3[index])*UINT16(e0) + aWeights3[index]*UINT16(e1) + 32) >> 6);
    else // indexprecision == 4
        return (UINT8) (((64 - aWeights4[index])*UINT16(e0) + aWeights4[index]*UINT16(e1) + 32) >> 6);
}
```

下列虛擬程式碼示範如何為色彩和 Alpha 元件擷取索引及位元計數的方式。 使用不同色彩和 Alpha 的區塊也有兩組索引資料︰一個用於向量通道，一個用於純量通道。 對於模式 4，這些索引有不同寬度 (2 或 3 位元)，而且有一個 1 位元選取器來指定向量或純量資料是否使用 3 位元索引。 (解壓縮 Alpha 位元計數類似於擷取色彩位元計數，但是具有以 **idxMode** 位元為基礎的反向行為。)

``` syntax
bitcount get_color_bitcount(block, mode)
{
    if (mode.type == 0 OR == 1)
        return 3;
    
    if (mode.type == 2 OR == 3 OR == 5 OR == 7)
        return 2;
    
    if (mode.type == 6)
        return 4;
        
    //The only remaining case is Mode 4 with 1-bit index selector
    idxMode = extract_idxMode(block);
    if (idxMode == 0)
        return 2;
    else
        return 3;
}
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11 中的材質區塊壓縮](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 