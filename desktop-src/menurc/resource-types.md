---
title: '資源類型 (Winuser .h) '
description: 以下是預先定義的資源類型。
ms.assetid: 8d27f79a-8165-4565-a975-f25b2344efdc
topic_type:
- apiref
api_name:
- RT_ACCELERATOR
- RT_ANICURSOR
- RT_ANIICON
- RT_BITMAP
- RT_CURSOR
- RT_DIALOG
- RT_DLGINCLUDE
- RT_FONT
- RT_FONTDIR
- RT_GROUP_CURSOR
- RT_GROUP_ICON
- RT_HTML
- RT_ICON
- RT_MANIFEST
- RT_MENU
- RT_MESSAGETABLE
- RT_PLUGPLAY
- RT_RCDATA
- RT_STRING
- RT_VERSION
- RT_VXD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cd11856ea1e500425a2d9767dd144ebc9f5e31f583cd07961376aba0ef585b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687152"
---
# <a name="resource-types"></a>資源類型

以下是預先定義的資源類型。



| 常數/值                                                                                                                                                                                                                                                           | 描述                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RT_ACCELERATOR"></span><span id="rt_accelerator"></span><dl> <dt>**RT \_加速器**</dt> <dt>MAKEINTRESOURCE (9)</dt> </dl>                                 | 快速鍵對應表。<br/>                                                                                                                                                                                                                                                                    |
| <span id="RT_ANICURSOR"></span><span id="rt_anicursor"></span><dl> <dt>**RT \_ANICURSOR**</dt> <dt>MAKEINTRESOURCE (21)</dt> </dl>                                      | 動畫游標。<br/>                                                                                                                                                                                                                                                                      |
| <span id="RT_ANIICON"></span><span id="rt_aniicon"></span><dl> <dt>**RT \_ANIICON**</dt> <dt>MAKEINTRESOURCE (22)</dt> </dl>                                            | 動畫圖標。<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_BITMAP"></span><span id="rt_bitmap"></span><dl> <dt>**RT \_點陣圖**</dt> <dt>MAKEINTRESOURCE (2)</dt> </dl>                                                | 點陣圖資源。<br/>                                                                                                                                                                                                                                                                      |
| <span id="RT_CURSOR"></span><span id="rt_cursor"></span><dl> <dt>**RT \_資料指標**</dt> <dt>MAKEINTRESOURCE (1)</dt> </dl>                                                | 硬體相依的資料指標資源。<br/>                                                                                                                                                                                                                                                   |
| <span id="RT_DIALOG"></span><span id="rt_dialog"></span><dl> <dt>**RT \_對話方塊**</dt> <dt>MAKEINTRESOURCE (5)</dt> </dl>                                                | 對話方塊。<br/>                                                                                                                                                                                                                                                                           |
| <span id="RT_DLGINCLUDE"></span><span id="rt_dlginclude"></span><dl> <dt>**RT \_DLGINCLUDE**</dt> <dt>MAKEINTRESOURCE (17)</dt> </dl>                                   | 允許資源編輯工具將字串與 .rc 檔產生關聯。 一般而言，此字串是提供符號名稱的標頭檔名稱。 資源編譯器會剖析字串，否則會忽略值。 例如 <br/> `1 DLGINCLUDE "MyFile.h"`<br/> |
| <span id="RT_FONT"></span><span id="rt_font"></span><dl> <dt>**RT \_字型**</dt> <dt>MAKEINTRESOURCE (8)</dt> </dl>                                                      | 字型資源。<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_FONTDIR"></span><span id="rt_fontdir"></span><dl> <dt>**RT \_FONTDIR**</dt> <dt>MAKEINTRESOURCE (7)</dt> </dl>                                             | 字型目錄資源。<br/>                                                                                                                                                                                                                                                              |
| <span id="RT_GROUP_CURSOR"></span><span id="rt_group_cursor"></span><dl> <dt>**RT \_群組資料 \_ 指標**</dt> <dt>MAKEINTRESOURCE ( (ULONG \_ PTR)  (RT \_ 游標) + 11)</dt> </dl> | 硬體獨立的資料指標資源。<br/>                                                                                                                                                                                                                                                 |
| <span id="RT_GROUP_ICON"></span><span id="rt_group_icon"></span><dl> <dt>**RT \_群組 \_ 圖示**</dt> <dt>MAKEINTRESOURCE ( (ULONG \_ PTR)  (RT \_ 圖示) + 11)</dt> </dl>         | 硬體獨立的圖示資源。<br/>                                                                                                                                                                                                                                                   |
| <span id="RT_HTML"></span><span id="rt_html"></span><dl> <dt>**RT \_HTML**</dt> <dt>MAKEINTRESOURCE (23)</dt> </dl>                                                     | HTML 資源。<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_ICON"></span><span id="rt_icon"></span><dl> <dt>**RT \_圖示**</dt> <dt>MAKEINTRESOURCE (3)</dt> </dl>                                                      | 硬體相依的圖示資源。<br/>                                                                                                                                                                                                                                                     |
| <span id="RT_MANIFEST"></span><span id="rt_manifest"></span><dl> <dt>**RT \_資訊清單**</dt> <dt>MAKEINTRESOURCE (24)</dt> </dl>                                         | 並存組件資訊清單。<br/>                                                                                                                                                                                                                                                       |
| <span id="RT_MENU"></span><span id="rt_menu"></span><dl> <dt>**RT \_功能表**</dt> <dt>MAKEINTRESOURCE (4)</dt> </dl>                                                      | 功能表資源。<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_MESSAGETABLE"></span><span id="rt_messagetable"></span><dl> <dt>**RT \_MESSAGETABLE**</dt> <dt>MAKEINTRESOURCE (11)</dt> </dl>                             | 訊息資料表專案。<br/>                                                                                                                                                                                                                                                                  |
| <span id="RT_PLUGPLAY"></span><span id="rt_plugplay"></span><dl> <dt>**RT \_PLUGPLAY**</dt> <dt>MAKEINTRESOURCE (19)</dt> </dl>                                         | 隨插即用資源。<br/>                                                                                                                                                                                                                                                               |
| <span id="RT_RCDATA"></span><span id="rt_rcdata"></span><dl> <dt>**RT \_RCDATA**</dt> <dt>MAKEINTRESOURCE (10)</dt> </dl>                                               | 應用程式定義的資源 (原始資料) 。<br/>                                                                                                                                                                                                                                              |
| <span id="RT_STRING"></span><span id="rt_string"></span><dl> <dt>**RT \_字串**</dt> <dt>MAKEINTRESOURCE (6)</dt> </dl>                                                | 字串資料表專案。<br/>                                                                                                                                                                                                                                                                   |
| <span id="RT_VERSION"></span><span id="rt_version"></span><dl> <dt>**RT \_版本**</dt> <dt>MAKEINTRESOURCE (16)</dt> </dl>                                            | 版本資源。<br/>                                                                                                                                                                                                                                                                     |
| <span id="RT_VXD"></span><span id="rt_vxd"></span><dl> <dt>**RT \_VXD**</dt> <dt>MAKEINTRESOURCE (20)</dt> </dl>                                                        | VXD。<br/>                                                                                                                                                                                                                                                                                  |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Winuser。h</dt> </dl> |



 

 





