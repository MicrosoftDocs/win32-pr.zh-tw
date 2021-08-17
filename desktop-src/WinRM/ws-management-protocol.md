---
title: WS-Management 通訊協定
description: 公用標準，可從遠端與任何執行通訊協定的電腦裝置交換管理資料。
ms.assetid: 2c47acd2-5d52-4e0f-8848-a11aff59f963
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a20900e77d7d686868e00f7067b23fff644255997a14c9d4c1cbdcf3d1951d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742729"
---
# <a name="ws-management-protocol"></a>WS-Management 通訊協定

WS-Management 通訊協定是由一組硬體和軟體製造商開發的一個公用標準，用來從遠端與實作通訊協定的任何電腦裝置交換管理資料。

## <a name="standards"></a>標準

如需 WS-Management 通訊協定的詳細資訊，請參閱 [管理的 Web 服務 (ws-management) 規格](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf)。

通訊協定的目的是要為各種裝置類型的管理作業提供一致性和互通性， (包括固件) 和作業系統。 您可以擴充 WS-Management 的通訊協定，因為 IT 產業會識別新的作業。

WS-Management 通訊協定目前的執行是以下列標準規格為基礎： HTTPS、SOAP over HTTP (WS-I 設定檔) 、SOAP 1.2、WS-ADDRESSING、WS-Transfer、WS-ADDRESSING 和 WS-事件。 如需 WS-Management 標準和 XML 架構的詳細資訊，請參閱 <https://dmtf.org/standards/wsman>

## <a name="messages"></a>訊息

WS-Management 通訊協定提供使用各種 web 服務標準（例如 [*ws-addressing*](windows-remote-management-glossary.md)和 [*ws-傳輸*](windows-remote-management-glossary.md)）來建立 XML [*訊息*](windows-remote-management-glossary.md)的標準。 這些標準會定義 web 服務訊息的 XML 架構。 這些訊息會使用 [*資源 URI*](windows-remote-management-glossary.md)來參考 [*資源*](windows-remote-management-glossary.md)。 WS-Management 通訊協定會為管理作業和值新增一組定義。 例如，WS-Transfer 會定義資源的 Get、Put、Create 和 Delete 作業。 WS-Management 通訊協定會新增重新命名、部分取得和部分 Put。

這些訊息遵循了 [*簡單物件存取通訊協定的慣例， (SOAP)*](windows-remote-management-glossary.md) ，而這些都是由所有的 web 服務通訊協定所使用。

下列程式碼範例顯示含有 Get 作業的訊息。 此範例會顯示為協助您瞭解基礎訊息的外觀。 您不需要知道如何產生 SOAP 訊息。 當您使用 **winrm** 命令列工具執行命令或執行以 [winrm 腳本 API](winrm-scripting-api.md)撰寫的腳本時，Windows 遠端管理會將這些訊息組合。

此訊息是從名為 RemoteComputer 的伺服器取得具有 **DeviceID** 屬性 "c：" 的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)實例的要求。 要求會透過埠80使用 HTTP 傳輸。 傳送要求的帳戶必須位於遠端電腦上的本機系統管理員群組中。

每個標記開頭的冒號前面的字元會指出哪個標準定義了 XML 元素。 例如， ` <wsa:To>` 表示 To 專案是由 WS-Addressing 標準所定義，並 `<s:Header>` 指出 SOAP 訊息中標頭內容的開頭。 請注意，大部分的訊息都是由 SOAP 或 WS-ADDRESSING 所定義的 XML 元素所組成。 WS-Management 通訊協定會新增 MaxEnvelopeSize、選取器和 SelectorSet。


```XML
<s:Envelope xmlns:s="https://www.w3.org/2003/05/soap-envelope" 
            xmlns:a="https://schemas.xmlsoap.org/ws/2004/08/addressing" 
            xmlns:w="https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd">
  <s:Header>
    <a:To>https://RemoteComputer:80/wsman</a:To> 
    <w:ResourceURI s:mustUnderstand="true">
      http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_logicaldisk
    </w:ResourceURI> 
    <a:ReplyTo>
    <a:Address s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </a:Address> 
    </a:ReplyTo>
    <a:Action s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </a:Action> 
    <w:MaxEnvelopeSize s:mustUnderstand="true">153600</w:MaxEnvelopeSize> 
    <a:MessageID>uuid:4ED2993C-4339-4E99-81FC-C2FD3812781A</a:MessageID> 
    <w:Locale xml:lang="en-US" s:mustUnderstand="false"/> 
    <w:SelectorSet>
    <w:Selector Name="DeviceId">c:</w:Selector> 
    </w:SelectorSet>
    <w:OperationTimeout>PT60.000S</w:OperationTimeout> 
  </s:Header>
  <s:Body/> 
</s:Envelope>
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> <dt>

[遠端硬體管理](remote-hardware-management.md)
</dt> </dl>

 

 