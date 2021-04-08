---
description: 此藍圖提供 Microsoft 提供的程式碼範例，示範如何在您的應用程式中使用其完成和程式碼片段。
ms.assetid: 3e55d32b-c036-4729-8b8f-d348d8b7cac4
title: RMS 案例、程式碼和工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07966769f72b48aa280223bdd061fabfbb509d62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691036"
---
# <a name="rms-scenarios-code-and-tools"></a>RMS 案例、程式碼和工具

此藍圖提供 Microsoft 提供的程式碼範例，示範如何完成此程式碼，以及您可以在應用程式中使用的程式碼片段。



| 項目                                                                                                                     | 作業系統           | 支援 SDK 版本                                                                                           | Description                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------|----------------------------|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [讀取 PFILE 保護的 PDF (英文)](/archive/blogs/rms/reading-a-pfile-protected-pdf)<br/> | Windows 桌面<br/> | [RMS SDK 2.1 和更新版本的 2.x SDK](/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal) | **讀取 PFILE 保護的 PDF** 是我們的 RMS 開發人員的專屬部落格上的簡單程式碼範例，其使用 MSIPC 檔案 API 來解密並開啟 PFILE 保護的 PDF 文件。<br/>                                                             |
| [IpcManagedAPI (英文)](https://github.com/AzureADSamples/rms-samples-for-net)<br/>                                        | Windows 桌面<br/> | [RMS SDK 2.1 和更新版本的 2.x SDK](/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal) | **IpcManagedAPI** 是為了方便受管理應用程式啟用 RMS 的 RMS SDK 2.1 的 .NET (C#) 表示法。<br/>                                                                                                       |
| [IPCNotepad](https://github.com/Azure-Samples/Azure-Information-Protection-Samples/tree/master/IpcNotepad)<br/>                                      | Windows 桌面<br/> | [RMS SDK 2.1 和更新版本的 2.x SDK](/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal) | **IPCNotepad** 是啟用 RMS 的應用程式範例，會帶領您完成每個啟用 RMS 的應用程式在保護和取用受限制的內容時應執行的基本步驟。<br/>                                          |
| [IpcDlp (英文)](https://github.com/AzureADSamples/rms-samples-for-net)<br/>                                               | Windows 桌面<br/> | [RMS SDK 2.1 和更新版本的 2.x SDK](/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal) | **IpcDlp** 是啟用 RMS 的資料流失防護 (DLP) 應用程式範例，會帶領您使用檔案 API 來保護和取用受限制的內容時，啟用 DLP RMS 的應用程式應執行的基本步驟。<br/> |
| [IpcAzureApp (英文)](https://github.com/AzureADSamples/rms-samples-for-net)<br/>                                          | Windows 桌面<br/> | [RMS SDK 2.1 和更新版本的 2.x SDK](/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal) | **IpcAzureApp** 是示範如何在 Azure 應用程式中使用 RMS SDK，以保護 Azure Blob 儲存體中資料的範例。<br/>                                                                                                          |
| [RmsDocumentInspector (英文)](https://github.com/AzureADSamples/rms-samples-for-net)<br/>                                 | Windows 桌面<br/> | [RMS SDK 2.1 和更新版本的 2.x SDK](/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal) | **RmsDocumentInspector** 是可提供任何 RMS 保護檔案相關資訊的工具，例如內容識別碼或使用者權限。<br/>                                                                                                               |
| [RmsFileWatcher (英文)](https://github.com/AzureADSamples/rms-samples-for-net)<br/>                                       | Windows 桌面<br/> | [RMS SDK 2.1 和更新版本的 2.x SDK](/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal) | **RmsFileWatcher** 是範例，示範如何建置 Windows 應用程式，在檔案系統中監看目錄，並在每次變更 RMS 保護原則，例如新增檔案或修改檔案。<br/>         |
| [iOS/OS X 使用案例](/previous-versions/windows/desktop/msipcthin2/ios-os-x-code-examples)<br/>                   | iOS / OS X<br/>      | [4.x SDK RMS SDK 4.2 和更新版本](/previous-versions/windows/desktop/msipcthin2/active-directory-rights-management-services-multi-platform-thin-client-sdk-portal) | **目標 C** 程式碼範例代表重要的開發案例，讓您習慣 RMS SDK。 範例包括使用 Microsoft 受保護的檔案格式、自訂受保護的檔案格式，以及自訂 UI 控制項。<br/>      |
| [UI 程式庫和範例應用程式 (英文)](https://github.com/AzureAD/rms-sdk-ui-for-ios)<br/>                                    | iOS<br/>             | [4.x SDK RMS SDK 4.2 和更新版本](/previous-versions/windows/desktop/msipcthin2/active-directory-rights-management-services-multi-platform-thin-client-sdk-portal) | GitHub 上的 **iOS 的 UI 程式庫和範例應用程式**，因此您可以快速地開始，並在您的應用程式中重複使用我們的標準 UI。<br/>                                                                                                            |
| [UI 程式庫和範例應用程式 (英文)](https://github.com/AzureAD/rms-sdk-ui-for-android)<br/>                                | Android<br/>         | [4.x SDK RMS SDK 4.2 和更新版本](/previous-versions/windows/desktop/msipcthin2/active-directory-rights-management-services-multi-platform-thin-client-sdk-portal) | GitHub 上的 **Android 的 UI 程式庫和範例應用程式**，因此您可以快速地開始，並在您的應用程式中重複使用我們的標準 UI。<br/>                                                                                                        |
| [Android 使用案例](/previous-versions/windows/desktop/msipcthin2/android-code)<br/>                    | Android<br/>         | [4.x SDK RMS SDK 4.2 和更新版本](/previous-versions/windows/desktop/msipcthin2/active-directory-rights-management-services-multi-platform-thin-client-sdk-portal) | **JAVA** 程式碼範例，代表可讓您習慣 RMS SDK 的重要開發案例。 範例包括使用 Microsoft 受保護的檔案格式、自訂受保護的檔案格式，以及自訂 UI 控制項。<br/>             |



 

 

