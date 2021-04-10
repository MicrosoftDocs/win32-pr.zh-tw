---
description: 將模組合併至安裝資料庫時，有兩種重要的語言。
ms.assetid: e815854f-a379-497a-ae37-b13de39dd516
title: 以特定語言開啟 Multiple-Language 合併模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b552c41d7696b29a86987d027e00ef4cb19bbb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026356"
---
# <a name="opening-a-multiple-language-merge-module-in-a-specific-language"></a>以特定語言開啟 Multiple-Language 合併模組

將模組合併至安裝資料庫時，有兩種重要的語言。 第一個是 [**ProductLanguage**](productlanguage.md) 在 [屬性資料表](property-table.md)中所指定之目標安裝套件的語言。 第二個是 [ModuleSignature 資料表](modulesignature-table.md)的 language 資料行中所顯示之 merge 模組的語言。

當封裝開啟進行合併時，合併工具可以將安裝封裝的語言傳遞給模組。 不過，有時候可能需要忽略目標的語言，並要求以另一種語言來開啟該模組，例如，從模組安裝英文和德文資源的英文套件。

使用語言要求開啟模組時，合併工具會針對 [ModuleSignature 資料表](modulesignature-table.md)的 language 資料行中所指定的語言，檢查要求的語言。

下列程式是用來決定要使用的語言。

**判斷要使用的語言**

1.  如果 [ModuleSignature 資料表](modulesignature-table.md) 中的語言等於或高於要求的語言，則會開啟模組。
2.  如果模組支援所要求的正確語言，則會使用該語言。
3.  如果模組支援使用語言群組的語言群組，例如，如果已要求1033但在步驟2中找不到，則檢查9。
4.  檢查是否有語言轉換將模組變更為中性。
5.  如果上述步驟都沒有成功，則模組不支援要求的語言，因此合併會失敗。

 

 



