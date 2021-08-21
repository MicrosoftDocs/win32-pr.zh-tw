---
title: 新的資源類型
description: 已在 Direct3D 11 中新增數個新的資源類型。
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- '位元組位址緩衝區 (總覽) '
- '讀取/寫入緩衝區 (總覽) '
- '結構化緩衝區 (總覽) '
- 未排序的存取緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ab9e6f1677770b1a40766b846f4675df9eaa3809b42838783ddb834044bfe2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566298"
---
# <a name="new-resource-types"></a>新的資源類型

已在 Direct3D 11 中新增數個新的資源類型。

-   [讀取/寫入緩衝區和紋理](#readwrite-buffers-and-textures)
-   [結構化緩衝區](#structured-buffer)
-   [位元組位址緩衝區](#byte-address-buffer)
-   [未排序的存取緩衝區或紋理](#unordered-access-buffer-or-texture)
    -   [附加和使用緩衝區](#append-and-consume-buffer)
-   [相關主題](#related-topics)

## <a name="readwrite-buffers-and-textures"></a>讀取/寫入緩衝區和紋理

著色器模型4資源是唯讀的。 著色器模型5會執行一組新的對應讀取/寫入資源：

-   [RWBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   [RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d)、 [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)
-   [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d)、 [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)
-   [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

這些資源需要資源變數以透過索引) 存取記憶體 (，因為沒有任何方法可以直接存取記憶體。 資源變數可在方程式的左右側邊使用;如果使用於右邊，則範本類型必須是單一元件 (float、int 或 uint) 。

## <a name="structured-buffer"></a>結構化緩衝區

結構化緩衝區是包含大小相等之元素的緩衝區。 使用具有一或多個成員類型的結構來定義專案。 以下是具有三個成員的結構。


```
struct MyStruct
{
    float4 Color;
    float4 Normal;
    bool isAwesome;
};
```



使用此結構來宣告結構化緩衝區，如下所示：


```
StructuredBuffer<MyStruct> mySB;
```



除了編制索引之外，結構化緩衝區支援存取單一成員，如下所示：


```
float4 myColor = mySb[27].Color;
```



您可以使用下列物件類型來存取結構化緩衝區：

-   [StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) 是唯讀的結構化緩衝區。
-   [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) 是一個讀寫結構化緩衝區。

可以在 **RWStructuredBuffer** 的 int 和 uint 元素上 [執行可執行](direct3d-11-advanced-stages-cs-atomic-functions.md)連鎖作業的不可部分完成函式。

## <a name="byte-address-buffer"></a>位元組位址緩衝區

位元組位址緩衝區是以位元組位移定址其內容的緩衝區。 一般來說，會使用每個元素的 stride 來為每個專案編制 [緩衝區](overviews-direct3d-11-resources-buffers-intro.md) 的內容， (s) 和元素編號 (N) 所指定的 n \* 。 位元組位址緩衝區也可以稱為原始緩衝區，它會使用緩衝區開頭的位元組值位移來存取資料。 位元組值必須是四的倍數，如此才會對齊 DWORD。 如果有提供任何其他值，則行為會是未定義的。

著色器模型5引進了存取 [唯讀位元組位址緩衝區](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) 以及 [讀寫位元組位址緩衝區](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)的物件。 位元組位址緩衝區的內容是設計成32位不帶正負號的整數;如果緩衝區中的值不是不帶正負號的整數，請使用像是 [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) 的函式來讀取它。

## <a name="unordered-access-buffer-or-texture"></a>未排序的存取緩衝區或紋理

未排序的存取資源 (，其中包括緩衝區、紋理和材質陣列，而不含多層式) ，可讓您從多個執行緒暫時未排序的讀取/寫入存取。 這表示此資源類型可以由多個執行緒同時讀取/寫入，而不會透過使用 [不可部分完成的函](direct3d-11-advanced-stages-cs-atomic-functions.md)式來產生記憶體衝突。

藉由呼叫 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer)或 [**ID3D11Device：： CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d)之類的函式，並從 D3D11 系結 [**\_ \_ 旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)標列舉傳遞 **D3D11 系結 \_ \_ 無排序 \_ 存取** 旗標，來建立未排序的存取緩衝區或紋理。

未排序的存取資源只能系結至圖元著色器和計算著色器。 執行期間，以平行方式執行的圖元著色器或計算著色器會系結相同的未排序存取資源。

### <a name="append-and-consume-buffer"></a>附加和使用緩衝區

附加和取用緩衝區是一種特殊類型的未排序資源，支援在緩衝區結尾新增和移除值，類似于堆疊的運作方式。

附加和取用緩衝區必須是結構化緩衝區：

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

透過其方法使用這些資源，這些資源就不會使用資源變數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[計算著色器總覽](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 