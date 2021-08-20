---
description: 語義類型的屬性類型是其中一種主要格式類型。 此類型是由使用者提供的屬性資料表中的外鍵所組成。
ms.assetid: 819e4e90-0bc3-41ba-851d-1d4c52b6eeea
title: 屬性類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6446b5a0ef5f2cf1bc969f531a3b8c35e6990a2ca3eee3c0002e4f62fbf4cea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145331"
---
# <a name="property-type"></a>屬性類型

[語義類型](semantic-types.md)的屬性類型是其中一種[主要格式類型](key-format-types.md)。 此類型是由使用者提供的 [屬性資料表](property-table.md) 中的外鍵所組成。

合併工具必須將有效的 Windows Installer[識別碼](identifier.md)取代為此類型的專案。 Mergemod.dll 不會強制執行這項限制，而是由合併工具所組成，以確保使用者在屬性工作表中提供有效的索引鍵。 屬性工作表的主要索引鍵是屬性名稱。

除非 msmConfigItemNonNullable 已包含在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 [屬性] 欄位中，否則 Null 對此型別是有效的值。

屬性類型可與下列種類的 CoNtextData 搭配使用。

**Null CoNtextData**

可設定的合併模組可以使用此類型，讓使用者能夠提供屬性名稱給模組中的資料庫資料表。 合併工具會將屬性的識別碼取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)之 [值] 資料行中的範本。 若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在 [類型] 資料行中輸入 "Property"，然後將 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 CoNtextData 資料行保留空白。

**公用 CoNtextData**

可設定的合併模組可以使用此類型，讓使用者能夠將 [公用屬性](public-properties.md) 的名稱提供給模組中的資料庫資料表。 合併工具會將屬性的識別碼取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)之 [值] 資料行中的範本。 若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在 [類型] 資料行中輸入 "Property"，然後在 ModuleConfiguration 資料表的 CoNtextData 資料行中輸入 "Public"。

**私用 CoNtextData**

可設定的合併模組可以使用此類型，讓使用者能夠將 [私用屬性](private-properties.md) 的名稱提供給模組中的資料庫資料表。 合併工具會將屬性的識別碼取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)之 [值] 資料行中的範本。 若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在 [類型] 資料行中輸入 "Property"，然後在 ModuleConfiguration 資料表的 CoNtextData 資料行中輸入「私用」。

 

 



