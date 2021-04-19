---
description: 以下是在 Cryptxml 中定義的執行時間錯誤碼，可由 CryptXML 函數傳回。
ms.assetid: c3678767-aab3-4771-b2f2-8d79545d420d
title: 'CryptXML 錯誤碼 (Cryptxml) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5906c406f14081844ddce042f0e170668950e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984731"
---
# <a name="cryptxml-error-codes"></a>CryptXML 錯誤碼

以下是在 Cryptxml 中定義的執行時間錯誤碼，可由 CryptXML 函數傳回。



| 常數/值                                                                                                                                                                                                                                                                             | Description                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_E_LARGE"></span><span id="crypt_xml_e_large"></span><dl> <dt>**CRYPT \_XML \_ E \_ 大型**</dt> <dt>0x80092101L</dt> </dl>                                               | 提供的值太大。<br/>                                                                        |
| <span id="CRYPT_XML_E_ENCODING"></span><span id="crypt_xml_e_encoding"></span><dl> <dt>**CRYPT \_XML \_ E \_ 編碼**</dt> <dt>0x80092103L</dt> </dl>                                      | 不支援指定的 XML 編碼。<br/>                                                              |
| <span id="CRYPT_XML_E_ALGORITHM"></span><span id="crypt_xml_e_algorithm"></span><dl> <dt>**CRYPT \_XML \_ E \_ 演算法**</dt> <dt>0x80092104L</dt> </dl>                                   | 不支援指定的 XML 演算法。<br/>                                                             |
| <span id="CRYPT_XML_E_TRANSFORM"></span><span id="crypt_xml_e_transform"></span><dl> <dt>**CRYPT \_XML \_ E \_ 轉換**</dt> <dt>0x80092105L</dt> </dl>                                   | 不支援指定的轉換。<br/>                                                                 |
| <span id="CRYPT_XML_E_HANDLE"></span><span id="crypt_xml_e_handle"></span><dl> <dt>**CRYPT \_XML \_ E \_ 控制碼**</dt> <dt>0x80092106L</dt> </dl>                                            | 提供的控制碼無效。<br/>                                                                       |
| <span id="CRYPT_XML_E_OPERATION"></span><span id="crypt_xml_e_operation"></span><dl> <dt>**CRYPT \_XML \_ E \_ OPERATION**</dt> <dt>0x80092107L</dt> </dl>                                   | 作業無效。<br/>                                                                             |
| <span id="CRYPT_XML_E_UNRESOLVED_REFERENCE"></span><span id="crypt_xml_e_unresolved_reference"></span><dl> <dt>**CRYPT \_XML \_ E \_ 無法解析的 \_ 參考**</dt> <dt>0x80092108L</dt> </dl> | 無法解析 **參考** 元素。<br/>                                                            |
| <span id="CRYPT_XML_E_INVALID_DIGEST"></span><span id="crypt_xml_e_invalid_digest"></span><dl> <dt>**CRYPT \_XML \_ E \_ 不正確 \_ 摘要**</dt> <dt>0x80092109L</dt> </dl>                   | 摘要值無效。<br/>                                                                          |
| <span id="CRYPT_XML_E_INVALID_SIGNATURE"></span><span id="crypt_xml_e_invalid_signature"></span><dl> <dt>**CRYPT \_XML \_ E \_ 無效 \_**</dt>的簽章 <dt>0x8009210AL</dt> </dl>          | 簽章值無效。<br/>                                                                       |
| <span id="CRYPT_XML_E_HASH_FAILED"></span><span id="crypt_xml_e_hash_failed"></span><dl> <dt>**CRYPT \_XML \_ E \_ 雜湊 \_ 失敗**</dt> <dt>0x8009210BL</dt> </dl>                            | 無法建立或計算雜湊。<br/>                                                                 |
| <span id="CRYPT_XML_E_SIGN_FAILED"></span><span id="crypt_xml_e_sign_failed"></span><dl> <dt>**CRYPT \_XML \_ E \_ SIGN \_ 失敗**</dt> <dt>0x8009210CL</dt> </dl>                            | 密碼編譯簽章操作失敗。<br/>                                                           |
| <span id="CRYPT_XML_E_VERIFY_FAILED"></span><span id="crypt_xml_e_verify_failed"></span><dl> <dt>**CRYPT \_XML \_ E \_ 驗證 \_ 失敗**</dt> <dt>0x8009210DL</dt> </dl>                      | 簽章驗證失敗。<br/>                                                                      |
| <span id="CRYPT_XML_E_TOO_MANY_SIGNATURES"></span><span id="crypt_xml_e_too_many_signatures"></span><dl> <dt>**CRYPT \_XML \_ E \_ 0x8009210EL \_ 過 \_ 多**</dt>的簽章 <dt></dt> </dl>   | 檔 **中的簽章元素數目** 超過最大允許的處理上限。<br/> |
| <span id="CRYPT_XML_E_INVALID_KEYVALUE"></span><span id="crypt_xml_e_invalid_keyvalue"></span><dl> <dt>**CRYPT \_XML \_ E \_ 不正確 \_ KEYVALUE**</dt> <dt>0x8009210FL</dt> </dl>             | 提供的金鑰值無效。<br/>                                                           |
| <span id="CRYPT_XML_E_UNEXPECTED_XML"></span><span id="crypt_xml_e_unexpected_xml"></span><dl> <dt>**CRYPT \_XML \_ E 非 \_ 預期的 \_ xml**</dt> <dt>0x80092110L</dt> </dl>                   | 遇到無效或非預期的 XML。<br/>                                                              |
| <span id="CRYPT_XML_E_SIGNER"></span><span id="crypt_xml_e_signer"></span><dl> <dt>**CRYPT \_XML \_ E \_ 簽署人**</dt> <dt>0x80092111L</dt> </dl>                                            | 找不到簽署者的金鑰。<br/>                                                                      |
| <span id="CRYPT_XML_E_NON_UNIQUE_ID"></span><span id="crypt_xml_e_non_unique_id"></span><dl> <dt>**CRYPT \_XML \_ E \_ 非 \_ 唯一 \_ 識別碼**</dt> <dt>0x80092112L</dt> </dl>                     | 找到非唯一的 **識別碼** 屬性。<br/>                                                                 |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Cryptxml。h</dt> </dl> |



 

 




