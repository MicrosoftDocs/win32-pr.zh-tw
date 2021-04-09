---
description: 若要從另一個 (用戶端) 電腦遠端存取 COM + 伺服器應用程式，用戶端電腦必須安裝伺服器應用程式的屬性子集，包括 DCOM/QC 介面遠端的 proxy/stub Dll 和型別程式庫。
ms.assetid: 293b424c-4cd4-43a9-9b56-687c753a34f2
title: 部署應用程式 proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5e6439574602005ca53917945fa9005f8959b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936535"
---
# <a name="deploying-application-proxies"></a>部署應用程式 proxy

若要從另一個 (用戶端) 電腦遠端存取 COM + 伺服器應用程式，用戶端電腦必須安裝伺服器應用程式的屬性子集，包括 DCOM/QC 介面遠端的 proxy/stub Dll 和型別程式庫。 這個子集稱為「 *應用程式 proxy*」。

您可以透過 [元件服務] 系統管理工具，輕鬆地將 COM + 伺服器應用程式匯出為應用程式 proxy。 若要讓 COM + 產生應用程式 proxy，必須安裝並不匯入伺服器應用程式中的所有元件。  (如需此差異的詳細資訊，請參閱匯 [入元件](importing-components.md)。 ) 這可確保應用程式包含所有必要的註冊資訊。

> [!Note]  
> 建議您將介面定義與類別的執行區隔開。 否則，COM + 應用程式 proxy 中包含的一組 Dll 或類型程式庫將會包含實際的伺服器程式碼。

 

COM + 產生的應用程式 proxy 是 Windows Installer 安裝套件。 安裝之後，應用程式 proxy 會顯示在用戶端電腦的 [新增/移除程式] 控制台 (除非使用 Windows Installer authoring tool) 修改 .msi 檔案。

## <a name="remote-access-via-application-proxies"></a>透過應用程式 proxy 進行遠端存取

產生應用程式 proxy 時，COM + 會自動提供下列資訊，讓應用程式 proxy 從遠端存取 COM + 伺服器應用程式時需要這些資訊：

-   類別身分識別資訊 (Clsid 和 Progid) 。 應用程式 proxy 支援最多兩個 Progid。
-   應用程式識別，以及類別與應用程式 (AppID) 的關聯性。
-   每個應用程式的位置資訊 (遠端伺服器名稱) 。
-   封送處理應用程式公開的所有介面的資訊 (例如，輸入程式庫和 proxy/存根) 。
-   MSMQ 佇列名稱和識別碼 (是否已針對應用程式) 啟用佇列元件服務。
-   類別、介面和方法屬性，不包括角色資訊。
-   應用程式屬性。

## <a name="installing-application-proxies-on-other-operating-systems"></a>在其他作業系統上安裝應用程式 proxy

與 COM + 伺服器應用程式不同的是，應用程式 proxy 可以安裝在任何支援 DCOM (和 Windows Installer) 的作業系統上。 在未執行 COM + 的電腦上，只會安裝 DCOM 遠端處理所需的資訊子集。 這項資訊會安裝到 Windows 登錄 (使用 HKEY \_ 類別 \_ ROOT、APPID/CLSID 機碼) 。

> [!Note]  
> 在未執行 COM + 的電腦上安裝應用程式 proxy ( .msi 檔案) ，必須在這些電腦上執行 Windows Installer。 建議開發人員提供 Windows Installer 可轉散發檔案 (instmsi.exe) 以及其應用程式的 .msi 檔案。 這可確保系統管理員在未執行 COM + 的用戶端上部署應用程式 proxy 時，有 Windows Installer 可供使用。

 

在執行 COM + 的電腦上，應用程式 proxy 資訊會安裝在 COM + 目錄中，而且會顯示在 [元件服務] 系統管理工具中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立 COM + 應用程式的安裝套件](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[COM + 類別目錄](the-com--catalog.md)
</dt> <dt>

[COMREPL 複製公用程式](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



