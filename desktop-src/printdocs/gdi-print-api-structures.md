---
description: GDI 列印 API 結構
ms.assetid: 7753a54d-5136-4e46-a5ba-024bcfb961dc
title: GDI 列印 API 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5af0087ed47123b29d6712df2c842a7f05c0d77997df7c3049cc42e0677a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971467"
---
# <a name="gdi-print-api-structures"></a>GDI 列印 API 結構

## <a name="in-this-section"></a>本節內容



| 結構                                                      | 描述                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**版**](/windows/win32/api/wingdi/ns-wingdi-devmodea)<br/>                          | [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)資料結構包含有關印表機或顯示裝置之初始化和環境的資訊。 <br/>                                                                                                              |
| [**DOCINFO**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa)<br/>                          | [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa)結構包含 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)函數所使用的輸入和輸出檔案名以及其他資訊。<br/>                                                                                                  |
| [**DRAWPATRECT**](/windows/desktop/api/Wingdi/ns-wingdi-drawpatrect)<br/>                  | [**DRAWPATRECT**](/windows/desktop/api/wingdi/ns-wingdi-drawpatrect)結構會定義要建立的矩形。<br/>                                                                                                                                                                         |
| [**PSFEATURE \_ CUSTPAPER**](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_custpaper)<br/> | [**PSFEATURE \_ CUSTPAPER**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_custpaper)結構包含 PostScript 驅動程式之自訂紙張大小的相關資訊。 此結構可搭配 [**GET \_ PS \_ FEATURESETTING**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)) 印表機 escape 函式使用。<br/> |
| [**PSFEATURE \_ 輸出**](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_output)<br/>       | [**PSFEATURE \_ 輸出**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_output)結構包含 PostScript 驅動程式輸出選項的相關資訊。 此結構可搭配 [**GET \_ PS \_ FEATURESETTING**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)) 印表機 escape 函式使用。<br/>                  |
| [**PSINJECTDATA**](/windows/desktop/api/Wingdi/ns-wingdi-psinjectdata)<br/>                | [**PSINJECTDATA**](/windows/desktop/api/wingdi/ns-wingdi-psinjectdata)結構是搭配 [**POSTSCRIPT \_ 插入**](/previous-versions/windows/desktop/legacy/dd162830(v=vs.85))印表機 escape 函式使用之輸入緩衝區的標頭。<br/>                                                                            |



 

 

