---
title: 不可部分完成函式
description: 若要存取新的資源類型或共用記憶體，請使用連鎖內建函式。 連鎖函式保證會以不可部分完成的方式運作。 也就是說，它們保證會以程式設計的順序發生。 本節列出不可部分完成的函式。
ms.assetid: de75482f-2919-4761-82d7-c8a8811046bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1b152560eeb97e1e8d3daf69edb7a094fd04b7d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508024"
---
# <a name="atomic-functions"></a>不可部分完成函式

若要存取新的資源類型或共用記憶體，請使用連鎖內建函式。 連鎖函式保證會以不可部分完成的方式運作。 也就是說，它們保證會以程式設計的順序發生。 本節列出不可部分完成的函式。

-   [**InterlockedAdd**](/windows/desktop/direct3dhlsl/interlockedadd)
-   [**InterlockedMin**](/windows/desktop/direct3dhlsl/interlockedmin)
-   [**InterlockedMax**](/windows/desktop/direct3dhlsl/interlockedmax)
-   [**InterlockedOr**](/windows/desktop/direct3dhlsl/interlockedor)
-   [**InterlockedAnd**](/windows/desktop/direct3dhlsl/interlockedand)
-   [**InterlockedXor**](/windows/desktop/direct3dhlsl/interlockedxor)
-   [**InterlockedCompareStore**](/windows/desktop/direct3dhlsl/interlockedcomparestore)
-   [**InterlockedCompareExchange**](/windows/desktop/direct3dhlsl/interlockedcompareexchange)
-   [**InterlockedExchange**](/windows/desktop/direct3dhlsl/interlockedexchange)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[計算著色器總覽](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 