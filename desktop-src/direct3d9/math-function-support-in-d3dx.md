---
description: 深入瞭解 D3DX 中的數學函數支援。 D3DX 是提供 helper 服務的公用程式庫。 它是 Direct3D 元件之上的一層。
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: D3DX (Direct3D 9) 中的數學函數支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77e3d75c692d4801e6a8af64bd980e72eb88f0d3276ff4e1364302b5a62357d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119368968"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a>D3DX (Direct3D 9) 中的數學函數支援

D3DX 是提供 helper 服務的公用程式庫。 它是 Direct3D 元件之上的一層。

## <a name="math"></a>數學

針對下列各項，提供包含在一組函數中的數學支援：

-   色彩計算
-   飛機
-   矩陣操作
-   四元
-   2D 向量
-   3D 向量
-   4D 向量

請注意，與 c + + 多載結合時，基本3D 數學類型的支援很廣泛。

如需這些函數的詳細資訊，請參閱 [D3DX 函數](dx9-graphics-reference-d3dx-functions.md)。 為了協助找出您所需的功能，它們會分成數個資料夾。

## <a name="float16"></a>FLOAT16

使用 FLOAT16 資料類型時，請務必將值限制為最多 D3DX \_ 16F \_ MAX。 任何超過此值的 FLOAT16 值都會導致管線中有未定義的行為。 請參閱 [其他 D3DX 常數](other-d3dx-constants.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



