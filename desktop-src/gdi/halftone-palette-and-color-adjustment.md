---
description: 只要裝置內容的延展模式設定為 [半色調]，就可以使用半色調調色板。
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: 半色調調色板和色彩調整
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8be13f780dc5496173ffb4ddb990a96f7dbe462223e41e8a48d4a58329451277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761002"
---
# <a name="halftone-palette-and-color-adjustment"></a>半色調調色板和色彩調整

只要裝置內容的延展模式設定為 [半色調]，就可以使用半色調調色板。 應用程式會使用 [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) 函式來建立半色調調色板。 在呼叫 [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) 或 [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) 函式之前，應用程式必須在裝置內容中選取並實現這個調色板。

每當應用程式呼叫 [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) 和 [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) 函式，且裝置內容的延展模式設定為 [半色調] 時，系統就會自動調整來源點陣圖的輸入色彩。 這些色彩調整會影響影像的某些屬性，例如對比和亮度。 應用程式可以使用 [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) 函數來設定色彩調整值。 應用程式可以使用 [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) 函式，來取得指定之裝置內容的色彩調整值。

 

 



