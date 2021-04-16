---
description: ICE84 會檢查 AdvtExecuteSequence 資料表、AdminExecuteSequence 資料表和 InstallExecuteSequence 資料表，以確認未在條件欄位中設定條件的下列標準動作。
ms.assetid: 0d1bbf4b-ffab-409e-a292-891dfa823433
title: ICE84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8960f53f5a01e9bec95a02bb3241487aa31aaae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320087"
---
# <a name="ice84"></a>ICE84

ICE84 會檢查 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md)、 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)和 [InstallExecuteSequence 資料表](installexecutesequence-table.md) ，以確認未在條件欄位中設定條件的下列 [標準動作](standard-actions.md) 。

-   [CostInitialize 動作](costinitialize-action.md)
-   [CostFinalize 動作](costfinalize-action.md)
-   [FileCost 動作](filecost-action.md)
-   [InstallValidate 動作](installvalidate-action.md)
-   [InstallInitialize 動作](installinitialize-action.md)
-   [InstallFinalize 動作](installfinalize-action.md)
-   [ProcessComponents 動作](processcomponents-action.md)
-   [PublishFeatures 動作](publishfeatures-action.md)
-   [PublishProduct 動作](publishproduct-action.md)
-   [RegisterProduct 動作](registerproduct-action.md)
-   [UnpublishFeatures 動作](unpublishfeatures-action.md)

如果找到條件，ICE84 會張貼警告。

## <a name="result"></a>結果

ICE84 會張貼下列警告。



| ICE84 錯誤                                                             | Description                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| \[ \] 在% s 資料表中找到的動作 ' 1 ' 是具有條件的必要動作。 | 已使用條件撰寫必要的動作。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



