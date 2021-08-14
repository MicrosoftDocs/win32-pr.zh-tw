---
title: 在裝置內容中使用的基本函數
description: 下列 WCS 函數會在裝置內容中提供基本的色彩對應功能。 這些應用程式對於所有需要以低額外負荷來執行色彩管理的應用程式，以及最少的使用者介入都很有用。
ms.assetid: 199fac5e-daba-4aa3-a631-bb1eb2270b2e
keywords:
- Windows色彩系統 (WCS) ，函數
- WCS (Windows 色彩系統) ，函數
- 影像色彩管理，函數
- 色彩管理，函數
- 色彩，函數
- WCS 參考，函數
- WCS、函數的參考
- Windows色彩系統 (WCS) 、裝置內容
- WCS (Windows 色彩系統) 、裝置內容
- 影像色彩管理、裝置內容
- 色彩管理，裝置內容
- 色彩、裝置內容
- WCS 參考，裝置內容
- WCS、裝置內容的參考
- 裝置內容
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a934c1737a7eea8b32a9589325e73300db82334a40ee47b411922b89cb61f568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118210977"
---
# <a name="basic-functions-for-use-within-a-device-context"></a>在裝置內容中使用的基本函數

下列 WCS 函數會在裝置內容中提供基本的 [色彩對應](c.md) 功能。 這些應用程式對於所有需要以低額外負荷來執行色彩管理的應用程式，以及最少的使用者介入都很有用。



| 函式                                                           | 描述                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckColorsInGamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                   | 檢查指定的色彩是否在裝置的範圍中。                                                                                                     |
| [**ColorCorrectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                 | 更正裝置內容之調色板中的專案。                                                                                             |
| [**ColorMatchToTarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                   | 針對預覽用途執行色彩對應。                                                                                                        |
| [**CreateColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                       | 建立色彩空間。                                                                                                                              |
| [**DeleteColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                       | 刪除色彩空間。                                                                                                                              |
| [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                         | 列舉適用于指定之裝置內容的輸出色彩設定檔。                                                                              |
| [**EnumICMProfilesProcCallback**](/windows/desktop/api/Wingdi/) | [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)的應用程式定義回呼函數。 這個函式的名稱也是由應用程式所定義。 |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | 取得裝置內容中目前的輸入色彩空間。 |
| [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                             | 取得裝置內容目前的輸出色彩設定檔。                                                                                          |
| [**GetLogColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                       | 取得裝置內容的 [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) 結構。                                                                      |
| [**SetColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                             | 設定裝置內容的輸入色彩空間。                                                                                                          |
| [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                   | 在裝置內容中開啟或關閉色彩管理。                                                                                               |
| [**SetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                             | 設定指定之裝置內容的輸出色彩設定檔。                                                                                           |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)               | 列舉符合指定設定檔管理範圍中的列舉準則的所有色彩設定檔。                                      |



 

 

 




