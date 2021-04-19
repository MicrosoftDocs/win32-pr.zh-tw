---
description: 下列識別碼用來識別 CNG 密碼編譯介面。
ms.assetid: 509c89ff-0c73-4e57-9c39-400522f2086e
title: 'CNG 介面識別碼 (Bcrypt .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f75de82e198e0471b48175a080012b9b40eed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973007"
---
# <a name="cng-interface-identifiers"></a>CNG 介面識別碼

下列識別碼用來識別 CNG 密碼編譯介面。 在 CNG 中，介面會識別提供者所支援的密碼編譯行為類型。 例如，提供者可以是亂數產生器，也可以是雜湊提供者。



| 常數/值                                                                                                                                                                                                                                                                                             | Description                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_CIPHER_INTERFACE"></span><span id="bcrypt_cipher_interface"></span><dl> <dt>**BCRYPT \_CIPHER \_ 介面**</dt> <dt>0x00000001</dt> </dl>                                               | 對稱式加密介面。<br/>                                                                                                                                        |
| <span id="BCRYPT_HASH_INTERFACE"></span><span id="bcrypt_hash_interface"></span><dl> <dt>**BCRYPT \_雜湊 \_ 介面**</dt> <dt>0x00000002</dt> </dl>                                                     | 雜湊介面。<br/>                                                                                                                                                    |
| <span id="BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></span><span id="bcrypt_asymmetric_encryption_interface"></span><dl> <dt>**BCRYPT \_非對稱式 \_ 加密 \_ 介面**</dt> <dt>0x00000003</dt> </dl> | 非對稱式加密介面。<br/>                                                                                                                                   |
| <span id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></span><span id="bcrypt_secret_agreement_interface"></span><dl> <dt>**BCRYPT \_秘密 \_ 合約 \_ 介面**</dt> <dt>0x00000004</dt> </dl>                | 秘密協定介面。<br/>                                                                                                                                        |
| <span id="BCRYPT_SIGNATURE_INTERFACE"></span><span id="bcrypt_signature_interface"></span><dl> <dt>**BCRYPT \_簽名 \_ 介面**</dt> <dt>0x00000005</dt> </dl>                                      | 簽名介面。<br/>                                                                                                                                               |
| <span id="BCRYPT_RNG_INTERFACE"></span><span id="bcrypt_rng_interface"></span><dl> <dt>**BCRYPT \_RNG \_ 介面**</dt> <dt>0x00000006</dt> </dl>                                                        | 亂數產生器介面。<br/>                                                                                                                                 |
| <span id="NCRYPT_KEY_STORAGE_INTERFACE"></span><span id="ncrypt_key_storage_interface"></span><dl> <dt>**NCRYPT \_金鑰 \_ 儲存 \_ 介面**</dt> <dt>0x00010001</dt> </dl>                               | 金鑰儲存介面。<br/>                                                                                                                                             |
| <span id="NCRYPT_SCHANNEL_INTERFACE"></span><span id="ncrypt_schannel_interface"></span><dl> <dt>**NCRYPT \_SCHANNEL \_ 介面**</dt> <dt>0x00010002</dt> </dl>                                         | Schannel 簽章介面。<br/>                                                                                                                                      |
| <span id="NCRYPT_SCHANNEL_SIGNATURE_INTERFACE"></span><span id="ncrypt_schannel_signature_interface"></span><dl> <dt>**NCRYPT \_SCHANNEL 簽章 \_ \_ 介面**</dt> <dt>0x00010003</dt> </dl>          | Schannel 加密套件介面。<br/> **Windows server 2008、Windows Vista、Windows server 2003、WINDOWS XP 及 windows 2000：** 不支援這個值。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                                                                |
| 標頭<br/>                   | <dl> <dt>Bcrypt .h;</dt><dt>Ncrypt .h</dt> </dl> |



 

 




