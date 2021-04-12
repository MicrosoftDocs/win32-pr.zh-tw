---
description: 合併模組提供一種標準方法，讓開發人員將共用 Windows Installer 元件和設定邏輯提供給其應用程式。
ms.assetid: 673de3ff-e58c-4153-9c8d-c3baebba5eb1
title: 合併模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499368b309909bcb06da45476d43d8cac28e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195088"
---
# <a name="merge-modules"></a>合併模組

合併模組提供一種標準方法，讓開發人員將共用 Windows Installer [*元件*](c-gly.md) 和設定邏輯提供給其應用程式。 合併模組是用來將共用程式碼、檔案、資源、登錄專案和安裝程式邏輯傳遞給應用程式，做為單一複合檔案。 撰寫新合併模組或使用現有合併模組的開發人員，應該遵循本節所述的標準。

合併模組在結構上類似于簡化的 Windows Installer [*.msi*](m-gly.md)檔。 不過，合併模組無法單獨安裝，它必須使用合併工具合併到安裝套件中。 想要使用合併模組的開發人員必須取得其中一個自由散發的合併工具，例如 Mergemod.dll，或向獨立軟體廠商購買合併工具。 開發人員可以使用許多用來建立 Windows Installer 安裝套件的相同軟體工具來建立新的合併模組，例如 Windows Installer SDK 所提供的資料庫資料表編輯器 Orca。

合併模組合併到應用程式的 .msi 檔案時，安裝合併模組所提供的元件所需的所有資訊和資源都會併入應用程式的 .msi 檔案中。 然後再也不需要合併模組來安裝這些元件，而且使用者不需要再存取合併模組。 由於安裝元件所需的所有資訊都是以單一檔案的形式提供，因此使用合併模組可以排除許多版本衝突實例、遺失登錄專案，以及不正確安裝的檔案。

如需合併模組的詳細資訊，請參閱：

-   [關於合併模組](about-merge-modules.md)
-   [使用合併模組](using-merge-modules.md)
-   [合併模組參考](merge-module-reference.md)

 

 



