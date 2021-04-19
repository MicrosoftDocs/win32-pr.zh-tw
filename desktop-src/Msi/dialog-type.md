---
description: 語義類型的對話類型是其中一種主要格式類型。 此類型是由使用者提供的對話方塊資料表中的外鍵所組成。
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: 對話方塊類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ed04dece5702d232f252caa7c0ee02e7576246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984580"
---
# <a name="dialog-type"></a>對話方塊類型

[語義類型](semantic-types.md)的對話類型是其中一種[主要格式類型](key-format-types.md)。 此類型是由使用者提供的 [對話方塊資料表](dialog-table.md) 中的外鍵所組成。

合併工具必須將有效的 Windows Installer [識別碼](identifier.md) 取代為此類型的專案。 Mergemod.dll 不會強制執行這項限制，而是由「合併」工具組成，以確保使用者在對話方塊資料表中提供有效的金鑰。

除非 msmConfigItemNonNullable 已包含在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 [屬性] 欄位中，否則 Null 對此型別是有效的值。

對話方塊類型可與下列種類的 CoNtextData 搭配使用。

**DialogNext CoNtextData**

可設定的合併模組可以使用此類型，讓使用者在對話方塊資料表中提供外鍵。 若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在 [類型] 資料行中輸入 "Dialog"，然後在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 CoNtextData 資料行中輸入 "DialogNext"。

**DialogPrev CoNtextData**

可設定的合併模組可以使用此類型，讓使用者在對話方塊資料表中提供外鍵。 若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在 [類型] 資料行中輸入 "Dialog"，然後在 ModuleConfiguration 資料表的 CoNtextData 資料行中輸入 "DialogPrev"。

 

 



