---
description: 一般地圖產生常數。
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4263237cedf92a5e322f2fe139e9afe2297f6b9b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342853"
---
# <a name="d3dx_normalmap"></a>D3DX \_ NORMALMAP

一般地圖產生常數。



| \#定義                            | Description                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX \_ NORMALMAP \_ 鏡像 \_ U          | 表示 u 軸上材質邊緣的圖元應進行鏡像，而不會換行。                                                                                                   |
| D3DX \_ NORMALMAP \_ 鏡像 \_ V          | 指出 v 軸上材質邊緣的圖元應進行鏡像，而不會換行。                                                                                                   |
| D3DX \_ NORMALMAP \_ 鏡像             | 與指定 D3DX \_ NORMALMAP \_ 鏡像 \_ U \| D3DX \_ NORMALMAP \_ 鏡像 V 相同 \_ 。                                                                                                                       |
| D3DX \_ NORMALMAP \_ INVERTSIGN         | 反轉每個標準的方向。                                                                                                                                                              |
| D3DX \_ NORMALMAP \_ COMPUTE \_ 遮蔽 | 計算每個圖元的遮蔽詞彙，然後將其編碼成 Alpha。 Alpha 為1表示圖元不會以任何方式隱藏，而 Alpha 為0表示圖元完全隱藏。 |



 

## <a name="constant-information"></a>常數資訊



| 需求                         | 值           |
|--------------------------|------------|
| 標頭                   | d3dx9tex。h |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[D3DX 常數](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[**D3DXComputeNormalMap**](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



