---
title: 'how to 主題 (DirectWrite) '
description: 請參閱 DirectWrite API 程式設計指南中的「如何」主題。 DirectWrite 可讓 Windows 應用程式增強 UI 和檔的文字體驗。
ms.assetid: da4817ee-0bff-433f-b595-4250199bcc14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42848fbf00e099926763f0db54338f3a87ff583782b939f8250a1aabb2b73ca5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048858"
---
# <a name="how-to-topics-directwrite"></a>how to 主題 (DirectWrite) 

下列主題提供[DirectWrite](direct-write-portal.md) API 的總覽。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                                                                   | 描述                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [如何對齊文字](how-to-align-text.md)<br/>                                                                                                                   | 您可以使用 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)介面的 [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment)方法來對齊 [DirectWrite](direct-write-portal.md)文字<br/>                                                                                                                                                                                                               |
| [如何新增多個監視器的支援](how-to-add-support-for-multiple-monitors.md)<br/>                                                                     | [DirectWrite](direct-write-portal.md)包含多個監視器的系統支援。 不同的監視器可能會有不同的圖元幾何 (RGB、BGR 或平面) 或其他屬性。 如需圖元幾何的詳細資訊，請參閱 [**DWRITE \_ 圖元 \_ 幾何**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) 參考主題。 本主題將說明如何將多個監視器的支援新增至您的 DirectWrite 應用程式。 <br/> |
| [如何確保您的應用程式在高 DPI 顯示器上正確顯示](how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays.md)<br/> | 描述如何建立在高 DPI 顯示器上適當顯示的視窗。<br/>                                                                                                                                                                                                                                                                                                                                               |
| [如何以正確的閱讀方向來確保文字顯示](how-to-ensure-text-is-displayed-with-the-correct-reading-direction.md)<br/>                 | 某些語言（例如阿拉伯文和希伯來文）需要由右至左的閱讀方向。 [DirectWrite](direct-write-portal.md)文字格式物件的，預設的閱讀方向是由左至右。 DirectWrite 不會自動從地區設定推斷讀取方向，因此您必須自行進行。<br/>                                                                                                   |
| [如何列舉字型](font-enumeration.md)<br/>                                                                                                               | 本總覽將示範如何依系列名稱列舉系統字型集合中的字型。<br/>                                                                                                                                                                                                                                                                                                                          |
| [如何針對文字版面配置執行點擊測試](how-to-perform-hit-testing-on-a-text-layout.md)<br/>                                                               | 提供簡短的教學課程，說明如何使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)介面將點擊測試新增至顯示文字的 [DirectWrite](direct-write-portal.md)應用程式。 <br/>                                                                                                                                                                                                                  |
| [如何將内嵌物件加入至文字版面配置](how-to-add-inline-objects-to-a-text-layout.md)<br/>                                                                 | 提供簡短的教學課程，說明如何在使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)介面顯示文字的 [DirectWrite](direct-write-portal.md)應用程式中加入内嵌物件。 <br/>                                                                                                                                                                                                                         |
| [如何將用戶端繪製效果新增至文字版面配置](how-to-add-custom-drawing-efffects-to-a-text-layout.md)<br/>                                                | 提供簡短的教學課程，說明如何將用戶端繪製效果新增至 [DirectWrite](direct-write-portal.md)應用程式，以使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)介面和自訂文字轉譯器來顯示文字。 <br/>                                                                                                                                                                                      |



 

 

