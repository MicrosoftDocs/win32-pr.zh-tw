---
description: CryptXML 會定義 Cryptxml .h 標頭檔中的下列全域限制。
ms.assetid: 8f4dc314-76fc-40ce-a1e1-a701ae39d66d
title: 'CryptXML 限制 (Cryptxml) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccc56ee6459be2160efdeb8e9874e7dd0c53518d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468885"
---
# <a name="cryptxml-limits"></a>CryptXML 限制

CryptXML 會定義 Cryptxml .h 標頭檔中的下列全域限制。



| 常數/值                                                                                                                                                                                                                                                             | Description                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_BLOB_MAX"></span><span id="crypt_xml_blob_max"></span><dl> <dt>**CRYPT \_XML \_ BLOB \_ MAX**</dt> <dt>0x7FFFFFF8</dt> </dl>                             | 編碼的資料不能超過 2 gb 的 (GB) 。<br/>                                                                                                                                                                               |
| <span id="CRYPT_XML_ID_MAX"></span><span id="crypt_xml_id_max"></span><dl> <dt>**CRYPT \_XML \_ 識別碼 \_ 最大值**</dt> <dt>256</dt> </dl>                                          | 識別碼長度不能超過256個字元。<br/>                                                                                                                                                                                    |
| <span id="CRYPT_XML_URI_MAX"></span><span id="crypt_xml_uri_max"></span><dl> <dt>**CRYPT \_XML \_ URI \_ 最大值**</dt> <dt>8 \* 1024</dt> </dl>                                   | URI 長度不能超過8192個字元。<br/>                                                                                                                                                                                  |
| <span id="CRYPT_XML_SIGNATURES_MAX"></span><span id="crypt_xml_signatures_max"></span><dl> <dt>**CRYPT \_XML 簽章 \_ \_ 上限**</dt> <dt>16</dt> </dl>                   | 每份 **檔的預設簽章元素數目** 上限。 將屬性值傳遞為 [**CRYPT \_ XML \_ 屬性**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_property) 結構時，可以指定新的最大值來覆寫這個值。<br/> |
| <span id="CRYPT_XML_TRANSFORM_MAX"></span><span id="crypt_xml_transform_max"></span><dl> <dt>**CRYPT \_XML \_ 轉換 \_ 上限**</dt> <dt>16</dt> </dl>                      | 每個參考的轉換數目上限（以 [**CRYPT \_ xml \_ 演算法**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm) 結構表示），以 [**CRYPT \_ xml \_ 參考**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_reference) 結構表示。<br/>          |
| <span id="CRYPT_XML_SIGNATURE_VALUE_MAX"></span><span id="crypt_xml_signature_value_max"></span><dl> <dt>**CRYPT \_XML \_ 簽名 \_ 值 \_ 最大值**</dt> <dt>2048</dt> </dl> | [**CRYPT \_ XML \_**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature)簽章結構的最大長度（以位元組為單位）。<br/>                                                                                                                         |
| <span id="CRYPT_XML_DIGEST_VALUE_MAX"></span><span id="crypt_xml_digest_value_max"></span><dl> <dt>**CRYPT \_XML \_ 摘要 \_ 值 \_ 最大值**</dt> <dt>128</dt> </dl>           | 摘要的最大長度（以位元組為單位）。<br/>                                                                                                                                                                                 |
| <span id="CRYPT_XML_OBJECTS_MAX"></span><span id="crypt_xml_objects_max"></span><dl> <dt>**CRYPT \_XML \_ 物件 \_ 最大**</dt> <dt>256</dt> </dl>                           | 在內部使用，以指定每個簽章允許的 **物件** 元素數目上限。<br/>                                                                                                                                |
| <span id="CRYPT_XML_REFERENCES_MAX"></span><span id="crypt_xml_references_max"></span><dl> <dt>**CRYPT \_XML \_ 參考 \_ MAX**</dt> <dt>0x7FF8</dt> </dl>               | 允許的 **參考** 元素數目上限。<br/>                                                                                                                                                                      |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Cryptxml。h</dt> </dl> |



 

 




