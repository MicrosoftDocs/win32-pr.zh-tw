---
description: 裝置的色彩功能（例如顯示器和印表機）可以範圍從單色到數千種色彩。
ms.assetid: 3d71c24c-77f4-4344-91c3-439052402fae
title: 色彩基本知識
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29bcae40ee6771a9c46b892af6e6a8bceb4dcbc6498fb863353d39f92d4c2cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105747"
---
# <a name="color-basics"></a>色彩基本知識

裝置的色彩功能（例如顯示器和印表機）可以範圍從單色到數千種色彩。 由於應用程式可能需要在此範圍內產生裝置的輸出，因此應該準備好處理不同的色彩功能。

應用程式可以使用 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函式來取得 NUMCOLORS 值，以探索指定裝置可用的色彩數目。 此值會指定應用程式可使用的色彩計數。 此計數通常會對應至輸出裝置的實體屬性，例如印表機中的墨水數目，或顯示器介面卡可以傳輸至監視器的相異色彩信號數目。

雖然 NUMCOLORS 值會指定色彩的計數，但並不會識別可用的色彩。 應用程式可以藉由列舉所有具有 PS 固態類型的畫筆來探索可用的色彩 \_ 。 因為支援指定裝置的設備磁碟機通常會有完整範圍的純色，而且因為系統要求實心畫筆只有裝置可以產生的色彩，所以列舉這些畫筆通常相當於列舉色彩。 應用程式可以使用 [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) 函數來列舉畫筆。 如需程式碼範例，請參閱 [列舉色彩](enumerating-colors.md)。

如需詳細資訊，請參閱下列主題：

-   [色彩值](color-values.md)
-   [色彩近似值和遞色](color-approximations-and-dithering.md)
-   [點陣圖中的色彩](color-in-bitmaps.md)
-   [色彩混合](color-mixing.md)

 

 



