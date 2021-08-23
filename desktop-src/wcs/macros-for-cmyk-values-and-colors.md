---
title: CMYK 值和色彩的宏
description: 下列宏在操作 CMYK 值時很有用。
ms.assetid: e5d107fb-e010-400b-9ec5-90c2c0381dbe
keywords:
- Windows色彩系統 (WCS) 、CMYK 宏
- WCS (Windows 色彩系統) 、CMYK 宏
- 影像色彩管理、CMYK 宏
- 色彩管理、CMYK 宏
- 色彩、CMYK 宏
- WCS 參考，CMYK 宏
- WCS、CMYK 宏的參考
- CMYK 宏
- '青色洋紅色黃色黑色 (CMYK) '
- 'CMYK (青色洋黃色黑色) '
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591c479686db45f1b0d6fc6097d5134de481307b144200604a15b360bcf2c146
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593358"
---
# <a name="macros-for-cmyk-values-and-colors"></a>CMYK 值和色彩的宏

下列宏在操作 CMYK 值時很有用。



| 巨集                          | 描述                                                                  |
|--------------------------------|------------------------------------------------------------------------------|
| [**CMYK**](/windows/desktop/api/Wingdi/nf-wingdi-cmyk)           | 從個別的青色、洋紅、黃色和黑色值建立 CMYK 值。 |
| [**GetCValue**](/windows/desktop/api/Wingdi/nf-wingdi-getcvalue) | 從 CMYK 色彩值抓取青色色彩值。                      |
| [**GetKValue**](/windows/desktop/api/Wingdi/nf-wingdi-getkvalue) | 從 CMYK 色彩值抓取黑色色彩值。                     |
| [**GetMValue**](/windows/desktop/api/Wingdi/nf-wingdi-getmvalue) | 從 CMYK 色彩值抓取洋紅值。                         |
| [**GetYValue**](/windows/desktop/api/Wingdi/nf-wingdi-getyvalue) | 從 CMYK 色彩值抓取黃色的色彩值。                    |



 

下列宏會搭配色彩使用。



| 巨集                                | 描述                                                                                                                                           |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetBValue**](/windows/win32/api/wingdi/nf-wingdi-getbvalue)       | 取得 RGB 藍色值。                                                                                                                               |
| [**GetGValue**](/windows/win32/api/wingdi/nf-wingdi-getgvalue)       | 取得 RGB 綠值。                                                                                                                              |
| [**GetRValue**](/windows/win32/api/wingdi/nf-wingdi-getrvalue)       | 取得 RGB 紅色值。                                                                                                                                |
| [**調色盤索引**](/previous-versions//dd162770(v=vs.85)) | 接受邏輯色彩調色板專案的索引，並傳回檔色板輸入規範。                                                              |
| [**PALETTERGB**](/windows/win32/api/wingdi/nf-wingdi-palettergb)     | 接受代表紅色、綠色和藍色之相對濃度的三個值，並傳回與調色板相關的紅色、綠色、藍色 (RGB) 規範。 |
| [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb)                       | 根據提供的引數和輸出裝置的色彩功能，選取紅色、綠色、藍色 (RGB) 色彩。                               |



 

 

 