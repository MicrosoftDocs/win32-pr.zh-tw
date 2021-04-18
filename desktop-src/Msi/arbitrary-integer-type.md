---
description: 語義類型的任意整數類型是其中一種整數格式類型。
ms.assetid: e35b27ca-be24-4aca-b12f-ca10ab153409
title: 任意整數類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f55f7b7cd1c66d75a6f3aeeef1741168fad6675
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115377"
---
# <a name="arbitrary-integer-type"></a>任意整數類型

[語義類型](semantic-types.md)的任意整數類型是其中一種[整數格式類型](integer-format-types.md)。 這種可設定的專案是使用者提供的整數。 合併工具會將這個整數取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)之 [值] 資料行中指定的範本。

若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入文字字串的名稱，在 [格式] 資料行中輸入 "2"，然後將 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 Type 和 CoNtextData 資料行保留空白。 Type 和 CoNtextData 資料行是保留的，而且必須是 null。

 

 



