---
title: ByteAddressBuffer
description: ByteAddressBuffer
ms.assetid: 809b5ee8-0a25-402e-8cf2-f5e7a8094ec6
keywords:
- ByteAddressBuffer HLSL
topic_type:
- apiref
api_name:
- ByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03e89f56522d941db4447b33b55cbedc7c73303f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971785"
---
# <a name="byteaddressbuffer"></a>ByteAddressBuffer

以位元組為單位編制索引的唯讀緩衝區。



| 方法                                                              | 描述                   |
|---------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-byteaddressbuffer-getdimensions.md) | 取得資源維度。 |
| [**載入**](byteaddressbuffer-load.md)                              | 取得一個值。               |
| [**Load2**](byteaddressbuffer-load2.md)                            | 取得兩個值。              |
| [**Load3**](byteaddressbuffer-load3.md)                            | 取得三個值。            |
| [**Load4**](byteaddressbuffer-load4.md)                            | 取得四個值。             |



 

當您使用原始緩衝區時，可以使用 **ByteAddressBuffer** 物件類型。 如需有關原始的緩衝區查看的詳細資訊，請參閱 [緩衝區的原始視圖](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro)。

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此物件。



| 著色器模型                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | 支援 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md)及更高的著色器模型 [著色器模型 4](dx-graphics-hlsl-sm4.md) (可透過 Direct3D 11 API 取得，方法是在支援計算著色器的裝置上，使用10.0 或10.1 功能等級 ([**D3D \_ 功能 \_ 等級**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) 。 如需舊版硬體上計算著色器支援的詳細資訊，請參閱 [下層硬體上的計算](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders)著色器 ) 。<br/> | 是       |



 

下列著色器類型支援此物件：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

如需有關位元組位址緩衝區的詳細資訊，請參閱 [位元組可定址的資源類型](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)。

著色器模型5也會實行 [讀寫位元組位址緩衝區](sm5-object-rwbyteaddressbuffer.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型5物件](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

