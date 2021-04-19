---
title: " (AppModel. h) 的識別常數"
description: 指定封裝之識別欄位的字串長度。
ms.assetid: C4F81822-B502-4360-AEA4-829F1AB926BF
topic_type:
- apiref
api_name:
- APPLICATION_USER_MODEL_ID_MAX_LENGTH
- APPLICATION_USER_MODEL_ID_MIN_LENGTH
- PACKAGE_ARCHITECTURE_MAX_LENGTH
- PACKAGE_ARCHITECTURE_MIN_LENGTH
- PACKAGE_FAMILY_NAME_MAX_LENGTH
- PACKAGE_FAMILY_NAME_MIN_LENGTH
- PACKAGE_FULL_NAME_MAX_LENGTH
- PACKAGE_FULL_NAME_MIN_LENGTH
- PACKAGE_NAME_MAX_LENGTH
- PACKAGE_NAME_MIN_LENGTH
- PACKAGE_PUBLISHERID_MAX_LENGTH
- PACKAGE_PUBLISHERID_MIN_LENGTH
- PACKAGE_PUBLISHER_MAX_LENGTH
- PACKAGE_PUBLISHER_MIN_LENGTH
- PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH
- PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH
- PACKAGE_RESOURCEID_MAX_LENGTH
- PACKAGE_RESOURCEID_MIN_LENGTH
- PACKAGE_VERSION_MAX_LENGTH
- PACKAGE_VERSION_MIN_LENGTH
api_location:
- AppModel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681a0aef767afe92cdb93eee3849df8ed6a5f080
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967323"
---
# <a name="identity-constants"></a>身分識別常數

指定封裝之識別欄位的字串長度。 長度是以字元來測量，而且不一定會包含 Null 結束字元的空間。

> [!Note]  
> 格式為的常數：**應用程式 \_ 使用者 \_ 模型 \_ 識別碼 \_ \* \_ 長度** 和 **套件 \_ 相對 \_ 應用程式 \_ 識別碼 \_ \* \_ 長度** 包括空白結束字元的空間，但格式為的常數：**套件 \_ \* \_ 長度** 不包含 null 結束字元的空間。

 



| 常數/值                                                                                                                                                                                                                                                                                                   | Description                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_USER_MODEL_ID_MAX_LENGTH"></span><span id="application_user_model_id_max_length"></span><dl> <dt>**應用程式 \_使用者 \_ 型號 \_ 識別碼 \_ 最大 \_ 長度**</dt> <dt>130</dt> </dl>                  | 應用程式使用者模型識別碼的最大長度。 包含 Null 結束字元的空間。<br/>                             |
| <span id="APPLICATION_USER_MODEL_ID_MIN_LENGTH"></span><span id="application_user_model_id_min_length"></span><dl> <dt>**應用程式 \_使用者 \_ 模型 \_ 識別碼 \_ 最小 \_ 長度**</dt> <dt>21</dt> </dl>                   | 應用程式使用者模型識別碼的最小長度。 包含 Null 結束字元的空間。<br/>                             |
| <span id="PACKAGE_ARCHITECTURE_MAX_LENGTH"></span><span id="package_architecture_max_length"></span><dl> <dt>**封裝 \_架構 \_ 最大 \_ 長度**</dt> <dt>7</dt> </dl>                                     | 架構的最大長度。 未包含 Null 結束字元的空間。<br/>                                          |
| <span id="PACKAGE_ARCHITECTURE_MIN_LENGTH"></span><span id="package_architecture_min_length"></span><dl> <dt>**封裝 \_架構 \_ 最小 \_ 長度**</dt> <dt>3</dt> </dl>                                     | 架構的最小長度。 未包含 Null 結束字元的空間。<br/>                                          |
| <span id="PACKAGE_FAMILY_NAME_MAX_LENGTH"></span><span id="package_family_name_max_length"></span><dl> <dt>**封裝 \_系列 \_ 名稱 \_ 最大 \_ 長度**</dt> <dt>64</dt> </dl>                                      | 系列名稱的最大長度。 未包含 Null 結束字元的空間。<br/>                                           |
| <span id="PACKAGE_FAMILY_NAME_MIN_LENGTH"></span><span id="package_family_name_min_length"></span><dl> <dt>**封裝 \_系列 \_ 名稱 \_ 最小 \_ 長度**</dt> <dt>17</dt> </dl>                                      | 系列名稱的最小長度。 未包含 Null 結束字元的空間。<br/>                                           |
| <span id="PACKAGE_FULL_NAME_MAX_LENGTH"></span><span id="package_full_name_max_length"></span><dl> <dt>**封裝 \_完整 \_ 名稱 \_ 最大 \_ 長度**</dt> <dt>127</dt> </dl>                                           | 完整名稱的最大長度。 未包含 Null 結束字元的空間。<br/>                                             |
| <span id="PACKAGE_FULL_NAME_MIN_LENGTH"></span><span id="package_full_name_min_length"></span><dl> <dt>**封裝 \_全名 \_ \_ \_ 長度下限**</dt> <dt>30</dt> </dl>                                            | 完整名稱的最小長度。 未包含 Null 結束字元的空間。<br/>                                             |
| <span id="PACKAGE_NAME_MAX_LENGTH"></span><span id="package_name_max_length"></span><dl> <dt>**封裝 \_名稱 \_ 最大 \_ 長度**</dt> <dt>50</dt> </dl>                                                            | 名稱的最大長度。 未包含 Null 結束字元的空間。<br/>                                                  |
| <span id="PACKAGE_NAME_MIN_LENGTH"></span><span id="package_name_min_length"></span><dl> <dt>**封裝 \_名稱 \_ 最小 \_ 長度**</dt> <dt>3</dt> </dl>                                                             | 名稱的最小長度。 未包含 Null 結束字元的空間。<br/>                                                  |
| <span id="PACKAGE_PUBLISHERID_MAX_LENGTH"></span><span id="package_publisherid_max_length"></span><dl> <dt>**封裝 \_PUBLISHERID \_ 最大 \_ 長度**</dt> <dt>13</dt> </dl>                                       | 發行者識別碼的最大長度。 未包含 Null 結束字元的空間。<br/>                                          |
| <span id="PACKAGE_PUBLISHERID_MIN_LENGTH"></span><span id="package_publisherid_min_length"></span><dl> <dt>**封裝 \_PUBLISHERID \_ 最小 \_ 長度**</dt> <dt>13</dt> </dl>                                       | 發行者識別碼的最小長度。 未包含 Null 結束字元的空間。<br/>                                          |
| <span id="PACKAGE_PUBLISHER_MAX_LENGTH"></span><span id="package_publisher_max_length"></span><dl> <dt>**封裝 \_發行者 \_ 最大 \_ 長度**</dt> <dt>8192</dt> </dl>                                           | 發行者的最大長度。 例如，CN =*publisher*。 未包含 Null 結束字元的空間。<br/>                |
| <span id="PACKAGE_PUBLISHER_MIN_LENGTH"></span><span id="package_publisher_min_length"></span><dl> <dt>**封裝 \_發行者 \_ 最小 \_ 長度**</dt> <dt>4</dt> </dl>                                              | 發行者的最小長度。 未包含 Null 結束字元的空間。<br/>                                             |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH"></span><span id="package_relative_application_id_max_length"></span><dl> <dt>**封裝 \_相對 \_ 應用程式 \_ 識別碼 \_ 最大 \_ 長度**</dt> <dt>65</dt> </dl> | 封裝相對應用程式識別碼的最大長度。 包含 Null 結束字元的空間。<br/>                       |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH"></span><span id="package_relative_application_id_min_length"></span><dl> <dt>**封裝 \_相對 \_ 應用程式 \_ 識別碼 \_ 最小 \_ 長度**</dt> <dt>2</dt> </dl>  | 封裝相對應用程式識別碼的最小長度。 包含 Null 結束字元的空間。<br/>                       |
| <span id="PACKAGE_RESOURCEID_MAX_LENGTH"></span><span id="package_resourceid_max_length"></span><dl> <dt>**封裝 \_RESOURCEID \_ 最大 \_ 長度**</dt>為 <dt>30</dt> </dl>                                          | 資源識別碼的最大長度。 未包含 Null 結束字元的空間。<br/>                                           |
| <span id="PACKAGE_RESOURCEID_MIN_LENGTH"></span><span id="package_resourceid_min_length"></span><dl> <dt>**封裝 \_RESOURCEID \_ 最小 \_ 長度**</dt>為 <dt>0</dt> </dl>                                           | 資源識別碼的最小長度。 未包含 Null 結束字元的空間。<br/>                                           |
| <span id="PACKAGE_VERSION_MAX_LENGTH"></span><span id="package_version_max_length"></span><dl> <dt>**封裝 \_版本 \_ 最大 \_ 長度**</dt> <dt>23</dt> </dl>                                                   | 版本的最大長度。 例如， *xxxxx*。*xxxxx**xxxxx**xxxxx* Null 結束字元/沒有包含空格<br/> |
| <span id="PACKAGE_VERSION_MIN_LENGTH"></span><span id="package_version_min_length"></span><dl> <dt>**封裝 \_版本 \_ 最小 \_ 長度**</dt> <dt>7</dt> </dl>                                                    | 版本的最小長度。 例如， *x*。*x*。*x*。*x*。 未包含 Null 結束字元的空間。<br/>                 |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>AppModel. h</dt> </dl> |



 

 





