---
description: 語義類型的列舉類型是其中一種文字格式類型。
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: 列舉類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c5df6b0f76cc789c148e841827a75e7184aca2892d7d6e2233843e26aac80f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869318"
---
# <a name="enum-type"></a>列舉類型

[語義類型](semantic-types.md)的列舉類型是其中一種[文字格式類型](text-format-types.md)。 此類型是由使用者從一組選擇所選擇的文字字串所組成。 合併工具會將選取的字串取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)的 [值] 資料行中指定的範本。

若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入文字字串的名稱，在 [格式] 資料行中輸入 "0"，在 [類型] 資料行中輸入 "Enum"，然後在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 CoNtextData 資料行中輸入可能的字串清單。 可能的字串清單必須以分號 deliminated 的字串清單形式提供。 每個選擇的格式都必須是 "Name = Value"。 您可以在分號前面加上反斜線字元，以將常值分號加入至值。 除非 msmConfigItemNonNullable 已包含在 ModuleConfiguration 資料表的 [屬性] 欄位中，否則 Null 是有效的值。

 

 



