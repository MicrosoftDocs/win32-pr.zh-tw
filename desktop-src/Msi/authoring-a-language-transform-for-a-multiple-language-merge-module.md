---
description: 將模組合併到具有不同預設語言的資料庫時，合併工具可能需要將語言轉換套用至模組，以提供最終的語言。 如需詳細資訊，請參閱多個語言合併模組。
ms.assetid: 51e8774e-f358-423f-a283-ad7beeabbbdb
title: 撰寫多個語言合併模組的語言轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970c8908ddbf89e31f0fc7a415358bb887f0838e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192457"
---
# <a name="authoring-a-language-transform-for-a-multiple-language-merge-module"></a>撰寫多個語言合併模組的語言轉換

將模組合併到具有不同預設語言的資料庫時，合併工具可能需要將語言轉換套用至模組，以提供最終的語言。 如需詳細資訊，請參閱 [多個語言合併模組](multiple-language-merge-modules.md)。

語言轉換會儲存在模組的 .msm 檔中，而且必須具有名稱和格式： \# MergeModule。 \# \# \# \# \# \# \# 代表最終語言的最多四位數[LANGID](localizing-the-error-and-actiontext-tables.md) 。 例如，MergeModule. Lang1033、MergeModule. Lang9 和 MergeModule. Lang0 轉換成美國英文、全球英文和中性語言。 這些與 [內嵌的轉換](embedded-transforms.md) 相同，您可以將它們新增至 .msm 檔案中的 substorages。

語言轉換應該執行下列作業：

-   將 [ModuleSignature 資料表](modulesignature-table.md) 的 [語言] 資料行中的預設語言變更為模組的新語言。
-   將 [ModuleComponents 資料表](modulecomponents-table.md) 的 [語言] 資料行中的預設語言變更為模組的新語言。 轉換可以加入或移除此資料表中的資料列。
-   如有必要，請將 RequiredLanguage 資料行中的語言或加入或刪除資料列，變更至 [ModuleDependency 資料表](moduledependency-table.md)。
-   如有必要，請將 ExcludedLanguage 資料行中的語言或加入或刪除資料列，變更至 [ModuleExclusion 資料表](moduleexclusion-table.md)。
-   轉換可以在模組上執行任何有效的轉換作業，包括新增或移除元件、檔案、登錄專案或動作。

請注意，開啟模組時套用語言轉換並不會變更預設語言或模組所支援的語言，而只會變更所要求的語言。 因此，[ [**範本摘要**](template-summary.md) ] 屬性不會變更，它應該已經列出模組支援的所有語言，而且會先列出預設語言。

所有可能語言轉換所需的所有檔案通常會儲存在模組隨附的單一封包檔中。 因為讓語言轉換修改此封包檔並不實用，所以最好在封包檔、檔案 [資料表](file-table.md)和語言轉換中使用全域檔案順序。 如需詳細資訊，請參閱在 [多個語言合併模組的 CAB 中排序檔案順序](ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module.md)

 

 



