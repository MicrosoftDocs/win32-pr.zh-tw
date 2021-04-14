---
description: 服務設定可讓 Windows Installer 自訂電腦上的服務。
ms.assetid: 164280b2-1c75-49d2-ac04-c3654be84134
title: 使用服務設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6e3040d51b1056a370490fc5328a6bafe07555
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468680"
---
# <a name="using-services-configuration"></a>使用服務設定

服務設定可讓 Windows Installer 自訂電腦上的 [服務](../services/services.md) 。 開發人員可以撰寫 Windows Installer 套件，在安裝期間使用 [ServiceControl](servicecontrol-table.md) 和 [ServiceInstall](serviceinstall-table.md) 資料表，以及 [InstallServices](installservices-action.md)、 [StopServices](stopservices-action.md) 和 [DeleteServices](deleteservices-action.md) 動作來安裝、停止、啟動和刪除服務。

從針對 Windows Installer 5.0 撰寫的封裝開始，開發人員也可以使用 [MsiConfigureServices](msiconfigureservices-action.md) 標準動作和 [MsiServiceConfig 資料表](msiserviceconfig-table.md) 來設定 Windows 7 和 windows Server 2008 R2 和 Windows Vista 和 windows server 2008 提供的擴充服務自訂選項。 針對未包含 MsiServiceConfig 資料表的 Windows Installer 版本所撰寫的現有安裝套件，仍然可以使用 Windows Installer 5.0 進行安裝。 Windows Installer 的 [服務設定] 功能無法設定網路服務帳戶、安裝共用服務主機 (svchost) 進程，或重新開機已在安裝過程中停止的服務。

**WINDOWS XP 和 Windows Server 2003 或更早版本：** 不支援。 從 windows 7 和 Windows Server 2008 R2 上執行的 Windows Installer 5.0 開始，以及在 Windows Vista 和 Windows Server 2008 上執行的 Windows Installer 4.5，皆可使用服務設定資料表和標準動作。

您必須在[InstallExecuteSequence](installexecutesequence-table.md)資料表中包含[MsiConfigureServices](msiconfigureservices-action.md)動作，以要求您在[MsiServiceConfig 資料表](msiserviceconfig-table.md)中指定的服務設定。 只有當 MsiConfigureServices 標準動作包含在順序資料表中時，Windows Installer 才會使用 MsiServiceConfig 資料表中的資訊。 MsiConfigureServices 標準動作也會使用 [ServiceControl](servicecontrol-table.md) 和 [ServiceInstall](serviceinstall-table.md) 資料表中的資訊。

若要要求系統只授與特定服務的必要許可權，請在 [MsiServiceConfig 資料表](msiserviceconfig-table.md)中指定服務和 **服務設定 \_ \_ 所需的 \_ 許可權 \_ 資訊** 設定選項。 從服務的進程權杖中移除不必要的許可權。 此選項可以用來設定在 LocalSystem、LocalService 或 NetworkService [服務使用者帳戶](../services/service-user-accounts.md)的安全性內容中執行的服務。

若要要求系統延遲啟動所有其他自動啟動服務之後的服務自動啟動，請在 [MsiServiceConfig 資料表](msiserviceconfig-table.md)中指定服務和 **服務設定 \_ \_ 延遲 \_ 自動 \_ 啟動** 選項。 目前的封裝必須安裝已延遲的服務，並 \_ \_ 在 [ServiceInstall](serviceinstall-table.md) 資料表中指定服務自動啟動，否則服務必須已安裝為自動啟動服務。

若要要求系統保留特定服務專屬使用的資源，請在 [MsiServiceConfig 資料表](msiserviceconfig-table.md)中指定服務、服務 SID 類型和 **服務設定 \_ \_ 服務 \_ sid \_ 資訊** 設定選項。 將服務的 SID 新增至資源的存取控制清單， (資源的 ACL) 。

若要要求 [服務控制管理員](../services/service-control-manager.md) (SCM) 在將 **服務 \_ 控制 \_ PRESHUTDOWN** 通知傳送至服務之後等候，請執行下列動作。 指定服務、SCM 應等候的時間長度，以及 [MsiServiceConfig 資料表](msiserviceconfig-table.md)中的 **服務 \_ 設定 \_ PRESHUTDOWN \_ 資訊** 設定選項。

若要設定系統在服務失敗後應執行動作的時機，請在 [MsiServiceConfig 資料表](msiserviceconfig-table.md)中指定服務和 **服務設定 \_ \_ 失敗 \_ 動作 \_ 旗** 標選項。 將要執行的動作加入至 [MsiServiceConfigFailureActions 資料表](msiserviceconfigfailureactions-table.md)。

如需 Windows Vista 和 Windows Server 2008 作業系統所引進的擴充服務自訂功能的詳細資訊，請參閱 [Windows vista 的服務變更](../services/service-changes-for-windows-vista.md)。

 

 
