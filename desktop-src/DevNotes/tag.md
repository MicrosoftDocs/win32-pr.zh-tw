---
description: 識別填充碼資料庫中的專案。
ms.assetid: c092592d-a4f4-4b2f-9b03-c07951ed214a
title: '標記 (Exposeenums2managed .h) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacbd3c8d29e1f41d7aaabc989848c561415ae4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990790"
---
# <a name="tag"></a>標記

識別填充碼資料庫中的專案。

下列專案是 **標記 \_ 類型 \_ 清單** (0x7000) 的類型。



| 常數/值                                                                                                                                                                                                                                                             | Description                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| <span id="TAG_DATABASE"></span><span id="tag_database"></span><dl> <dt>**標記 \_資料庫**</dt> <dt> (0x1 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                               | 資料庫專案。<br/>                                                |
| <span id="TAG_LIBRARY"></span><span id="tag_library"></span><dl> <dt>**標記 \_程式庫**</dt> <dt> (0x2 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                                  | 程式庫專案。<br/>                                                 |
| <span id="TAG_INEXCLUDE"></span><span id="tag_inexclude"></span><dl> <dt>**標記 \_INEXCLUDE**</dt> <dt> (0x3 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                            | 包含與排除專案。<br/>                                     |
| <span id="TAG_SHIM"></span><span id="tag_shim"></span><dl> <dt>**標記 \_填充碼**</dt> <dt> (0x4 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                                           | 包含名稱和用途資訊的填充碼專案。<br/>     |
| <span id="TAG_PATCH"></span><span id="tag_patch"></span><dl> <dt>**標記 \_PATCH**</dt> <dt> (0x5 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                                        | 包含記憶體中修補資訊的 Patch 專案。<br/>  |
| <span id="TAG_APP"></span><span id="tag_app"></span><dl> <dt>**標記 \_應用程式**</dt> <dt> (0x6 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                                              | 應用程式專案。<br/>                                             |
| <span id="TAG_EXE"></span><span id="tag_exe"></span><dl> <dt>**標記 \_EXE**</dt> <dt> (0x7 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                                              | 可執行檔專案。<br/>                                              |
| <span id="TAG_MATCHING_FILE"></span><span id="tag_matching_file"></span><dl> <dt>**標記 \_相符 \_**</dt>的檔案 <dt> (0x8 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>               | 相符的檔案專案。<br/>                                           |
| <span id="TAG_SHIM_REF"></span><span id="tag_shim_ref"></span><dl> <dt>**標記 \_填充碼 \_ 參考**</dt> <dt> (0x9 \| 標記 \_ 類型 \_ 清單)</dt> </dl>                                   | 填充碼定義專案。<br/>                                         |
| <span id="TAG_PATCH_REF"></span><span id="tag_patch_ref"></span><dl> <dt>**標記 \_PATCH \_ REF**</dt> <dt> (0xA \| **TAG \_ TYPE \_ LIST**)</dt> </dl>                           | 修補定義專案。<br/>                                        |
| <span id="TAG_LAYER"></span><span id="tag_layer"></span><dl> <dt>**標記 \_圖層**</dt> <dt> (0xB \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                                        | 圖層填充碼專案。<br/>                                              |
| <span id="TAG_FILE"></span><span id="tag_file"></span><dl> <dt>**標記 \_FILE**</dt> <dt> (0xC \| **TAG \_ TYPE \_ LIST**)</dt> </dl>                                           | 填充碼專案中使用的檔案屬性。<br/>                           |
| <span id="TAG_APPHELP"></span><span id="tag_apphelp"></span><dl> <dt>**標記 \_APPHELP**</dt> <dt> (0xD \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                                  | Apphelp 資訊專案。<br/>                                     |
| <span id="TAG_LINK"></span><span id="tag_link"></span><dl> <dt>**標記 \_連結**</dt> <dt> (0xE \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                                           | Apphelp online 連結資訊專案。<br/>                         |
| <span id="TAG_DATA"></span><span id="tag_data"></span><dl> <dt>**標記 \_資料**</dt> <dt> (0xF \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                                           | 名稱值對應專案。<br/>                                      |
| <span id="TAG_MSI_TRANSFORM"></span><span id="tag_msi_transform"></span><dl> <dt>**標記 \_MSI \_ 轉換**</dt> <dt> (0x10 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>              | MSI 轉換專案。<br/>                                      |
| <span id="TAG_MSI_TRANSFORM_REF"></span><span id="tag_msi_transform_ref"></span><dl> <dt>**標記 \_MSI \_ 轉換 \_ 參考**</dt> <dt> (0x11 \| **標記 \_ 類型 \_ 清單**)</dt> </dl> | MSI 轉換定義專案。<br/>                           |
| <span id="TAG_MSI_PACKAGE"></span><span id="tag_msi_package"></span><dl> <dt>**標記 \_MSI \_ 套件**</dt> <dt> (0x12 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                    | MSI 封裝專案。<br/>                                             |
| <span id="TAG_FLAG"></span><span id="tag_flag"></span><dl> <dt>**標記 \_旗**</dt>標 <dt> (0x13 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                                          | 旗標專案。<br/>                                                    |
| <span id="TAG_MSI_CUSTOM_ACTION"></span><span id="tag_msi_custom_action"></span><dl> <dt>**標記 \_MSI \_ 自訂 \_ 動作**</dt> <dt> (0x14 \| **標記 \_ 類型 \_ 清單**)</dt> </dl> | MSI 自訂動作專案。<br/>                                       |
| <span id="TAG_FLAG_REF"></span><span id="tag_flag_ref"></span><dl> <dt>**標記 \_旗標 \_ REF**</dt> <dt> (0x15 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                             | 旗標定義專案。<br/>                                         |
| <span id="TAG_ACTION"></span><span id="tag_action"></span><dl> <dt>**標記 \_動作**</dt> <dt> (0x16 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                                    | 未使用的。<br/>                                                        |
| <span id="TAG_LOOKUP"></span><span id="tag_lookup"></span><dl> <dt>**標記 \_查閱**</dt> <dt> (0x17 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                                    | 用於查閱驅動程式資料庫的查閱專案。<br/>             |
| <span id="TAG_STRINGTABLE"></span><span id="tag_stringtable"></span><dl> <dt>**標記 \_STRINGTABLE**</dt> <dt> (0x801 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                    | 字串資料表專案。<br/>                                            |
| <span id="TAG_INDEXES"></span><span id="tag_indexes"></span><dl> <dt>**標記 \_索引**</dt> <dt> (0x802 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                                | 在填充碼資料庫中定義所有索引的索引項目。<br/> |
| <span id="TAG_INDEX"></span><span id="tag_index"></span><dl> <dt>**標記 \_索引**</dt> <dt> (0x803 \| **標記 \_ 類型 \_ 清單**)</dt> </dl>                                      | 在填充碼資料庫中定義索引的索引項目。<br/>          |



下列專案的類型為 **TAG \_ type \_ STRINGREF** (0x6000) 。



| 常數/值                                                                                                                                                                                                                                                                     | Description                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="TAG_NAME"></span><span id="tag_name"></span><dl> <dt>**標記 \_名稱**</dt> <dt> (0x1 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                                              | Name 屬性。<br/>                                                                    |
| <span id="TAG_DESCRIPTION"></span><span id="tag_description"></span><dl> <dt>**標記 \_描述**</dt> <dt> (0x2 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                         | 描述專案。<br/>                                                                 |
| <span id="TAG_MODULE"></span><span id="tag_module"></span><dl> <dt>**標記 \_MODULE**</dt> <dt> (0x3 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                                        | Module 屬性。<br/>                                                                  |
| <span id="TAG_API"></span><span id="tag_api"></span><dl> <dt>**標記 \_API**</dt> <dt> (0x4 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                                                 | API 專案。<br/>                                                                         |
| <span id="TAG_VENDOR"></span><span id="tag_vendor"></span><dl> <dt>**標記 \_廠商**</dt> <dt> (0x5 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                                        | 廠商名稱屬性。<br/>                                                             |
| <span id="TAG_APP_NAME"></span><span id="tag_app_name"></span><dl> <dt>**標記 \_應用程式 \_ 名稱**</dt> <dt> (0x6 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                                 | 描述填充碼資料庫中應用程式專案的應用程式名稱屬性。<br/> |
| <span id="TAG_COMMAND_LINE"></span><span id="tag_command_line"></span><dl> <dt>**標記 \_命令 \_ 行**</dt> <dt> (0x8 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                     | 例如，將引數傳遞給填充碼時，所使用的命令列屬性。<br/> |
| <span id="TAG_COMPANY_NAME"></span><span id="tag_company_name"></span><dl> <dt>**標記 \_公司 \_ 名稱**</dt> <dt> (0x9 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                     | 公司名稱屬性。<br/>                                                            |
| <span id="TAG_DLLFILE"></span><span id="tag_dllfile"></span><dl> <dt>**標記 \_DLLFILE**</dt> <dt> (0xA \| **TAG \_ TYPE \_ STRINGREF**)</dt> </dl>                                     | 填充碼專案的 DLL 檔案屬性。<br/>                                               |
| <span id="TAG_WILDCARD_NAME"></span><span id="tag_wildcard_name"></span><dl> <dt>**標記 \_萬用字元 \_ 名稱**</dt> <dt> (0xB \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                  | 以萬用字元做為檔案名的可執行專案之萬用字元名稱屬性。<br/>  |
| <span id="TAG_PRODUCT_NAME"></span><span id="tag_product_name"></span><dl> <dt>**標記 \_產品 \_ 名稱**</dt> <dt> (0x10 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                    | 產品名稱屬性。<br/>                                                            |
| <span id="TAG_PRODUCT_VERSION"></span><span id="tag_product_version"></span><dl> <dt>**標記 \_產品 \_ 版本**</dt> <dt> (0x11 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>           | Product version 屬性。<br/>                                                         |
| <span id="TAG_FILE_DESCRIPTION"></span><span id="tag_file_description"></span><dl> <dt>**標記 \_檔案 \_ 描述**</dt> <dt> (0x12 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>        | 檔案 description 屬性。<br/>                                                        |
| <span id="TAG_FILE_VERSION"></span><span id="tag_file_version"></span><dl> <dt>**標記 \_檔案 \_ 版本**</dt> <dt> (0x13 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                    | 檔案版本屬性。<br/>                                                            |
| <span id="TAG_ORIGINAL_FILENAME"></span><span id="tag_original_filename"></span><dl> <dt>**標記 \_原始 \_ 檔案名**</dt> <dt> (0x14 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>     | 原始檔案名稱屬性。<br/>                                                      |
| <span id="TAG_INTERNAL_NAME"></span><span id="tag_internal_name"></span><dl> <dt>**標記 \_內部 \_ 名稱**</dt> <dt> (0x15 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                 | 內部檔案名屬性。<br/>                                                      |
| <span id="TAG_LEGAL_COPYRIGHT"></span><span id="tag_legal_copyright"></span><dl> <dt>**標記 \_法律 \_ 著作權**</dt> <dt> (0x16 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>           | 著作權屬性。<br/>                                                               |
| <span id="TAG_16BIT_DESCRIPTION"></span><span id="tag_16bit_description"></span><dl> <dt>**標記 \_ 16BIT \_ 描述**</dt> <dt> (0x17 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>     | 16位 description 屬性。<br/>                                                      |
| <span id="TAG_APPHELP_DETAILS"></span><span id="tag_apphelp_details"></span><dl> <dt>**標記 \_APPHELP \_ 詳細資料**</dt> <dt> (0x18 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>           | Apphelp 詳細資料訊息資訊屬性。<br/>                                     |
| <span id="TAG_LINK_URL"></span><span id="tag_link_url"></span><dl> <dt>**標記 \_連結 \_ URL**</dt> <dt> (0x19 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                                | Apphelp online 連結 URL 屬性。<br/>                                                 |
| <span id="TAG_LINK_TEXT"></span><span id="tag_link_text"></span><dl> <dt>**標記 \_連結 \_ 文字**</dt> <dt> (0x1A \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                             | Apphelp online link text 屬性。<br/>                                                |
| <span id="TAG_APPHELP_TITLE"></span><span id="tag_apphelp_title"></span><dl> <dt>**標記 \_APPHELP \_ 標題**</dt> <dt> (0x1b \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                 | Apphelp 標題屬性。<br/>                                                           |
| <span id="TAG_APPHELP_CONTACT"></span><span id="tag_apphelp_contact"></span><dl> <dt>**標記 \_APPHELP \_ CONTACT**</dt> <dt> (0x1C \| **TAG \_ TYPE \_ STRINGREF**)</dt> </dl>           | Apphelp 廠商連絡人屬性。<br/>                                                  |
| <span id="TAG_SXS_MANIFEST"></span><span id="tag_sxs_manifest"></span><dl> <dt>**標記 \_SXS \_ 資訊清單**</dt> <dt> (bugcheck 0x1d \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                    | 並存資訊清單專案。<br/>                                                       |
| <span id="TAG_DATA_STRING"></span><span id="tag_data_string"></span><dl> <dt>**標記 \_資料 \_ 字串**</dt> <dt> (0x1E \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                       | 資料輸入的字串屬性。<br/>                                                 |
| <span id="TAG_MSI_TRANSFORM_FILE"></span><span id="tag_msi_transform_file"></span><dl> <dt>**標記 \_MSI \_ 轉換 \_**</dt>檔案 <dt> (0x1F \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl> | MSI 轉換專案的檔案名屬性。<br/>                                |
| <span id="TAG_16BIT_MODULE_NAME"></span><span id="tag_16bit_module_name"></span><dl> <dt>**標記 \_ 16BIT \_ 模組 \_ 名稱**</dt> <dt> (0x20 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>    | 16位模組名稱屬性。<br/>                                                      |
| <span id="TAG_LAYER_DISPLAYNAME"></span><span id="tag_layer_displayname"></span><dl> <dt>**標記 \_圖層 \_ DISPLAYNAME**</dt> <dt> (0x21 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>     | 未使用的。<br/>                                                                            |
| <span id="TAG_COMPILER_VERSION"></span><span id="tag_compiler_version"></span><dl> <dt>**標記 \_編譯器 \_ 版本**</dt> <dt> (0x22 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>        | 填充碼資料庫編譯器版本。<br/>                                                    |
| <span id="TAG_ACTION_TYPE"></span><span id="tag_action_type"></span><dl> <dt>**標記 \_動作 \_ 類型**</dt> <dt> (0x23 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                       | 未使用的。<br/>                                                                            |
| <span id="TAG_EXPORT_NAME"></span><span id="tag_export_name"></span><dl> <dt>**標記 \_匯出 \_ 名稱**</dt> <dt> (0x24 \| **標記 \_ 類型 \_ STRINGREF**)</dt> </dl>                       | 匯出檔案名屬性。<br/>                                                        |



下列專案是 **標記 \_ 類型 \_ DWORD** (0x4000) 的類型。



| 常數/值                                                                                                                                                                                                                                                                    | Description                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| <span id="TAG_SIZE"></span><span id="tag_size"></span><dl> <dt>**標記 \_大小**</dt> <dt> (0x1 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                                                 | 檔案大小屬性。<br/>                                                                                  |
| <span id="TAG_OFFSET"></span><span id="tag_offset"></span><dl> <dt>**標記 \_OFFSET**</dt> <dt> (0x2 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                                           | 未使用的。<br/>                                                                                               |
| <span id="TAG_CHECKSUM"></span><span id="tag_checksum"></span><dl> <dt>**標記 \_CHECKSUM**</dt> <dt> (0x3 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                                     | 檔案總和檢查碼屬性。<br/>                                                                              |
| <span id="TAG_SHIM_TAGID"></span><span id="tag_shim_tagid"></span><dl> <dt>**標記 \_填充碼 \_ TAGID**</dt> <dt> (0x4 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                              | 填充碼 **TAGID** 屬性。<br/>                                                                             |
| <span id="TAG_PATCH_TAGID"></span><span id="tag_patch_tagid"></span><dl> <dt>**標記 \_PATCH \_ TAGID**</dt> <dt> (0x5 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                           | 修補 **TAGID** 屬性。<br/>                                                                            |
| <span id="TAG_MODULE_TYPE"></span><span id="tag_module_type"></span><dl> <dt>**標記 \_模組 \_ 類型**</dt> <dt> (0x6 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                           | 模組類型屬性。<br/>                                                                                |
| <span id="TAG_VERDATEHI"></span><span id="tag_verdatehi"></span><dl> <dt>**標記 \_VERDATEHI**</dt> <dt> (0x7 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                                  | 檔案版本日期屬性的高序位部分。<br/>                                                |
| <span id="TAG_VERDATELO"></span><span id="tag_verdatelo"></span><dl> <dt>**標記 \_VERDATELO**</dt> <dt> (0x8 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                                  | 檔案版本日期屬性的低序位部分。<br/>                                                 |
| <span id="TAG_VERFILEOS"></span><span id="tag_verfileos"></span><dl> <dt>**標記 \_VERFILEOS**</dt> <dt> (0x9 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                                  | 作業系統 file version 屬性。<br/>                                                              |
| <span id="TAG_VERFILETYPE"></span><span id="tag_verfiletype"></span><dl> <dt>**標記 \_VERFILETYPE**</dt> <dt> (0xA \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                            | 檔案類型屬性。<br/>                                                                                  |
| <span id="TAG_PE_CHECKSUM"></span><span id="tag_pe_checksum"></span><dl> <dt>**標記 \_PE 總和 \_ 檢查**</dt>碼 <dt> (0xB \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                           | PE 檔案總和檢查碼屬性。<br/>                                                                           |
| <span id="TAG_PREVOSMAJORVER"></span><span id="tag_prevosmajorver"></span><dl> <dt>**標記 \_PREVOSMAJORVER**</dt> <dt> (0xC \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                   | 主要作業系統版本屬性。<br/>                                                             |
| <span id="TAG_PREVOSMINORVER"></span><span id="tag_prevosminorver"></span><dl> <dt>**標記 \_PREVOSMINORVER**</dt> <dt> (0xD \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                   | 次要 [作業系統版本] 屬性。<br/>                                                             |
| <span id="TAG_PREVOSPLATFORMID"></span><span id="tag_prevosplatformid"></span><dl> <dt>**標記 \_PREVOSPLATFORMID**</dt> <dt> (0xE \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>             | 作業系統平臺識別碼屬性。<br/>                                                       |
| <span id="TAG_PREVOSBUILDNO"></span><span id="tag_prevosbuildno"></span><dl> <dt>**標記 \_PREVOSBUILDNO**</dt> <dt> (0xF \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                      | 作業系統組建編號屬性。<br/>                                                              |
| <span id="TAG_PROBLEMSEVERITY"></span><span id="tag_problemseverity"></span><dl> <dt>**標記 \_PROBLEMSEVERITY**</dt> <dt> (0x10 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>               | Apphelp 專案的 Block 屬性。 這可判斷應用程式是不是固定的，還是已被軟封鎖。<br/> |
| <span id="TAG_LANGID"></span><span id="tag_langid"></span><dl> <dt>**標記 \_LANGID**</dt> <dt> (0x11 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                                          | Apphelp 專案的語言識別項。<br/>                                                              |
| <span id="TAG_VER_LANGUAGE"></span><span id="tag_ver_language"></span><dl> <dt>**標記 \_VER \_ LANGUAGE**</dt> <dt> (0x12 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>                       | 檔案的語言版本屬性。<br/>                                                                 |
| <span id="TAG_ENGINE"></span><span id="tag_engine"></span><dl> <dt>**標記 \_引擎**</dt> <dt> (0x14 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                                          | 未使用的。<br/>                                                                                               |
| <span id="TAG_HTMLHELPID"></span><span id="tag_htmlhelpid"></span><dl> <dt>**標記 \_HTMLHELPID**</dt> <dt> (0x15 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                              | Apphelp 專案的 Help identifier 屬性。<br/>                                                       |
| <span id="TAG_INDEX_FLAGS"></span><span id="tag_index_flags"></span><dl> <dt>**標記 \_索引 \_ 旗標**</dt> <dt> (0x16 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                          | 索引項目的旗標屬性。<br/>                                                                   |
| <span id="TAG_FLAGS"></span><span id="tag_flags"></span><dl> <dt>**標記 \_旗標**</dt> <dt> (0x17 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                                             | Apphelp 專案的旗標屬性。<br/>                                                                 |
| <span id="TAG_DATA_VALUETYPE"></span><span id="tag_data_valuetype"></span><dl> <dt>**標記 \_DATA \_ VALUETYPE**</dt> <dt> (0x18 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                 | 資料輸入的資料類型屬性。<br/>                                                                 |
| <span id="TAG_DATA_DWORD"></span><span id="tag_data_dword"></span><dl> <dt>**標記 \_資料 \_ dword**</dt> <dt> (0x19 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                             | 資料輸入的 **DWORD** 值屬性。<br/>                                                           |
| <span id="TAG_LAYER_TAGID"></span><span id="tag_layer_tagid"></span><dl> <dt>**標記 \_圖層 \_ TAGID**</dt> <dt> (0x1A \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                          | 圖層填充碼 **TAGID** 屬性。<br/>                                                                       |
| <span id="TAG_MSI_TRANSFORM_TAGID"></span><span id="tag_msi_transform_tagid"></span><dl> <dt>**標記 \_MSI \_ 轉換 \_ TAGID**</dt> <dt> (0x1b \| **標記 \_ 類型 \_ DWORD**)</dt> </dl> | MSI 轉換 **TAGID** 屬性。<br/>                                                                    |
| <span id="TAG_LINKER_VERSION"></span><span id="tag_linker_version"></span><dl> <dt>**標記 \_連結器 \_ 版本**</dt> <dt> (0x1C \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                 | 檔案的連結器版本屬性。<br/>                                                                   |
| <span id="TAG_LINK_DATE"></span><span id="tag_link_date"></span><dl> <dt>**標記 \_連結 \_ 日期**</dt> <dt> (bugcheck 0x1d \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                                | 檔案的連結日期屬性。<br/>                                                                        |
| <span id="TAG_UPTO_LINK_DATE"></span><span id="tag_upto_link_date"></span><dl> <dt>**標記 \_最高的 \_ 連結 \_ 日期**</dt> <dt> (0x1E \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                | 檔案的連結日期屬性。 比對會完成至，並包含這個連結日期。<br/>                   |
| <span id="TAG_OS_SERVICE_PACK"></span><span id="tag_os_service_pack"></span><dl> <dt>**標記 \_OS \_ SERVICE \_ PACK**</dt> <dt> (0x1F \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>             | 可執行檔專案的作業系統 service pack 屬性。<br/>                                      |
| <span id="TAG_FLAG_TAGID"></span><span id="tag_flag_tagid"></span><dl> <dt>**標記 \_旗標 \_ TAGID**</dt> <dt> (0x20 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                             | 旗標 **TAGID** 屬性。<br/>                                                                            |
| <span id="TAG_RUNTIME_PLATFORM"></span><span id="tag_runtime_platform"></span><dl> <dt>**標記 \_執行時間 \_ 平臺**</dt> <dt> (0x21 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>           | 檔案的執行時間平臺屬性。<br/>                                                                |
| <span id="TAG_OS_SKU"></span><span id="tag_os_sku"></span><dl> <dt>**標記 \_OS \_ SKU**</dt> <dt> (0x22 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                                         | 可執行檔專案的作業系統 SKU 屬性。<br/>                                               |
| <span id="TAG_OS_PLATFORM"></span><span id="tag_os_platform"></span><dl> <dt>**標記 \_OS \_ 平臺**</dt> <dt> (0x23 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                          | 作業系統平臺屬性。<br/>                                                                  |
| <span id="TAG_APP_NAME_RC_ID"></span><span id="tag_app_name_rc_id"></span><dl> <dt>**標記 \_應用程式 \_ 名稱 \_ RC \_ 識別碼**</dt> <dt> (0x24 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>               | Apphelp 專案的應用程式名稱資源識別碼屬性。<br/>                                   |
| <span id="TAG_VENDOR_NAME_RC_ID"></span><span id="tag_vendor_name_rc_id"></span><dl> <dt>**標記 \_廠商 \_ 名稱 \_ RC \_ 識別碼**</dt> <dt> (0x25 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>      | Apphelp 專案的廠商名稱資源識別碼屬性。<br/>                                        |
| <span id="TAG_SUMMARY_MSG_RC_ID"></span><span id="tag_summary_msg_rc_id"></span><dl> <dt>**標記 \_摘要 \_ 訊息 \_ RC \_ 識別碼**</dt> <dt> (0x26 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>      | Apphelp 專案的摘要訊息資源識別碼屬性。<br/>                                    |
| <span id="TAG_VISTA_SKU"></span><span id="tag_vista_sku"></span><dl> <dt>**標記 \_VISTA \_ SKU**</dt> <dt> (0x27 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                                | Windows Vista SKU 屬性。<br/>                                                                          |
| <span id="TAG_DESCRIPTION_RC_ID"></span><span id="tag_description_rc_id"></span><dl> <dt>**標記 \_描述 \_ RC \_ 識別碼**</dt> <dt> (0x28 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>       | Apphelp 專案的描述資源識別碼屬性。<br/>                                        |
| <span id="TAG_PARAMETER1_RC_ID"></span><span id="tag_parameter1_rc_id"></span><dl> <dt>**標記 \_PARAMETER1 \_ RC \_ ID**</dt> <dt> (0x29 \| **TAG \_ TYPE \_ DWORD**)</dt> </dl>          | Apphelp 專案的 Parameter1 資源識別碼屬性。<br/>                                         |
| <span id="TAG_TAGID"></span><span id="tag_tagid"></span><dl> <dt>**標記 \_TAGID**</dt> <dt> (0x801 \| **標記 \_ 類型 \_ DWORD**)</dt> </dl>                                            | **TAGID** 屬性。<br/>                                                                                  |



下列專案是類型 **標記 \_ 類型 \_ 字串** (0x8000) 。



| 常數/值                                                                                                                                                                                                                                                            | Description                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------|
| <span id="TAG_STRINGTABLE_ITEM"></span><span id="tag_stringtable_item"></span><dl> <dt>**標記 \_STRINGTABLE \_ 專案**</dt> <dt> (0x801 \| **標記 \_ 類型 \_ 字串**)</dt> </dl> | 字串資料表專案專案。<br/> |



下列專案的類型 **標記 \_ 類型 \_ 為 Null** (0x1000) 。



| 常數/值                                                                                                                                                                                                                                                                            | Description                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| <span id="TAG_INCLUDE"></span><span id="tag_include"></span><dl> <dt>**標記 \_包含**</dt> <dt> (0x1 \| **標記 \_ 類型 \_ Null**)</dt> </dl>                                                 | 包含清單專案。<br/>                           |
| <span id="TAG_GENERAL"></span><span id="tag_general"></span><dl> <dt>**標記 \_一般**</dt> <dt> (0x2 \| **標記 \_ 類型 \_ 為 Null**)</dt> </dl>                                                 | 一般用途填充碼專案。<br/>                   |
| <span id="TAG_MATCH_LOGIC_NOT"></span><span id="tag_match_logic_not"></span><dl> <dt>**標記 \_比對 \_ 邏輯 \_ 不**</dt> <dt> (0x3 \| **標記 \_ 類型 \_ Null**)</dt> </dl>                       | 不符合相符的邏輯專案。<br/>                  |
| <span id="TAG_APPLY_ALL_SHIMS"></span><span id="tag_apply_all_shims"></span><dl> <dt>**標記 \_將 \_ 所有 \_ 填充**</dt>碼 <dt> (0x4 \| **標記 \_ 類型 \_ Null**)</dt> </dl>                       | 未使用的。<br/>                                       |
| <span id="TAG_USE_SERVICE_PACK_FILES"></span><span id="tag_use_service_pack_files"></span><dl> <dt>**標記 \_使用 \_ SERVICE \_ PACK \_**</dt>檔案 <dt> (0x5 \| **標記 \_ 類型 \_ Null**)</dt> </dl> | Apphelp 專案的 Service pack 資訊。<br/> |
| <span id="TAG_MITIGATION_OS"></span><span id="tag_mitigation_os"></span><dl> <dt>**標記 \_緩和 \_ 作業系統**</dt> <dt> (0x6 \| **標記 \_ 類型 \_ Null**)</dt> </dl>                              | 作業系統範圍專案的緩和措施。<br/>   |
| <span id="TAG_BLOCK_UPGRADE"></span><span id="tag_block_upgrade"></span><dl> <dt>**標記 \_封鎖 \_ 升級**</dt> <dt> (0x7 \| **標記 \_ 類型 \_ Null**)</dt> </dl>                              | 升級封鎖專案。<br/>                          |
| <span id="TAG_INCLUDEEXCLUDEDLL"></span><span id="tag_includeexcludedll"></span><dl> <dt>**標記 \_INCLUDEEXCLUDEDLL**</dt> <dt> (0x8 \| **標記 \_ 類型 \_ Null**)</dt> </dl>                   | DLL 包含/排除專案。<br/>                    |



下列專案是 **標記 \_ 類型 \_ QWORD** (0x5000) 的類型。



| 常數/值                                                                                                                                                                                                                                                                                   | Description                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TAG_TIME"></span><span id="tag_time"></span><dl> <dt>**標記 \_TIME**</dt> <dt> (0x1 \| **標記 \_ 類型 \_ QWORD**)</dt> </dl>                                                                | 時間屬性。<br/>                                                                                     |
| <span id="TAG_BIN_FILE_VERSION"></span><span id="tag_bin_file_version"></span><dl> <dt>**標記 \_BIN \_ 檔案 \_ 版本**</dt> <dt> (0x2 \| **標記 \_ 類型 \_ QWORD**)</dt> </dl>                          | 檔案專案的 [Bin 檔案版本] 屬性。<br/>                                                        |
| <span id="TAG_BIN_PRODUCT_VERSION"></span><span id="tag_bin_product_version"></span><dl> <dt>**標記 \_BIN \_ 產品 \_ 版本**</dt> <dt> (0x3 \| **標記 \_ 類型 \_ QWORD**)</dt> </dl>                 | 檔案專案的 Bin product version 屬性。<br/>                                                     |
| <span id="TAG_MODTIME"></span><span id="tag_modtime"></span><dl> <dt>**標記 \_MODTIME**</dt> <dt> (0x4 \| **標記 \_ 類型 \_ QWORD**)</dt> </dl>                                                       | 未使用的。<br/>                                                                                             |
| <span id="TAG_FLAG_MASK_KERNEL"></span><span id="tag_flag_mask_kernel"></span><dl> <dt>**標記 \_旗標 \_ 遮罩 \_ KERNEL**</dt> <dt> (0x5 \| **標記 \_ 類型 \_ QWORD**)</dt> </dl>                          | 核心旗標遮罩屬性。<br/>                                                                         |
| <span id="TAG_UPTO_BIN_PRODUCT_VERSION"></span><span id="tag_upto_bin_product_version"></span><dl> <dt>**標記 \_最多 \_ BIN \_ 產品 \_ 版本**</dt> <dt> (0x6 \| **標記 \_ 類型 \_ QWORD**)</dt> </dl> | 檔案的 Bin product version 屬性。 比對是在此產品版本中完成。<br/> |
| <span id="TAG_DATA_QWORD"></span><span id="tag_data_qword"></span><dl> <dt>**標記 \_資料 \_ qword**</dt> <dt> (0x7 \| **標記 \_ 類型 \_ QWORD**)</dt> </dl>                                             | 資料輸入的 **ULONGLONG** value 屬性。<br/>                                                     |
| <span id="TAG_FLAG_MASK_USER"></span><span id="tag_flag_mask_user"></span><dl> <dt>**標記 \_旗標 \_ 遮罩 \_ 使用者**</dt> <dt> (0x8 \| **標記 \_ 類型 \_ QWORD**)</dt> </dl>                                | 使用者旗標遮罩屬性。<br/>                                                                           |
| <span id="TAG_FLAGS_NTVDM1"></span><span id="tag_flags_ntvdm1"></span><dl> <dt>**標記 \_旗標 \_ NTVDM1**</dt> <dt> (0x9 \| **標記 \_ 類型 \_ QWORD**)</dt> </dl>                                       | NTVDM1 旗標遮罩屬性。<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM2"></span><span id="tag_flags_ntvdm2"></span><dl> <dt>**標記 \_旗標 \_ NTVDM2**</dt> <dt> (0xA \| **標記 \_ 類型 \_ QWORD**)</dt> </dl>                                       | NTVDM2 旗標遮罩屬性。<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM3"></span><span id="tag_flags_ntvdm3"></span><dl> <dt>**標記 \_旗標 \_ NTVDM3**</dt> <dt> (0xB \| **標記 \_ 類型 \_ QWORD**)</dt> </dl>                                       | NTVDM3 旗標遮罩屬性。<br/>                                                                         |
| <span id="TAG_FLAG_MASK_SHELL"></span><span id="tag_flag_mask_shell"></span><dl> <dt>**標記 \_旗標 \_ 遮罩 \_ SHELL**</dt> <dt> (0xC \| **標記 \_ 類型 \_ QWORD**)</dt> </dl>                             | Shell 旗標遮罩屬性。<br/>                                                                          |
| <span id="TAG_UPTO_BIN_FILE_VERSION"></span><span id="tag_upto_bin_file_version"></span><dl> <dt>**標記 \_最大的 \_ BIN 檔案 \_ \_ 版本**</dt> <dt> (0xD \| **標記 \_ 類型 \_ QWORD**)</dt> </dl>          | 檔案的 [Bin 檔案版本] 屬性。 比對會完成，並包含這個檔案版本。<br/>       |
| <span id="TAG_FLAG_MASK_FUSION"></span><span id="tag_flag_mask_fusion"></span><dl> <dt>**標記 \_旗標 \_ 遮罩 \_ 融合**</dt> <dt> (0xE \| **標記 \_ 類型 \_ QWORD**)</dt> </dl>                          | 融合旗標遮罩屬性。<br/>                                                                         |
| <span id="TAG_FLAG_PROCESSPARAM"></span><span id="tag_flag_processparam"></span><dl> <dt>**標記 \_旗標 \_ PROCESSPARAM**</dt> <dt> (0xF \| **標記 \_ 類型 \_ QWORD**)</dt> </dl>                        | 處理 param 旗標屬性。<br/>                                                                       |
| <span id="TAG_FLAG_LUA"></span><span id="tag_flag_lua"></span><dl> <dt>**標記 \_旗標 \_ LUA**</dt> <dt> (0x10 \| **標記 \_ 類型 \_ QWORD**)</dt> </dl>                                                  | LUA 旗標屬性。<br/>                                                                                 |
| <span id="TAG_FLAG_INSTALL"></span><span id="tag_flag_install"></span><dl> <dt>**標記 \_旗標 \_ 安裝**</dt> <dt> (0x11 \| **標記 \_ 類型 \_ QWORD**)</dt> </dl>                                      | 安裝旗標屬性。<br/>                                                                             |



下列專案是 **標記 \_ 類型 \_ BINARY** (0x9000) 的類型。



| 常數/值                                                                                                                                                                                                                                                     | Description                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span id="TAG_PATCH_BITS"></span><span id="tag_patch_bits"></span><dl> <dt>**標記 \_PATCH \_ BITS**</dt> <dt> (0x2 \| **標記 \_ 類型 \_ BINARY**)</dt> </dl>              | Patch file bits 屬性。<br/>                          |
| <span id="TAG_FILE_BITS"></span><span id="tag_file_bits"></span><dl> <dt>**標記 \_檔案 \_ 位**</dt> <dt> (0x3 \| **標記 \_ 類型 \_ BINARY**)</dt> </dl>                 | File bits 屬性。<br/>                                |
| <span id="TAG_EXE_ID"></span><span id="tag_exe_id"></span><dl> <dt>**標記 \_EXE \_ 識別碼**</dt> <dt> (0x4 \| **標記 \_ 類型 \_ BINARY**)</dt> </dl>                          | 可執行檔專案的 **GUID** 屬性。<br/>          |
| <span id="TAG_DATA_BITS"></span><span id="tag_data_bits"></span><dl> <dt>**標記 \_資料 \_ 位**</dt> <dt> (0x5 \| **標記 \_ 類型 \_ BINARY**)</dt> </dl>                 | 資料位屬性。<br/>                                |
| <span id="TAG_MSI_PACKAGE_ID"></span><span id="tag_msi_package_id"></span><dl> <dt>**標記 \_MSI \_ 封裝 \_ 識別碼**</dt> <dt> (0x6 \| **標記 \_ 類型 \_ BINARY**)</dt> </dl> | MSI 套件的 MSI 封裝識別碼屬性。<br/> |
| <span id="TAG_DATABASE_ID"></span><span id="tag_database_id"></span><dl> <dt>**標記 \_資料庫 \_ 識別碼**</dt> <dt> (0x7 \| **標記 \_ 類型 \_ BINARY**)</dt> </dl>           | 資料庫的 **GUID** 屬性。<br/>                   |
| <span id="TAG_INDEX_BITS"></span><span id="tag_index_bits"></span><dl> <dt>**標記 \_索引 \_ 位**</dt> <dt> (0x801 \| **標記 \_ 類型 \_ BINARY**)</dt> </dl>            | 索引位屬性。<br/>                               |



下列專案的類型 **標記類型為 \_ \_ WORD** (0x3000) 。



| 常數/值                                                                                                                                                                                                                                      | Description                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="TAG_MATCH_MODE"></span><span id="tag_match_mode"></span><dl> <dt>**標記 \_符合 \_ 模式**</dt> <dt> (0x1 \| **標記 \_ 類型 \_ WORD**)</dt> </dl> | Match 模式屬性。<br/>                   |
| <span id="TAG_TAG"></span><span id="tag_tag"></span><dl> <dt>**標記 \_標記**</dt> <dt> (0x801 \| **標記 \_ 類型 \_ WORD**)</dt> </dl>                     | 標記專案。<br/>                              |
| <span id="TAG_INDEX_TAG"></span><span id="tag_index_tag"></span><dl> <dt>**標記 \_索引 \_ 標記**</dt> <dt> (0x802 \| **標記 \_ 類型 \_ WORD**)</dt> </dl>  | 索引項目的索引標記屬性。<br/> |
| <span id="TAG_INDEX_KEY"></span><span id="tag_index_key"></span><dl> <dt>**標記 \_索引 \_ 鍵**</dt> <dt> (0x803 \| **標記 \_ 類型 \_ WORD**)</dt> </dl>  | 索引項目的索引鍵屬性。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Exposeenums2managed (包含 Axextendenums) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[標記類型](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




