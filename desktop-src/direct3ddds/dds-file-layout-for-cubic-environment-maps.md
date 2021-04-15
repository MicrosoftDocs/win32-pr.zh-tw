---
title: DDS Cube 對應範例
description: 針對三種環境對應，cube 的一或多個臉部會使用未壓縮或壓縮的格式寫入檔案，而且所有臉部都必須是相同的大小。
ms.assetid: a77234f6-ba10-40dd-902f-33e600384aa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235749bc0cf95a2e2120f66f3bcfb8a46e158628
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507296"
---
# <a name="dds-cube-map-example"></a>DDS Cube 對應範例

針對三種環境對應，cube 的一或多個臉部會使用未壓縮或壓縮的格式寫入檔案，而且所有臉部都必須是相同的大小。 每個臉部都可以定義 mipmap，不過所有臉部都必須有相同數目的 mipmap 層級。 如果檔案包含 cube 對應， \_ 就必須設定 DDSCAPS COMPLEX、DDSCAPS2 \_ 立方體貼圖，以及一或多個 DSCAPS2 \_ 立方體貼圖 \_ POSITIVEX/y/z 及/或 DDSCAPS2 立方體貼圖 \_ \_ NEGATIVEX/y/z。 臉部的寫入順序如下：正面 x、負 x、正 y、負 y、正 z、負 z，並省略任何遺漏的臉部。 每個臉部都會以其主要影像來寫入，後面接著任何 mipmap 層級。

例如，具有正 x、負 y 和正 z 面的 256 256 cube 地圖、DXT1 的像素格式，以及所有 mipmap 層級都會包含下列各項：



| DDS 元件                                      | \# 位元組 |
|-----------------------------------------------------|----------|
| header                                              | 128      |
| 256-256 正 x 主要影像                    | 32768    |
| 128-128 正 x mipmap 影像                  | 8192     |
| 64-64 正 x mipmap 影像                    | 2048     |
| 32-32 正 x mipmap 影像                    | 512      |
| 16×16正 x mipmap 影像                    | 128      |
| 8 x 8 的正 x mipmap 影像                      | 32       |
| 4 x 4 的正 x mipmap 影像                      | 8        |
| 2×2的正 x mipmap 影像                      | 8        |
| 1-1 個正 x mipmap 影像                      | 8        |
| 針對 y mipmap 影像重複先前的9層 | 43704    |
| 針對 z mipmap 影像重複前9層 | 43704    |



 

從 DirectX 8 開始，會儲存 cube 對應和所有定義的臉部。

## <a name="dxgi-cube-maps"></a>DXGI Cube 對應

Direct3D 10. x 和 Direct3D 11 中的三層環境對應相當於具有6個影像的2D 材質陣列，而且可以像這樣儲存在 DDS 檔案中。 使用 Direct3D 10.1 和 Direct3D 11 時，硬體也可以支援 cubemaps 陣列，也就是具有6個影像的倍數的2D 材質陣列 (6、12、18、24等 ) 。

例如，以下是以 BC6H 格式儲存 mipmap 層級的256到256立方體貼圖，作為2D 材質陣列：



| DDS 元件                                                                                                                                                                                                  | \# 位元組 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| "DX10" 的標頭 (FourCC )                                                                                                                                                                                        | 128      |
| 延伸標頭 (DXGI 格式設定為 95 \[ dxgi \_ 格式 \_ BC6H \_ UF16 \] ，維度值為 3 \[ D3Dxx \_ 資源 \_ 維度 \_ TEXTURE2D \] ，陣列大小為6，其他旗標為 0x4 \[ D3Dxx \_ 資源 \_ 其他 \_ TEXTURECUBE \])  | 20       |
| 256-256 陣列專案 0 (正 x) 主要影像                                                                                                                                                                | 65536    |
| 128-128 陣列專案 0 (正 x) mipmap 影像                                                                                                                                                              | 16384    |
| 64-64 陣列專案 0 (正 x) mipmap 影像                                                                                                                                                                | 4096     |
| 32-32 陣列專案 0 (正 x) mipmap 影像                                                                                                                                                                | 1024     |
| 16×16個數組專案 0 (正 x) mipmap 影像                                                                                                                                                                | 256      |
| 8 x 8 的陣列專案 0 (正 x) mipmap 影像                                                                                                                                                                  | 64       |
| 4 x 4 陣列專案 0 (正 x) mipmap 影像                                                                                                                                                                  | 16       |
| 2到2個數組專案 0 (正 x) mipmap 影像                                                                                                                                                                  | 16       |
| 1-1 個數組專案 0 (正 x) mipmap 影像                                                                                                                                                                  | 16       |
| 針對陣列專案1重複前9層 (負 x) mipmap 影像                                                                                                                                        | 87408    |
| 針對陣列專案2，重複前9個圖層 (正 y) mipmap 影像                                                                                                                                        | 87408    |
| 針對陣列專案 3 (負 y) mipmap 影像重複前9個圖層                                                                                                                                        | 87408    |
| 針對陣列專案4，重複前9個圖層 (正 z) mipmap 影像                                                                                                                                        | 87408    |
| 針對陣列專案5重複前9層 (負 z) mipmap 影像                                                                                                                                        | 87408    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DDS 程式設計指南](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




