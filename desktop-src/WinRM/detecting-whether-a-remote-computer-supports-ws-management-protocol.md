---
title: 偵測遠端電腦是否支援 WS-Management 的通訊協定
description: 您可以使用此會話。識別或 Iwsmansession.invoke。識別方法以判斷遠端電腦是否有支援 WS-Management 通訊協定的服務。
ms.assetid: 4d11ac02-fa8b-45d7-bceb-a18f561bc928
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82284b38b2a101c767766d44eb975ff7e1dadc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967425"
---
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a>偵測遠端電腦是否支援 WS-Management 的通訊協定

您可以使用此 [**會話。**](session-identify.md) 識別或 [**iwsmansession.invoke。識別**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) 方法以判斷遠端電腦是否有支援 WS-Management 通訊協定的服務。

如果在遠端電腦上設定了 WS-Management 的通訊協定服務，並且正在接聽要求，則服務可以透過標頭中的下列 XML 來偵測識別要求。


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



接收要求的 WS-Management 通訊協定服務會在訊息本文中傳回下列清單中所包含的資訊：

-   WS-Management 的通訊協定版本。 例如，"https://schemas.dmtf.org/wbem/wsman/1/wsman"。
-   產品廠商，例如「Microsoft Corporation」。
-   產品版本。 如果在 *旗標* 參數中使用 **WSManFlagUseNoAuthentication** 傳送要求，則不會傳回任何產品版本資訊。 如果要求是以作用中的預設驗證或指定的另一個驗證模式來傳送，則可以傳回產品版本資訊。

偵測遠端電腦是否有設定和接聽 WS-Management 通訊協定服務的要求，可以在腳本開頭與其他作業中執行。 這會確認目的電腦是否可以回應進一步 WS-Management 的通訊協定要求。 您也可以在個別的腳本中進行驗證。

**偵測 WS-Management 的通訊協定服務**

1.  建立 [**WSMan**](wsman.md) 物件。

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  判斷是否應將要求傳送至已驗證或未驗證，並且在 [**CreateSession**](wsman-createsession.md)的呼叫中適當地設定 *flags* 參數。

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  呼叫 [**會話。識別**](session-identify.md)。

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會將未經驗證的識別要求傳送至相同網域中名為 "Remote1" 的遠端電腦。


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



下列回應會顯示遠端電腦所傳回的 XML。 WS-Management 通訊協定版本 ( " https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd " ) 和作業系統廠商 ( "Microsoft Corporation" ) 是在傳回的 XML 中指定。 因為訊息會以未驗證的方式傳送，Windows 遠端管理服務不會傳回產品版本。


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



下列 VBScript 程式碼範例會將已驗證的識別要求傳送至遠端電腦。


```VB
set ObjWSMan = CreateObject("Wsman.Automation")
set objSession = WSMan.CreateSession("Remote1", _
  objWSMan.SessionFlagUseKerberos)
WScript.Echo objSession.Identify
```



由於要求是以驗證傳送，因此會傳回版本資訊。


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 6.0.5384 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> <dt>

[使用 Windows 遠端管理](using-windows-remote-management.md)
</dt> <dt>

[Windows 遠端管理參考](windows-remote-management-reference.md)
</dt> </dl>

 

 




