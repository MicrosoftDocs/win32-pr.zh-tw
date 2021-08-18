---
title: ADSI 列舉
description: Active Directory 服務介面 (ADSI) 定義和使用下表所列的列舉。
ms.assetid: f0ad5ce5-742d-40dc-ac5a-31d779e40bfd
ms.tgt_platform: multiple
keywords:
- ADSI ADSI、參考、列舉
- 列舉 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10d5aed5688e7128a64a32dee2f83efa22ab5bf292231517026299ccb592886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023906"
---
# <a name="adsi-enumerations"></a>ADSI 列舉

Active Directory 服務介面 (ADSI) 定義和使用下表所列的列舉。



| 列舉型別                                                           | 描述                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ADS \_ ACEFLAG \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum)                        | 指定將繼承的存取控制專案的安全性傳播 (Ace) 和系統 ACE 的審核類型。                                                                                                                                             |
| [**ADS \_ ACETYPE \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_acetype_enum)                        | 指定 ACE 類型。                                                                                                                                                                                                                                           |
| [**ADS \_ 驗證 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_authentication_enum)          | 指定用於驗證用戶端的安全性層級。                                                                                                                                                                                                     |
| [**廣告會將 \_ \_ 參考 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)       | 指定參考追蹤的行為。                                                                                                                                                                                                                       |
| [**ADS \_ DEREFENUM**](/windows/win32/api/iads/ne-iads-ads_derefenum)                               | 指定別名取值的行為。                                                                                                                                                                                                                    |
| [**ADS \_ 顯示 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_display_enum)                        | 指定路徑的顯示方式。                                                                                                                                                                                                                                |
| [**ADS \_ ESCAPE \_ 模式 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)               | 指定特殊字元是否要經過轉義、非字串或不變。                                                                                                                                                                                        |
| [**ADS \_ FLAGTYPE \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum)                      | 指定 ACE 中的 **ObjectType** 或 **InheritedObjectType** 欄位是否存在。                                                                                                                                                                         |
| [**ADS \_ 格式 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_format_enum)                          | 指定路徑名稱物件中的數值型別。                                                                                                                                                                                                                |
| [**ADS \_ 群組 \_ 類型 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_group_type_enum)                 | 指定成員的群組類型。                                                                                                                                                                                                                           |
| [**ADS \_ 名稱 \_ INITTYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_name_inittype_enum)           | 指定要在名稱轉譯物件上執行的初始化類型。                                                                                                                                                                                  |
| [**ADS \_ 名稱 \_ 類型 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_name_type_enum)                   | 指定用來表示辨別名稱的格式。                                                                                                                                                                                                       |
| [**ADS \_ 選項 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_option_enum)                          | 指定 [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) 介面用來操作目錄物件的可用選項。                                                                                                                        |
| [**ADS \_ 密碼 \_ 編碼 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_password_encoding_enum)   | 用來識別 [**IADsObjectOptions：： GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption)和 [**IADsObjectOptions：： SetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption)方法中，與 **ADS \_ 選項 \_ 密碼 \_ 方法** 選項搭配使用的密碼編碼類型。 |
| [**ADS \_ PATHTYPE \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_pathtype_enum)                      | 指定修改安全描述項的物件類型。                                                                                                                                                                                        |
| [**ADS \_ 喜好設定 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_preferences_enum)                | 指定 ADSI 的 OLE DB 查詢喜好設定。                                                                                                                                                                                                           |
| [**ADS \_ 屬性 \_ 運算 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) | 指定在屬性快取中更新屬性值的方式。                                                                                                                                                                                               |
| [**ADS \_ 許可權 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_rights_enum)                          | 指定目錄服務物件的存取權限。                                                                                                                                                                                                        |
| [**ADS \_ SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum)                               | 指定目錄搜尋的範圍。                                                                                                                                                                                                                        |
| [**ADS \_ SD \_ CONTROL \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum)                 | 指定當將新的許可權以遞迴方式套用至目錄樹狀結構時，要保護 (ACL) 的存取控制清單。                                                                                                                                  |
| [**ADS \_ SD \_ 格式 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_sd_format_enum)                   | 指定用於轉換安全描述項的格式。                                                                                                                                                                                                      |
| [**ADS \_ SD \_ REVISION \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_sd_revision_enum)               | 指定 ACE 或 ACL 的修訂編號。                                                                                                                                                                                                                   |
| [**ADS \_ SEARCHPREF \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_searchpref_enum)                  | 指定搜尋的喜好設定。                                                                                                                                                                                                                              |
| [**ADS \_ 安全性 \_ 資訊 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_security_info_enum)           | 指定檢查安全性資料的選項。                                                                                                                                                                                                                |
| [**ADS \_ >ADVANCED.FIELD.SETTYPE \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_settype_enum)                        | 指定 [**IADsPathname：： Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)中的路徑格式。                                                                                                                                                                                       |
| [**ADS \_ STATUSENUM**](/windows/win32/api/iads/ne-iads-ads_statusenum)                             | 指定搜尋喜好設定的狀態。                                                                                                                                                                                                                       |
| [**ADS \_ SYSTEMFLAG \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum)                  | 指定 **attributeSchema** 物件所表示之屬性的類型。                                                                                                                                                                                   |
| [**ADS \_ 使用者 \_ 旗標 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)                   | 指定用於操作使用者屬性的旗標。                                                                                                                                                                                                            |
| [**ADSI \_ 方言 \_ 列舉**](/windows/win32/api/iads/ne-iads-adsi_dialect_enum)                      | 指定可用的 ADSI 查詢方言。                                                                                                                                                                                                                          |
| [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)                                    | 指定用來解讀 ADSI 擴充語法字串的資料類型。                                                                                                                                                                                            |



 

## <a name="remarks"></a>備註

由於 Visual Basic 腳本撰寫版應用程式無法從類型程式庫讀取資料，因此 VBScript 應用程式無法辨識這些列舉中所定義的符號常數。 請改用數值常數來設定 VBScript 應用程式中適當的旗標。 若要使用符號常數作為良好的程式設計實務，請在 VBScript 應用程式中撰寫這類常數的明確宣告（如這裡所述）。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
</dt> <dt>

[**IADsPathname：： Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)
</dt> </dl>

 

 




