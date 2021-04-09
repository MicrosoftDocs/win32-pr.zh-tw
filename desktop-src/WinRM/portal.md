---
title: Windows 遠端管理
description: Windows 遠端管理 (Windows 遠端管理) 是 Microsoft WS-Management 通訊協定的採用，這是一種標準的 SOAP 型、可供防火牆使用的通訊協定，可讓不同廠商的硬體與作業系統交互操作。
ms.assetid: 6429e748-e0bf-431a-8989-db5b211665d5
ms.tgt_platform: multiple
keywords:
- Windows 遠端管理 (WinRM) 、起始頁
- WS-Management
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbOrient
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27311699fe0321eddc1d3117b17acf3e49e9d518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933270"
---
# <a name="windows-remote-management"></a>Windows 遠端管理

## <a name="purpose"></a>目的

Windows 遠端管理 (WinRM) 是 Microsoft 在 [WS-Management 通訊協定](ws-management-protocol.md)方面的實作，它是以簡易物件存取通訊協定 (SOAP) 為基礎、防火牆適用的通訊協定，允許不同廠商的硬體和作業系統互相操作。

WS-Management 通訊協定規格提供了一種常見的方式，讓系統在整個 IT 基礎結構之間存取及交換管理資訊。 WinRM 和 [*智慧型平臺管理介面 (IPMI)*](windows-remote-management-glossary.md)，而 [事件收集器](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) 則是 [Windows 硬體管理](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) 功能的元件。

## <a name="where-applicable"></a>適用時

您可以使用 WinRM 腳本物件、WinRM 命令列工具或 Windows 遠端 Shell 命令列工具 WinRS 來取得本機和遠端電腦上的管理資料，這些電腦可能會有 [*(bmc)*](windows-remote-management-glossary.md)的基礎板管理控制器。 如果電腦執行包含 WinRM 的 Windows 作業系統版本，管理資料會由 [Windows Management Instrumentation (WMI) ](/windows/desktop/WmiSdk/wmi-start-page)提供。

您也可以從企業中 Windows 以外的作業系統上執行的 WS-Management 通訊協定實作獲取硬體和系統資料。 WinRM 會透過以 SOAP 為基礎的 WS-Management 通訊協定與遠端電腦建立工作階段，而不是透過與 DCOM 的連線，就像 WMI 一樣。 傳回到 WS-Management 通訊協定的資料會使用 XML 格式，而不是物件格式。

[智慧型平臺管理介面 (IPMI) ](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI 提供者是標準的 wmi 提供者，其類別可從具有適當硬體的電腦取得 BMC 感應器資料。 您可以使用 WinRM 腳本 API、WMI [腳本](/windows/desktop/WmiSdk/scripting-api-for-wmi)或 [COM](/windows/desktop/WmiSdk/com-api-for-wmi) api 來存取 IPMI 資料。

## <a name="developer-audience"></a>開發人員對象

開發人員物件是一位 IT 專業人員，負責撰寫腳本，以自動化伺服器的管理，或 ISV 開發人員為管理應用程式取得資料。

## <a name="run-time-requirements"></a>執行階段需求求

WinRM 是作業系統的一部分。 不過，若要從遠端電腦取得資料，您必須 [*設定 WinRM 接聽*](windows-remote-management-glossary.md#l)程式。 如需詳細資訊，請參閱 [Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。 如果在系統啟動時偵測到 BMC，則會載入 IPMI 提供者;否則，仍然可以使用 WinRM 腳本物件和 WinRM 命令列工具。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> <dd>

連結至公用 WS-Management 通訊協定規格、WinRM 架構、與 WMI 的關聯性、使用 IPMI 提供者的硬體管理、設定和安裝。

</dd> <dt>

[使用 Windows 遠端管理](using-windows-remote-management.md)
</dt> <dd>

開始使用 WinRM 腳本 API 和硬體管理。

</dd> <dt>

[Windows 遠端管理參考](windows-remote-management-reference.md)
</dt> <dd>

由 Microsoft Web Services for Management 所定義的指令碼介面清單 (WS-MANAGEMENT) 自動化和由 IPMI 提供者所建立之 WMI 類別的類別定義，以及與 IPMI 驅動程式通訊的類別，以取得基礎板 [管理控制器 (BMC) ](windows-remote-management-glossary.md) 資料。

</dd> </dl>

 

 