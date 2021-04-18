---
title: DDS 磁片區材質範例
description: 若為磁片區材質，請使用 DDSCAPS \_ COMPLEX、DDSCAPS2 \_ VOLUME、DDSD \_ DEPTH、flags 及 set 和 dwDepth。 磁片區材質是 Direct3D 9 標準材質的延伸;您可以使用或不使用 mipmap 來定義磁片區材質。
ms.assetid: c1675a6d-129a-4e95-993f-e1be905781cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d82faa8041f2b5c99ef57ee2386ff5de84d787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968639"
---
# <a name="dds-volume-texture-example"></a>DDS 磁片區材質範例

若為磁片區材質，請使用 DDSCAPS \_ COMPLEX、DDSCAPS2 \_ VOLUME、DDSD \_ DEPTH、flags 及 set 和 dwDepth。 磁片區材質是 Direct3D 9 標準材質的延伸;您可以使用或不使用 mipmap 來定義磁片區材質。

針對沒有 mipmap 的磁片區，每個深度配量都會依序寫入至檔案。 如果包含 mipmap，則會將指定 mipmap 層級的所有深度配量一起寫入，其中每個層級都包含與上一個層級一半相同的配量，最少為1。

例如，使用 R8G8B8 像素格式的64到64的磁片區對應 (3 個位元組的每圖元) ，而且所有 mipmap 層級都會包含下列各項：



| DDS 元件                      | \# 位元組    |
|-------------------------------------|-------------|
| header                              | 128位元組   |
| 四個主要影像的 64-64 配量1。   | 12288位元組 |
| 四個主要影像的 64-64 配量2。   | 12288位元組 |
| 四個主要影像的 64-64 配量3。   | 12288位元組 |
| 四個主要映射的 64-64 配量4。   | 12288位元組 |
| 32-32 mipmap 影像中的配量第1個磁區。 | 3072位元組  |
| 32-32 mipmap 影像中的配量2。 | 3072位元組  |
| 1個 mipmap 影像的 16 x 16 磁區1。 | 768位元組   |
| 1個 mipmap 影像的8到8個配量1。   | 192位元組   |
| 1 mipmap 映射的4到4配量1。   | 48位元組    |
| 1個 mipmap 影像的2到2個配量1。   | 12個位元組    |
| 1 mipmap 影像的1到1配量1。   | 3個位元組     |



 

請注意，最小的 mipmap 層級只有3個位元組，因為 bitcount 是24，而且此層級沒有額外的壓縮。

已在 DirectX 8 中新增對磁片區紋理的支援。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DDS 程式設計指南](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




