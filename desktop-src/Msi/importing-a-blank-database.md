---
description: 若要重現範例，您必須使用軟體工具（Windows Installer 資料庫檔案）複製或建立。
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: 匯入空白資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b654b0de118013e8f211a9b06e896cc3f486faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193682"
---
# <a name="importing-a-blank-database"></a>匯入空白資料庫

若要重現範例，您必須使用軟體工具（Windows Installer 資料庫檔案）複製或建立。 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)提供了完全空白的安裝資料庫，Schema.msi。 SDK 也會提供部分空白的資料庫 uisample.msi，其中包含簡單使用者介面所需的建議順序資料表和資料。 製作 uisample.msi 的複本，並將它移至包含您在 [規劃安裝](planning-the-installation.md)時所建立之 [記事本] 資料夾的相同目錄中。 MNP2000.msi 重新命名檔案。 安裝資料庫檔案和來源檔案都必須位於相同目錄的根目錄中。 例如：

C： \\ 範例 \\MNP2000.msi

C： \\ 範例 \\ 記事本\\

如果您不使用 Uisample.msi，則必須取得空白的資料庫（例如 Schema.msi），並使用資料庫編輯工具（例如，在 SDK 中提供的 Orca）或其他資料庫編輯器來輸入安裝的資訊。

[繼續](specifying-directory-structure.md)

 

 



