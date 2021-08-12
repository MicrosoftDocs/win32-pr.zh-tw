---
title: DDS 紋理範例
description: 若是未壓縮的材質，請使用 DDSD \_ 音調和 DDPF \_ RGB 旗標; 若為壓縮的材質，請使用 DDSD \_ LINEARSIZE 和 DDPF \_ FOURCC 旗標。
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47fe1d7da71727c2c84bb3745772a10520367ac1cf6e9c4033932548d86c1302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289795"
---
# <a name="dds-texture-example"></a>DDS 紋理範例

若是未壓縮的材質，請使用 DDSD \_ 音調和 DDPF \_ RGB 旗標; 若為壓縮的材質，請使用 DDSD \_ LINEARSIZE 和 DDPF \_ FOURCC 旗標。 針對 mipmapped 材質，請使用 DDSD \_ MIPMAPCOUNT、DDSCAPS \_ MIPMAP 和 DDSCAPS \_ 複雜旗標以及 MIPMAP count 成員。 如果產生 mipmap，通常會寫入所有層級，直到1到1為止。

針對壓縮的材質，每個 mipmap 層級影像的大小通常是先前大小的一四，最少為 8 (DXT1) 或 16 (DXT2-5) 位元組 (用於正方形紋理) 。 您可以使用下列公式來計算非正方形材質的每個層級大小：


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



下表列出每個圖層針對 256 256 R8G8B8 材質所佔用的空間量，而不使用壓縮。



| DDS 元件          | \# 位元組 |
|-------------------------|----------|
| header                  | 128      |
| 256-256 的主要影像   | 196608   |
| 128-128 mipmap 影像 | 49152    |
| 64-64 mipmap 影像   | 12288    |
| 32-32 mipmap 影像   | 3072     |
| 16 x 16 mipmap 影像   | 768      |
| 8 x 8 mipmap 影像     | 192      |
| 四 mipmap 影像     | 48       |
| 2 mipmap 影像     | 12       |
| 1對 1 mipmap 影像     | 3        |



 

下表列出使用壓縮 (DXT1) 的相同材質，各圖層所佔用的空間量。



| DDS 元件         | \# 位元組 |
|------------------------|----------|
| header                 | 128      |
| 256-64 的主要影像   | 8192     |
| 128-32 mipmap 影像 | 2048     |
| 64-16 mipmap 影像  | 512      |
| 32-8 mipmap 影像   | 128      |
| 16-4 mipmap 影像   | 32       |
| 每2個 mipmap 影像    | 16       |
| mipmap 影像的 4 x 1    | 8        |
| mipmap 影像    | 8        |
| 1對 1 mipmap 影像    | 8        |



 

下表列出使用 DXGI 壓縮格式之相同材質的每個圖層所佔用的空間量 (在此案例中為 BC3 \_ UNORM) ，因此需要延伸標頭：



| DDS 元件                                                | \# 位元組 |
|---------------------------------------------------------------|----------|
| 標頭 (FourCC 設為 "DX10" )                                  | 128      |
| 延伸標頭 (DXGI 格式設定為 DXGI \_ 格式 \_ BC3 \_ UNORM)  | 20       |
| 256-64 的主要影像                                          | 16384    |
| 128-32 mipmap 影像                                        | 4096     |
| 64-16 mipmap 影像                                         | 1024     |
| 32-8 mipmap 影像                                          | 256      |
| 16-4 mipmap 影像                                          | 64       |
| 每2個 mipmap 影像                                           | 32       |
| mipmap 影像的 4 x 1                                           | 16       |
| mipmap 影像                                           | 16       |
| 1對 1 mipmap 影像                                           | 16       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DDS 程式設計指南](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




