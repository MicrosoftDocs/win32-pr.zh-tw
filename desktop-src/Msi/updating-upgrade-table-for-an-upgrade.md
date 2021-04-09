---
description: 若要使用 Windows Installer 來套用主要升級，原始產品安裝套件必須指定 UpgradeCode 屬性（如準備應用程式以進行未來的主要升級所述），而且升級套件必須有升級資料表。
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: 更新升級的升級資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1b4c2cc2b650d49fb4ba40f97d69ed84911273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115080"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a>更新升級的升級資料表

若要使用 Windows Installer 來套用主要升級，原始產品安裝套件必須指定 [**UpgradeCode**](upgradecode.md) 屬性（如 [準備應用程式以進行未來的主要升級](preparing-an-application-for-future-major-upgrades.md)所述），而且升級套件必須有 [升級資料表](upgrade-table.md)。

如需有關主要升級的詳細資訊，請參閱[修補和升級](patching-and-upgrades.md)的[主要升級](major-upgrades.md)。

MNP2000.msi 的安裝套件指派了 [**UpgradeCode**](upgradecode.md) 屬性，如 [指定屬性](specifying-properties.md)一節中所述。

如果使用者已安裝1.0 至1.4 版的 MNP2000，則 Windows Installer 會套用升級， (包含的英文語言版本) 。 Windows Installer 將所有原始產品的功能設定遷移到升級的產品。 安裝程式會移除屬於產品升級未使用之原始產品的檔案。

如果您的 MNP2001.msi 副本不包含 [升級資料表](upgrade-table.md)、使用 Orca 或另一個資料表編輯器，將空的升級資料表從 Schema.msi 匯入至資料庫。 SDK 提供 Schema.msi 的複本。 使用您的資料庫編輯器開啟 MNP2001.msi，並將下列資料輸入空白的升級資料表中。



| UpgradeCode                            | VersionMin | VersionMax | 語言 | 屬性 | 移除 | ActionProperty |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} | 01.00.0000 | 01.40.0000 | 1033     | 769        |        | OLDAPPFOUND    |



 

[繼續](updating-properties-for-an-upgrade.md)

 

 



