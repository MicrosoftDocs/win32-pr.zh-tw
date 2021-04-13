---
title: '驗證常數 (WSManDisp .h) '
description: 指定驗證方法，以及如何處理要求之 HTTPS 傳輸的憑證伺服器。
ms.assetid: adfefbc9-c386-48db-a0c2-145aa4f91bfa
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagCredUsernamePassword
- WSManFlagSkipCACheck
- WSManFlagSkipCNCheck
- WSManFlagUseNoAuthentication
- WSManFlagUseDigest
- WSManFlagUseNegotiate
- WSManFlagUseBasic
- WSManFlagUseKerberos
- WSManFlagNoEncryption
- WSManFlagUseClientCertificate
- WSManFlagUseCredSsp
- WSManFlagSkipRevocationCheck
- WSManFlagAllowNegotiateImplicitCredentials
- WSManFlagUseSsl
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce45d1474cf6c925149c05ae348231333c3356e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509239"
---
# <a name="authentication-constants"></a>驗證常數

驗證常數是 **\_ \_ WSManSessionFlags** 列舉中的常數，可指定驗證方法，以及如何處理要求之 HTTPS 傳輸的憑證伺服器。

在呼叫 [**CreateSession**](wsman-createsession.md)或 [**IWSMan：： CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)連接至遠端電腦的呼叫中，*旗標* 參數中列出的一個或多個常數是必要的。

<dl> <dt>

<span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**
</dt> <dd> <dl> <dt>

4096 (0x1000) 
</dt> <dt>



使用使用者名稱和密碼做為認證。 當您建立 [**ConnectionOptions**](connectionoptions.md) 物件並提供使用者 [**名稱**](connectionoptions-username.md) 和 [**密碼**](connectionoptions-password.md)時，請設定此旗標。 認證可以是網域帳戶或本機電腦上的帳戶。 根據預設，此帳戶必須是本機或遠端電腦上本機系統管理員群組的成員。 不過，您可以將 WinRM 服務設定為允許其他使用者。 如需詳細資訊，請參閱 [Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。 當您指定 Negotiate 驗證的認證 (也稱為「 [*Windows 整合式驗證*](windows-remote-management-glossary.md)) 或 [*基本驗證*](windows-remote-management-glossary.md)時，您可以設定此旗標。

相關聯的腳本方法是 [**WSMan. SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md)，而 c + + 方法是 [**IWSManEx. SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**
</dt> <dd> <dl> <dt>

8192 (0x2000) 
</dt> <dt>



透過 HTTPS 連線時，用戶端並不會驗證伺服器憑證是否由信任的憑證授權單位單位簽署 (CA) 。 只有在遠端電腦受其他方法信任時才使用此值，例如，如果遠端電腦是實體安全且隔離之網路的一部分，或在 WinRM 設定中將遠端電腦列為受信任的主機。

相關聯的腳本方法是 [**WSMan. SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md)，而 c + + 方法是 [**IWSManEx. SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**
</dt> <dd> <dl> <dt>

16384 (0x4000) 
</dt> <dt>



透過 HTTPS 連線時，用戶端將不會驗證伺服器憑證中 (CN) 的一般名稱是否符合連接字串中的電腦名稱稱。 只有在遠端電腦受其他方法信任時才使用，例如，如果遠端電腦是實體安全且隔離之網路的一部分，或在 WinRM 設定中將遠端電腦列為受信任的主機。

相關聯的腳本方法是 [**WSMan. SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md)，而 c + + 方法是 [**IWSManEx. SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**
</dt> <dd> <dl> <dt>

32768 (0x8000) 
</dt> <dt>



不使用驗證。 當測試與遠端電腦的連線時，請指定這個常數，以判斷是否已將執行 WS-Management 通訊協定的服務設定為接聽資料要求。 **WSManFlagUseNoAuthentication** 無法與任何其他 [**會話**](session.md) 常數合併。 相關聯的腳本方法是 [**WSMan. SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md)，而 c + + 方法是 [**WSManEx. SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**
</dt> <dd> <dl> <dt>

65536 (0x10000) 
</dt> <dt>



使用摘要式驗證。 只有用戶端電腦可以起始摘要式驗證要求。 用戶端會將要求傳送至伺服器，以驗證並接收來自伺服器的權杖字串。 然後，用戶端會傳送資源要求，包括使用者名稱和密碼的密碼編譯雜湊與權杖字串合併。 HTTP 和 HTTPS 支援摘要式驗證。 WinRM 用戶端腳本和應用程式可以指定摘要式驗證，但不能指定服務。

相關聯的腳本方法是 [**WSMan. SessionFlagUseDigest**](wsman-sessionflagusedigest.md)，而 c + + 方法是 [**IWSManEx. SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**
</dt> <dd> <dl> <dt>

131072 (0x20000) 
</dt> <dt>



使用 Negotiate 驗證。 用戶端會將要求傳送至伺服器以進行驗證。 伺服器會決定是要使用 Kerberos 或 NTLM。 選取 [Kerberos] 以驗證網域帳戶，並選取 [本機電腦帳戶的 NTLM]。 使用者名稱應以網域 \\ 使用者名稱或 \\ 伺服器電腦上本機使用者的 servername 使用者名稱來指定。

[ (UAC) 的使用者帳戶控制 ](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) 會影響 WinRM 服務的存取權。 當您在工作組或網域中使用「協商驗證」時，只有內建的系統管理員帳戶可以存取該服務。 若要允許 Administrators 群組中的所有帳戶存取服務，請將下列登錄機碼設定為1： **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ 原則 \\ 系統 \\ LocalAccountTokenFilterPolicy**。

相關聯的腳本方法是 [**WSMan. SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md)，而 c + + 方法是 [**IWSManEx. SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**
</dt> <dd> <dl> <dt>

262144 (0x40000) 
</dt> <dt>



使用基本驗證。 用戶端會以使用者名稱和密碼的形式呈現認證，直接在要求訊息中傳輸。 您只能指定識別遠端電腦上本機系統管理員帳戶的認證。

相關聯的腳本方法是 [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md)，而 c + + 方法是 [**IWSManEx. SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**
</dt> <dd> <dl> <dt>

524288 (0x80000) 
</dt> <dt>



使用 Kerberos 驗證。 用戶端和伺服器會使用 Kerberos 票證相互驗證。

相關聯的腳本方法是 [**WSMan. SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md)，而 c + + 方法是 [**IWSManEx. SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**
</dt> <dd> <dl> <dt>

1048576 (0x100000) 
</dt> <dt>



不使用加密。 預設不允許未加密的流量，而且必須同時在用戶端和伺服器上啟用。

相關聯的腳本方法是 [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md)，而 c + + 方法是 [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**
</dt> <dd> <dl> <dt>

2097152 (0x200000) 
</dt> <dt>



使用以用戶端憑證為基礎的驗證。

相關聯的腳本方法是 [**WSMan. SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md)，而 c + + 方法是 [**IWSManEx2. SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**
</dt> <dd> <dl> <dt>

16777216 (0x1000000) 
</dt> <dt>



使用認證安全性支援提供者 (CredSSP) 驗證。

相關聯的腳本方法是 [**WSMan. SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md)，而 c + + 方法是 [**IWSManEx3. SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**
</dt> <dd> <dl> <dt>

0x2000000
</dt> <dt>



請勿在驗證期間檢查憑證撤銷。


</dt> </dl> </dd> <dt>

<span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**
</dt> <dd> <dl> <dt>

0x4000000
</dt> <dt>



允許隱含的認證。


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**
</dt> <dd> <dl> <dt>

0x8000000
</dt> <dt>



使用安全通訊端層，啟用 HTTPS。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[會話常數](session-constants.md)
</dt> </dl>

 

 





