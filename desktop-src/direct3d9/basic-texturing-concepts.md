---
description: 早期電腦產生的 3D 影像，雖然普遍對當代而言算先進，但通常會有具光澤的塑膠感。
ms.assetid: 548ae140-c746-4fab-8000-421289d4f0a2
title: " (Direct3D 9) 的基本紋理概念"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba8c4971f70cbe5b7b371f71191de6edb4c2be46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972570"
---
# <a name="basic-texturing-concepts-direct3d-9"></a> (Direct3D 9) 的基本紋理概念

早期電腦產生的 3D 影像，雖然普遍對當代而言算先進，但通常會有具光澤的塑膠感。 其缺乏可讓 3D 物件看起來逼真且複雜的標記類型，例如磨損、裂縫，指紋及指尖。 在最近幾年，紋理在開發人員之間獲得了更熱門的功能，以增強電腦產生的3D 影像的真實性。

在日常的使用中，文字紋理是指物件的平滑或粗糙度。 不過，在電腦圖形中，紋理是像素色彩的點陣圖，讓物件具有紋理的外觀。

因為 Direct3D 紋理為點陣圖，所以任何點陣圖都可套用至 Direct3D 原始物件。 例如，應用程式可以建立並操控似乎具備木紋圖樣的物件。 草地、泥土和岩石可套用至形成山丘的一組 3D 原始物件。 結果為逼真的山坡。 您也可以添加紋理來建立效果，例如路旁的路標、懸崖的岩石層，或地板大理石的外觀。

此外，Direct3D 支援更進階的添加紋理技術，例如紋理混合 (選擇性搭配透明度) 及光線對應。 如需詳細資訊，請參閱使用 [) 的材質混合 (direct3d 9 ](texture-blending.md) 和 [紋理的燈光對應 (Direct3D 9) ](light-mapping-with-textures.md)。

如果您的應用程式建立硬體抽象層 (HAL) 裝置或軟體裝置，其可以使用 8、16、24、32、64 或 128 位元紋理。

下列主題包含其他資訊。

-   [ (Direct3D 9) 的材質定址模式 ](texture-addressing-modes.md)
-   [ (Direct3D 9) 的材質中途區域 ](texture-dirty-regions.md)
-   [ (Direct3D 9) 的材質調色板 ](texture-palettes.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 紋理](direct3d-textures.md)
</dt> </dl>

 

 



