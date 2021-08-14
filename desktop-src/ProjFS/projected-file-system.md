---
title: Windows投射的檔案系統
description: '概述 Windows 投射的檔案系統 (ProjFS) '
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/14/2018
ms.topic: article
ms.openlocfilehash: d5cb20b123e72ec8e031036019a16ef1bbe2b8dc4b9bb53446c8faaced4d796b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792655"
---
# <a name="windows-projected-file-system-projfs"></a>Windows投射的檔案系統 (ProjFS) 

Windows 投射的檔案系統 (ProjFS) 允許稱為「提供者」的使用者模式應用程式，將階層式資料從支援資料存放區投射到檔案系統，使其顯示為檔案系統中的檔案和目錄。 例如，簡單的提供者可以將 Windows 登錄投射到檔案系統中，讓登錄機碼和值分別顯示為檔案和目錄。 更複雜的提供者範例是 [適用于 git 的 VFS](https://github.com/Microsoft/VFSForGit)，可用來將非常大型的 git 存放庫虛擬化。

> [!NOTE]
> ProjFS 的設計目的是要搭配高速支援資料存放區使用。 其中一個設計目標是要讓投射的資料看起來像是在本機出現，並隱藏資料可能是遠端的事實。 因此，ProjFS 並不提供：報告資料回收進度的機制;指出檔案的線上與離線狀態;以及當您使用緩慢的支援資料存放區時，可能需要的其他功能。 在這類情況下，請考慮改為使用 [雲端檔案 API](../cfapi/cloud-files-api-portal.md)。

## <a name="in-this-section"></a>本節內容

| 主題                                                                                                       | 描述 |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Windows投射的檔案系統程式設計指南](projfs-programming-guide.md)                              | 有關執行 ProjFS 提供者應用程式的概念資訊。
| [Windows預計的檔案系統 API 參考](projfs-reference.md)                                          | ProjFS 程式設計介面的參考資訊。
| [Windows預計的檔案系統詞彙](projfs-glossary.md)                                                | ProjFS 中使用的特殊字詞。

## <a name="additional-resources"></a>其他資源

| 主題                                                                                                             | 描述                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [RegFS 範例](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | 將 Windows 登錄投射到檔案系統的範例 ProjFS 提供者。 |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->