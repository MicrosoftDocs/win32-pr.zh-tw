---
description: 應用程式要逼真呈現 3D 場景，必須考慮光源效果對場景外觀的影響。
ms.assetid: ff2037e4-2cf6-4247-b93f-13f0078f3b58
title: 使用 (Direct3D 9) 的材質進行淺色對應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5652446562e4c66390d67e11fa624a4a5659b85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972526"
---
# <a name="light-mapping-with-textures-direct3d-9"></a>使用 (Direct3D 9) 的材質進行淺色對應

應用程式要逼真呈現 3D 場景，必須考慮光源效果對場景外觀的影響。 雖然平面和 Gouraud shading 這方面的技術都是難能可貴的工具，但可能無法滿足您的需求。 Direct3D 支援物件多重紋理混合。 這些功能可讓應用程式的轉譯具有比單獨使用陰影技術呈現的場景更逼真的外觀場景。 藉由套用一或多個光線對應，您的應用程式可將光線和陰影區域對應到其基本類型。

光線對應為紋理或紋理群組，其包含 3D 場景中的照明相關資訊。 您可以在光線對應 alpha 值或色彩值或兩者中，儲存光源資訊。

如果您使用物件多重紋理混合執行光線對應，您的應用程式應將光線對應轉譯到第一輪基本類型。 它應該使用第二輪來呈現基底紋理。 例外是反射光線對應。 若是如此，第一次呈現基本紋理，接著新增光線對應。

多個紋理混合可讓應用程式一次呈現光線對應與基本紋理。 如果使用者的硬體提供多個紋理混合，您的應用程式應該利用它執行光線對應。 這會大幅改善應用程式效能。

使用光線對應，當在轉譯基本類型時，Direct3D 應用程式可以獲得各種照明效果。 它不僅可以在場景中對應單色及彩色光線，也可以新增細節，例如反射強光，並擴散光源。

有關使用 Direct3D 紋理混合執行光線對應的資訊，顯示於下列主題中。

-   [ (Direct3D 9) 的單色燈光地圖 ](monochrome-light-maps.md)
-   [ (Direct3D 9) 的色彩淺色地圖 ](color-light-maps.md)
-   [ (Direct3D 9) 的鏡面燈光地圖 ](specular-light-maps.md)
-   [ (Direct3D 9) 的擴散燈光地圖 ](diffuse-light-maps.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質混色](texture-blending.md)
</dt> </dl>

 

 



