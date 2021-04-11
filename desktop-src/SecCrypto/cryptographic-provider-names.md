---
description: 搭配 CryptAcquireCoNtext 和 CryptSetProvider 函數使用。
ms.assetid: 97e9a708-83b5-48b3-9d16-f7b54367dc4e
title: '密碼編譯提供者名稱 (Wincrypt .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58a5cbe497e56144a9948dab96be0c03dd5a99f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943338"
---
# <a name="cryptographic-provider-names"></a>密碼編譯提供者名稱

下列 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 名稱是在 Wincrypt 中定義。 這些常數會搭配 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 和 [**CryptSetProvider**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovidera) 函數使用。



| 常數/值                                                                                                                                                                                                                                                                                          | Description                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MS_DEF_DH_SCHANNEL_PROV"></span><span id="ms_def_dh_schannel_prov"></span><dl> <dt>**MS \_DEF \_ DH \_ schannel \_ >PROV**</dt> <dt>"Microsoft DH schannel 密碼編譯提供者"</dt> </dl>      | [MICROSOFT DSS 和 diffie-hellman/Schannel 密碼編譯提供者](microsoft-dss-and-diffie-hellman-schannel-cryptographic-provider.md)。<br/>                                         |
| <span id="MS_DEF_DSS_DH_PROV"></span><span id="ms_def_dss_dh_prov"></span><dl> <dt>**MS \_DEF \_ dss \_ DH \_ >prov**</dt> <dt>"Microsoft Base DSS And Diffie-Hellman 密碼編譯提供者"</dt> </dl>     | [Microsoft 基底 DSS 和 Diffie-Hellman 密碼編譯提供者](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md)。<br/>                                                 |
| <span id="MS_DEF_DSS_PROV"></span><span id="ms_def_dss_prov"></span><dl> <dt>**MS \_DEF \_ dss \_ >prov**</dt> <dt>"Microsoft Base DSS 密碼編譯提供者"</dt> </dl>                                  | [MICROSOFT DSS 密碼編譯提供者](microsoft-dss-cryptographic-provider.md)。<br/>                                                                                                 |
| <span id="MS_DEF_PROV"></span><span id="ms_def_prov"></span><dl> <dt>**MS \_DEF \_ >prov**</dt> 「 <dt>Microsoft 基礎密碼編譯提供者 1.0</dt>版」 </dl>                                              | [Microsoft 基礎密碼編譯提供者](microsoft-base-cryptographic-provider.md)。<br/>                                                                                               |
| <span id="MS_DEF_RSA_SCHANNEL_PROV"></span><span id="ms_def_rsa_schannel_prov"></span><dl> <dt>**MS \_DEF \_ RSA \_ schannel \_ >PROV**</dt> <dt>"Microsoft RSA schannel 密碼編譯提供者"</dt> </dl>  | [MICROSOFT RSA/Schannel 密碼編譯提供者](microsoft-rsa-schannel-cryptographic-provider.md)。<br/>                                                                               |
| <span id="MS_DEF_RSA_SIG_PROV"></span><span id="ms_def_rsa_sig_prov"></span><dl> <dt>**MS \_DEF \_ rsa \_ SIG \_ >PROV**</dt> <dt>"Microsoft RSA Signature 密碼編譯提供者"</dt> </dl>                | 不支援 [MICROSOFT RSA Signature 密碼編譯提供者](microsoft-rsa-signature-cryptographic-provider.md) 。<br/>                                                            |
| <span id="MS_ENH_DSS_DH_PROV"></span><span id="ms_enh_dss_dh_prov"></span><dl> <dt>**MS \_ENH \_ DSS \_ DH \_ >prov**</dt> 「 <dt>Microsoft 增強式 DSS 和 Diffie-Hellman 密碼編譯提供者</dt>」 </dl> | [Microsoft 增強的 DSS 和 Diffie-Hellman 密碼編譯提供者](microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider.md)。<br/>                                         |
| <span id="MS_ENH_RSA_AES_PROV"></span><span id="ms_enh_rsa_aes_prov"></span><dl> <dt>**MS \_ENH \_ RSA \_ AES \_ >prov**</dt> 「 <dt>MICROSOFT 增強型 Rsa 和 AES 密碼編譯提供者</dt>」 </dl>         | [MICROSOFT AES 密碼編譯提供者](microsoft-aes-cryptographic-provider.md)。<br/> * * Windows XP： * * Microsoft 增強型 RSA 和 AES 密碼編譯提供者 (原型) 」<br/> |
| <span id="MS_ENHANCED_PROV"></span><span id="ms_enhanced_prov"></span><dl> <dt>**MS \_增強的 \_ >prov**</dt> 「 <dt>Microsoft 增強型密碼編譯提供者 1.0</dt>版」 </dl>                           | [Microsoft 增強型密碼編譯提供者](microsoft-enhanced-cryptographic-provider.md)。<br/>                                                                                       |
| <span id="MS_SCARD_PROV"></span><span id="ms_scard_prov"></span><dl> <dt>**MS \_捨棄 \_ >prov**</dt> 「 <dt>Microsoft 基礎智慧卡密碼編譯提供者</dt>」 </dl>                                         | [Microsoft 基礎智慧卡密碼編譯服務提供者](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)。<br/>                                                    |
| <span id="MS_STRONG_PROV"></span><span id="ms_strong_prov"></span><dl> <dt>**MS \_強式 \_ >prov**</dt> 「 <dt>Microsoft 強式密碼編譯提供者</dt>」 </dl>                                        | [Microsoft 強式密碼編譯提供者](microsoft-strong-cryptographic-provider.md)。<br/>                                                                                           |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Wincrypt。h</dt> </dl> |



 

 
