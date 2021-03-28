---
description: 本主題列出 Region 類別的函式。 如需完整的類別清單，請參閱 Region 類別。
ms.assetid: 94f4971c-defa-43e0-a0c0-4000557b0a5c
title: Region 函數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 98663587fab3722d689c9d34578d60daad922a2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115249"
---
# <a name="regionregion-constructors"></a>Region 函數

本主題列出 [**Region**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region) 類別的函式。 如需完整的類別清單，請參閱 **Region 類別**。

### <a name="overload-list"></a>多載清單



| 建構函式                                                                 | 描述                                                                                                                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**區域 (HRGN)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inhrgn))                  | 建立區域，該區域與 GDI 區域的控制碼所指定的區域相同。<br/>                                                                                       |
| [**區域 (Rect&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrect_))            | 建立由矩形定義的區域。<br/>                                                                                                                                      |
| [**區域 (RectF&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrectf_))          | 建立由矩形定義的區域。<br/>                                                                                                                                      |
| [**區域 (位元組 \* 、INT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstbyte_inint)) | 建立區域，該區域是由其他區域所取得的資料所定義。 <br/>                                                                                                               |
| [**區域 (GraphicsPath \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstgraphicspath))        | 建立一個區域，該區域是由 [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath)) 物件 (路徑所定義，且具有 **GraphicsPath** 物件中所含的填滿模式。<br/> |
| [**區域 ()**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(constregion_))                           | 建立無限的區域。 這是預設建構函式。 <br/>                                                                                                                  |



 

 
