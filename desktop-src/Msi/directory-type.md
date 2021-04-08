---
description: 語義類型的目錄類型是其中一種主要格式類型，其中包含由使用者提供的目錄資料表中的外鍵。
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: 目錄類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3ba336dd5de7cd45ef9215f0397ba51ce544d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850220"
---
# <a name="directory-type"></a>目錄類型

[語義類型](semantic-types.md)的目錄類型是其中一種[主要格式類型](key-format-types.md)，其中包含由使用者提供的[目錄資料表](directory-table.md)中的外鍵。

合併工具必須將有效的 Windows Installer [識別碼](identifier.md) 取代為此類型的專案。 Mergemod.dll 不會強制執行這項限制，而是由「合併」工具組成，以確保使用者在目錄資料表中提供有效的金鑰。

目錄類型的可設定專案只能修改安裝的目的地目錄，而不會修改來源映射。 因此，此類型的可設定專案應只修改目錄資料表的外鍵，而不會直接修改目錄資料表。

因為 \_ [元件資料表](component-table.md) 的目錄資料行不可為 null，所以即使 msmConfigItemNonNullable 未在 [屬性] 資料行中設定，null 也是此類型的可設定專案的無效值。

目錄類型可搭配兩種 CoNtextData 使用。

**IsolationDirectory CoNtextData**

可設定的合併模組可以使用此類型，讓使用者能夠提供模組中檔案的目的地目錄。 合併工具會在 [ModuleSubstitution 資料表](modulesubstitution-table.md)的 [值] 資料行中，將目錄的識別碼取代為範本。 若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入目錄的名稱，在 [格式] 資料行中輸入 "1"，在 [類型] 資料行中輸入 "Directory"，然後在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 CoNtextData 資料行中輸入 "IsolationDirectory"。

**ShortcutLocation CoNtextData**

可設定的合併模組可以使用此類型，讓使用者能夠提供模組中快捷方式的目的地目錄。 合併工具會在 [ModuleSubstitution 資料表](modulesubstitution-table.md)的 [值] 資料行中，將快捷方式的識別碼取代為範本。 若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入目錄的名稱，在 [格式] 資料行中輸入 "1"，在 [類型] 資料行中輸入 "Directory"，然後在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 CoNtextData 資料行中輸入 "ShortcutLocation"。

 

 



