---
description: 若要使用 Windows Installer 來套用主要升級，原始產品安裝套件必須指定 UpgradeCode 屬性（如準備應用程式以進行未來的主要升級所述），而且升級套件必須有升級資料表。
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: 更新升級的升級資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba65db43019c09e27824c54265244c65b900e4f3c94dacd24405e7fac2e0272a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809748"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a>更新升級的升級資料表

若要使用 Windows Installer 來套用主要升級，原始產品安裝套件必須指定 [**UpgradeCode**](upgradecode.md)屬性（如 [準備應用程式以進行未來的主要升級](preparing-an-application-for-future-major-upgrades.md)所述），而且升級套件必須有 [升級資料表](upgrade-table.md)。

如需有關主要升級的詳細資訊，請參閱[修補和升級](patching-and-upgrades.md)的[主要升級](major-upgrades.md)。

MNP2000.msi 的安裝套件指派了 [**UpgradeCode**](upgradecode.md) 屬性，如 [指定屬性](specifying-properties.md)一節中所述。

Windows如果使用者已安裝1.0 至1.4 版)  (英文版的英文語言 MNP2000，安裝程式會套用升級。 Windows安裝程式會將所有原始產品的功能設定遷移到升級的產品。 安裝程式會移除屬於產品升級未使用之原始產品的檔案。

如果您的 MNP2001.msi 副本不包含 [升級資料表](upgrade-table.md)、使用 Orca 或另一個資料表編輯器，將空的升級資料表從 Schema.msi 匯入至資料庫。 SDK 提供 Schema.msi 的複本。 使用您的資料庫編輯器開啟 MNP2001.msi，並將下列資料輸入空白的升級資料表中。



| UpgradeCode                            | VersionMin | VersionMax | 語言 | 屬性 | 移除 | ActionProperty |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} | 01.00.0000 | 01.40.0000 | 1033     | 769        |        | OLDAPPFOUND    |



 

[繼續](updating-properties-for-an-upgrade.md)

 

 



