---
description: 描述如何在執行一般電腦和網路管理工作的腳本和應用程式中，尋找要使用的正確 WMI 類別和程式。
ms.assetid: fe15b67c-8ae6-4360-a2ee-1eda292dd05a
ms.tgt_platform: multiple
title: 腳本和應用程式的 WMI 工作
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e2a18791f5055a7574b9e130cf10c0cd1246f6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513060"
---
# <a name="wmi-tasks-for-scripts-and-applications"></a>腳本和應用程式的 WMI 工作

下列各節說明各種電腦和網路管理工作，並提供用來執行這些工作的 WMI 類別或類別的連結。 如需詳細資訊，請參閱 [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)。 如需使用 WMI 的詳細資訊，請參閱 [進一步的資訊](further-information.md)。 如需有關使用 WMI 的詳細資訊，請參閱 [TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)。  (這些資源可能無法在每個語言或國家/地區使用。 ) 

如需如何將資料提供給 WMI 的詳細資訊，請參閱 [使用 wmi](using-wmi.md)，其將參考有關撰寫 WMI [*提供者*](gloss-p.md)的主題。

腳本範例中所顯示的作業可以由 c + + 或 Visual Basic 中的應用程式執行。 如需詳細資訊，請參閱 [使用 c + +](creating-a-wmi-application-using-c-.md) 和 [Wmi c + + 應用程式範例](wmi-c---application-examples.md)建立 wmi 應用程式。

下表列出工作的分類。



| 工作分類                                                               | Description                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [帳戶和網域](wmi-tasks--accounts-and-domains.md)                   | 取得電腦網域或目前登入的使用者之類的資訊。 許多網域或帳戶相關的工作，最好是使用 [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) 腳本來執行。 如需範例，請參閱 TechNet ScriptCenter，網址為 [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 。 |
| [電腦硬體](wmi-tasks--computer-hardware.md)                         | 取得硬體元件的狀態、狀態或屬性的相關資訊。 例如，您可以判斷電腦是否為桌上型電腦或膝上型電腦。                                                                                                                                                                                             |
| [電腦軟體](wmi-tasks--computer-software.md)                         | 取得 Windows Installer (MSI) 和軟體版本所安裝的軟體等資訊。                                                                                                                                                                                                                                              |
| [連接至 WMI 服務](wmi-tasks--connecting-to-the-wmi-service.md) | 若要從本機電腦或從遠端電腦取得 WMI 的資料，您必須連接到特定的 [*命名空間*](gloss-n.md)，以連線至 wmi 服務。 在大部分情況下，請使用速記的 [標記](creating-a-wmi-script.md) 連接或 [**定位器**](swbemlocator-connectserver.md) 連接。    |
| [日期和時間](wmi-tasks--dates-and-times.md)                             | 有 WMI 類別和腳本物件可剖析或轉換 [CIM datetime](date-and-time-format.md) 格式。                                                                                                                                                                                                                                     |
| [桌面管理](wmi-tasks--desktop-management.md)                       | 從遠端桌面取得或控制資料。 例如，您可以判斷螢幕保護裝置是否需要密碼。 WMI 也提供您關閉遠端電腦的能力。                                                                                                                                                               |
| [磁片和檔案系統](wmi-tasks--disks-and-file-systems.md)               | 取得磁片磁碟機硬體狀態的相關資訊、邏輯磁片區。                                                                                                                                                                                                                                                                                      |
| [事件記錄](wmi-tasks--event-logs.md)                                       | 從 NT 事件記錄檔取得事件資料，並執行備份或清除記錄檔等作業。                                                                                                                                                                                                                                                   |
| [檔案和資料夾](wmi-tasks--files-and-folders.md)                         | 透過 WMI 變更檔案或資料夾屬性，包括建立共用或重新命名檔案。                                                                                                                                                                                                                                                              |
| [網路功能](wmi-tasks--networking.md)                                       | 管理和取得連線和 IP 或 MAC 位址的相關資訊。                                                                                                                                                                                                                                                                                  |
| [作業系統](wmi-tasks--operating-systems.md)                         | 取得作業系統的相關資訊，例如版本、是否已啟用，或已安裝的修補程式。                                                                                                                                                                                                                                  |
| [效能監控](wmi-tasks--performance-monitoring.md)               | 使用從效能計數器取得資料的 WMI 類別，存取和重新整理有關電腦效能的資料。                                                                                                                                                                                                                                     |
| [處理序](wmi-tasks--processes.md)                                         | 取得資訊，例如正在執行進程的帳戶。 您可以執行動作，例如建立進程。                                                                                                                                                                                                                                 |
| [印表機與列印](wmi-tasks--printers-and-printing.md)                 | 管理和取得印表機的相關資料，例如尋找或設定預設印表機。                                                                                                                                                                                                                                                                    |
| [登錄](wmi-tasks--registry.md)                                           | 建立和修改登錄機碼和值。                                                                                                                                                                                                                                                                                                               |
| [排定的工作](wmi-tasks--scheduled-tasks.md)                             | 建立並取得已排程工作的相關資訊。                                                                                                                                                                                                                                                                                                         |
| [服務](wmi-tasks--services.md)                                           | 取得服務的相關資訊，包括相依或之前的服務。                                                                                                                                                                                                                                                                            |



 

 

 
