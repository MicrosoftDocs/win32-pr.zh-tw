---
title: '子資源 (Direct3D 11 圖形) '
description: 本主題說明紋理子資源或資源的部分。
ms.assetid: 57444cb5-6c8b-4dac-8d6b-ca2b45eafac9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a432dbfbcbf08c4359ea436a3e8fa025c801d12
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024396"
---
# <a name="subresources-direct3d-11-graphics"></a>子資源 (Direct3D 11 圖形) 

本主題說明紋理子資源或資源的部分。

Direct3D 可以參考整個資源，或參考資源的子集。 子資源這個詞彙指的是資源的子集。

緩衝區定義為單一的子資源。 紋理稍微複雜一點，因為有數種不同的材質類型 (1D、2D 等等，) 某些支援 mipmap 層級和/或材質陣列的部分。 從最簡單的案例開始，1D 紋理定義為單一子資源，如下圖所示。

![1D 紋理的圖例](images/d3d10-1d-texture.png)

這表示組成 1D 紋理的紋理陣列包含在單一子資源中。

如果您展開有三個 mipmap 層級的一維紋理，就可以像下圖一樣視覺化。

![包含三個 mipmap 層級的1d 材質圖例](images/d3d10-resource-texture1d.png)

將此視為由三個子資源組成的單一材質。 您可以使用單一材質的詳細層級 (」 LOD) 來編制 subresource 索引。 使用紋理的陣列時，存取特定的 subresource 需要」 LOD 和特定的材質。 此外，API 會將這兩項資訊合併為單一以零為基礎的 subresource 索引，如下圖所示。

![以零起始的子資源索引的圖例](images/d3d10-resource-texture1darray-sub-indexing.png)

## <a name="selecting-subresources"></a>選取子資源

某些 Api 會存取整個資源 (例如 [**>id3d11devicecoNtext：： CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) 方法) ，其他人會存取一部分的資源 (例如 [**>id3d11devicecoNtext：： UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) 方法或 [**>id3d11devicecoNtext：： CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) 方法) 。 存取某個資源部分的方法通常會使用 view description (例如 [**D3D11 \_ TEX2D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) structure) 來指定要存取的子資源。

下列各節中的圖例顯示存取材質陣列時，視圖描述所使用的詞彙。

### <a name="array-slice"></a>陣列切片

根據紋理的陣列，每個使用 mipmap 的材質（ *陣列* 配量 (以白色矩形表示）) 包含一個材質和其所有的子資源，如下圖所示。

![陣列配量的圖例](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a>Mip 切片

 (由白色矩形表示的 *mip* 配量，) 為數組中的每個材質包含一個 mipmap 層級，如下圖所示。

![mip 配量的圖例](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a>選取單一子資源

您可以使用這兩種切片來選擇單一子資源，如下圖所示。

![使用陣列配量和 mip 配量來選擇 subresource 的圖例](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a>選取多個子資源

或者，您可以使用這兩種類型的配量來搭配 mipmap 層級和/或紋理數目，以選擇多個子資源，如下圖所示。

![選擇多個 subresource 的圖例](images/d3d10-resource-subresources-2.png)

> [!Note]  
> 轉譯 [**目標視圖**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) 只能使用單一 subresource 或 mip 配量，且不能包含來自一個以上 mip 配量的子資源。 也就是說，轉譯目標視圖中的每個材質都必須是相同的大小。 [**著色器資源檢視**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)可以選取子資源的任何矩形區域，如下圖所示。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 




