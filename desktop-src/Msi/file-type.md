---
description: 語義類型的檔案類型是其中一種主要格式類型。 此類型包含使用者所提供之檔案資料表中的外鍵。
ms.assetid: cbcaa016-879e-48c2-93c6-b0e91e1eb9ed
title: 檔案類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b47e76f4a910b336c749a4f0d5001c8568cead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984625"
---
# <a name="file-type"></a>檔案類型

[語義類型](semantic-types.md)的檔案類型是其中一種[主要格式類型](key-format-types.md)。 此類型包含使用者所提供之檔案 [資料表](file-table.md) 中的外鍵。

檔案類型可與下列種類的 CoNtextData 搭配使用。

**AssemblyCoNtext CoNtextData**

您可以使用此類型來讓使用者設定 Win32 或 common language runtime 元件的外鍵。 合併工具必須在[ModuleSubstitution 資料表](modulesubstitution-table.md)的 [值] 資料行中，將此類型的專案 Windows Installer[識別碼](identifier.md)取代為範本。 Mergemod.dll 不會強制執行這項工作，而是由「合併」工具組成，以確保使用者在檔案資料表中提供有效的金鑰。

除非 msmConfigItemNonNullable 已包含在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 [屬性] 欄位中，否則 Null 對此型別是有效的值。

 

 



