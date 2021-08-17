---
title: 投射的檔案系統程式設計指南
description: 有關執行 ProjFS 提供者應用程式的概念資訊。
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: d935c99b73e11a2110e739a4e45fdde0f7a24300a2664a2b25d6217bd2235fa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792541"
---
# <a name="projected-file-system-projfs-programming-guide"></a>投射的檔案系統 (ProjFS) 程式設計指南

Windows 投射的檔案系統 (ProjFS) 允許名為「提供者」的使用者模式應用程式將階層式資料投射到檔案系統，使其顯示為檔案系統中的檔案和目錄。

## <a name="in-this-section"></a>本節內容

| 主題                                                                                                       | 描述 |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [提供者總覽](provider-overview.md)                                                                   | 提供者應用程式的概念總覽。
| [虛擬化根中的快取狀態](cache-state.md)                                                    | 描述不同的快取狀態：提供者所管理的檔案或目錄可能具有。 
| [啟用 Windows 投射的檔案系統](enabling-windows-projected-file-system.md)                         | 說明如何啟用 ProjFS 選用元件。
| [虛擬化實例生命週期](virtualization-instance-lifecycle.md)                                   | ProjFS 虛擬化實例的生命週期總覽。
| [列舉檔案和目錄](enumerating-files-and-directories.md)                                   | 描述 ProjFS 提供者如何參與目錄列舉。
| [提供檔案資料](providing-file-data.md)                                                               | 描述提供者如何提供預留位置資訊和檔案資料。
| [檔案系統作業通知](file-system-operation-notifications.md)                               | 描述提供者如何接收檔案系統作業的通知。
| [處理視圖變更](handling-view-changes.md)                                                           | 說明如何更新提供者備份存放區的用戶端視圖。
| [非同步回呼處理](asynchronous-callback-handling.md)                                         | 描述提供者如何以非同步方式服務回呼。
| [Windows預計的檔案系統 API 參考](/windows/desktop/api/_projfs) | ProjFS 程式設計介面的參考資訊。

## <a name="additional-resources"></a>其他資源

| 主題                                                                                                             | 描述                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [RegFS 範例](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | 將 Windows 登錄投射到檔案系統的範例 ProjFS 提供者。 |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->