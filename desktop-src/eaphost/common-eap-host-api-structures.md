---
title: 常見的 EAPHost API 結構
description: 瞭解一般 EAPHost API 結構。 查看所有 EAPHost 技術所使用的結構清單。
ms.assetid: f6f3b909-1e89-47f8-853c-c0f3f2414817
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b44a94aae1f18336dae8c11a1dc0217dc7c8d08
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683129"
---
# <a name="common-eaphost-api-structures"></a>常見的 EAPHost API 結構

下表列出所有 EAPHost API 技術通用的結構。



| 結構                                                                | Description                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EAP \_ 屬性**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)                                  | 包含 EAP 屬性。                                                                                                                                                                                              |
| [**EAP \_ 屬性**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes)                                | 包含 EAP 屬性的陣列。                                                                                                                                                                                    |
| [**EAP \_ 設定 \_ 輸入 \_ 欄位 \_ 陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | 包含一組 [**EAP 設定 \_ \_ 輸入 \_ 欄位 \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) 結構，其中共同包含從 EAP 單一登入 (SSO) 設定對話方塊取得的使用者輸入欄位資料。 |
| [**EAP \_ 設定 \_ 輸入 \_ 欄位 \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | 包含與 EAP 單一登入 (SSO) 設定] 對話方塊中單一輸入欄位相關聯的資料。                                                                                                              |
| [**EAP \_ 錯誤**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)                                          | 包含在 EAPHost 作業期間發生之錯誤的相關資料。                                                                                                                                                 |
| [**EAP \_ 方法 \_ 資訊**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info)                             | 包含 EAP 方法的特定資料。                                                                                                                                                                               |
| [**EAP \_ 方法 \_ 資訊， \_ 例如**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_ex)                      | Windows Vista Service Pack 1 (SP1) 或更新版本：包含 EAP 方法的特定資料。                                                                                                                             |
| [**EAP \_ 方法 \_ 資訊 \_ 陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array)                | 包含用戶端電腦上所安裝之 EAP 方法的資訊。                                                                                                                                                   |
| [**EAP \_ 方法 \_ 資訊 \_ 陣列 \_ 例如**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array_ex)         | Windows Vista SP1 或更新版本：包含用戶端電腦上安裝的所有 EAP 方法的相關資訊。                                                                                                    |
| [**EAP \_ 方法 \_ 類型**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type)                             | 包含 EAP 方法的類型、識別和撰寫資料。                                                                                                                                                       |
| [**EAP \_ 類型**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type)                                            | 包含 EAP 方法的型別和廠商識別資料。                                                                                                                                                         |
| [**EapPacket**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket)                                           | 包含在 EAP 驗證會話期間傳送之不透明資料的封包。                                                                                                                                             |



 

 

 




