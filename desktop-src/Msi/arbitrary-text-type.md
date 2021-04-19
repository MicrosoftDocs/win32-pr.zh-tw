---
description: 語義類型的任意文字類型是其中一種文字格式類型。
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: 任意文字類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9709a560398472fe79a2c77db827acdfa7994148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106995831"
---
# <a name="arbitrary-text-type"></a>任意文字類型

[語義類型](semantic-types.md)的任意文字類型是其中一種[文字格式類型](text-format-types.md)。 此類型是由使用者提供之任何長度的任意文字字串所組成。 合併工具會將此任一字元串取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)的 [值] 資料行中所指定的範本。

若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入文字字串的名稱，在 [格式] 資料行中輸入 "0"，並將 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 Type 和 CoNtextData 資料行保留空白。任意文字字串可能是與資料庫字碼頁相容的任何語言。 如需詳細資料，請參閱 [字碼頁處理 (Windows Installer) ](code-page-handling-windows-installer-.md)。 Null 是文字字串的有效值，除非 msmConfigItemNonNullable 已包含在 ModuleConfiguration 資料表的 Attributes 欄位中。

 

 



