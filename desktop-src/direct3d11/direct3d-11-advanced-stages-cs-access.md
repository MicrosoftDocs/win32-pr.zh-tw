---
title: 存取資源
description: 有數種方式可存取資源。
ms.assetid: 83950c4d-5df2-4ed1-9d8f-222a62791c18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69ab7bffd22b2271c4d648c3a95ec8d98656973
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990971"
---
# <a name="accessing-resources"></a>存取資源

有數種方式可存取 [資源](overviews-direct3d-11-resources-types.md)。 無論如何，Direct3D 保證會針對任何超出範圍存取的資源傳回零。

-   [以位元組位移存取](#access-by-byte-offset)
-   [依索引存取](#access-by-index)
-   [由 Mips 方法存取](#access-by-mips-method)
-   [相關主題](#related-topics)

## <a name="access-by-byte-offset"></a>以位元組位移存取

您可以使用位元組位移來存取兩個新的緩衝區類型：

-   [**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) 是唯讀緩衝區。
-   [**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) 是讀取或寫入緩衝區。

## <a name="access-by-index"></a>依索引存取

資源類型可以使用索引來參考資源中的特定位置。 請考慮此範例：


```
uint2 pos;
Texture2D<float4> myTexture;
float4 myVar = myTexture[pos];
```



此範例會將位於 *myTexture* 2d 材質資源中 *pos* 位置的材質所儲存的4個 float 值，指派給 *myVar* 變數。

> [!Note]  
> 以這種方式存取材質的預設值是 mipmap 層級零 () 最詳細的層級。

 

> [!Note]  
> "Float4 myVar = myTexture \[ pos \] ;" 行相當於 "float4 MyVar = MyTexture. Load (uint3 (pos，0) ) ;"。 依索引存取是新的 HLSL 語法增強功能。

 

> [!Note]  
> 在2010年6月版的 DirectX SDK 和更新版本中，編譯器可讓您編制除了 [位元組位址緩衝區](direct3d-11-advanced-stages-cs-resources.md)以外的所有資源類型。

 

> [!Note]  
> 2010年6月編譯器和更新版本可讓您宣告本機資源變數。 您可以將全域定義的資源指派 (例如，將) *myTexture* 至這些變數，並使用與全域對應專案相同的方式來使用它們。

 

## <a name="access-by-mips-method"></a>由 Mips 方法存取

材質物件有 **mips** 方法 (例如， [**Texture2D**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))) ，您可以用它來指定 mipmap 層級。 此範例會讀取2D 材質中 mipmap 層級 2 (7、16) 所儲存的色彩：


```
uint x = 7;
uint y = 16;
float4 myColor = myTexture.mips[2][uint2(x,y)];
```



這是2010年6月編譯器和更新版本的增強功能。 "MyTexture mips \[ 2 \] \[ uint2 (x，y) \] " 運算式相當於 "myTexture. Load (uint3 (x，y，2) ) "。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[計算著色器總覽](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 