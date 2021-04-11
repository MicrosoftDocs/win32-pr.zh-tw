---
description: Windows Management Instrumentation (WMI) 是 Microsoft 在 Web 架構企業管理 (WBEM) 方面的實作，這是一種開發標準技術的業界措施，用於存取企業環境中的管理資訊。
ms.assetid: d745cf25-a139-439d-9ac5-e7720b640516
ms.tgt_platform: multiple
title: 關於 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cf42ead6c3ae1b364ab8f83c83a744afa28734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320343"
---
# <a name="about-wmi"></a>關於 WMI

Windows Management Instrumentation (WMI) 是 Microsoft 在 Web 架構企業管理 (WBEM) 方面的實作，這是一種開發標準技術的業界措施，用於存取企業環境中的管理資訊。 WMI 使用通用訊息模型 (CIM) 業界標準來代表系統、應用程式、網路、裝置和其他受管理元件。 CIM 是由分散式管理工作強制 ([DMTF](https://www.dmtf.org/standards/wsman)) 所開發及維護。

> [!Note]  
> 新一代的 WMI （稱為 Windows 管理基礎結構 (MI) ）目前可供使用。 MI 與舊版 WMI 完全相容，並提供一系列的功能和優點，讓設計和開發提供者和用戶端比以往更容易。 例如，許多較新的提供者都是使用 MI 架構來撰寫，但可以使用 WMI 腳本和應用程式來存取。 如需這兩種技術之間差異的詳細資訊，請參閱 [為何要使用 MI？](/previous-versions/windows/desktop/wmi_v2/why-use-mi-)

 

## <a name="managing-remote-computer-systems-with-wmi"></a>使用 WMI 管理遠端電腦系統

從遠端電腦獲取管理資料的能力就是 WMI 的用途。 遠端 WMI 連線是透過 DCOM 完成的。 替代方法是使用 Windows 遠端管理 ([WinRM](/windows/desktop/WinRM/portal)) ，它會使用以 WS-Management SOAP 為基礎的通訊協定取得遠端 WMI 管理資料。

## <a name="programming-with-wmi"></a>使用 WMI 進行程式設計

管理應用程式或腳本可以透過各種語言的 WMI 取得資料或執行作業。 如需詳細資訊，請參閱 [Windows Management Instrumentation](wmi-start-page.md)的「開發人員物件」一節。

許多 Windows 功能都有相關聯的 WMI 提供者，例如 [開機設定資料 (BCD) 提供者](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) 或 [存放磁片區提供者](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)。 WMI 提供者會執行 WMI 類別方法和屬性所描述的功能，以管理相關聯的 Windows 功能。 如需詳細資訊，請參閱 [Wmi 提供者](wmi-providers.md) 和 [wmi 類別](wmi-classes.md)。

如需如何撰寫提供者以提供新硬體或應用程式資料的詳細資訊，請參閱 [將資料提供給 WMI](providing-data-to-wmi.md)。

如需如何執行這項技術的詳細資訊，請參閱 [使用 WMI](using-wmi.md)。

下表列出本節所包含的主題。



| 區段                                                                                                | 描述                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WMI 的新功能](what-s-new-in-wmi.md)                                                             | WMI 中的新功能。                                                                                                                                                                                                                              |
| [WMI 元件的作業系統可用性](operating-system-availability-of-wmi-components.md) | 某些元件已無法再使用，或可作為選擇性安裝。                                                                                                                                                             |
| [WMI 架構](wmi-architecture.md)                                                               | 管理應用程式會使用各種不同的介面（例如 Visual Basic、c + +、ODBC 和 ActiveX）來與 WMI 通訊。 所有 WMI 介面都是以元件物件模型為基礎， (COM) 。                                              |
| [通用訊息模型](common-information-model.md)                                               | 與語言無關的程式設計模型，使用物件導向技術來描述企業。                                                                                                                                          |
| [受管理物件格式](managed-object-format--mof-.md)                                               | 一種格式，可讓您建立人們看得懂的程式碼，作業系統可以將它轉譯成一組 CIM 類別。 您可以使用新的類別來為企業建立新技術的模型並加以控制。                                 |
| [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)                                       |  (UAC) 的使用者帳戶控制會影響傳回的 WMI 資料、遠端存取，以及腳本必須如何執行。 如需詳細資訊，請參閱 [使用 Windows Vista 的使用者帳戶控制開始使用](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista)。 |
| [存取 WMI 安全物件](access-to-wmi-securable-objects.md)                                 | WMI 使用標準的 Windows 安全性物件和程式來控制及保護對安全物件（例如 WMI 命名空間、印表機、服務及 DCOM 應用程式）的存取。                                                                      |
| [效能程式庫和 WMI](performance-libraries-and-wmi.md)                                     | 系統效能計數器中的資料可在 WMI 類別中使用。                                                                                                                                                                            |
| [WMI 中的 IPv6 和 IPv4 支援](ipv6-and-ipv4-support-in-wmi.md)                                       | WMI [IP 路由提供者](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) 和網路類別可提供 IPv4 位址的資料。 從 Windows Vista 開始，WMI 也提供對 IPv6 網路功能的有限支援。                                       |
| [日期和時間格式](date-and-time-format.md)                                                       | WMI 會使用分散式管理工作強制 CIM 規格所定義的日期和時間格式。 如需詳細資訊，請參閱「 [DMTF](https://www.dmtf.org/)」。                                                          |
| [腳本存取 WMI](scripting-access-to-wmi.md)                                                 | 撰寫 WMI 腳本來執行管理工作。                                                                                                                                                                                                    |
| [WMI 疑難排解](wmi-troubleshooting.md) \(英文\)                                                         | 存取應用程式或腳本中的 WMI 本機或遠端資料時，您可能會收到錯誤，範圍從遺漏的類別到拒絕存取。 提供者也有可用的偵錯工具選項和疑難排解類別。                           |
| [詳細資訊](further-information.md)                                                         | 關於 WMI 的網站、書籍和文章。                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WMI](using-wmi.md)
</dt> <dt>

[WMI 參考](wmi-reference.md)
</dt> </dl>

 

 
