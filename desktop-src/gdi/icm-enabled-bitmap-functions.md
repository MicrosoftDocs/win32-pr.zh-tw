---
description: Microsoft 影像色彩管理 (ICM) 可確保色彩影像、繪圖物件或文字物件在任何裝置上都能盡可能地轉譯成其原始意圖，儘管裝置之間的映射技術和色彩功能有所差異。
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: ICM-Enabled 點陣圖函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b89dac569aafad1ef94b066bc97f588bac62c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848551"
---
# <a name="icm-enabled-bitmap-functions"></a>ICM-Enabled 點陣圖函數

Microsoft 影像色彩管理 (ICM) 可確保色彩影像、繪圖物件或文字物件在任何裝置上都能盡可能地轉譯成其原始意圖，儘管裝置之間的映射技術和色彩功能有所差異。 無論您是要掃描彩色掃描器上的影像或其他圖形、在螢幕上進行觀看或編輯，或是列印在紙張、電影或其他媒體上，ICM 2.0 都能協助您保持一致且精確的色彩。 如需 ICM 的詳細資訊，請參閱 [Windows 色彩系統](/previous-versions//dd372446(v=vs.85))。

圖形裝置介面中有各種不同的函式 (使用或操作色彩資料的 GDI) 。 下列點陣圖函數可用於 ICM：

-   [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [**CreateDIBSection**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [**SetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
