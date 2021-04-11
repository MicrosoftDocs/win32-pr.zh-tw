---
description: 在 Direct3D 中，所有二維 (2D) 影像都是由稱為 surface 的線性範圍記憶體表示。
ms.assetid: 33430f01-cd26-45f4-9ce8-ca2c17c7ae6b
title: " (Direct3D 9) 的表面格式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78aad64940510a080ba05d0513e7f66d33912a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109376"
---
# <a name="surface-formats-direct3d-9"></a> (Direct3D 9) 的表面格式

在 Direct3D 中，所有二維 (2D) 影像都是由稱為 surface 的線性範圍記憶體表示。 您可以將介面視為2D 陣列，其中每個專案都有一個代表影像小型區段的色彩值，稱為圖元。 影像的詳細層級是由代表影像所需的圖元數，以及影像的色頻所需的位數來定義。 例如，以800圖元寬、600圖元高，且每個 (圖元的32位（以 800x600x32) 撰寫）的影像，將會比以 640x480x16) 撰寫的每個 (圖元的480圖元高度為640圖元的影像更詳細。 同樣地，更詳細的影像也需要較大的介面來儲存資料。 針對800x600x32 影像，介面的陣列維度將會是800x600，而且每個元素都會保存32位值以代表其色彩。

所有表面都有大小，並且會儲存代表色彩的特定位數。 代表色彩的位會分成個別的色彩元素：紅色、綠色和藍色。 在 Direct3D 中，所有色彩元素都是由 [D3DFORMAT](d3dformat.md) 列舉型別定義。 Direct3D 色彩格式會細分為每個色彩所保留的 byes 數目。 例如，Direct3D 中的16位色彩格式定義為 D3DFMT \_ R5G6B5，其中5位會保留給 red (R) 、6位表示綠色 (G) ，以及5位表示藍色 (B) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 表面](direct3d-surfaces.md)
</dt> </dl>

 

 



