---
description: ICEM04 會確認合併模組的必要空白資料表是空的。 若無法修正 ICEM04 報表的錯誤，可能會導致合併模組的合併不正確。
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8388cbccd576b89a70716dd7c2ca6c82ac49fb30c8c39776904753de00b68dba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050158"
---
# <a name="icem04"></a>ICEM04

ICEM04 會確認合併模組的必要空白資料表是空的。 若無法修正 ICEM04 報表的錯誤，可能會導致合併模組的合併不正確。

## <a name="result"></a>結果

當合併模組的必要空白資料表不是空白時，ICEM04 會張貼錯誤。

## <a name="example"></a>範例

ICEM04 會針對包含所顯示資料庫專案的模組，張貼下列錯誤訊息。

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

下表顯示部分 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md)。



| 動作         | 順序 |
|----------------|----------|
| CostInitialize | 1        |



 

下列清單顯示 MergeModule 的部分內容：

-   ModuleInstallExecuteSequence
-   ModuleAdvtExecuteSequence
-   InstallUISequence

下列範例會顯示另一個可能的錯誤。

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

如果合併模組包含模組順序資料表，它必須包含對應的空白順序資料表，無論模組順序資料表是否為空白。 例如，如果 merge 模組包含 [ModuleAdminExecuteSequence 資料表](moduleadminexecutesequence-table.md)，它也必須包含空的 AdminExecuteSequence 資料表。

[FeatureComponents 資料表](featurecomponents-table.md)在所有合併模組中都是必要的，而且必須是空的。

下列程式說明如何修正錯誤。

**若要修正錯誤**

1.  將空的 [FeatureComponents 資料表](featurecomponents-table.md) 加入至合併模組。
2.  將空的 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 加入至合併模組。
3.  從 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md)中移除 ' CostInitialize ' 動作。
    > [!Note]  
    > 在合併模組中，此資料表必須是空的。 動作只能出現在 ModuleAdvtExecuteSequence 資料表中。

     

## <a name="tables-used-during-execution"></a>執行期間所使用的資料表

下列清單會識別執行期間所使用的資料表：

-   [FeatureComponents 資料表](featurecomponents-table.md)
-   模組 \* 順序資料表和對應 \* 的順序資料表。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於合併模組](about-merge-modules.md)
</dt> <dt>

[Merge Module ICE 參考](merge-module-ice-reference.md)
</dt> </dl>

 

 



