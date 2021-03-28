---
description: 本主題列出字型類別的函式。 如需完整的類別清單，請參閱字型類別。
ms.assetid: a0169751-50f6-41d9-bd59-3c85aec1bb78
title: 字型. 字型函式
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: bdf533e292734956c02d3f8a424ca619cb722c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194989"
---
# <a name="fontfont-constructors"></a>字型. 字型函式

本主題列出 [**字型**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) 類別的函式。 如需完整的類別清單，請參閱 **字型類別**。

### <a name="overload-list"></a>多載清單



| 建構函式                                                                                                                   | 描述                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**字型 (HDC、HFONT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont))                                                                | 使用 GDI **LOGFONT** 結構的控制碼，間接地從 gdi 邏輯字型建立 [**字型：： font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont))物件。<br/>                                                                                                                                   |
| [**字型 (HDC、LOGFONTA \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta))                                            | 直接從 GDI 邏輯字型建立 [**字型：： font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta)) 物件。 GDI 邏輯字型是 **LOGFONTA** 結構，也就是邏輯字型的單一位元組字元版本。 提供此函式的目的是為了與 GDI 相容。<br/> |
| [**字型 (HDC、LOGFONTW \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw))                                            | 直接從 GDI 邏輯字型建立 [**字型：： font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw)) 物件。 GDI 邏輯字型是 **LOGFONTW** 結構，也就是邏輯字型的寬字元版本。 提供此函式的目的是為了與 GDI 相容。<br/>     |
| [**字型 (FontFamily \* 、REAL、INT、Unit)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit))                                | 根據 [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)物件、大小、字型樣式和度量單位，建立 [**字型：： font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit))物件。<br/>                                                                               |
| [**字型 (WCHAR \* 、REAL、INT、Unit、FontCollection \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) | 根據字型系列、大小、字型樣式、測量單位和 [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection)物件，建立 [**Font：： font-family**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection))物件。<br/>                                     |
| [**字型 (HDC)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc))                                                                            | 根據目前選取到指定之裝置內容中的 GDI 字型物件，建立 [**font：： font-family**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc)) 物件。 提供此函式的目的是為了與 GDI 相容。 <br/>                                                                           |



 

 
