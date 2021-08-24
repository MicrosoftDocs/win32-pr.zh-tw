---
description: RTF 類型的語義類型是其中一種文字格式類型。
ms.assetid: 91fc47c1-520a-4002-9dbe-4ee2b56f84b3
title: RTF 類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269b378644fbf41e906993097cea8bb4fb27f969cbda046aab59700896513774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039688"
---
# <a name="rtf-type"></a>RTF 類型

RTF 類型的 [語義類型](semantic-types.md) 是其中一種 [文字格式類型](text-format-types.md)。 此類型是由使用者提供之任何長度的 rtf)  (RTF 格式的任意文字字串所組成。 合併工具會將此字串取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)之 [值] 資料行中指定的範本。

若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入文字字串的名稱，在 [格式] 資料行中輸入 "0"，在 [類型] 資料行中輸入 "RTF"，並將 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 CoNtextData 資料行保留空白。字串可能是與資料庫字碼頁相容的任何語言。 請參閱[字碼頁處理 (Windows Installer) ](code-page-handling-windows-installer-.md)。 Null 是文字字串的有效值，除非 msmConfigItemNonNullable 已包含在 ModuleConfiguration 資料表的 Attributes 欄位中。

 

 



