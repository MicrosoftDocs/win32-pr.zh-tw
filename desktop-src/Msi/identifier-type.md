---
description: 語義類型的識別碼類型是其中一種文字格式類型。
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: 識別碼類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1061f6d813b0803dbe1aa0d8e49e7f93cffba6e100f778901441f4bc4ed710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634779"
---
# <a name="identifier-type"></a>識別碼類型

[語義類型](semantic-types.md)的識別碼類型是其中一種[文字格式類型](text-format-types.md)。 這個型別是由使用者以 Windows Installer[識別碼](identifier.md)的格式所提供的文字字串所組成。 合併工具會將此字串取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)之 [值] 資料行中指定的範本。

若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入文字字串的名稱，在 [格式] 資料行中輸入 "0"，在 [類型] 資料行中輸入 "Identifier"，並將 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 CoNtextData 資料行保留空白。字串可能是與資料庫字碼頁相容的任何語言。 請參閱[字碼頁處理 (Windows Installer) ](code-page-handling-windows-installer-.md)。 Null 是文字字串的有效值，除非 msmConfigItemNonNullable 已包含在 ModuleConfiguration 資料表的 Attributes 欄位中。

 

 



