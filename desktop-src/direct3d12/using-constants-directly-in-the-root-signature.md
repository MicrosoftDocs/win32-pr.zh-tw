---
title: 直接在根簽章中使用常數
description: 應用程式可以在根簽章中定義根常數，每個常數都是一組32位值。 它們會以高階的陰影語言顯示 (HLSL) 作為常數緩衝區。 請注意，記錄原因的常數緩衝區會視為4x32 位值的集合。
ms.assetid: F9A2640F-D1FA-481C-BDF1-B15372E3C512
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3cd3980bede72d6e2f4b163abe11b249970eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104892"
---
# <a name="using-constants-directly-in-the-root-signature"></a>直接在根簽章中使用常數

應用程式可以在根簽章中定義根常數，每個常數都是一組32位值。 它們會以高階的陰影語言顯示 (HLSL) 作為常數緩衝區。 請注意，記錄原因的常數緩衝區會視為4x32 位值的集合。

每一組使用者常數都會被視為32位值的純量陣列，可動態編制索引，而且是從著色器的唯讀。 指定根常數集合的超出範圍索引會產生未定義的結果。 在 HLSL 中，可以提供資料結構定義給使用者常數，以提供它們類型。 例如，如果根簽章定義4個根常數的集合，HLSL 可以在其上重迭下列結構。

``` syntax
struct DrawConstants
{
    uint foo;
    float2 bar;
    int moo;
};
ConstantBuffer<DrawConstants> myDrawConstants : register(b1, space0);
```

因為不支援根簽章空間中的動態索引編制，所以不允許在會對應至根常數的常數緩衝區中使用陣列。 例如，在常數緩衝區中有一個專案（例如）是不正確 `float myArray[2];` 。 對應至根常數的常數緩衝區本身不能是陣列;因此，對應 `cbuffer myCBArray[2]` 至根常數是不正確。

可以部分設定常數。 例如，如果根簽章在 *RootTableBindSlot* 2 定義 4 32 位的值，則可以一次設定四個常數的任何子集， (其他常數保持不變) 。 這在會繼承根簽章狀態並可部分變更的組合中很有用。

設定常數時，請小心著色器預期的常數緩衝區配置。 例如，常數可以填補至 `vec4` 界限。 若要驗證預期的版面配置，請從 HLSL 著色器檢查反映資訊。

下列 (自 [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) 介面的 api) 用於直接在根簽章上設定常數：

-   [**SetGraphicsRoot32BitConstant**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)
-   [**SetGraphicsRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants)
-   [**SetComputeRoot32BitConstant**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [**SetComputeRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)

此外，請參閱 [**D3D12 \_ 根 \_ 常數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) 結構。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[根簽章](root-signatures.md)
</dt> </dl>

 

 




