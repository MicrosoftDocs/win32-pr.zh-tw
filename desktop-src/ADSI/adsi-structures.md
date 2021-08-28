---
title: ADSI 結構
description: Active Directory 服務介面 (ADSI) 定義和使用下表所列的結構。
ms.assetid: 3ee0e469-9932-4135-8798-27d318011786
ms.tgt_platform: multiple
keywords:
- ADSI ADSI、參考、結構
- 結構 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c8c954f55ef53cc1607957a9251ec960908a981ce33e2166f45eef42251abb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962177"
---
# <a name="adsi-structures"></a>ADSI 結構

Active Directory 服務介面 (ADSI) 定義和使用下表所列的結構。



| 結構                                                                      | Description                                                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**ADS \_ ATTR \_ 定義**](/windows/desktop/api/Iads/ns-iads-ads_attr_def)<br/>                              | 描述 **attributeSchema** 物件的一組屬性定義。<br/>                          |
| [**ADS \_ ATTR \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)<br/>                            | 保存命名屬性的值，並指定修改屬性的作業。<br/>              |
| [**ADS \_ BACKLINK**](/windows/win32/api/iads/ns-iads-ads_backlink)<br/>                               | 表示 **後置連結** 屬性的 ADSI 標記法。<br/>                                   |
| [**ADS \_ CASEIGNORE \_ 清單**](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)<br/>                | 代表 **案例忽略清單** 屬性的 ADSI 標記法。<br/>                            |
| [**ADS \_ 類別 \_ DEF**](/windows/desktop/api/Iads/ns-iads-ads_class_def)<br/>                            | 描述物件的架構資料。<br/>                                                                |
| [**\_ \_ 使用二進位的 ADS DN \_**](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)<br/>                 | 將辨別名稱對應至物件 **GUID** 的 ADSI 定義結構。<br/>                     |
| [**\_ \_ 具有字串的 ADS DN \_**](/windows/win32/api/iads/ns-iads-ads_dn_with_string)<br/>                 | ADSI 定義的結構，可將物件的辨別名稱對應至 nonvarying 字串值。<br/> |
| [**ADS \_ 電子郵件**](/windows/win32/api/iads/ns-iads-ads_email)<br/>                                     | 代表 **電子郵件** 屬性的 ADSI 標記法。<br/>                                       |
| [**ADS \_ FAXNUMBER**](/windows/win32/api/iads/ns-iads-ads_faxnumber)<br/>                             | 代表 **傳真呼叫號碼** 屬性的 ADSI 標記法。<br/>                  |
| [**廣告 \_ 持有**](/windows/win32/api/iads/ns-iads-ads_hold)<br/>                                       | 表示 **保存** 屬性的 ADSI 標記法。<br/>                                        |
| [**ADS \_ NETADDRESS**](/windows/win32/api/iads/ns-iads-ads_netaddress)<br/>                           | 表示 **Net Address** 屬性的 ADSI 標記法。<br/>                                 |
| [**ADS \_ NT \_ 安全 \_ 描述項**](/windows/win32/api/iads/ns-iads-ads_nt_security_descriptor)<br/> | 描述安全描述項。<br/>                                                                    |
| [**ADS \_ 物件 \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_object_info)<br/>                        | 描述目錄服務物件資料。<br/>                                                            |
| [**ADS \_ 八位 \_ 清單**](/windows/desktop/api/Iads/ns-iads-ads_octet_list)<br/>                          | 代表 **八位清單** 屬性的 ADSI 標記法。<br/>                                  |
| [**ADS \_ 八進位 \_ 字串**](/windows/win32/api/iads/ns-iads-ads_octet_string)<br/>                      | 代表 **八位字串** 屬性的 ADSI 標記法。<br/>                                |
| [**ADS \_ 路徑**](/windows/win32/api/iads/ns-iads-ads_path)<br/>                                       | 表示 **Path** 屬性的 ADSI 標記法。<br/>                                        |
| [**ADS \_ POSTALADDRESS**](/windows/win32/api/iads/ns-iads-ads_postaladdress)<br/>                     | 代表 **郵政位址** 屬性的 ADSI 標記法。<br/>                              |
| [**ADS \_ >PROV \_ 特定**](/windows/win32/api/iads/ns-iads-ads_prov_specific)<br/>                    | 描述提供者特定的資料類型。<br/>                                                            |
| [**ADS \_ REPLICAPOINTER**](/windows/win32/api/iads/ns-iads-ads_replicapointer)<br/>                   | 表示複本指標屬性的 ADSI 標記法。<br/>                                 |
| [**ADS \_ 搜尋資料 \_ 行**](/windows/desktop/api/Iads/ns-iads-ads_search_column)<br/>                    | 表示目錄查詢所產生的資料行。<br/>                                               |
| [**ADS \_ SEARCHPREF \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)<br/>                | 描述查詢喜好設定。<br/>                                                                        |
| [**ADS \_ SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey)<br/>                                 | 描述用來排序查詢的排序關鍵字。<br/>                                                    |
| [**ADS \_ 時間戳記**](/windows/win32/api/iads/ns-iads-ads_timestamp)<br/>                             | 代表 **時間戳記** 屬性的 ADSI 標記法。<br/>                                   |
| [**ADS \_ TYPEDNAME**](/windows/win32/api/iads/ns-iads-ads_typedname)<br/>                             | 代表具 **類型名稱** 屬性的 ADSI 標記法。<br/>                                  |
| [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)<br/>                                        | 描述 ADSI 資料類型的值。<br/>                                                           |
| [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv)<br/>                                         | 指定從伺服器傳回搜尋結果時，應使用虛擬清單視圖。<br/>  |



 

 

 





