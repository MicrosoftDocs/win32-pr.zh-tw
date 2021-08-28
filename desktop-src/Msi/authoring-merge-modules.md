---
description: 下列程式說明撰寫合併模組的一般步驟。
ms.assetid: 4b3871c0-f452-4935-9ee3-78b0ac847e67
title: 撰寫合併模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078956c0e3586e12105fc5ea33b1d7e8908c19461aaa4533c7b3cccc32c014ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328418"
---
# <a name="authoring-merge-modules"></a>撰寫合併模組

下列程式說明撰寫合併模組的一般步驟。

**若要建立新的合併模組**

1.  取得可用來編輯合併模組資料庫的軟體工具。
2.  取得空白的合併模組資料庫。
3.  產生合併模組的 [GUID](guid.md) 。 在合併模組中撰寫資料庫資料表的主鍵時，您必須使用此 GUID。
4.  將記錄加入至合併所傳遞之每個元件的 [元件資料表](component-table.md) 中。 每個合併模組都需要元件資料表。 請注意，合併模組會操作元件，而不是功能。 不過，在某些情況下，資料庫資料表專案可能需要參考功能。 如需詳細資訊，請參閱 [合併模組中的參考功能](referencing-features-in-merge-modules.md)。
5.  將 [目錄資料表](directory-table.md) 加入至合併模組，以指定合併模組新增至目標資料庫的目錄配置。 每個合併模組都需要目錄資料表。
6.  將空白的 [FeatureComponents 資料表](featurecomponents-table.md) 匯入到合併模組資料庫中。 如果 .msi 檔案未包含它自己的 FeatureComponents 資料表，則此空白資料表會提供合併工具的指導方針。
7.  收集由此合併模組提供的所有檔案，並建立 [MergeModule.CABinet](mergemodule-cabinet.md) 封包檔。 將封包加入至合併模組，作為 .msm 檔案內的資料流程。
8.  針對儲存在 MergeModule.CABinet 中的每個檔案，將記錄新增至檔案資料表。
9.  在 [ModuleSignature 資料表](modulesignature-table.md)中，加入識別合併模組所需的資訊。 每個合併模組都需要 ModuleSignature 資料表。
10. 列出 [ModuleComponents 資料表](modulecomponents-table.md)中 merge 模組的元件。 每個合併模組都需要 ModuleComponents 資料表。
11. 只有在合併模組必須修改目標安裝資料庫的 [*順序資料表*](s-gly.md) 時，才將 merge module sequence 資料表加入至 .msm 檔。
12. 將 \_ 驗證資料表加入至合併模組。 合併模組需要 \_ 驗證資料表才能通過驗證。
13. 合併模組在少數情況下只需要使用者介面。 不建議包含包含合併模組的 UI。 在需要使用者介面的情況下，可以將 UI 資料表合併到 .msi 檔案中，與其他資料表相同。
14. 將登錄資訊加入至合併模組資料庫中的適當登錄資料表。 將類型程式庫、類別、延伸模組和動詞的登錄資訊新增至 [TypeLib](typelib-table.md)、 [類別](class-table.md)、 [AppId](appid-table.md)、 [ProgId](progid-table.md)、 [延伸](extension-table.md)模組、 [動詞](verb-table.md)或 [MIME](mime-table.md) 資料表。 所有其他登錄資訊都可以進入登錄 [表](registry-table.md)。 不建議使用 SelfReg 資料表。
15. 將摘要資訊加入至 [合併模組摘要資訊資料流程](merge-module-summary-information-stream-reference.md)。
16. 請先在所有合併模組上執行驗證，再嘗試安裝。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[取得空白合併模組資料庫](obtaining-blank-merge-module-databases.md)
</dt> <dt>

[取得合併模組撰寫工具](obtaining-merge-module-authoring-tools.md)
</dt> <dt>

[命名合併模組資料庫中的主鍵](naming-primary-keys-in-merge-module-databases.md)
</dt> <dt>

[撰寫合併模組元件資料表](authoring-merge-module-component-tables.md)
</dt> <dt>

[撰寫合併模組目錄資料表](authoring-merge-module-directory-tables.md)
</dt> <dt>

[撰寫合併模組 FeatureComponents 資料表](authoring-merge-module-featurecomponents-tables.md)
</dt> <dt>

[產生 MergeModule.CABinet 封包檔](generating-mergemodule-cabinet-cabinet-files.md)
</dt> <dt>

[撰寫合併模組檔案資料表](authoring-merge-module-file-tables.md)
</dt> <dt>

[撰寫 ModuleSignature 資料表](authoring-modulesignature-tables.md)
</dt> <dt>

[撰寫 ModuleComponents 資料表](authoring-modulecomponents-tables.md)
</dt> <dt>

[撰寫合併模組順序資料表](authoring-merge-module-sequence-tables.md)
</dt> <dt>

[驗證合併模組](validating-merge-modules.md)
</dt> <dt>

[在合併模組中撰寫使用者介面](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[撰寫合併模組登錄資料表](authoring-merge-module-registry-tables.md)
</dt> <dt>

[撰寫合併模組摘要資訊資料流程](authoring-merge-module-summary-information-streams.md)
</dt> <dt>

[合併模組摘要資訊資料流程參考](merge-module-summary-information-stream-reference.md)
</dt> <dt>

驗證合併模組
</dt> <dt>

[使用64位合併模組](using-64-bit-merge-modules.md)
</dt> </dl>

 

 



