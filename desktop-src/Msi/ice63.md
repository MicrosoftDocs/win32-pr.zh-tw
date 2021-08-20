---
description: ICE63 會檢查是否有適當的 RemoveExistingProducts 動作順序。
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f0de847a3b79c87b8ddc7dbaf3be64f88b9ef34df80d92737b6d9005ffdad24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142492"
---
# <a name="ice63"></a>ICE63

ICE63 會檢查是否有適當的 [RemoveExistingProducts 動作](removeexistingproducts-action.md)順序。 可能會放置 RemoveExistingProducts 動作：

1.  介於 InstallValidate 和 InstallInitialize 之間
2.  緊接在 InstallInitialize 之後，或在 InstallInitialize 之後，如果 InstallInitialize 和 RemoveExistingProducts 之間的動作未產生任何腳本動作。
3.  緊接在 InstallExecute 或 InstallExecuteAgain 之後，以及 InstallFinalize 之前 (上述的相同限制適用于) 。
4.  InstallFinalize 之後。

若無法修正 ICE63 回報的警告或錯誤，會導致升級失敗。

## <a name="result"></a>結果

如果 RemoveExistingProducts 動作的排序不正確，ICE63 會張貼警告或錯誤。

## <a name="example"></a>範例

ICE63 會針對所顯示的範例報告下列錯誤。

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

' MyCustomAction ' 動作發生于 InstallInitialize 和 RemoveExistingProducts 之間。 如果 MyCustomAction 在腳本中產生任何動作，這會造成安裝中的問題。

若要修正這個錯誤，請確認 MyCustomAction 不會產生任何腳本動作或重新排序動作。

[InstallExecuteSequence 資料表](installexecutesequence-table.md)



| 動作                 | 條件 | 順序 |
|------------------------|-----------|----------|
| InstallInitialize      |           | 1000     |
| MyCustomAction         |           | 1010     |
| RemoveExistingProducts |           | 1020     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



