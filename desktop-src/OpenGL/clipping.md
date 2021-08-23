---
title: '裁剪 (OpenGL) '
description: 裁剪會以兩個步驟進行
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- OpenGL 處理管線，裁剪
- 裁剪 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb518b9208b73dad2071531f6a30cdff6cab2ec5dcbe937fa3e66fea8bb0a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289038"
---
# <a name="clipping-opengl"></a>裁剪 (OpenGL) 

裁剪會以兩個步驟進行：

1.  **查看磁片區 clippingApplication 特定的剪輯。** 在組合基本專案之後，就會視需要針對您使用 [**glClipPlane**](glclipplane.md)定義的任何裁剪平面，將它們裁剪為眼睛座標。  (OpenGL 必須支援至少六個這類應用程式特定的裁剪平面。 ) 
2.  投射矩陣會將基本專案轉換成剪輯座標，並由對應的視圖音量裁剪。 此矩陣可由矩陣轉換函式控制 (查看 [矩陣轉換](matrix-transformations.md)) 但通常是由 [**glFrustum**](glfrustum.md) 或 [**glOrtho**](glortho.md)所指定。

點、線段和多邊形會在裁剪期間以不同方式處理：

-   點會以原始狀態保留 (如果它們位於剪輯磁片區中) 或捨棄 (（如果它們位於剪輯磁片區) 以外）。
-   如果線段或多邊形的部分位於剪輯音量之外，就會在剪輯點產生新頂點。
-   若為多邊形，可能需要在剪輯點產生的新頂點之間建立整個邊緣。
-   若為已裁剪的線段和多邊形，則會將邊緣旗標、色彩和材質資訊指派給所有新頂點。

 

 




