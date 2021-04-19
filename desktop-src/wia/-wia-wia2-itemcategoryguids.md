---
description: Windows 映像取得 (WIA) 2.0 專案會分組為類別，以定義如何處理或使用 IWiaItem2。
ms.assetid: 927f4957-aedf-4eef-8892-91cf9b56e1a2
title: 'WIA 2.0 專案類別目錄 Guid (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CATEGORY_AUTO
- WIA_CATEGORY_FEEDER
- WIA_CATEGORY_FEEDER_BACK
- WIA_CATEGORY_FEEDER_FRONT
- WIA_CATEGORY_FILM
- WIA_CATEGORY_FINISHED_FILE
- WIA_CATEGORY_FLATBED
- WIA_CATEGORY_FOLDER
- WIA_CATEGORY_ROOT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: e2785d7d82e28641ebeefad730f02b3561a537a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966722"
---
# <a name="wia-20-item-category-guids"></a>WIA 2.0 專案類別目錄 Guid

Windows 映像取得 (WIA) 2.0 專案會分組為類別，以定義如何處理或使用 [**IWiaItem2**](-wia-iwiaitem2.md) 。 例如，如果專案代表送紙器，則應用程式應該會預期它包含所需的檔送紙器屬性，並如同檔輸送器般運作。 如果專案代表已完成的檔案，則 WIA 2.0 應用程式應該以這種方式處理，並假設資料是靜態的，而且位於裝置上。  (每個專案的規則都會在其個別規格檔中定義。 ) 每個類別都有 GUID 類型常數。



| 常數                                                                                                                                                                                               | 描述                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_CATEGORY_AUTO"></span><span id="wia_category_auto"></span><dl> <dt>**WIA \_ 類別 \_ AUTO**</dt> </dl>                             | 代表支援自動設定掃描之 WIA 2.0 掃描器裝置自動設定設定的專案。<br/>                                   |
| <span id="WIA_CATEGORY_FEEDER"></span><span id="wia_category_feeder"></span><dl> <dt>**WIA \_ 類別 \_ 送紙器**</dt> </dl>                       | 這是可程式化資料來源的送紙器專案，並遵循支援檔送紙器所需的標準規則和屬性集。<br/>                             |
| <span id="WIA_CATEGORY_FEEDER_BACK"></span><span id="wia_category_feeder_back"></span><dl> <dt>**WIA \_ 類別 \_ 送 \_ 回送回**</dt> </dl>       | 描述雙工基底送紙器專案的後端資料來源的可程式化資料來源。<br/>                                                                       |
| <span id="WIA_CATEGORY_FEEDER_FRONT"></span><span id="wia_category_feeder_front"></span><dl> <dt>**WIA \_ 類別 \_ 送紙器 \_ 正面**</dt> </dl>    | 描述雙工基底送紙器專案之前端資料來源的可程式化資料來源。<br/>                                                                      |
| <span id="WIA_CATEGORY_FILM"></span><span id="wia_category_film"></span><dl> <dt>**WIA \_ 類別 \_ 膠捲**</dt> </dl>                             | 這是可程式化資料來源的電影專案，並遵循支援膠捲掃描單位所需的標準規則和屬性集。<br/>                            |
| <span id="WIA_CATEGORY_FINISHED_FILE"></span><span id="wia_category_finished_file"></span><dl> <dt>**WIA \_ 類別 \_ 已完成檔案 \_**</dt> </dl> | 不是可程式化資料來源的專案，或以完成檔案格式提供資料的專案，或包含已完成檔案格式專案的資料夾專案。<br/> |
| <span id="WIA_CATEGORY_FLATBED"></span><span id="wia_category_flatbed"></span><dl> <dt>**WIA \_ 類別的 \_ 平板**</dt> </dl>                    | 平板專案，它是可程式化的資料來源，並遵循支援平板影印掃描所需的標準規則和屬性集。<br/>                     |
| <span id="WIA_CATEGORY_FOLDER"></span><span id="wia_category_folder"></span><dl> <dt>**WIA \_ 類別 \_ 目錄資料夾**</dt> </dl>                       | 資料夾儲存專案 (不是可程式化的資料來源，) 包含其他資料夾專案或完成的檔案或兩者。<br/>                                                     |
| <span id="WIA_CATEGORY_ROOT"></span><span id="wia_category_root"></span><dl> <dt>**WIA \_ 類別 \_ 根目錄**</dt> </dl>                             | 裝置的根專案。 <br/>                                                                                                                                      |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wiadef。h</dt> </dl> |



 

 




