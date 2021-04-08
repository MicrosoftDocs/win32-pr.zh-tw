---
description: 語義類型的格式化類型是其中一種文字格式類型。
ms.assetid: 44af5b5c-bbf9-4043-8076-0881680a36c1
title: 格式化類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b97e0c0c1763352f75424bf54d01f6871604f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026434"
---
# <a name="formatted-type"></a>格式化類型

[語義類型](semantic-types.md)的格式化類型是其中一種[文字格式類型](text-format-types.md)。 這個型別是由使用者提供的任意長度的任意文字字串，以及 Windows Installer 格式的文字格式所組成。 如需詳細資訊，請參閱 [格式化](formatted.md)。 合併工具會將此字串取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)之 [值] 資料行中指定的範本。

若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入文字字串的名稱，在 [格式] 資料行中輸入 "0"，在 [類型] 資料行中輸入「格式化」，然後將 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 CoNtextData 資料行保留空白。字串可能是與資料庫字碼頁相容的任何語言。 如需詳細資料，請參閱 [字碼頁處理 (Windows Installer) ](code-page-handling-windows-installer-.md)。 Null 是文字字串的有效值，除非 msmConfigItemNonNullable 已包含在 ModuleConfiguration 資料表的 Attributes 欄位中。

 

 



