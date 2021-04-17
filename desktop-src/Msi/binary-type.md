---
description: 語義類型的二進位類型是其中一種主要格式類型。 此類型是由使用者提供的二進位資料表中的索引鍵所組成。
ms.assetid: b6a25100-9f3e-4207-b56f-0c27ee16f188
title: 二進位類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda0711b53f865bbd844514ed2429d97d91e07a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513233"
---
# <a name="binary-type"></a>二進位類型

[語義類型](semantic-types.md)的二進位類型是其中一種[主要格式類型](key-format-types.md)。 此類型是由使用者提供的 [二進位資料表](binary-table.md) 中的索引鍵所組成。

合併工具必須將有效的 Windows Installer [識別碼](identifier.md) 取代為此類型的專案。 Mergemod.dll 不會強制執行這項限制，而是由「合併」工具組成，以確保使用者在二進位資料表中提供有效的金鑰。

除非 msmConfigItemNonNullable 已包含在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 [屬性] 欄位中，否則 Null 對此型別是有效的值。

二進位類型可搭配下列種類的 CoNtextData 使用。

**點陣圖 CoNtextData**

可設定的合併模組可以使用此型別，讓使用者在包含點陣圖影像的二進位資料表中，提供資料列的外鍵。 Mergmod.dll 不保證任何特定大小或點陣圖類型，而且合併工具必須確定資料是有效的影像。 若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在類型資料行中輸入 "Binary"，然後在 ModuleConfiguration 資料表的 CoNtextData 資料行中輸入 "Bitmap"。

**圖示 CoNtextData**

可設定的合併模組可以使用此型別，讓使用者在包含圖示影像的二進位資料表中，提供一個資料列的外鍵。 Mergmod.dll 不保證任何特定大小或類型的圖示，且合併工具必須確定資料是有效的影像。 若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在類型資料行中輸入 "Binary"，然後在 ModuleConfiguration 資料表的 CoNtextData 資料行中輸入 "Icon"。 這種類型不適合用在公告資料表中。

**EXE CoNtextData**

可設定的合併模組可以使用此型別，讓使用者在包含32位可執行檔映射的二進位資料表中，提供資料列的外鍵。 Mergmod.dll 不會驗證資料是否有效，且合併工具必須確定資料是有效的 PE 檔案。 若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在類型資料行中輸入 "Binary"，然後在 ModuleConfiguration 資料表的 CoNtextData 資料行中輸入 "EXE"。

**EXE64 CoNtextData**

可設定的合併模組可以使用此型別，讓使用者可以在包含32位或64位可執行檔映射的二進位資料表中，提供資料列的外鍵。 Mergmod.dll 不會驗證資料是否有效，且合併工具必須確定資料是有效的 PE 檔案。 若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在類型資料行中輸入 "Binary"，然後在 ModuleConfiguration 資料表的 CoNtextData 資料行中輸入 "EXE64"。

 

 



