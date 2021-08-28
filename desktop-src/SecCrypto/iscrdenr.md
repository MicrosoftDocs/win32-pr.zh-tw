---
description: 代表智慧卡註冊控制項。
ms.assetid: ae872206-81e7-4627-b807-4222f75f8ab6
title: ISCrdEnr 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 2471f3acbb483af7e1882102527d392a69e2c7494a929f37718b51a17405c92b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867888"
---
# <a name="iscrdenr-interface"></a>ISCrdEnr 介面

**ISCrdEnr** 介面代表智慧卡註冊控制項。 開發人員在不使用自動化時，主要是很重要的。 如需 Visual Basic 或其他自動化語言的程式設計，請參閱 [**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85))物件。

## <a name="members"></a>成員

**ISCrdEnr** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ISCrdEnr** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**ISCrdEnr** 介面具有這些方法。



| 方法                                                                    | 描述                                                                                                                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**註冊**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))                                         | 代表使用者要求憑證，並將產生的 [*憑證*](../secgloss/c-gly.md) 儲存在使用者的 [*智慧卡*](../secgloss/s-gly.md)上。<br/>                                                                                                                                                |
| [**enumCAName**](iscrdenr-enumcaname.md)                                 | 針對指定的憑證範本名稱，列舉 (Ca) 的 [*憑證授權單位*](../secgloss/c-gly.md) 單位名稱。<br/>                                                                                                                                                                                                       |
| [**enumCertTemplateName**](iscrdenr-enumcerttemplatename.md)             | 列舉憑證範本名稱。<br/>                                                                                                                                                                                                                                                                                                                                                               |
| [**enumCSPName**](iscrdenr-enumcspname.md)                               | 列舉 (Csp) 的可用 [*密碼編譯服務提供者*](../secgloss/c-gly.md) 的名稱。<br/>                                                                                                                                                                                                               |
| [**getCACount**](iscrdenr-getcacount.md)                                 | 傳回願意根據指定憑證範本發出憑證的 Ca 數目。<br/>                                                                                                                                                                                                                                                                                                    |
| [**getCAName**](iscrdenr-getcaname.md)                                   | 取得指定憑證範本的指定 CA 名稱。<br/>                                                                                                                                                                                                                                                                                                                                 |
| [**getCertTemplateCount**](iscrdenr-getcerttemplatecount.md)             | 抓取憑證範本的數目。<br/>                                                                                                                                                                                                                                                                                                                                                           |
| [**getCertTemplateName**](iscrdenr-getcerttemplatename.md)               | 抓取憑證範本的名稱。<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**getCertTemplateSMIME**](iscrdenr-getcerttemplatesmime.md)             | 判斷憑證範本是否包含 szOID PKIX 的 \_ \_ \_ 電子郵件 \_ 保護金鑰使用方式。 如果此金鑰使用方式是憑證範本的一部分，憑證範本支援 [*安全/多用途網際網路郵件延伸*](../secgloss/s-gly.md) (S/MIME) 作業。<br/> |
| [**getEnrolledCertificateName**](iscrdenr-getenrolledcertificatename.md) | 抓取 [**ISCrdEnr：：註冊**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))的先前成功呼叫所產生的憑證名稱。 這個方法也可以用來在對話方塊中顯示憑證。<br/>                                                                                                                                                                                                 |
| [**getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)   | 從簽署憑證抓取主體名稱。 這個方法也可以用來在對話方塊中顯示憑證。 <br/>                                                                                                                                                                                                                                                                       |
| [**getUserName**](iscrdenr-getusername.md)                               | 抓取要作為憑證註冊目標之使用者的名稱。<br/>                                                                                                                                                                                                                                                                                                                   |
| [**resetUser**](iscrdenr-resetuser.md)                                   | 從智慧卡控制項清除使用者名稱。<br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)     | 顯示 [ **選取憑證** ] 對話方塊，允許簽署憑證 (也稱為要選取的 *註冊代理程式憑證*) 。<br/>                                                                                                                                                                                                                                                           |
| [**selectUserName**](iscrdenr-selectusername.md)                         | 顯示允許選取使用者名稱的 [ **選取使用者** ] 對話方塊。 使用者名稱會套用至代表憑證註冊的使用者。<br/>                                                                                                                                                                                                                                     |
| [**setCAName**](iscrdenr-setcaname.md)                                   | 指定 CA 的名稱。<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**setCertTemplateName**](iscrdenr-setcerttemplatename.md)               | 指定憑證範本的名稱。<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**setSigningCertificate**](iscrdenr-setsigningcertificate.md)           | 指定簽署憑證 (也稱為 *註冊代理程式憑證*) 。<br/>                                                                                                                                                                                                                                                                                                                      |
| [**setUserName**](iscrdenr-setusername.md)                               | 指定要在其上註冊憑證的使用者名稱。<br/>                                                                                                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>屬性

**ISCrdEnr** 介面具有這些屬性。



| 屬性                                         | 存取類型           | 描述                                                          |
|:-------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [**CSPCount**](iscrdenr-cspcount.md)<br/> | 唯讀<br/>  | 指定 Csp 的數目。 這是唯讀的屬性。<br/> |
| [**CSPName**](iscrdenr-cspname.md)<br/>   | 讀取/寫入<br/> | CSP 的名稱。 這是可讀寫的屬性。 <br/>        |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



 

 
