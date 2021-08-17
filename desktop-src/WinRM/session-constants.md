---
title: 會話常數
description: WSManSessionFlags 列舉中的會話常數 \_ \_ 會針對連線到遠端電腦的 WSMan. CreateSession 或 IWSMan CreateSession 呼叫指定驗證和其他資訊。
ms.assetid: 5df52696-ac2c-42b7-8b0f-99a27b58575b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584eb15c4b235a006b52551de8f9999ddb65459412af68db81f0500a0828888b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743222"
---
# <a name="session-constants"></a>會話常數

**\_ \_ WSManSessionFlags** 列舉中的會話常數會指定 [**CreateSession**](wsman-createsession.md)或 [**IWSMan：： CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)呼叫的驗證和其他資訊，以連接到遠端電腦。 這些常數也與 **Winrm** 命令列工具參數密切相關。

## <a name="using-session-constants"></a>使用會話常數

您可以透過兩種不同的方式，設定 [**CreateSession**](wsman-createsession.md) 呼叫的會話旗標。 其中一個是較短且更簡單的。 如下列範例所示，較長的方法是找出您想要使用的旗標值，並在腳本中使用該值建立常數。 然後，常數會用來設定 *iFlags* 參數的值。

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

如下列範例所示，建議的方式是使用與旗標相關聯的 [**WSMan**](wsman.md) 物件方法。

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**驗證常數**](authentication-constants.md)
</dt> <dd>

指定驗證方法，以及如何處理憑證伺服器。

</dd> <dt>

<span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**其他會話常數**](other-session-constants.md)
</dt> <dd>

指定編碼、加密和服務主體名稱埠。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WinRM 常數和列舉](winrm-constants-and-enumerations.md)
</dt> <dt>

[**WSMan. CreateSession**](wsman-createsession.md)
</dt> <dt>

[遠端連線的驗證](authentication-for-remote-connections.md)
</dt> </dl>

 

 




