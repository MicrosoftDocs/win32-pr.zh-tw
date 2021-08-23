---
description: 可設定資料的文字格式類型可以是任何長度的文字字串。 不允許內嵌的 null。
ms.assetid: 71b89f87-43ba-41cd-a969-765d45da4ba4
title: 文字格式類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a77ef5e6948320deba8df992e2cf9447cbda82d6a20fc4329f97e761f425164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626328"
---
# <a name="text-format-types"></a>文字格式類型

可設定資料的文字格式類型可以是任何長度的文字字串。 不允許內嵌的 null。

下列文字格式類型存在：

[任意文字](arbitrary-text-type.md)

[RTF](rtf-type.md)

[格式 化](formatted-type.md)

[列舉](enum-type.md)

[識別碼類型](identifier-type.md)

文字格式類型的可設定專案會用於非二進位資料庫欄位，而且一般可以由任何長度的任何字串取代。 不過，特定可設定的專案也有語義限制。 例如，在特定資料表中必須是外鍵的可設定專案具有其他語義限制。 Mergemod.dll 不會強制執行這類語義限制，因此模組作者應該準備好處理任何符合指定文字格式類型的字串。

 

 



