---
title: 使用 Visual Studio 編譯範例應用程式
description: 使用 Visual Studio 編譯範例應用程式
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Windows Media 裝置管理員，範例
- 裝置管理員，範例
- 桌面應用程式、範例
- Windows Media 裝置管理員，桌面應用程式範例
- 裝置管理員，桌面應用程式範例
- 範例，桌面應用程式
- 範例，使用 Visual Studio 編譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf47f7a45ad17711145df810926fafb0f2aedcec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021218"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a>使用 Visual Studio 編譯範例應用程式

Windows Media 裝置管理員 SDK 包含與 Microsoft Visual Studio 2005 相容的 Visual Studio 解決方案。

在編譯範例應用程式之前，您必須將標頭檔 shtypes.idl 重新命名，以避免與 Microsoft Platform SDK 中的相同名稱的檔案發生衝突。 例如，您可以重新命名 <*sdk 安裝路徑* > \\ WMFSDK11 \\ 包含 \\ shtypes.idl，以 <*SDK 安裝路徑* > \\ WMFSDK11 \\ 包括 \\ shtypes.idl.. h. 備份。

若要建立應用程式，請啟動 Visual Studio 2005 的實例、開啟方案檔 wmdmapp .sln （位於資料夾 <*SDK 安裝路徑* > \\ WMFSDK11 apps wmdmapp 中）， \\ \\ 然後選擇 [**組建/組建] 方案** 選項。 這會建立兩個專案檔： helper 專案、proghelp vcproj，以及主要應用程式 wmdmapp。 vcproj。 此外，它還會建立進度協助程式 DLL 和主應用程式 (WMDMApp.exe) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**桌面應用程式範例**](sample-desktop-application.md)
</dt> </dl>

 

 




