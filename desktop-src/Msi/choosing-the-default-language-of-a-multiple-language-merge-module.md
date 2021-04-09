---
description: 合併模組的預設語言是套用語言轉換之前，模組的 ModuleSignature 資料表中所列的語言。 這也是 [範本摘要] 屬性中所列的第一種語言。
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: 選擇多重語言合併模組的預設語言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758a3b47b7a41777652a11a1cdc1b7f380055cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848940"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a>選擇多重語言合併模組的預設語言

合併模組的預設語言是套用語言轉換之前，模組的 [ModuleSignature 資料表](modulesignature-table.md) 中所列的語言。 這也是 [ [**範本摘要**](template-summary.md) ] 屬性中所列的第一種語言。

模組的預設語言應該是您所支援的其中一種最特定語言，因為預設語言會先進行檢查，如果它符合要求的語言，則會使用它，即使另一個語言更相符也是一樣。 例如，如果模組支援1033和0，則1033應該是預設語言。 如果0是預設語言，它一定會滿足任何要求，而且永遠不會使用1033轉換，即使1033是所要求的正確語言。

 

 



