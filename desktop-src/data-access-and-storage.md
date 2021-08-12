---
description: Windows 具有 api、元件和服務，可在資料存取和儲存體中支援您的桌面應用程式。
ms.assetid: 8097ee91-f9f9-4e49-a501-5c54153eced8
title: 資料存取和儲存體
ms.topic: reference
ms.date: 02/06/2019
ms.openlocfilehash: cb921444d38516c1ec45a2e7f115166714f5a75f0372f74a030fe46531050fbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545529"
---
# <a name="data-access-and-storage"></a>資料存取和儲存體

Windows 具有 api、元件和服務，可在資料存取和儲存體中支援您的桌面應用程式。 它們提供：

-   檔案和檔案系統管理。
-   資料庫存取。
-   資料傳輸、同步處理和複寫的支援。
-   存取 XML、封裝和記錄檔。
-   映射主控。
-   備份支援。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                            | 描述                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [背景智慧型傳送服務](/windows/desktop/Bits/background-intelligent-transfer-service-portal)<br/>        | 背景智慧型傳送服務 (BITS) 會在用戶端和伺服器之間傳輸檔案 (下載或上傳)，並提供有關傳輸的進度資訊。 您也可以從對等端下載檔案。 <br/>                                                                          |
| [Backup](/windows/desktop/Backup/backup)<br/>                                              | 備份和還原的登錄機碼可讓備份應用程式與其他應用程式和服務進行備份和還原作業的通訊。 磁帶備份 API 可讓備份應用程式將資料封存到磁帶。  (SIS) API 的單一實例存放區可讓備份應用程式使用 SIS 架構，以最少的額外負荷來維護重複的檔案。 原始加密 API 可讓您備份及還原加密的檔案。<br/> |
| [雲端同步引擎](cfapi/cloud-files-api-portal.md)<br/>                                                   | 從 Windows 10 版本1709開始，Windows 提供雲端檔案 *API*。 此 API 會將雲端同步引擎的支援正規化，並處理工作，例如建立和管理預留位置檔案和目錄。 此 API 的使用者通常是同步處理提供者，而 Windows 應用程式的範圍。<br/>                   |
| [通用記錄檔系統](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)<br/>                                            | 通用記錄檔系統 (CLFS) API 提供可供專用用戶端應用程式使用的高效能、一般用途的記錄檔子系統，以及多個用戶端可共用以將記錄存取優化。<br/>                                                                                          |
| [分散式檔案系統](/previous-versions/windows/desktop/dfs/distributed-file-system)<br/>                                                | 分散式檔案系統 (DFS) 函式可讓您以邏輯方式將多部伺服器上的共用群組在一起，並以透明方式將共用連結至單一階層命名空間。<br/>                                                                                                             |
| [分散式檔案系統複寫](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)<br/>                | 分散式檔案系統 Replication (DFSR) service 是以狀態為基礎的多宿主複寫引擎，可支援複寫排程和頻寬節流。<br/>                                                                                                                           |
| [可擴充的儲存體引擎](/previous-versions/windows/desktop/Gg269259(v=EXCHG.10))<br/>         | 可延伸的儲存體引擎 (ESE) 是 (ISAM) 儲存體技術的先進索引和循序存取方法。 ESE 可讓應用程式使用索引或連續資料指標流覽來儲存和取出資料表中的資料。<br/>                                                                |
| [File 管理 API (FMAPI) ](/previous-versions/windows/desktop/fmapi/file-management-api--fmapi-)<br/>                                      | 檔案管理 Api 提供一種方式，讓開發人員從未加密的磁片區探索和還原已刪除的檔案。 檔案管理 Api 也可讓您使用密碼或修復金鑰檔，從 BitLocker 加密的磁片區探索和復原已刪除的檔案。<br/> |
| [映射主控 API](/windows/desktop/imapi/portal)<br/>                                                                   | 映射主控 API 可讓應用程式將映射預備和燒錄至 CD 和 DVD 光學儲存體媒體。 以相同方式配置影像的其他類似光碟的媒體也可以使用此 API。 <br/>                                                                                                      |
| [影像處理 API](/previous-versions/msdn10/dd851933(v=msdn.10))<br/>                 | Windows 影像處理介面參考會說明用來管理 Windows 映像 ( .wim) 檔案的程式設計方法。<br/>                                                                                                                                                                               |
| [iSCSI 探索程式庫 API](/previous-versions/windows/desktop/iscsidisc/iscsi-discovery-library-api-portal)<br/>                           | ISCSI 探索程式庫 API 可讓啟動器找出任何可存取的目標裝置，以及具有最少量必要設定的相關聯位址。<br/>                                                                                                                  |
| [iSCSI 軟體目標 API](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)<br/>                               | ISCSI 軟體目標 API 提供用於管理 Microsoft iSCSI 軟體目標的 WMI 介面，例如建立虛擬磁片並將其呈現給用戶端。<br/>                                                                                                                             |
| [本機檔案系統](/previous-versions/windows/desktop/legacy/aa364407(v=vs.85))<br/>                                                                 | 描述目錄、磁片、檔案和磁片區管理。 也說明交易式 NTFS (TxF) 。<br/>                                                                                                                                                                                                 |
| [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85))<br/>                                                         | Microsoft XML Core Services (MSXML) 可讓使用 JScript、Visual Basic 腳本版本 (VBScript) 和 Microsoft Visual Studio 的客戶建立高效能的 XML 應用程式。<br/>                                                                                                   |
| [非動態記憶體程式庫 (NVML) ](./persistent-memory-programming-in-windows---nvml-integration.md)<br/> | 可讓開發人員利用 NVML api，在 Windows 環境中編寫持續性記憶體的程式碼。<br/>                                                                                                                                                                                           |
| [離線檔案](/previous-versions/windows/desktop/offlinefiles/offline-files-portal)<br/>                                                              | 離線檔案 API 可讓應用程式以程式設計方式控制和監視離線檔案的行為。<br/>                                                                                                                                                                                 |
| [包裝](/previous-versions/windows/desktop/opc/packaging)<br/>                                                                            | 封裝 Api 可提供應用程式的支援，這些應用程式會產生或取用與開放式封裝慣例相容的檔案（稱為套件）。<br/>                                                                                                                                      |
| [投射的檔案系統](ProjFS/projected-file-system.md)<br/>                                                                             | 投射的檔案系統 (ProjFS) 可讓使用者模式應用程式在檔案系統中投影階層式資料存放區，並在其中顯示為檔案和目錄。  內容會視需要快取到本機檔案系統，讓極大型的資料存放區在本機出現，而不會有太大的本機儲存體。<br/> |
| [遠端差異壓縮](/previous-versions/windows/desktop/rdc/remote-differential-compression)<br/>                                | 遠端差異壓縮 (RDC) 可讓應用程式以有效率的方式在兩部電腦之間同步處理資料。<br/>                                                                                                                                                                      |
| [使用者狀態管理 API](/previous-versions/windows/desktop/usm/user-state-management-api-portal)<br/>                                     | 使用者狀態管理 API 提供另一種方式來設定和取得與使用者狀態相關之 Windows 元件的目前狀態。 透過這些 api 公開設定和狀態的 Windows 元件是資料夾重新導向、離線檔案和漫遊設定檔。<br/> |
| [虛擬磁碟服務](/windows/desktop/VDS/virtual-disk-service-portal)<br/>                                              | 虛擬磁碟服務 (VDS) 管理各種不同的存放裝置設定，從單一磁片桌面到外部存放裝置陣列。<br/>                                                                                                                                                             |
| [虛擬儲存體](/windows/desktop/VStor/virtual-storage)<br/>                                                              | 虛擬硬碟 (VHD) 格式是一種公開可用的映射格式規格，可指定封裝在單一檔案中的虛擬硬碟，而且能夠裝載原生檔案系統，同時支援標準磁片和檔案作業。<br/>                                               |
| [磁碟區陰影複製服務](/windows/desktop/VSS/volume-shadow-copy-service-portal)<br/> | 磁碟區陰影複製服務 (VSS) 是一組 COM 介面，可在系統上的應用程式繼續寫入磁片區時，利用這些介面來執行架構，以允許進行磁片區備份。<br/>                                                                                                                                                                                                                                                           |
| [Windows Data Access Component](/previous-versions/windows/desktop/legacy/aa968814(v=vs.85))<br/>                                | Windows資料存取元件 (Windows DAC) 6.0 是一組技術，可讓您存取整個企業中的資訊。 這些技術包括 microsoft ActiveX Data Objects (ADO) 、OLE DB 和 microsoft 開放式資料庫連接 (ODBC) 。<br/>                                    |
| [Windows 儲存裝置管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)<br/>                      | Windows 儲存體管理 API 用來管理各種不同的儲存體設定，從單一磁片桌面到外部存放裝置陣列都是如此。<br/>                                                                                                                                               |
| [Windows同步](/previous-versions/windows/desktop/winsync/windows-sync)<br/>                                                                  | Microsoft Windows 同步 API 可讓開發人員撰寫自訂同步處理提供者，讓裝置能夠與電腦或網路上的資料存放區同步處理資料。<br/>                                                                                                   |
| [NFS 的 WMI 提供者](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)<br/>                                            | Microsoft Services for Network File System (NFS) 提供檔案共用解決方案，可讓您在執行 Windows 的電腦和協力廠商作業系統之間，使用 NFS 通訊協定來傳輸檔案。<br/>                                                                                 |
| [XmlLite](/previous-versions/windows/desktop/ms752872(v=vs.85))<br/>                                                       | XmlLite 是輕量的 XML 剖析器，專為方便使用、效能和標準合規性而設計。<br/>                                                                                                                                                                                             |



 

 

