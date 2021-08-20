---
title: RWByteAddressBuffer
description: 以位元組為單位索引的讀取/寫入緩衝區。
ms.assetid: 8370c14c-5822-4240-942d-565aa223d48c
keywords:
- RWByteAddressBuffer HLSL
topic_type:
- apiref
api_name:
- RWByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 931d2592c02b59a38068aa0fe9205d6be7cd1b9a504782f4407144101d09d4ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905768"
---
# <a name="rwbyteaddressbuffer"></a>RWByteAddressBuffer

以位元組為單位索引的讀取/寫入緩衝區。



| 方法                                                                                          | 描述                         |
|-------------------------------------------------------------------------------------------------|-------------------------------------|
| [**GetDimensions**](sm5-object-rwbyteaddressbuffer-getdimensions.md)                           | 取得資源維度。       |
| [**InterlockedAdd**](sm5-object-rwbyteaddressbuffer-interlockedadd.md)                         | 以不可部分完成的方式加入。                   |
| [**InterlockedAnd**](sm5-object-rwbyteaddressbuffer-interlockedand.md)                         | 以不可部分完成的方式 And。                   |
| [**InterlockedCompareExchange**](sm5-object-rwbyteaddressbuffer-interlockedcompareexchange.md) | 以不可部分完成的方式比較和交換。 |
| [**InterlockedCompareStore**](sm5-object-rwbyteaddressbuffer-interlockedcomparestore.md)       | 以不可部分完成的方式比較和儲存。    |
| [**InterlockedExchange**](sm5-object-rwbyteaddressbuffer-interlockedexchange.md)               | 以不可部分完成的方式交換。              |
| [**InterlockedMax**](sm5-object-rwbyteaddressbuffer-interlockedmax.md)                         | 以不可部分完成的方式尋找最大值。          |
| [**InterlockedMin**](sm5-object-rwbyteaddressbuffer-interlockedmin.md)                         | 以不可部分完成的方式尋找最小值。           |
| [**InterlockedOr**](sm5-object-rwbyteaddressbuffer-interlockedor.md)                           | 以不可部分完成的方式 Or。                    |
| [**InterlockedXor**](sm5-object-rwbyteaddressbuffer-interlockedxor.md)                         | 以不可部分完成的方式執行 xor。                   |
| [**載入**](rwbyteaddressbuffer-load.md)                                                        | 取得一個值。                     |
| [**Load2**](rwbyteaddressbuffer-load2.md)                                                      | 取得兩個值。                    |
| [**Load3**](rwbyteaddressbuffer-load3.md)                                                      | 取得三個值。                  |
| [**Load4**](rwbyteaddressbuffer-load4.md)                                                      | 取得四個值。                   |
| [**儲存**](sm5-object-rwbyteaddressbuffer-store.md)                                           | 設定一個值。                     |
| [**Store2**](sm5-object-rwbyteaddressbuffer-store2.md)                                         | 設定兩個值。                    |
| [**Store3**](sm5-object-rwbyteaddressbuffer-store3.md)                                         | 設定三個值。                  |
| [**Store4**](sm5-object-rwbyteaddressbuffer-store4.md)                                         | 設定四個值。                   |



 

RWByteAddressBuffer 物件的前面可以加上儲存類別 **globallycoherent**。 此儲存類別會造成記憶體阻礙和同步處理，以排清整個 GPU 上的資料，讓其他群組可以看到寫入。 如果沒有這個規範，記憶體屏障或同步將只會在目前群組內排清 UAV。

系結到此資源的 UAV 格式必須以 DXGI 格式 R32 無型別格式來建立 \_ \_ \_ 。

系結至此資源的 UAV 必須已建立 [**D3D11 \_ 緩衝區 \_ UAV \_ 旗標 \_ RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag)。

當您使用原始緩衝區時，可以使用 **RWByteAddressBuffer** 物件類型。 如需有關原始的緩衝區查看的詳細資訊，請參閱 [緩衝區的原始視圖](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro)。

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此物件。



| 著色器模型                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | 支援 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md)及更高的著色器模型 [著色器模型 4](dx-graphics-hlsl-sm4.md) (可透過 Direct3D 11 API 取得，方法是在支援計算著色器的裝置上，使用10.0 或10.1 功能等級 ([**D3D \_ 功能 \_ 等級**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) 。 如需舊版硬體上計算著色器支援的詳細資訊，請參閱 [下層硬體上的計算](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders)著色器 ) 。<br/> | 是       |



 

下列著色器類型支援此物件：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型5物件](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

