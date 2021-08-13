---
description: 語義類型的圖示類型是其中一種主要格式類型。 此類型是由使用者提供的圖示表格中的索引鍵所組成。
ms.assetid: 8e155846-cc29-43f4-b1f7-9880320edbec
title: 圖示類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28510eff674d1f25e632b1181943af70da73d9fc97a6a64ec5abd0807fe15cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634951"
---
# <a name="icon-type"></a>圖示類型

[語義類型](semantic-types.md)的圖示類型是其中一種[主要格式類型](key-format-types.md)。 此類型是由使用者提供的 [圖示表格](icon-table.md) 中的索引鍵所組成。

合併工具必須將有效的 Windows Installer[識別碼](identifier.md)取代為此類型的專案。 Mergemod.dll 不會強制執行這項限制，而是由合併工具所組成，以確保使用者在圖示表格中提供有效的金鑰。

除非 msmConfigItemNonNullable 已包含在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 [屬性] 欄位中，否則 Null 對此型別是有效的值。

二進位類型可搭配下列種類的 CoNtextData 使用。

**ShortcutIcon CoNtextData**

可設定的合併模組可以使用此型別，讓使用者在 [圖示資料表](icon-table.md) 中提供一個資料列的外鍵，其中包含適合用來做為快捷方式圖示的影像。 若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在 [類型] 資料行中輸入 "Icon"，然後在 ModuleConfiguration 資料表的 CoNtextData 資料行中輸入 "ShorcutIcon"。 此類型不適合在使用者介面資料表中使用。 若要將索引鍵修改為這些資料表中的圖示表格，請參閱 [ [二進位類型](binary-type.md)] 下的圖示 CoNtextData。

 

 



