---
description: 可以撰寫合併模組 ( .msm 檔案) ，以包含可由合併模組的取用者設定的屬性。
ms.assetid: 461436f0-3a91-4a49-934a-f975bf13df40
title: 可設定的合併模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716688d947ae84279dc3409bf97abe4eb58a69d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980065"
---
# <a name="configurable-merge-modules"></a>可設定的合併模組

可以撰寫合併模組 ( .msm 檔案) ，以包含可由合併模組的取用者設定的屬性。 這可讓合併模組在安裝套件和模組與使用者合併及安裝時進行設定。 可設定的合併模組需要 Mergemod.dll 2.0 版，但可以在任何版本的 Windows Installer 上執行。

可設定合併模組的執行是由兩個部分所組成。 首先，建立合併模組 ( .msm 檔) 時，合併模組作者會將資訊加入模組資料庫，以指定可修改哪些專案，以及模組使用者如何設定這些專案。 作者將專案加入至[合併模組資料庫資料表](merge-module-database-tables.md)，這些資料表保留給可設定的資訊 ([ModuleConfiguration 資料表](moduleconfiguration-table.md)和[ModuleSubstitution 資料表](modulesubstitution-table.md)) 、更新[ \_ 驗證資料表](-validation-table.md)，以及將可設定合併模組資料表的專案加入至[ModuleIgnoreTable 資料表](moduleignoretable-table.md)。 ModuleIgnore 資料表的新增專案是使模組與2.0 之前的 Mergemod.dll 版本相容所需的專案。

其次，將模組合併到安裝套件 ( .msi 檔案) 時，模組的使用者會使用合併工具。 合併工具會呼叫 Mergemod.dll，以將模組中的設定資訊公開至用戶端設定工具。 設定工具可能與終端使用者互動，但不需要公開所有可能的設定選項。 如果使用者拒絕提供可設定專案的選取專案，模組可能會提供預設值。 當使用者提供設定工具的選取專案之後，合併工具就會呼叫 Mergemod.dll 來執行合併。

可設定的合併模組與早于 Mergemod.dll 2.0 版的工具完全相容。 在這些情況下，工具會使用模組中的預設值。

如需詳細資訊，請參閱 [使用可設定的合併模組](using-configurable-merge-modules.md)。

 

 



