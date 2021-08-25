---
title: 關於 Windows 遠端管理
description: Windows遠端系統管理是 Windows 硬體管理功能的一個元件，可在本機和遠端管理伺服器硬體。
ms.assetid: f58add53-0746-4423-9ab8-02ba05f82fa7
ms.tgt_platform: multiple
keywords:
- 關於 Windows 遠端管理
- Windows遠端系統管理，關於
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a83df38de4af354f826b9bbba59ddab76e1b656c72e1c3dc74301da883f875cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858908"
---
# <a name="about-windows-remote-management"></a>關於 Windows 遠端管理

Windows遠端系統管理是[Windows 硬體管理](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10))功能的一個元件，可在本機和遠端管理伺服器硬體。 這些功能包括一項服務，此服務會透過基礎板管理控制器來執行 [*ws-management*](windows-remote-management-glossary.md) 通訊協定、硬體診斷和控制 ([*Bmc*](windows-remote-management-glossary.md)) ，以及 COM API 和 [腳本物件](winrm-scripting-api.md) ，可讓您撰寫透過 WS-Management 通訊協定從遠端通訊的應用程式。 如需 WS-Management 通訊協定之公用規格的詳細資訊，請參閱 [管理 (ws-management) 的 Web 服務 ](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf)。

## <a name="components-of-winrm-and-hardware-management"></a>WinRM 和硬體管理的元件

以下是 WinRM 和硬體監視所提供的元件和功能清單：

-   [WinRM 腳本 API](winrm-scripting-api.md)

    此腳本 API 可讓您使用執行 WS-Management 通訊協定作業的腳本，從遠端電腦取得資料。

-   **Winrm**

    這項適用于系統管理的命令列工具是在 Visual Basic 腳本版本檔案中執行， (Winrm.vbs 使用 WinRM 腳本 API 撰寫的) 。 此工具可讓系統管理員設定 WinRM，以及取得資料或管理資源。 如需詳細資訊，請參閱命令列 **Winrm** **/？** 所提供的線上說明。

-   **Winrs.exe**

    此命令列工具可讓系統管理員使用 WS-Management 通訊協定，從遠端執行大部分的 Cmd.exe 命令。 如需詳細資訊，請參閱命令列 **Winrs** **/？** 所提供的線上說明。

-   智慧型平臺管理介面 (IPMI) 驅動程式和 WMI 提供者

    透過 [*智慧型平臺管理介面 (IPMI)*](windows-remote-management-glossary.md) 提供者和驅動程式的硬體管理，可讓您在作業系統未執行或部署時，透過 bmc 控制及診斷遠端伺服器硬體。

    如需詳細資訊，請參閱 [IPMI 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)。

-   WMI 服務

    WMI 服務會繼續與 WinRM 並存執行，並透過 [*WMI 外掛程式*](windows-remote-management-glossary.md)提供要求的資料或控制。 您可以繼續從標準 WMI 類別（例如 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)），以及 IPMI 提供的資料取得資料。 如需 WinRM 所需設定和安裝的詳細資訊，請參閱 [硬體管理簡介](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10))。

-   WS-Management 通訊協定

    WS-Management 通訊協定（SOAP 型、可感知防火牆的通訊協定）是專為找出和交換管理資訊的系統所設計。 WS-Management 通訊協定規格的目的是要提供企業系統的互通性和一致性，讓電腦在不同廠商的各種作業系統上執行。

    WS-Management 通訊協定是以下列標準 web 服務規格為基礎： HTTPS、SOAP over HTTP (WS-I 設定檔) 、SOAP 1.2、WS-ADDRESSING、WS-Transfer、WS-Enumeration 和 WS-事件。 如需目前規格草稿的詳細資訊，請參閱 [管理規格索引頁面](/previous-versions/dotnet/articles/ms951267(v=msdn.10))。

## <a name="working-with-winrm"></a>使用 WinRM

如需有關撰寫 WinRM 腳本的詳細資訊，請參閱[使用 Windows 遠端管理](using-windows-remote-management.md)。

下表列出的主題提供有關 WS-Management 的通訊協定、WinRM 和 WMI 的資訊，以及如何指定磁片磁碟機或處理常式等管理資源。



| 主題                                                                                                                            | 描述                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows 遠端管理的安裝和設定](installation-and-configuration-for-windows-remote-management.md) | [*WinRM 接聽*](windows-remote-management-glossary.md)程式需要在用戶端和伺服器電腦上進行設定。                                                                                                                                                                                                                               |
| [Windows遠端系統管理架構](windows-remote-management-architecture.md)                                             | 說明 WinRM 元件的圖表，以及在用戶端和伺服器電腦上找到的元件。                                                                                                                                                                                                                                                               |
| [WS-Management 通訊協定](ws-management-protocol.md)                                                                             | 公用標準 WS-Management 通訊協定的說明，可從遠端傳送和接收管理資料到任何執行通訊協定的電腦裝置。                                                                                                                                                                                                             |
| [Windows 遠端管理中的腳本](scripting-in-windows-remote-management.md)                                             | WinRM 腳本 API 類似于 WS-Management 通訊協定的動作。 腳本所抓取的資料會以 XML 格式，而不是物件的格式。                                                                                                                                                                                                                                  |
| [遠端連線的驗證](authentication-for-remote-connections.md)                                               | WS-Management 通訊協定可支援多種標準的驗證方法和訊息加密，以維護電腦之間資料傳輸的安全性。                                                                                                                                                                                                                |
| [Windows遠端系統管理和 WMI](windows-remote-management-and-wmi.md)                                                       | 由於 WinRM 已與[Windows Management Instrumentation (WMI) ](/windows/desktop/WmiSdk/wmi-start-page)整合，因此您可以使用使用[winrm 腳本 API](winrm-scripting-api.md)的腳本或應用程式，或透過 winrm 命令列工具，來取得 WMI 資料。                                                                                                                     |
| [資源 URI](resource-uris.md)                                                                                               | [*資源 URI*](windows-remote-management-glossary.md)是管理作業或值的識別碼。 例如，磁片磁碟機代表一種資源類型。                                                                                                                                                                              |
| [遠端硬體管理](remote-hardware-management.md)                                                                     | [IPMI 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)所提供的[類別](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)和資料，會描述基礎板管理控制器 (BMC) 硬體管理網域、網域中的 bmc 電腦系統，以及 bmc 感應器。 其他物件代表 BMC 系統事件記錄檔 (的 SEL) 和記錄檔中的訊息。 |
| [事件](events.md)                                                                                                             | 您無法透過 WinRM 腳本取得事件，但您可以使用 Wevtutil.exe 命令列工具來查看 [事件收集器](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) 事件。                                                                                                                                                                                        |



 

 

 